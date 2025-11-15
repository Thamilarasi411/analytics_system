# Website Analytics System

A FastAPI + Redis Queue + PostgreSQL asynchronous analytics backend.
---
## 🚀 Architecture

### Service 1: Ingestion API
- Accepts POST /event  
- Very fast response  
- Pushes event into Redis queue  

### Service 2: Processor Worker  
- Continuously pulls events from Redis  
- Writes them into PostgreSQL  

### Service 3: Reporting API  
- GET /stats?site_id=xxx&date=2025-11-12  
- Returns aggregated analytics  
---

