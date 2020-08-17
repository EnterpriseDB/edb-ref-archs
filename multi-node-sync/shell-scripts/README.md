![EDB Logo](../../images/logo.png "EDB Logo")

# EDB Reference Architectures

## Multi node database cluster with synchronous replication - Shell script deployment

This directory contains shell scripts for deploying EDB Postgres Advanced 
Server or PostgreSQL in a multi node configuration with syncrhronous 
replication.

### Usage

This deployment is split into two parts:

1. Deploy the hardware
2. Deploy the software

Choose the appropriate script to deploy the virtual machines in your environment
of choice. If you wish to use an environment for which no script is provided
you can either deploy the machines manually or use one of the provided scripts
as a template for your own:

* [Amazon Web Services](deploy-hardware-aws.sh)
* [Google Cloud](deploy-hardware-google.sh)
* [Microsoft Azure](deploy-hardware-azure.sh)

These scripts require that the command line tools for your environment are 
installed on your machine and configured with credentials as appropriate.

Once the hardware is deployed, the [software deployment](deploy-software.sh) 
script should be run as a superuser on each machine.