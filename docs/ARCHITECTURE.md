# Architecture — Authenticator

## Architecture status

**A similarly named auth repository was listed but not readable via the connected action; a separate public authentik fork is NOT evidence that it is the intended Authenticator project.**

## Public high-level flow

```text
Concept only: device authenticator interface ↔ approved identity service; actual security architecture requires source verification
```

## Verified high-level design

Do not implement real TOTP/passkey/security features on the strength of mock documentation. A genuine release would require independent security design, threat modeling, protected key storage, clock-drift strategy and audit.

## Technology references

- Actual Authenticator application framework not verified
- Authentication protocols and storage mechanisms not verified

## Trust boundaries

1. The public showcase is a separate documentation/presentation boundary. It is not authorized to access production accounts or protected datasets.
2. Authentication, authorization, storage operations and confidential business rules, if applicable, belong to private reviewed services—not public mock UI.
3. An iframe is a nested browser context, not a substitute for server authentication or entitlement checks.
4. Device frames alter dimensions and appearance, not actual native runtime behavior.

## Unverified or intentionally omitted

- No statement of MFA standards compliance, cryptographic correctness, security review or App Store availability.
- Never store or publish OTP seeds, backup codes, signing secrets, issuer metadata or real QR enrollment payloads.

## Security/design review before going live

- [ ] Confirm any referenced architecture is approved for public disclosure.
- [ ] Use invented demo identifiers, content and accounts.
- [ ] Verify no private URL or client organization names appear in HTML, CSS, JS, screenshots or history.
- [ ] Test browser permissions and iframe CSP on the actual demo host.
- [ ] Confirm accessibility and responsive behavior separately on representative devices.
