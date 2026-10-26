# Security Policy

## Scope and deployment boundary
This repository is a fork/derivative of NorskHelsenett's ROR-API. It integrates with infrastructure such as Vault, Valkey, RabbitMQ, MongoDB and OIDC. A successful build or candidate rehearsal does not certify a deployment, integration or health-data workflow as secure.

## Data and secrets
- Use synthetic test data for local development and rehearsals.
- Never commit production credentials, Vault tokens, OIDC secrets, private keys, patient data or environment files.
- Review `.env.example`, Compose profiles, Vault policies, OIDC scopes, network exposure and secret rotation before deployment.
- Candidate/release workflows must not publish a release or artifact unless the documented approval and verification gates pass.
- Do not expose optional UI/admin tools or development ports to untrusted networks.

## Reporting
For vulnerabilities affecting the upstream project, use NorskHelsenett's official security-reporting process. For fork-specific issues, use GitHub private vulnerability reporting if enabled or contact the maintainer privately. Include the affected commit and a redacted reproduction; never attach live health data or credentials.

## Verification limits
CI, integration rehearsals and release-candidate checks cover only their configured scenarios. They are not a full threat model, penetration test, privacy assessment or production approval.
