# Product Photography via Shopify

```mermaid
sequenceDiagram
participant Shopify Admin
participant Shopify Photo App
participant Photographer's App
participant Raw Photo Storage
participant Photo Instance

Shopify Admin->>Shopify Photo App: Shopify Admin sends request for photos to Shopify Photo App
Shopify Photo App->>Photographer's App: Shopify Photo App sends enriched and encrypted request to Photographer's App
Photographer's App->>Raw Photo Storage: Query for all unenriched leads
Raw Photo Storage->>Photo Instance: Enrich and Score Lead the same as in the New Lead Process
Photo Instance->>Shopify Photo App: Lower load photos are available for Merchant reivew and are sent to Shopify Photo App
Shopify Photo App->>Shopify Admin: Instances of photos are uploded, Shopify sends a notification to Merchant that photo previews are available for review
Shopify Admin->>Shopify Photo App: Mercahtn requests another set of photos
```
