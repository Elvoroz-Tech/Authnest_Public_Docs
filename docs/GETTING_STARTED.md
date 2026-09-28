# Get started in 10 minutes

You will need a website or app of your own (even a small test one is fine) and, for the SDK steps,
[Node.js](https://nodejs.org) installed.

## 1. Create your account

Go to **[authnest.org/client/signup](https://authnest.org/client/signup)**, fill in your details and verify your
email with the code we send you. New accounts start on the **Free plan**. No card is needed.

## 2. Connect your website

When you sign up, you tell AuthNest the address of your website and of its server. AuthNest creates your first
**API key** and **secret key** for it automatically.

> **Keep the secret key on your server only.** Never put it in front-end code, a public repository or a screenshot.
> If it leaks, replace it from your dashboard.

## 3. Choose how people sign in

Open **Login methods** in your dashboard and switch on the methods you want. Then open the **sign-up form** settings to
choose which fields your users are asked for.

## 4. Install an SDK

Pick what fits your project ([details](SDKS.md)):

```
npm install @elvoroz/authnest-server     # Node.js / Express backend
npm install @elvoroz/authnest-react      # React front end
npm install @elvoroz/authnest-client     # any JavaScript app, React Native, Expo
```

## 5. Add sign-up and login to your pages

Follow the short guide in the documentation for your stack:
**[authnest.org/docs/introduction](https://authnest.org/docs/introduction)**.
In outline: your page sends the visitor to AuthNest to sign up or log in, AuthNest sends them back signed in, and your
server reads the verified user.

## 6. Try it as a user

Open your site in a private window, sign up with a test email, log out, and log in again. Then look in your dashboard:
you should see the new user and their activity.

## If something doesn't work

| Symptom | Likely cause |
|---|---|
| Users are sent back to the wrong place after login | The website addresses registered in your dashboard don't match where your site is running. |
| The server can't read the user | The API key or secret key is missing or wrong in your server's environment. |
| A login method isn't showing | It isn't switched on, or your plan doesn't include it. The Login methods page says which plan unlocks it. |
| The verification email doesn't arrive | Check spam, then try resending. If it still fails, tell us. |

Still stuck? [Ask a question](../../../issues/new/choose) or use [contact us](https://authnest.org/contact-us).
**Early users get personal help.** Tell us your stack and we will help you get it working.
