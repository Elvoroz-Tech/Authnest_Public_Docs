# Frequently asked questions

## The basics

**What is AuthNest?**
A hosted service that adds sign-up, login, account security and user management to your website. See
[How it works](HOW_IT_WORKS.md).

**Who is it for?**
Developers, small teams, freelancers and agencies who want accounts working quickly and securely.

**Is it free?**
There is a **Free plan** you can start on today. Paid plans add more capacity and features, and they are listed on the
[pricing page](https://authnest.org/pricing).

**Do I need a card to try it?**
No. You can create an account and use the Free plan without one.

## Trust

**Why is this repository documentation only?**
AuthNest is a hosted commercial service and its source code is private. This repository exists so you can read how
it works, how it is secured and where it is heading before you sign up.

**Is it open source?**
No. The platform and SDKs are proprietary and owned by Elvoroz. The SDKs are free to install, but they are licensed and not sold, and using them needs an AuthNest account. See [LICENSE](../LICENSE) and the license inside each package.

**Can I use the SDKs in a client's website, or in an app I sell?**
Yes. You may include the SDK, unmodified, in an application that connects to AuthNest, including one you build for a client, as long as it's used to work with the service. You can't publish or redistribute the SDK on its own, or use it with another service. The precise terms are in each package's license.

**You're new. Why should I trust you?**
Fair question. You don't have to take our word for it:
1. Try the Free plan on a test project.
2. Read [Security and trust](SECURITY_AND_TRUST.md), including the section on what we do **not** claim.
3. Check the [status page](https://authnest.org/status), [changelog](https://authnest.org/changelog) and
   [roadmap](https://authnest.org/public-roadmap).
4. Keep your own product logic separate from AuthNest so that you are never locked in, and ask us how to plan a
   move if that matters to you.

**Is it certified (SOC 2, ISO 27001…)?**
Not yet, and we say so plainly. See [Security and trust](SECURITY_AND_TRUST.md).

**What happens if AuthNest has an outage?**
Users can't sign in while it is down. We publish live health on the [status page](https://authnest.org/status). We do
not offer an uptime guarantee yet.

## Using it

**Which technologies does it work with?**
A Node.js/Express server SDK, a React SDK, and a framework-independent JavaScript client that also supports
**React Native and Expo**. See [SDKs](SDKS.md).

**Can I move my existing users over?**
Yes. A bulk import (CSV or JSON) is available on plans that include it, and existing password hashes are supported so
users don't have to reset their passwords.

**Which sign-in methods are supported?**
Email and password, Google and GitHub, one-time codes, magic links, and passkeys, with more social providers being
switched on step by step. Some depend on your plan. See [Features](FEATURES.md).

**Which languages are supported?**
English, Hindi, Spanish, French, Mandarin Chinese and Arabic (right-to-left) in the core sign-up and login flows.

**Can I brand the pages my users see?**
You can design the sign-up form and choose your login methods. On the top plan, Theme Studio lets you match the pages
to your brand.

## Data

**Who owns my users' data?**
You do. See [Privacy and your data](PRIVACY_AND_DATA.md).

**Do you store card numbers?**
No. Payments use the provider's own hosted checkout.

## Getting help

**How do I get help?**
See [SUPPORT.md](../SUPPORT.md). Early users get personal help getting set up.

**How do I report a security problem?**
Privately, as described in [SECURITY.md](../SECURITY.md).

**Something I need isn't there.**
Tell us with a [feature request](../../../issues/new/choose). Requests from real users shape the
[roadmap](ROADMAP.md).
