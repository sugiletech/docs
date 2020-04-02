# Azure API Management

- Helps organizations unlock the potential of their data and services by publishing APIs to external partners, and internal developers.
- Enables you to carefully identify and control who can access the data published by your APIs
- Provides the core competencies to ensure a successful API program through developer engagement, business insights, analytics, security, and protection. You can use APIM to take any backend and launch a full-fledged API program based on it.

## Steps:

- Administrators define APIs in the portal
- Each API consists of one or more operations, and can be added to one or more products.Each API consists of one or more operations, and can be added to one or more products.
- To use an API, developers subscribe to a product that contains that API, and then call the API's operation, subject to any usage policies that might be in effect.
 
 ## Components

 ### API Gateway - is the endpoint that

 - Accepts API calls and routes them to the backend.
 - Verifies API keys, JWT tokens, certificates, and other credentials
 - Enforces usage quotas and rate limits.
 - Transforms your API on the fly without code modifications.
 - Caches backend responses where set up.
 - Logs call metadata for analytics purposes.

### Azure Portal

- Administrative interface where you set up your API program
- Used to:
  - Define or import API schema.
  - Package APIs into products.
  - Set up policies such as quotas or transformations on the APIs.
  - Get insights from analytics.
  - Manage users.

### Developer Portal

- Serves as the main web presence for developers
- Used to:
  - Read API documentation.
  - Try out an API via the interactive console.
  - Create an account and subscribe to get API keys.
  - Access analytics on their own usage.

## Terms

### Product

- Collection of one or more APIs that you configure in API Management
- You can assign APIs to more than one product
- Products can have different access rules, usage quotas, and terms of use
- You use the Azure portal to associate APIs with a product