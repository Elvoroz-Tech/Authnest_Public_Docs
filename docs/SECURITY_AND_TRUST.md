# Security and trust

An authentication service is only worth using if you can trust it. This page explains, in plain language, how
AuthNest protects accounts, **and what we do not claim**. If something here is unclear, ask us. We would rather
answer a hard question than have you guess.

## Passwords

- Passwords are never stored as text. They are turned into salted hashes using **bcrypt**, with a configurable cost
  (the default is deliberately slow to make guessing expensive).
- New client accounts must meet a strong password rule: length, upper and lower case, a number and a symbol.
- Clients can set a stronger policy for their own team.

## Sessions and tokens

- **Short-lived access tokens** and **rotating refresh tokens**. Each use of a refresh token replaces it. If an old
  one is replayed, the whole session is ended.
- **Tokens never appear in web addresses.** Where two sites must hand a user over, a single-use code that expires
  within minutes is exchanged.
- **Logging out ends the session on the server**, not only in the browser.
- **Sensitive actions ask for a recent sign-in.** If you signed in a while ago and try something risky, you are asked
  to confirm your identity again.

## Second step (MFA)

- **Authenticator-app codes.** A code that was already accepted cannot be used again.
- **Passkeys**, built on the WebAuthn standard using well-known open-source libraries rather than home-made
  cryptography. Each passkey has a counter, so a cloned device can be detected.
- **Backup codes** for the day a phone is lost.
- Social sign-in **never skips** a user's second step.

## Social sign-in safety

- A social account is linked to an existing account **only if the provider confirms the email address is verified**.
  Providers that don't give that guarantee can never take over an existing account.
- Redirect addresses for mobile apps must match exactly what the client registered.

## Platform hardening

- Security headers with a content security policy.
- Protection against database-injection style attacks on incoming data.
- Cross-site request forgery protection.
- Rate limiting on sensitive endpoints, to slow down guessing and abuse.
- Separate keys for each client, and dynamic cross-origin rules per client.

## Watching what happens

- **Audit logs** record important account and administrative actions, and clients can see their own and their users'
  activity.
- Clients on plans that include it can **send security events to their own monitoring system** (SIEM).
- Threat detection and risk-based extra checks are available on higher plans.

## How we run the team side

- New administrator accounts **must be approved by a Super Admin** before they can sign in.
- Administrator powers are **limited by role**. Only a Super Admin can do the most sensitive things, such as approving
  other administrators or changing platform-wide settings.
- Actions taken by administrators are **logged**.

## Payments

When paid plans are switched on, card details are entered on the **payment provider's own hosted checkout**
(Stripe or Razorpay). **AuthNest's servers never receive card numbers, expiry dates or security codes.** We keep only
the small, non-sensitive details that providers give back, such as the last four digits and card brand.

## What we do **not** claim

We think honesty matters more than a long list of badges.

- We are **not** SOC 2, ISO 27001, HIPAA or PCI certified. We have prepared internal documentation toward some of
  these and we will tell you when an independent audit is complete.
- Our security reviews so far have been done by us. We have not yet had an independent third-party audit.
- We do not publish an uptime guarantee (SLA) yet. Current health is on the [status page](https://authnest.org/status).
- No system is unbreakable. We work to reduce risk, watch for problems, and fix issues quickly and openly.

## Found a problem?

Please tell us privately. See [SECURITY.md](../SECURITY.md). Good-faith reports are welcome and we will credit you if
you wish.

## Related

[Privacy and your data](PRIVACY_AND_DATA.md) · [How it works](HOW_IT_WORKS.md) · [FAQ](FAQ.md)
