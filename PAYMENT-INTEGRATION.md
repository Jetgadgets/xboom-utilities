# XBOOM Utilities — Payment setup

## Current client-demo flow
Customer → Cart → Customer details → QR / UPI app → Payment → Presentation confirmation.

### Merchant UPI details in the supplied QR
- UPI ID: `ynotna4168@ptyes`
- Payee: `Mr Antonyraj J E`
- Currency: INR
- The supplied QR has no fixed amount. The **Open UPI app** link adds the current cart amount dynamically.

## Real automatic verification
A static HTML/JavaScript site cannot read a bank account or independently prove that a UPI payment was received.

Production architecture:
`Customer → Merchant payment gateway/UPI → provider webhook → backend verification → order marked PAID → confirmation`

The merchant must onboard with the chosen payment provider. Never put secret API keys in front-end JavaScript.

The current confirmation screen is deliberately labelled as a **presentation confirmation**. It can demonstrate the intended customer journey after a real payment, but automatic payment confirmation requires the gateway/backend integration above.
