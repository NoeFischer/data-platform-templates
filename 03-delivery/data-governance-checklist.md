# Data Governance Checklist: [Project Name]

> Use this checklist to ensure governance is built into the platform from the start, not bolted on later. Review during design and revisit before go-live.

| Field | Details |
|-------|---------|
| **Prepared by** | |
| **Date** | |
| **Reviewed by** | |
| **Last review date** | |

---

## 1. Data ownership and stewardship

- [ ] Every dataset / domain has an identified **data owner** (accountable for quality and usage)
- [ ] **Data stewards** are assigned for day-to-day governance tasks
- [ ] Ownership is documented in the data catalog
- [ ] Escalation path is clear when ownership is disputed

| Domain | Data Owner | Data Steward | Notes |
|--------|-----------|-------------|-------|
| | | | |
| | | | |

## 2. Data catalog and documentation

- [ ] Data catalog tool is selected and configured
- [ ] All production datasets are registered in the catalog
- [ ] Each table/dataset has a description, owner, and update frequency documented
- [ ] Key business terms are defined in a glossary
- [ ] Column-level descriptions exist for critical fields
- [ ] Users know how to search and browse the catalog

## 3. Data quality

- [ ] Data quality dimensions are defined (completeness, accuracy, timeliness, uniqueness, consistency)
- [ ] Automated quality checks run on ingestion and transformation
- [ ] Quality thresholds are defined per dataset
- [ ] Alerting is configured for quality failures
- [ ] A process exists for investigating and resolving quality issues
- [ ] Quality metrics are visible to data consumers

| Quality check type | Tool / approach | Coverage | Notes |
|-------------------|----------------|----------|-------|
| Freshness | | | |
| Completeness (null checks) | | | |
| Uniqueness (duplicate checks) | | | |
| Schema drift detection | | | |
| Value range / referential integrity | | | |

## 4. Security and access control

- [ ] Data classification scheme is defined (e.g. Public, Internal, Confidential, Restricted)
- [ ] All datasets are classified
- [ ] Role-based access control (RBAC) is implemented
- [ ] Row-level and/or column-level security is applied where needed
- [ ] PII and sensitive data is identified and protected (masking, encryption, or restricted access)
- [ ] Access request and approval process is documented
- [ ] Access is reviewed periodically (quarterly recommended)
- [ ] Service accounts and API keys are managed and rotated

| Data classification | Access policy | Example datasets |
|--------------------|--------------|-----------------|
| Public | Anyone in the org | Product catalog, public KPIs |
| Internal | Authenticated users | Sales reports, operational metrics |
| Confidential | Approved roles only | Customer PII, financial details |
| Restricted | Named individuals only | Salary data, M&A data |

## 5. Data lineage

- [ ] Lineage tracking is enabled (tool or manual documentation)
- [ ] Users can trace data from source to dashboard
- [ ] Lineage is used for impact analysis before making changes
- [ ] Lineage documentation is kept up to date (automated preferred)

## 6. Data retention and lifecycle

- [ ] Retention policies are defined per dataset
- [ ] Archival process is in place for expired data
- [ ] Deletion process complies with regulatory requirements (e.g. GDPR right to be forgotten)
- [ ] Storage costs are monitored and optimized

| Dataset / Domain | Retention period | Archive strategy | Regulatory driver |
|-----------------|-----------------|-----------------|------------------|
| | | | |

## 7. Compliance and privacy

- [ ] Applicable regulations are identified (GDPR, HIPAA, CCPA, SOC2, industry-specific)
- [ ] Data processing agreements (DPAs) are in place with vendors
- [ ] Consent management is implemented where required
- [ ] Audit logging is enabled for data access
- [ ] Privacy impact assessment completed (if applicable)

## 8. Change management for data

- [ ] Schema changes go through a review process
- [ ] Breaking changes are communicated to downstream consumers
- [ ] Versioning strategy is defined for APIs and datasets
- [ ] Rollback plan exists for failed data deployments

## 9. Governance operating model

- [ ] Governance roles and responsibilities are documented
- [ ] Governance cadence is established (e.g. monthly data governance meeting)
- [ ] Issue escalation process is defined
- [ ] Governance metrics are tracked (catalog coverage, quality scores, access reviews completed)

---

_Review this checklist at project milestones: design complete, pre-go-live, and quarterly thereafter._
