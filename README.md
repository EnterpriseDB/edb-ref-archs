![EDB Logo](images/logo.png "EDB Logo")

# EDB Reference Architectures

## Introduction

This repository contains reference architectures and supporting materials and 
code for the deployment of 
[EDB Postgres Advanced Server](https://www.enterprisedb.com/products/edb-postgres-advanced-server-secure-ha-oracle-compatible),
[PostgreSQL](https://www.postgresql.org) and related tools for high availability,
monitoring, and management.

## Selecting an Architecture

The reference architectures offered are split into the core database server
and a number of optional add ons.

Each database server architecture is designed to meet different needs and 
requirements, offering a range of scalability and availability and redundancy
options offering different levels of:

* [Recovery Time Objective](https://en.wikipedia.org/wiki/Disaster_recovery#Recovery_Time_Objective) (RTO)
* [Recovery Point Objective](https://en.wikipedia.org/wiki/Disaster_recovery#Recovery_Point_Objective) (RPO)
* Geographic Redundancy Objective (GRO)
* [Target Availability](https://en.wikipedia.org/wiki/Availability)

Select and implement the most appropriate reference architecture to meet your
needs, and then implement one or more of the Add On options to provide the
additional functionality you require.

### Database Clusters

* [Single node](single-node/README.md)
* [Multi node with asynchronous replication](multi-node-async/README.md)
* [Multi node with synchronous replication](multi-node-sync/README.md)

Architecture     | Redundancy | Automatic Failover | Multi node commit | Recommended Use                                 |
-----------------|:----------:|:------------------:|:-----------------:|-------------------------------------------------|
Single Node      | No         | No                 | No                | Development/testing                             |
Multi Node Async | Yes        | Yes                | No                | Production, with transaction loss acceptable    |
Multi Node Sync  | Yes        | Yes                | Yes               | Production, with no transaction loss acceptable |

### Add Ons

* [Load balancing with pgBouncer](pgbouncer/README.md)
* [Load balancing and query routing with pgPool](pgpool/README.md)
* [Monitoring with EDB PEM](edb-pem/README.md)
* [Backup & Recovery with EDB BART](edb-bart/README.md)

## Improvements and Issues

If you want to suggest any improvements or report any problems you may have 
found, please create a 
[Pull Request](https://github.com/EnterpriseDB/edb-ref-archs/pulls) or log an
[Issue](https://github.com/EnterpriseDB/edb-ref-archs/issues).

## License

The contents of this repository are licensed under the 
[PostgreSQL License](LICENSE.md).