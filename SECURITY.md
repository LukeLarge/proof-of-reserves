# Security Policy

This repository implements components of a Merkle‑based Proof‑of‑Reserves verification system.  
Because the code interacts with cryptographic primitives, hashing, and user‑provided configuration files, we maintain strict security expectations for contributors and users.

---

## Supported Versions

Security updates are provided only for actively maintained branches.

| Version | Status |
|--------|--------|
| master | Supported |
| dev / feature branches | Supported (best‑effort) |
| archived tags | Not supported |

---

## Security Principles

- **No private keys or secrets** may ever be committed to this repository.  
- **Deterministic builds** and **reproducible verification** are required for all PoR‑related code.  
- **Cryptographic integrity** must never be weakened, replaced, or bypassed.  
- **User‑provided configs** (e.g., `user_config.json`) must be treated as untrusted input.  
- **Hashing, Merkle proofs, and circuit logic** must remain transparent, auditable, and verifiable.  
- **Dependencies** must be kept current and monitored for CVEs.

---

## Reporting a Vulnerability

If you discover a vulnerability that affects:

- Merkle tree construction or verification  
- Hashing or proof validation logic  
- Circuit integrity  
- Dependency security  
- Input‑validation or file‑handling issues  
- Any behavior that could misrepresent Proof‑of‑Reserves results  

please report it privately.

### How to Report

Send an email to:

**security@<your‑org‑domain>.com**  
(Replace with your actual security inbox.)

Include:

- A clear description of the issue  
- Steps to reproduce  
- Impact assessment (if known)  
- Relevant logs, stack traces, or proof files  
- Suggested remediation (optional)

### Response Expectations

- You will receive an acknowledgment within **72 hours**.  
- A triage decision will be provided within **7 days**.  
- Valid vulnerabilities will be assigned a severity rating and tracked internally.  
- Fixes for critical issues will be prioritized and patched as quickly as possible.  
- You will be notified when the issue is resolved or if more information is required.

---

## Responsible Disclosure

We request that you:

- Do **not** publicly disclose vulnerabilities until a fix is released.  
- Do **not** exploit or weaponize discovered issues.  
- Do **not** test against production systems without permission.  

We commit to:

- Treating all reports seriously  
- Maintaining transparency about fixes  
- Crediting researchers who request acknowledgment  

---

## Security Hardening for Contributors

Before submitting a PR:

- Run `go vet`, `go test`, and static analysis tools  
- Avoid introducing new dependencies unless necessary  
- Ensure no sensitive data is logged or written to disk  
- Validate all user‑provided input  
- Maintain compatibility with existing verification workflows  
- Document any cryptographic changes clearly

---

## Additional Notes

This repository does **not** store user balances, private keys, or exchange‑side data.  
It only provides **client‑side verification logic** for Merkle‑based Proof‑of‑Reserves.

