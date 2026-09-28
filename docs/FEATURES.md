# Features

Which plan includes each feature can change as we grow. The [pricing page](https://authnest.org/pricing) is always the
source of truth. Where a feature depends on setup or plan, this page says so.

## Signing in

| Feature | Notes |
|---|---|
| Email and password | Passwords are stored only as salted hashes. |
| Social sign-in | **Google and GitHub** are available. Microsoft, Facebook, LinkedIn, Discord, GitLab and Apple are built and are being switched on one at a time after real-world testing. Plan-dependent. |
| One-time codes and magic links | Sign in with a code or a link sent by email. Plan-dependent. |
| SMS one-time codes | Plan-dependent, and it needs an SMS service to be configured. |
| Passkeys | Sign in with a fingerprint, face or device PIN, with no password to steal. |
| Second step (MFA) | Authenticator app codes, passkeys as a second factor, and backup codes for emergencies. |
| Safe social login rules | A social sign-in never skips a user's second step, and an existing account is only linked when the provider confirms the email is verified. |

## Signing up and recovery

- **Sign-up form you design.** Choose the standard fields and add your own.
- **Email verification** with a one-time code.
- **Password recovery** with several recovery options.
- **Consent records.** Acceptance of terms and the privacy policy version are recorded with a timestamp.

## What your users get

Ready-made pages, so you do not have to build any of them:
profile, security settings, signed-in devices, activity log, notifications and a support page. Users move between
your site and these pages without feeling they have left.

## What you get (your dashboard)

- **Analytics** for sign-ups and activity.
- **User list** and **logs** for your own account activity and your users' activity.
- **Login methods** page: pick social providers and passwordless methods; see which plan unlocks what.
- **Bulk user import** (CSV or JSON) to move existing users over, with existing password hashes supported so people
  do not have to reset their passwords. Row limits depend on your plan.
- **Team members.** Invite colleagues to help manage your account.
- **Mobile redirect settings** for React Native and Expo apps.
- **Custom login domain** (top plan).
- **Billing page** for your subscription.

## Look and feel

- **Theme Studio** (top plan): matching navigation bars, footers and full-page themes, including 3D options, so
  the pages your users see match your brand.
- **Legal pages settings** in your dashboard, for your own terms and privacy pages.

## Security and visibility

- Activity and audit logs, for you and for your users.
- Threat detection and risk-based extra checks (plan-dependent).
- Exporting security events to your own monitoring system (SIEM), per client (plan-dependent).
- Sensitive actions ask people to confirm their identity again if they signed in a while ago.

Details: [Security and trust](SECURITY_AND_TRUST.md).

## Reach and accessibility

- **Six languages** in the core sign-up and login flows: English, Hindi, Spanish, French, Mandarin Chinese and
  Arabic, with a proper right-to-left layout for Arabic. Some pages deeper in the site are still English only.
- An **accessibility toolbar** and a published accessibility statement.

## For developers

- Three SDKs: [server, React and client](SDKS.md).
- A machine-readable description (OpenAPI) of the end-user API.
- Documentation at [authnest.org/docs](https://authnest.org/docs/introduction).

## Transparency

- A public [status page](https://authnest.org/status).
- A public [changelog](https://authnest.org/changelog) and [roadmap](https://authnest.org/public-roadmap).
