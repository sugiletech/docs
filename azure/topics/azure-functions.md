# Azure Functions

> - FaaS (Functions as a Service)
> - Supports C#, JavaScript etc.
> - Connect to any database

## Function Apps

- Unit of deployment
- Contains multiple functions
- Share common configurations
- Scale together
- Logically related

## Triggers

- Http Request
- Timer (Schedule using CRON time string format)
- Message / Queue
- Blob
- Cosmos DB
- Service Bus

## Bindings

- Removes boilerplate code
- Several built-in bindings / More available as extension
- Defined in function.json
- Supports Queue/CosmosDB/SendGrid/Blob/ServiceBus/TableStorage etc.

### Input Bindings

- Blog, Cosmos DB

### Output Bindings

- Queue, SendGrid

## Serverless Architecture

- Simpler
- Per-second billing
- Monthly Free Grant
- AutoScale

## Development Environment

- Azure Portal
- Visual Studio
- Azure Functions Core Tools (Cross Platform - VSCode)

## Security

- Manual Validation
- Function Keys / API Keys
- Identity Provider Integration

## Durable Functions

- Define Workflows
- Run tasks in parallel
- Retries and Error Handling

## Proxies

- Route incoming requests
- Static Website
- Request/Response Transformation
- Stored in proxies.json

## Deployment

### Manual

- Visual Studio or VS Code
- Create a new Function App
- Publish to a ne or an existing Function App

### Git

- Automated deployment
- Configure in portal
- GitHub or VSTS

### Zip

- Kudu API
- Azure Functions Core Tools
- Azure CLI
- Best choice for CI/CD

## Hosting Options

### Consumtion Plan

- Per second

### Azure AppService Plan

- Reserved Servers
- Monthly billing

### Azure Function Containerization

- Cloud agnostic (On-premise / Other cloud providers)
- Consistent deployment model
- Azure Container Instance (ACI)
- Azure Kubernetes Service
- No AutoScale
- No Consumption Plan
- Not connected to Azure Services by default
