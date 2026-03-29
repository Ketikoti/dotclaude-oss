# Rule: API Conventions

## REST Standards

- Use nouns, not verbs in endpoint paths: `/users` not `/getUsers`
- Use HTTP methods correctly: GET (read), POST (create), PUT/PATCH (update), DELETE (remove)
- Use plural resource names: `/users`, `/products`, `/orders`
- Nest resources logically: `/users/{id}/orders`
- Version your API: `/api/v1/`

## Request & Response

- Always return JSON with `Content-Type: application/json`
- Use consistent response envelope:

```json
{
  "data": {},
  "error": null,
  "meta": { "page": 1, "total": 100 }
}
```

- Return appropriate HTTP status codes:
  - 200: OK
  - 201: Created
  - 400: Bad Request (validation error)
  - 401: Unauthorized
  - 403: Forbidden
  - 404: Not Found
  - 422: Unprocessable Entity
  - 500: Internal Server Error

## Naming

- Use `snake_case` for JSON field names
- Use ISO 8601 for dates: `2026-03-29T15:00:00Z`
- Use `id` not `_id` or `userId` for primary keys in responses

## Pagination

- Default page size: 20
- Max page size: 100
- Use cursor-based pagination for large datasets
- Include `next`, `prev` links in response meta

## Error Handling

- Always return structured error responses:

```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Email is required",
    "field": "email"
  }
}
```

- Never expose stack traces in production responses
- Log full error server-side, return safe message to client
