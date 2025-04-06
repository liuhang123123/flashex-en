# Security Mechanism (OAuth 2.0)

## Is API binding secure?

Absolutely.

FlashEX uses the industry-standard **OAuth 2.0 authorization framework**, widely adopted by banking systems, cloud platforms, and crypto exchanges. It ensures full control over user accounts and absolute fund security. Key security advantages include:

* **No account credentials required**: During the authorization process, users never need to provide exchange login credentials. Authentication is conducted through official channels, reducing the risk of sensitive data exposure.
* **Revocable at any time**: Users can disable or delete their API keys or tokens anytime via the exchange’s backend. FlashEX cannot bypass this mechanism—authorization is always user-controlled.
* **Assets always remain in your exchange account**: FlashEX never holds or accesses user funds. It cannot withdraw or transfer your assets. All trading actions are user-initiated, and FlashEX acts only as an auxiliary execution tool.
* **Minimal permission design**: FlashEX only requests "Read Market Data" and "Place Order" permissions. It never requires withdrawal or fund transfer access. API permissions are clearly presented before authorization.

## **Security is FlashEX's top design principle.**
