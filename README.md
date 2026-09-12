# plaid-oauth-redirect

A single blank page that exists to satisfy one Plaid requirement.

Plaid will not redirect a bank's OAuth login to `localhost`: the redirect URI
has to be a public HTTPS address. moneymap, the app this serves, runs only on
its owner's own Mac. This page bridges the two by handing the URL the bank
produced back to the local app.

It holds no data, sets no cookies, stores nothing, and makes no requests. The
destination is hardcoded rather than read from the URL, so it cannot be used as
an open redirect.

Served at <https://subashbhu.github.io/plaid-oauth-redirect/>.
