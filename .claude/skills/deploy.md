# Skill: deploy

> Pre-deployment checklist and deployment workflow.
> Use before every production deployment to avoid preventable incidents.

## Pre-Deployment Checklist

### Code
- [ ] All tests passing (unit + integration)
- [ ] No known failing tests skipped
- [ ] No debug code or console.logs in production code
- [ ] No hardcoded secrets or credentials
- [ ] Dependencies are pinned and audited

### Review
- [ ] PR reviewed and approved
- [ ] Security review done for auth/data changes
- [ ] Breaking changes documented
- [ ] Migration scripts tested

### Infrastructure
- [ ] Environment variables set in production
- [ ] Database migrations are backwards-compatible
- [ ] Rollback plan documented
- [ ] Monitoring and alerts are in place

### Communication
- [ ] Team notified of deployment window
- [ ] Changelog or release notes written
- [ ] Customer-facing changes communicated if needed

## Deployment Steps

1. **Backup** — Verify recent DB backup exists
2. **Run migrations** — Apply DB migrations before deploying new code
3. **Deploy** — Push new version to production
4. **Smoke test** — Test critical paths immediately after deploy
5. **Monitor** — Watch error rates, latency, and alerts for 15 minutes
6. **Confirm** — Mark deployment as successful

## Rollback Trigger

Rollback immediately if:
- Error rate increases > 5% from baseline
- P95 latency increases > 2x from baseline
- Any critical user-facing feature is broken
- Database corruption is detected

## Post-Deployment

- [ ] Update deployment log / changelog
- [ ] Close related tickets
- [ ] Document any issues encountered and how they were resolved
