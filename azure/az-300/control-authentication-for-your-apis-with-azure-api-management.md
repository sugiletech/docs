- [Control authentication for your APIs with Azure API Management](#control-authentication-for-your-apis-with-azure-api-management)
  - [Methods to secure access to an API in Azure API Management:](#methods-to-secure-access-to-an-api-in-azure-api-management)
    - [Subscriptions](#subscriptions)
      - [Subscription Key](#subscription-key)
      - [Scope of Subscriptions](#scope-of-subscriptions)
    - [Client Certificates](#client-certificates)
      - [TLS Client Authentication](#tls-client-authentication)

# Control authentication for your APIs with Azure API Management

## Methods to secure access to an API in Azure API Management:

### Subscriptions

- Subscriptions are used to segment the access levels to an API

#### Subscription Key

- `A subscription key` is a `unique auto-generated key` that can be passed through in the `headers` of the client request or as a `query string` parameter.
- Every subscription has two keys, a `primary` and a `secondary`
- You can regenerate these subscription keys at any time
- Developers can obtain a key by submitting a `subscription request`
- The default header name is `Ocp-Apim-Subscription-Key`, and the default query string is `subscription-key`

#### Scope of Subscriptions

| **Scope**   | **Details**                        |
| :---------- | ------------------------------ |
| All APIs    | Applies to every API accessible from the gateway|
| Single API  | Applies to a single imported API and all of its endpoints|
| Product     | A product                       |



### Client Certificates

- Can be used to provide `TLS mutual authentication` between the client and the API gateway
- The `authorization` at the gateway level is handled through `inbound policies`


#### TLS Client Authentication

- API Management gateway can inspect the certificate contained within the client request and check for properties like Certificate Authority, Thumbprint, Subject, Expiry Date etc.
- Two common ways to `verify a certificate`
  - Check who issued the certificate. You can configure the `trusted certificate authorities` in the Azure portal to automate this process.
  - If the certificate is issued by the partner, verify that it came from them. For example, if they deliver the certificate in person, you can be sure of its authenticity. These are known as `self-signed certificates`

