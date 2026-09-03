# Data Science & Stats Tutor

An interactive 10-week Statistics, Linear Models & Python Data Science course, with a landing/pricing page and Razorpay checkout.

## Structure

- **`index.html`** — Landing & pricing page. Includes plan selection, demo sign-in/sign-up (stored locally in the browser), a Razorpay Standard Checkout integration, and a feedback form.
- **`course.html`** — The full interactive course: 9 modules (descriptive statistics, probability, OLS/linear regression, ML, time series, etc.), live Python/SQL playground, calculators, cheat sheets, an AI chatbot tutor, and a feedback section.

## Payments (Razorpay)

`index.html` ships with Razorpay's **public test key** (`rzp_test_1DP5mmOlF5G5ag`) by default, so payments won't actually charge anyone out of the box. To go live:

1. Open the deployed site and click **"Payment settings (admin)"** at the bottom of the pricing section.
2. Paste in your own Razorpay **Key ID** (`rzp_live_...` for real payments, or your own `rzp_test_...` for testing).

This is stored in the browser's `localStorage`, so it needs to be set once per browser/device you administer from.

> **Note:** this is a *client-side only* Razorpay Standard Checkout integration — there's no backend order creation or payment signature verification. It's suitable for getting started quickly, but for production use at scale you'd typically add a small backend to create orders server-side and verify payment signatures via Razorpay's webhooks/APIs.

## Feedback

Both pages include a feedback form that emails submissions to the instructor via [FormSubmit](https://formsubmit.co/) — no backend required. The first submission triggers a one-time confirmation email that must be approved.

## Deploying

This is a static site — any static host works (GitHub Pages, Netlify, Vercel, etc.). For GitHub Pages: **Settings → Pages → Deploy from branch → `main` / root**.
