# Product Photography via Shopify

```mermaid
sequenceDiagram
participant Shopify Admin
participant Shopify Photo App
participant Photographer's App
participant Raw Photo Storage
participant Photo Instance
Shopify Admin->>Shopify Photo App:Shopify Admin sends request for photos to Shopify Photo App
Shopify Photo App->>Photographer's App:Shopify Photo App sends enriched and encrypted request to Photographer's App
Photographer's App->>Raw Photo Storage:Raw photos of images are stored via CDN or S3 or somethin’
Raw Photo Storage->>Photo Instance:Thumbnails are created, maybe via Sidekiq, to show merchant for preview. Also makes raw images available upon approval from Merchant
Photo Instance->>Shopify Photo App: Lower load photos are available for Merchant review and are sent to Shopify Photo App
Shopify Photo App->>Shopify Admin: Instances of photos are uploaded, Shopify sends a notification to Merchant that photo previews are available for review
Shopify Admin->>Shopify Photo App: Merchant requests another set of photos

