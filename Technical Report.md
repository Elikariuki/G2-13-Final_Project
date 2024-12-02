# Introduction

This report provides a detailed migration strategy for the existing infrastructure of GlobalTech Solutions. The report outlines a comprehensive overview of the planned transition to a new cloud-based platform. The report will describe the proposed cloud infrastructure and the step-by-step migration plan using Microsoft Azure. By leveraging Azure's services, GlobalTech Solutions will achieve enhanced scalability, performance, and compliance with international regulations.

## Migration Strategy for SQL Database Cluster on Azure

### High-Level Architecture Diagram

### Migration Phases
Phase 1: Assessment


### Phase 2: Planning
The table below shows the timeframe required for each task in the planning phase. The tasks can run concurrently, but the total duration is approximately 8-14 weeks

1. Shortest Possible Duration: 7 weeks (if all tasks are done in parallel and without delays)
2. Longest Possible Duration: 14 weeks (considering potential overlaps and delays)



| **Component**                          | **Task**                         | **Estimated Time** |
|----------------------------------------|----------------------------------|--------------------|
| **Rehosting using Azure Migrate**      |                                  |                    |
|                                        | Assessment and Planning          | 1-2 weeks          |
|                                        | Replication and Migration        | 2-4 weeks          |
|                                        | Testing and Validation           | 1-2 weeks          |
|                                        | **Total Estimated Time**         | **4-8 weeks**      |
| **ERP System (Microsoft Dynamics 365)**|                                  |                    |
|                                        | Planning and Setup               | 2-4 weeks          |
|                                        | Data Migration                   | 2-4 weeks          |
|                                        | Configuration and Customization  | 2-4 weeks          |
|                                        | Training and Go-Live             | 1-2 weeks          |
|                                        | **Total Estimated Time**         | **7-14 weeks**     |
| **SQL Database**                       |                                  |                    |
|                                        | Assessment and Planning          | 1-2 weeks          |
|                                        | Data Migration                   | 2-4 weeks          |
|                                        | Testing and Optimization         | 1-2 weeks          |
|                                        | **Total Estimated Time**         | **4-8 weeks**      |
| **Mainframe System**                   |                                  |                    |
|                                        | Assessment and Planning          | 2-4 weeks          |
|                                        | Rehosting and Migration          | 4-6 weeks          |
|                                        | Testing and Validation           | 2-4 weeks          |
|                                        | **Total Estimated Time**         | **8-14 weeks**     |




Phase 3: Execution


Phase 4: Validation


Phase 5: Optimization and Handover


### Recommendations for Tools and Services


### Address Legacy System Modernization


### Cost Estimation
3y reserved
Azure hybrid for everything

#### virtual machines
- 50 vms - 20 Canada central, 20 Sweden central, 10 south east Asia linux
- d2s v3, 8GB ram

#### ERP system 
3 micro services: 
- microsoft dynamics 365 supply chain management: 
- microsoft dynamics 365 finance: 210/user
- microsoft dynamics 365 intelligent order management: 

#### Payroll and reporting system
Web App Services: 1
Canada central
Tier: standard
Instance: S2

#### e-commerce applications
AKS:
- 3 clusters: high availability, failover
- D4AS standard
- vm 4-5 linux
- tier: standard

#### Database:
- 9 sql db: 2 (ERP) + 5(e-commerce applications) + 1 (customer and operational data)
one for each micro services, best practices, recommended to avoid bottleneck
Bussines critical
stanand Series Gen5
8v cores
geo replica
Geo redundancy
storage data 32GB  
- 2 cosmos db: ERP + payroll
multi-region: Canada central, Sweden central, south east Asia
- 1 general storage account for everything else: Sweden central
blog storage
standrad
geo-redandunt
1TB
3y reserved
- Azure Monitor:
Sweden central
- Vnets 2:
Sweden central ->Canada central, Sweden central -> south east Asia
- load balancer 3: 
Sweden central Canada central  south east Asia
tier: standard
- application gateway 3: Sweden central Canada central  south east Asia
standard v2
- VPN gateway 3: Sweden central Canada central  south east Asia
basic vpn
- traffic manager
Canada central
3 endploints
- retention policy
1 interactive retention - default
31 days - free
- DDos
Canada central
Tier:network protection
Vnets 

- Migration Tool:
1. Azure Migrate - free
2. Azure database Migration services - free
Canada central
standard

Total $44,532.92


### Compliance and Security

