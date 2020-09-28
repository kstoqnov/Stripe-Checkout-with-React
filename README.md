# Accept payments with Stripe Checkout

The CheckoutSessions API allows for dynamic amounts and line items but requires a server to create the session.

<img src="https://storage.googleapis.com/stripe-samples-flow-charts/checkout-one-time-client-server.png" alt="A flowchart of the Checkout flow" align="center">

# .env config

# Stripe API keys
STRIPE_PUBLISHABLE_KEY=pk_
STRIPE_SECRET_KEY=sk_

# Required to run webhook
# See README on how to use the Stripe CLI to setup
STRIPE_WEBHOOK_SECRET=whsec_2020

STATIC_DIR=../../client/html 

# Create a Price on Stripe using the Dashboard or API 
PRICE=price_2020
DOMAIN=http://localhost:4242
# DOMAIN="http://localhost:3000" # When using the React client

# Supported payment methods for the store.
# Some payment methods support only a subset of currencies.
PAYMENT_METHODS="card"
# PAYMENT_METHODS="card, ideal" # Requires CURRENCY=eur
# PAYMENT_METHODS="card, fpx" # Requires CURRENCY=myr
