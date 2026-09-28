# How AuthNest works

This page explains the idea behind AuthNest without any code, so you can decide whether it fits your project.

## The problem it solves

Every product with user accounts needs the same set of features: sign-up, login, verifying an email address,
resetting a forgotten password, remembering who is signed in, protecting accounts with a second step, and giving
people a place to manage their details. Each of those has security traps. AuthNest builds them once, properly, and
lets many websites use them.

## Who is who

- **You (the "Client")** own a website or app and want accounts on it.
- **Your customers (the "Users")** sign up and log in on your site.
- **AuthNest** provides the sign-up and login pages, checks passwords and codes, keeps sessions safe, and stores the
  account records.

Your website keeps its own data and its own business logic. AuthNest only answers the question *"who is this person,
and have they proven it?"*

## A user's journey

1. A visitor clicks **Sign up** or **Log in** on your website.
2. They arrive on an AuthNest page that is set up for your site: your sign-up form, your login methods, your name.
3. They register or log in. AuthNest verifies their email, checks their password or one-time code, and asks for a
   second step if they turned that on.
4. They are sent back to your website, signed in.
5. Your server asks AuthNest for the verified user's details and carries on.
6. Any time later, the user can open their account area (profile, security, devices) on AuthNest pages. A link
   labelled **Back to your site** brings them home. If they are already signed in on your site, they are not asked to
   log in again.

## A client's journey

1. **Create an account.** New accounts start on the Free plan.
2. **Connect your website.** You register where it lives; AuthNest creates your first API key automatically.
3. **Choose how people sign in** and **design the sign-up form** in your dashboard.
4. **Install an SDK** and add sign-up and login to your pages. See [Get started](GETTING_STARTED.md).
5. **Watch it work.** The dashboard shows users, activity and logs.

## What happens to sessions

- Sign-in produces a short-lived access token and a longer-lived refresh token.
- The refresh token **rotates**: each time it is used, it is replaced. If an old one is ever replayed, the whole
  session is ended. This limits the damage if a token is stolen.
- Tokens are never placed in web addresses. Where a handoff between sites is needed, a single-use code that expires
  within minutes is exchanged instead.
- Logging out ends the session on the server as well as in the browser.

## What AuthNest is, and isn't

**It is** a way to get accounts and their security in place quickly, with sensible defaults and real controls.

**It isn't** a replacement for your own product logic. It does not decide what your users are allowed to see in your
app. It tells you who they are and gives you their verified details.

## Where to go next

- [Features](FEATURES.md) for the complete list
- [Get started in 10 minutes](GETTING_STARTED.md)
- [Security and trust](SECURITY_AND_TRUST.md)
