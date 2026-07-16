# Contributing

`cloud-itonami-isic-4742` accepts contributions to the OSS blueprint,
capability bindings, policy tests, documentation and operator model.

## Development

```bash
clojure -M:test
clojure -M:lint
```

## Rules
- Do not commit real customer, employee, supplier or warranty-claim
  incident data.
- Keep sales-record logging, staffing/delivery scheduling, supply-order
  coordination and warranty-concern flagging behind the
  AudioVideoRetailGovernor.
- Treat AV-store-operations workflows as high-risk: add tests for
  store/vendor verification, effect discipline, scope exclusion,
  escalation and audit logging.
- Never phrase a governor scope-exclusion term as a bare noun (e.g.
  "warranty", "claim", "counterfeit") -- phrase it as the finalization/
  execution ACTION (e.g. "approved the warranty claim"), and add/extend
  the `default-mock-advisor-proposals-never-self-trip-scope-exclusion`
  regression test for any new term. A bare-noun term will self-trip this
  actor's own legitimate `:flag-warranty-concern` happy path -- see
  `avretailops.governor/scope-excluded-terms`'s docstring.
- Document any new business-model or operator assumption in `docs/`.

## Pull Requests
PRs should describe: what behavior changed, which policy invariant is
affected, how it was tested, whether operator or certification docs need
updates.
