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

### Apache Iceberg: The Foundation

  * Open table format designed for massive analytic datasets
  * Provides ACID transactions and time travel capabilities
  * Schema evolution and partition evolution
  * Hidden partitioning and metadata handling
  * Optimized for cloud object stores like S3
  * Supported by multiple execution engines

Reasoning: Iceberg provides critical capabilities for a multi-engine architecture:

* Transaction support prevents data corruption when multiple engines write
* Schema evolution allows engines to evolve tables independently
* Snapshot isolation ensures consistent reads during writes
* Metadata handling is optimized for cloud storage performance

## Interoparability across catalogs - Approach

##### Centralized Governance and Consistency
  * Single Source of Truth
  * Uniform Data Governance
    
##### Interoperability Between Compute Engines
  * Seamless Read Access
  * Supporting Heterogeneous Write Workloads

##### Performance and Operational Flexibility
  * Observability and Benchmarking
  * Workload Isolation

##### Future-proofing and Agility
  * Adaptability to Protocol Advances
  * Reduced Lock-in Risks

##### Enhanced Data Lakehouse Integrity
  * Metadata Synchronization as a Key Consistency Mechanism
  * Ecosystem Validation
    
##### A unified S3-based lakehouse platform that:
  
  * Stores all data in Apache Iceberg format on S3
  * Uses AWS Glue as the central metadata catalog
  * Connects multiple execution engines directly to the same data
  * Routes workloads to the most appropriate engine
  * Synchronizes metadata changes back to the central catalog


