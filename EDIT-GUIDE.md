# XBOOM Utilities — Quick Edit Guide

### 1. Change product details
Open `products.js` and edit:
- `name`
- `variant`
- `price`
- `category`
- `img`

### 2. Change the username display
The signup name is stored in the browser and shown as `Hi, <username>` in the header. This is the key user-facing account feature in this demo.

### 3. Login / signup
Sign in asks for:
- Email
- Password

Sign up asks for:
- User name
- Email
- Password
- Confirm Password

For testing, any non-empty email/password can sign in. A hidden demo administrator credential is also supported internally; it is deliberately not shown anywhere in the website UI.

**Security note:** because this is front-end-only, no credential should be treated as secret. For production, move authentication to a backend and use proper password hashing/session management/OAuth/SSO if required.

### 4. Contact email
In `index.html`, replace `your-email@example.com` with the client's real business email.

### 5. Product images
For production, download/obtain licensed images and use local paths such as:
`assets/products/dji-mini-4-pro.jpg`
Then change `img` in `products.js`.

### 6. Payment
The current QR is intentionally a placeholder. Replace it later with the client's QR or, preferably for production, connect a payment gateway with server-side payment verification.

### 7. Current demo image references
The current source uses Wikimedia Commons images remotely. Check each source's license before commercial use and add attribution where required.
