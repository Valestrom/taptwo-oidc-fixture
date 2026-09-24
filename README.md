# OIDC denial fixture

The owner approved this isolated public fixture and its genuine fork,
`Valestrom/taptwo-oidc-fixture` and `allybelle/taptwo-oidc-fixture`, for bounded OIDC
denial observations. They contain no application code/history, credentials or
private workflow dependency. Repository identities and fixture-only settings have
been read back; actual STS observations and their independent acceptance remain
pending.

The reusable workflow has no inputs, checkout, dependencies or resource operations.
A separately reviewed caller in each repository will pin the actual published
harness commit. Only native manual runs on `main` are supported. Both fixtures have
local `stage` environments restricted to `main`, immutable OIDC subjects and
read-only default workflow permissions. No environment secrets, PR write tokens or
secret forwarding are introduced. Issuer and STS audience remain fixed; missing or
wrong environment claims and legacy subjects are refused.

The resolved subjects are:

- `repo:Valestrom@226228449/taptwo-oidc-fixture@1386158341:environment:stage`
- `repo:allybelle@118649845/taptwo-oidc-fixture@1386158475:environment:stage`

The observer calls only public GitHub metadata endpoints, the runner's GitHub OIDC
endpoint and `AssumeRoleWithWebIdentity` at regional Ohio STS. Six HTTP403
`AccessDenied` responses are required. Unexpected credentials are neither parsed nor
used and make the run fail. Tokens, bearer values, raw errors and credentials never
enter output, arguments or files. Output contains only nonsecret context, lineage
and denial observations.

One parent and one fork native run are initially approved, with no automatic retry,
six STS exchanges per run and five-minute job ceilings. Logs have seven-day
retention. The coordinator must first establish accepted active stage-publisher
trust and fresh both-account role/policy inventories, then bind them around each
actual run. Publishing this reusable workflow alone launches nothing.

The coordinator must independently verify completed run/attempt identity, exact
reviewed caller/harness commits and bytes, genuine parent/source lineage and
unchanged AWS RoleId/trust/permission evidence. Parsed claims and imported JSON are
not independent provenance; denial alone does not establish that a role existed.
A rerun requires fresh bracketing evidence and coordinator admission. Parked
production-role denials prove no future active production trust. No observation
itself grants deployment authority.

The owner accepted a genuine isolated fixture-fork native identity as the fork
criterion. This is not a fork PR against the private cloud repository. No PR events,
`pull_request_target`, fork-PR write tokens or PR code execution are used here.
Fixture fork-PR issuance, if later separately approved, would remain distinct from
an AWS denial and from cloud-fork PR evidence. The latter is not claimed by this
fixture.

Fixed AWS role ARNs/account IDs are deliberately nonsecret public metadata.
Do not place credentials, application data or additional code in this fixture.
