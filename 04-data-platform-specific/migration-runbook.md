# Migration Runbook: [Migration Name]

> This runbook is the step-by-step playbook for migrating data to the new platform. It should be detailed enough that someone who wasn't involved in planning can execute it. Practice it in a dry run before the real cutover.

| Field | Details |
|-------|---------|
| **Prepared by** | |
| **Date** | |
| **Migration lead** | |
| **Cutover date** | |
| **Rollback deadline** | _Point of no return — after this, rollback is no longer feasible_ |

---

## 1. Migration scope

### In scope

| Source system | Dataset / Tables | Volume (rows / GB) | Target location | Migration method |
|--------------|-----------------|-------------------|----------------|-----------------|
| | | | | Full / Incremental / CDC |
| | | | | |
| | | | | |

### Out of scope

-
-

## 2. Pre-migration checklist

_Complete all items before starting the migration._

| # | Task | Owner | Status | Notes |
|---|------|-------|--------|-------|
| 1 | Source system access confirmed | | | |
| 2 | Target platform provisioned and tested | | | |
| 3 | Network connectivity verified (firewalls, VPN, whitelisting) | | | |
| 4 | Migration scripts developed and code-reviewed | | | |
| 5 | Validation queries prepared | | | |
| 6 | Dry run completed successfully | | | |
| 7 | Rollback procedure documented and tested | | | |
| 8 | Stakeholders notified of migration window | | | |
| 9 | Monitoring and alerting configured | | | |
| 10 | Support team on standby | | | |

## 3. Migration steps

_Execute in order. Record actual times during execution._

| Step | Time (planned) | Time (actual) | Action | Command / Procedure | Owner | Verification | Status |
|------|---------------|--------------|--------|---------------------|-------|-------------|--------|
| 1 | | | Freeze source system writes (if applicable) | | | Confirm no new writes | |
| 2 | | | Take source snapshot / backup | | | Verify backup completeness | |
| 3 | | | Run extraction scripts | | | Row counts match expected | |
| 4 | | | Load data into staging area | | | Staging row counts match extract | |
| 5 | | | Run transformations | | | Transformation logs clean | |
| 6 | | | Load into production tables | | | Production row counts match | |
| 7 | | | Run validation queries | | | All checks pass (see section 4) | |
| 8 | | | Update downstream connections (BI tools, apps) | | | Dashboards load correctly | |
| 9 | | | Smoke test with end users | | | Users confirm data looks right | |
| 10 | | | Decommission old source connection (or mark read-only) | | | Old path no longer active | |
| 11 | | | Send completion notification | | | Stakeholders informed | |

## 4. Validation checks

| Check | Query / Method | Expected result | Actual result | Pass? |
|-------|---------------|----------------|--------------|-------|
| Row count: [table] | `SELECT COUNT(*) FROM ...` | | | |
| Sum of [amount field] | `SELECT SUM(amount) FROM ...` | | | |
| Date range coverage | `SELECT MIN(date), MAX(date) FROM ...` | | | |
| Null check on key fields | `SELECT COUNT(*) WHERE key_field IS NULL` | 0 | | |
| Duplicate check | `SELECT key, COUNT(*) ... HAVING COUNT(*) > 1` | 0 rows | | |
| Sample record comparison | Compare 10 random records against source | Match | | |
| Dashboard spot check | Verify key metrics match old reports | Within tolerance | | |

## 5. Rollback plan

_If something goes wrong, here's how to revert._

**Rollback trigger criteria:**
- Validation checks fail on >X% of tables
- Data corruption detected
- Performance degradation beyond acceptable limits
- Stakeholder / sponsor decision to abort

**Rollback steps:**

| Step | Action | Owner | Notes |
|------|--------|-------|-------|
| 1 | Stop migration process | | |
| 2 | Revert downstream connections to old source | | |
| 3 | Truncate / drop newly loaded tables | | |
| 4 | Restore source system to pre-migration state (if modified) | | |
| 5 | Notify stakeholders of rollback | | |
| 6 | Conduct root cause analysis | | |
| 7 | Reschedule migration | | |

## 6. Communication during migration

| Event | Notify | Channel | Message |
|-------|--------|---------|---------|
| Migration starting | All stakeholders | Email + Slack | "Migration window has begun. [System] will be read-only until [time]." |
| Migration 50% complete | Core team | Slack | Progress update |
| Migration complete — validating | Core team | Slack | "Data loaded, running validation checks." |
| Migration successful | All stakeholders | Email + Slack | "Migration complete. New platform is live." |
| Rollback initiated | All stakeholders | Email + Slack + phone | "Migration rolled back. Old system restored. Details to follow." |

## 7. Post-migration tasks

- [ ] Monitor platform performance for 48 hours
- [ ] Monitor data quality checks for one full refresh cycle
- [ ] Collect user feedback on data accuracy
- [ ] Schedule old system decommission date
- [ ] Update documentation and data catalog
- [ ] Conduct migration retrospective
- [ ] Archive migration scripts and runbook

## 8. Contacts

| Role | Name | Phone | Email | Available during cutover? |
|------|------|-------|-------|--------------------------|
| Migration lead | | | | Yes |
| DBA / Platform admin | | | | Yes |
| Source system owner | | | | On call |
| Network / Infrastructure | | | | On call |
| Sponsor (escalation) | | | | On call |
