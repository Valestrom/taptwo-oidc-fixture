# OIDC denial fixture — proposed public contents

This small fixture observes whether six fixed AWS roles refuse a real GitHub OIDC
identity from this repository or its genuine public fork. It contains no application
code, application history, credentials or private workflow dependency. Repository
names and public publication are proposals pending owner approval.

The reusable workflow has no inputs, checkout, dependencies or resource operations.
A reviewed caller in this parent and its fork will pin the accepted reusable workflow
commit. Only native manual runs on `main` are supported. The reusable job requires
a fixture-local `stage` environment in both repositories and the exact immutable
subject `repo:OWNER@OWNER_ID/REPOSITORY@REPOSITORY_ID:environment:stage`.
Issuer and STS audience remain fixed; missing/wrong environment or legacy subjects
are refused.
The draft's null IDs block all token and API access. Actual repository/owner IDs and
subject settings must be read back, resolved and independently reviewed first.
Fixture-only Actions enablement, main-only stage-environment rules and immutable
OIDC subject settings need owner approval before configuration; no cloud or
organization settings change. No secrets or elevated fork-PR tokens are added.

The observer calls only public GitHub metadata endpoints, the runner's GitHub OIDC
endpoint and `AssumeRoleWithWebIdentity` at regional Ohio STS. Six HTTP403
`AccessDenied` responses are required. Any credentials unexpectedly returned are
neither parsed nor used and make the run fail. Tokens, bearer values, raw errors and
credentials are never printed, placed in arguments or written to files. Output is
limited to nonsecret context, lineage and denial observations.

The coordinator must independently verify the actual run/attempt, reviewed caller
and harness commits, workflow bytes, public fork parent/source lineage and unchanged
AWS role identities/policies before and after the run. Parsed JWT claims and imported
JSON are not independent provenance. An AWS denial does not prove a role existed.
A rerun needs fresh bracketing evidence. Repository-boundary evidence for the
stage publisher requires its separately accepted active trust; a parked deny alone
does not prove the future active boundary. Production roles remaining parked also
provide no future-active-production trust proof. No observation authorizes deployment.

A native run in a genuine fork is not a fork pull request. This fixture does not run
PR events, enable fork-PR write tokens/secrets or exercise a fork PR against any
application repository. Token-issuance refusal, if separately approved and measured,
would be recorded as an issuance result rather than an AWS denial.

The fixed role ARNs and AWS account IDs are deliberately nonsecret public metadata.
Do not place credentials, application data or additional code in this fixture.
