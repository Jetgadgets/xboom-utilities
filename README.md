# XBOOM Utilities — DJI Drone Website

A separate website based on the same working structure and visual system as the MoFiMobiles demo, but with a completely different brand/content focus: **XBOOM Utilities**, focused on DJI camera drones.

## Included
- Responsive desktop + mobile design
- DJI-focused product catalogue
- Product filters
- Cart with quantity controls and localStorage
- Sign in: email + password
- Sign up: username + email + password + confirm password
- The signup username is displayed in the header after login
- Demo account flow accepts arbitrary non-empty email/password for testing
- Hidden demo administrator credentials are not displayed in the UI
- Demo checkout/payment screen
- Easy product editing in `products.js`

## Important
This is a front-end demo. Login is browser/localStorage based, not real SSO or server authentication. Payment is also a demo until a real backend/payment provider is connected.

The product prices in `products.js` are **illustrative placeholders**, because no XBOOM price sheet was provided. Replace them with the client's actual prices before delivery.

## Images
The demo uses Wikimedia Commons images remotely. Some files have Creative Commons/public-domain licenses; verify each file's current license and attribution requirements before production use. For a client website, replace these with client-owned/licensed product photographs and use local files under `assets/products/`.

## Run in Termux / Windows
```bash
cd XBOOM_Utilities_Demo
python -m http.server 8080
```
Open: `http://127.0.0.1:8080`

## Main edit points
- `index.html` — layout, branding, text, login/signup flow, checkout UI, contact email
- `products.js` — DJI models, variants, prices, image URLs
- `assets/` — place local licensed/client images here when ready


## Updated payment/demo flow
- Includes a real UPI deep-link QR based on the supplied payment account.
- Cart total is inserted into the UPI intent when the customer taps Open UPI app.
- The “I've completed the test payment” button is presentation-only and simulates verification so the demo can show Payment received → Order confirmation.
- It does NOT independently verify a bank transaction. For production, replace the demo verification with a merchant payment gateway webhook/server verification (e.g. Razorpay/Cashfree or another provider after merchant onboarding).
- Product and account data remain front-end demo data.


Payment: the supplied QR is the real UPI destination. Automatic receipt verification requires a merchant gateway/backend webhook.
