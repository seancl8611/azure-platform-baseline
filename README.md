# Azure Platform Baseline (IaC) — Cloud Ops Starter

## What this is
A secure-by-default Azure baseline you can deploy repeatedly. Designed to demonstrate Cloud Ops fundamentals: identity, access control, networking boundaries, and operational visibility.

**Status:** Coming this week (active build)

---

## Problem
Cloud environments drift when the baseline is configured manually. Common issues include inconsistent RBAC, unclear network segmentation, missing logs, and deployments that are hard to reproduce.

## Solution
An Infrastructure-as-Code baseline that provisions:
- Core network layout (VNet + subnets + NSGs)
- Central logging (Log Analytics / Monitor baseline)
- Secure secrets pattern (Key Vault; no secrets committed)
- RBAC assignments with least privilege defaults
- Clear teardown steps to control cost

---

## Architecture
Add diagram here: `docs/architecture.png`

Suggested components (initial):
- Resource Group(s)
- VNet + subnets (app, data, management)
- NSGs + rules
- Log Analytics Workspace
- Key Vault
- Diagnostic settings (where applicable)
- RBAC role assignments (scoped)

---

## Tech
- Azure
- IaC: **(choose one)** Terraform *or* Bicep
- Git + documentation
- Optional: Azure CLI for local auth and deploy

---

## How to deploy (WIP)
> Deploy instructions will be finalized this week.

### Prereqs
- Azure subscription
- Azure CLI authenticated (`az login`)
- IaC tool installed (Terraform/Bicep)

### Deploy
1. Clone repo
2. Configure variables (WIP)
3. Run deploy (WIP)

### Teardown / cost control
1. Destroy resources (WIP)
2. Confirm deletion in portal (WIP)

---

## Security notes
- No secrets in source control
- RBAC uses least-privilege defaults
- Network rules deny-by-default where applicable
- Logging enabled to support troubleshooting and auditing

---

## Evidence (to be added in /docs)
- `docs/architecture.png` — architecture diagram
- `docs/deploy-output.png` — successful deployment output
- `docs/resource-map.png` — Azure resource view
- `docs/monitoring.png` — Log Analytics / Monitor proof

---

## Roadmap
- [ ] Finalize Terraform/Bicep implementation
- [ ] Add policy/guardrails notes (baseline standards)
- [ ] Add a small workload example to validate networking + logging
