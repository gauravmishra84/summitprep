# Presentation Deck

## Agenda

#### Background and the Problem Statement

#### How are we using best of Snowflake and Iceberg for Lakehouse Generalisation

#### How it drives efficiency and interoprability across platforms

#### Q&A



## Problem Statement

#### Data Silos: 
  Traditional architectures require copying data between platforms
#### Metadata Synchronization: 
  Multiple catalogs become out of sync
#### Cost Inefficiency: 
  Replicating large datasets is expensive
#### Workload Specialization: 
  Different engines excel at different types of processing
#### Governance Complexity: 
  Scattered data means scattered governance
#### Interoperability: 
  Seamless working across multiple platform with shared data access


## Why Iceberg?

## Why Multiple Catalogs?


## Interoparability across catalogs - Approach
  
##### A unified S3-based lakehouse platform that:
  
  * Stores all data in Apache Iceberg format on S3
  * Uses AWS Glue as the central metadata catalog
  * Connects multiple execution engines directly to the same data
  * Routes workloads to the most appropriate engine
  * Synchronizes metadata changes back to the central catalog


