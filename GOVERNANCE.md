# Governance

`cloud-itonami-isic-4742` is an OSS open-business blueprint for
audio/video-equipment specialty retail operations coordination (ISIC
Rev.5 4742 -- retail sale of audio and video equipment in specialized
stores).

## Maintainers
Maintainers may merge changes that preserve these invariants:
- a proposal for an unverified/unregistered store, or a supply order
  naming an unverified/unregistered vendor, can never commit.
- the AudioVideoRetailGovernor remains independent of the advisor.
- hard policy violations (non-`:propose` effect, warranty-claim-
  finalization content, an op outside the closed allowlist) cannot be
  overridden by human approval.
- every sales-record log, staffing/delivery schedule, supply-order
  coordination and warranty-concern flag is auditable.
- customer, employee and supplier data stays outside Git.

## Decision Records
Architecture decisions live in `docs/adr/`. Changes to the trust model,
storage contract, public business model, operator certification or
license should add or update an ADR.

## Operator Governance
Anyone may fork and operate independently. itonami.cloud certification is
a separate trust mark and should require security, audit and data-flow
review.

Certified operators can lose certification for:
- bypassing sale-record, staffing, supply-order or warranty-concern
  policy checks
- mishandling customer, employee or supplier data
- misrepresenting certification status
- failing to respond to security or warranty-dispute incidents
