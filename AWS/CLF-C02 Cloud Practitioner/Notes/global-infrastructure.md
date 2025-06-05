# Understanding Global Infrastructure

## How AWS physically and logically structures it's data centers, connectivity, and service availability across the world. 

### 1. Region
- Geographical Area
- Contains Isolate Availability Zones
- Ex: us-east-1, eu-west-2
- Many resources are region-scoped
- Pick your region based on compliance, cost, and customer proximity

### 2. Availability Zone (AZ)
- Physically separate data center (or group) within a region
- Each region has 2-3 AZs
- Ex: us-east-1a, us-east-1b, us-east-1c
- Always design multi-AZ architectures for high availability (at a minimum)

### 3. Edge Location
- Used by CloudFront, Route 53, and Global Accelerator
- Caches content closer to end users
- Over 400+ globally, not tied to regions
- CDN: Content Delivery Network