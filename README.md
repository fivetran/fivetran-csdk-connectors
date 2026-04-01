<p align="center">
  <a href="https://www.fivetran.com/">
    <img src="https://cdn.prod.website-files.com/6130fa1501794ed4d11867ba/63d9599008ad50523f8ce26a_logo.svg" alt="Fivetran">
  </a>
</p>

<p align="center">
  Fivetran Connector SDK allows Real-time, efficient data replication to your destination of choice.
</p>

<p align="center">
  <a href="https://github.com/fivetran/fivetran-csdk-connectors/stargazers" target="_blank"><img src="https://img.shields.io/github/stars/fivetran/fivetran-csdk-connectors?style=social&label=Star"></a>
  <a href="https://github.com/fivetran/fivetran-csdk-connectors/blob/main/LICENSE" target="_blank"><img src="https://img.shields.io/badge/License-MIT-blue" alt="License"></a>
  <a href="https://github.com/fivetran/fivetran-csdk-connectors/blob/main/README.md" target="_blank"><img src="https://img.shields.io/badge/Managed-Yes-green/" alt="Managed"></a>
</p>

# Fivetran Connector SDK - Connector Catalog

Explore practical examples and ready-to-use connectors for building custom data connectors with the Fivetran [Connector SDK](https://fivetran.com/docs/connectors/connector-sdk). This repository contains 100+ community-contributed connectors and helpful resources to extend Fivetran's capabilities to fit your data integration needs.

## Overview

This repository is a comprehensive catalog of connector examples demonstrating how to integrate various data sources with Fivetran using the Connector SDK. Whether you're looking to connect to a specific database, API, or data source, you'll find practical examples and patterns to get started quickly.

For SDK installation and setup, visit the main [Fivetran Connector SDK repository](https://github.com/fivetran/fivetran_connector_sdk).

## Why Connector SDK?

Fivetran Connector SDK allows you to code a custom data connector using Python and deploy it as an extension of Fivetran. Fivetran automatically manages running Connector SDK connections on your scheduled frequency and manages the required compute resources, eliminating the need for a third-party provider.

Connector SDK provides native support for many Fivetran features and relies on existing Fivetran technology. It also eliminates timeout and data size limitations seen in AWS Lambda.

## Requirements

- Python version ≥3.10 and ≤3.14
- Operating system:
  - Windows: 10 or later (64-bit only)
  - macOS: 13 (Ventura) or later (Apple Silicon [arm64] or Intel [x86_64])
  - Linux: Distributions such as Ubuntu 20.04 or later, Debian 10 or later, or Amazon Linux 2 or later (arm64 or x86_64)

## Getting Started

1. **Install the Connector SDK**: See [Setup guide](https://fivetran.com/docs/connectors/connector-sdk/setup-guide) to get started.
2. **Choose a connector example**: Browse the [community connectors](#community-connectors) below to find an example similar to your use case.
3. **Customize and deploy**: Modify the connector code to fit your requirements and deploy using the Fivetran CLI.

Run the `.github/scripts/setup-hooks.sh` script from the root of the repository to set up pre-commit hooks. This ensures that your code is formatted correctly and passes all tests before you commit them.
## Community Connectors

> Note: To simplify the processes of building and maintaining connectors with Connector SDK, we've removed the need to use the Python generator pattern with Connector SDK operations, `yield`, starting with Connector SDK version 2.0.0. This change is fully backward compatible, so your existing Connector SDK connections will continue to function without modification. For more information, refer to our [Connector SDK release notes](https://fivetran.com/docs/connector-sdk/changelog#august2025).

These are ready-to-use connectors, requiring minimal modifications to get started. Browse by category or search for your specific data source:

<details class="details-heading" open="open">
<summary>📋 Full List of Connectors (98 connectors)</summary>

### Databases

- **[apache_hbase](apache_hbase)** - Connect and sync data from Apache HBase using happybase and thrift libraries
- **[apache_hive/using_pyhive](apache_hive/using_pyhive)** - Sync data from Apache Hive using PyHive
- **[apache_hive/using_sqlalchemy](apache_hive/using_sqlalchemy)** - Sync data from Apache Hive using SQLAlchemy with PyHive
- **[arango_db](arango_db)** - Sync document and edge collections from ArangoDB multi-model database
- **[cassandra](cassandra)** - Connect and sync data from Cassandra database
- **[clickhouse](clickhouse)** - Sync data from ClickHouse database
- **[couchbase_capella](couchbase_capella)** - Sync data from Couchbase Capella
- **[couchbase_magma](couchbase_magma)** - Sync data from self-managed Couchbase Server using Magma storage
- **[dgraph](dgraph)** - Sync e-commerce product catalog from Dgraph graph databases
- **[documentdb](documentdb)** - Connect to AWS DocumentDB and sync collections (Hybrid Deployment compatible)
- **[dolphin_db](dolphin_db)** - Sync data from DolphinDB database
- **[dragonfly_db](dragonfly_db)** - Sync high-performance in-memory data from DragonflyDB
- **[firebird_db](firebird_db)** - Sync data from Firebird DB
- **[greenplum_db](greenplum_db)** - Sync data from Greenplum database
- **[ibm_db2](ibm_db2)** - Connect and sync data from IBM Db2 using ibm_db library
- **[ibm_informix_using_ibm_db](ibm_informix_using_ibm_db)** - Connect and sync data from IBM Informix
- **[influx_db](influx_db)** - Sync time-series data from InfluxDB
- **[neo4j](neo4j)** - Extract data from Neo4j graph databases
- **[quest_db](quest_db)** - Sync high-performance time series data from QuestDB
- **[raven_db](raven_db)** - Sync document data from RavenDB NoSQL database
- **[redis](redis)** - Sync gaming leaderboards and player statistics from Redis
- **[rethink_db](rethink_db)** - Sync data from RethinkDB real-time database
- **[sap_hana_sql](sap_hana_sql)** - Connect to SAP HANA SQL Server using hdbcli
- **[sql_server](sql_server)** - Connect to SQL Server using pyodbc
- **[teradata](teradata)** - Sync data from Teradata Vantage database
- **[tidb](tidb)** - Incremental replication from TiDB databases
- **[timescale_db](timescale_db)** - Sync time-series and vector data from TimescaleDB
- **[yugabyte_db](yugabyte_db)** - Sync data from YugabyteDB distributed SQL database

### Cloud Data Warehouses

- **[aws_athena/using_boto3](aws_athena/using_boto3)** - Sync data from AWS Athena using Boto3
- **[aws_athena/using_sqlalchemy](aws_athena/using_sqlalchemy)** - Sync data from AWS Athena using SQLAlchemy with PyAthena
- **[aws_dynamo_db_authentication](aws_dynamo_db_authentication)** - Connect and sync data from AWS DynamoDB
- **[aws_rds_oracle](aws_rds_oracle)** - Connect and sync data from AWS Oracle
- **[redshift/simple_redshift_connector](redshift/simple_redshift_connector)** - Sync records from Redshift
- **[redshift/large_data_volume](redshift/large_data_volume)** - Sync large data volumes from Redshift
- **[redshift/using_unload](redshift/using_unload)** - Sync data from Redshift using UNLOAD to S3

### Message Queues & Streaming

- **[apache_pulsar](apache_pulsar)** - Fetch data from Apache Pulsar topics with Reader API
- **[gcp_pub_sub](gcp_pub_sub)** - Sync data from Google Cloud Pub/Sub
- **[rabbitmq](rabbitmq)** - Sync messages from RabbitMQ queues
- **[solace](solace)** - Sync messages from Solace queue

### SaaS & APIs

- **[awardco](awardco)** - Sync data from Awardco rewards platform
- **[betterstack](betterstack)** - Sync uptime monitoring data from Better Stack
- **[checkly](checkly)** - Sync monitoring check data and analytics from Checkly
- **[clerk](clerk)** - Sync user data from Clerk authentication
- **[commonpaper](commonpaper)** - Sync agreement data from Common Paper
- **[courier](courier)** - Sync notifications data from Courier multi-channel platform
- **[customer_thermometer](customer_thermometer)** - Sync customer feedback from Customer Thermometer
- **[data_camp](data_camp)** - Sync course catalog from DataCamp LMS
- **[discord](discord)** - Sync data from Discord
- **[docusign](docusign)** - Sync data from Docusign eSignature API
- **[elastic_email](elastic_email)** - Sync email marketing data from Elastic Email
- **[fleetio](fleetio)** - Sync fleet management data from Fleetio
- **[fred](fred)** - Sync economic data from Federal Reserve Economic Data (FRED)
- **[github](github)** - Sync repository data, commits, and pull requests from GitHub
- **[github_traffic](github_traffic)** - Sync GitHub repository traffic data
- **[gnews](gnews)** - Sync news articles from GNews API
- **[google_trends](google_trends)** - Sync search interest data from Google Trends
- **[goshippo](goshippo)** - Sync shipment data from Goshippo API
- **[grey_hr](grey_hr)** - Sync HR data from greytHR API
- **[gumroad](gumroad)** - Sync sales, products, and subscribers from Gumroad
- **[harness_io](harness_io)** - Connect and sync data from Harness.io
- **[healthchecks](healthchecks)** - Sync health check monitoring from Healthchecks.io
- **[hubspot](hubspot)** - Sync event data from HubSpot
- **[iterate](iterate)** - Sync NPS survey data from Iterate REST API
- **[keycloak](keycloak)** - Sync IAM data from Keycloak Admin API
- **[leavedates](leavedates)** - Sync leave report data from LeaveDates API
- **[mailerlite](mailerlite)** - Sync email marketing data from MailerLite
- **[mastertax](mastertax)** - Sync data from MasterTax API
- **[meilisearch](meilisearch)** - Sync index metadata and documents from MeiliSearch
- **[microsoft_excel](microsoft_excel)** - Sync data from Microsoft Excel files
- **[microsoft_intune](microsoft_intune)** - Retrieve managed devices from Microsoft Intune
- **[n8n](n8n)** - Sync workflow automation data from n8n
- **[netlify](netlify)** - Sync sites, deploys, and forms from Netlify API
- **[newsapi](newsapi)** - Sync news articles from NewsAPI
- **[noaa](noaa)** - Sync weather observations from National Weather Service
- **[npi_registry](npi_registry)** - Sync healthcare provider data from NPPES NPI Registry
- **[oauth2_and_accelo_api_connector_multithreading_enabled](oauth2_and_accelo_api_connector_multithreading_enabled)** - Sync data from Accelo API with OAuth 2.0 and multithreading
- **[odata_api](odata_api)** - Sync data from OData APIs (versions 2 and 4)
- **[oktopost](oktopost)** - Sync social media exports from Oktopost BI API
- **[owasp_api_vulns](owasp_api_vulns)** - Sync OWASP API vulnerability data from NVD 2.0
- **[partech](partech)** - Sync POS data from Partech (formerly Punchh)
- **[pindrop](pindrop)** - Sync nightly report data from Pindrop
- **[prefect](prefect)** - Sync workflow orchestration data from Prefect Cloud
- **[prometheus](prometheus)** - Sync metrics and time series from Prometheus
- **[resend](resend)** - Sync email data from Resend API
- **[s3_csv_validation](s3_csv_validation)** - Read and validate CSV files from Amazon S3
- **[sam_gov](sam_gov)** - Sync government contracting opportunities from SAM.gov
- **[sap_ariba](sap_ariba)** - Sync procurement data from SAP Ariba
- **[sendcloud](sendcloud)** - Sync shipment data from Sendcloud API
- **[sensor_tower](sensor_tower)** - Sync mobile app market intelligence from Sensor Tower
- **[sensource](sensource)** - Sync traffic and occupancy metrics from SenSource
- **[similarweb](similarweb)** - Sync website performance metrics from SimilarWeb
- **[smartsheets](smartsheets)** - Sync sheets and reports from Smartsheets
- **[snipeitapp](snipeitapp)** - Sync IT asset management data from Snipe-IT
- **[status_cake](status_cake)** - Sync uptime monitoring from StatusCake
- **[suitedash](suitedash)** - Sync CRM data from SuiteDash API
- **[supabase](supabase)** - Sync employee data from Supabase database
- **[talon_one](talon_one)** - Sync events data from Talon.One
- **[toast](toast)** - Sync POS data from Toast
- **[tulip_interfaces](tulip_interfaces)** - Sync data from Tulip Tables
- **[veeva_vault/basic_auth](veeva_vault/basic_auth)** - Authenticate to Veeva Vault with basic auth
- **[veeva_vault/session_id_auth](veeva_vault/session_id_auth)** - Authenticate to Veeva Vault with session ID
- **[vercel](vercel)** - Sync deployment data from Vercel REST API
- **[zigpoll](zigpoll)** - Sync polling data from Zigpoll

</details>

## Documentation & Resources

- **[_template_connector](_template_connector)** - Reference template for building new connectors
- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Guide for contributing to this repository
- **[PYTHON_CODING_STANDARDS.md](PYTHON_CODING_STANDARDS.md)** - Python coding standards and best practices
- **[FIVETRAN_CODING_PRINCIPLES.md](FIVETRAN_CODING_PRINCIPLES.md)** - Code review principles and PR guidelines
- **[Connector SDK Documentation](https://fivetran.com/docs/connectors/connector-sdk)** - Official SDK documentation
- **[Connector SDK Best Practices](https://fivetran.com/docs/connector-sdk/best-practices)** - Best practices guide

## Contributing

We welcome contributions from the community! Whether you want to add a new connector, improve existing ones, or fix bugs, your contributions are appreciated.

Please read our [CONTRIBUTING.md](CONTRIBUTING.md) guide for detailed information on:
- How to fork and create a pull request
- Coding standards and guidelines
- Testing requirements
- Review process

## Issue

Found an issue? Submit an [issue](https://github.com/fivetran/fivetran-csdk-connectors/issues) and get connected to a Fivetran developer.

## Support

Learn how we [support Fivetran Connector SDK](https://fivetran.com/docs/connector-sdk#support).

## Additional Considerations

We provide examples to help you effectively use Fivetran's Connector SDK. While we've tested the code provided in these examples, Fivetran cannot be held responsible for any unexpected or negative consequences that may arise from using these examples.

Note that API calls made by your Connector SDK connection may count towards your service's API call allocation. Exceeding this limit could trigger rate limits, potentially impacting other uses of the source API.

It's important to choose the right design pattern for your target API. Using an inappropriate pattern may lead to data integrity issues. We recommend that you review all our examples carefully to select the one that best suits your target API. Keep in mind that some APIs may not support patterns for which we currently have examples.

As with other new connectors, SDK connectors have a [14-day trial period](https://fivetran.com/docs/getting-started/free-trials#newconnectorfreeuseperiod) during which your usage counts towards free [MAR](https://fivetran.com/docs/usage-based-pricing). After the 14-day trial period, your usage counts towards paid MAR. To avoid incurring charges, pause or delete any connections you created to run these examples before the trial ends.

## Maintenance

The `fivetran-csdk-connectors` repository is actively maintained by Fivetran Developers. Reach out to our [Support team](https://support.fivetran.com/hc/en-us) for any inquiries.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
