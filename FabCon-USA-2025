# Post FabCon USA 2025 review

[Fabric March 2025 Feature Summary](https://blog.fabric.microsoft.com/en-us/blog/fabric-march-2025-feature-summary)

## Deployements, CI/CD, DataOps

### 🎉 Variable libraries

Placeholder to store and share configuration values between Fabric artefacts (Data Pipelines, Notebooks, shortcuts) at the workspace level. Used to simplify CI/CD deployments, by being directly available in Git repositories, and thanks to value sets. Learn documentation: [What is a Variable library?](https://learn.microsoft.com/en-us/fabric/cicd/variable-library/variable-library-overview), [Tutorial: Use Variable libraries to customize and share item configurations](https://learn.microsoft.com/en-us/fabric/cicd/variable-library/tutorial-variable-library)

Jun 2025: support in notebooks, thru notebookutils (`notebookutils.variableLibrary`)

### Service Principal Support

The service principals can be used to authenticate for some Fabric REST APIs, like:

- [Deployment Pipelines](https://learn.microsoft.com/en-gb/rest/api/fabric/core/deployment-pipelines)
- [Git](https://learn.microsoft.com/en-gb/rest/api/fabric/core/git)
- And Admin APIs
- [Git automation](https://learn.microsoft.com/fabric/cicd/git-integration/git-automation)
- [Pipeline Automation in Fabric](https://learn.microsoft.com/fabric/cicd/deployment-pipelines/pipeline-automation-fabric)
- [Fabric CICD Python library](https://microsoft.github.io/fabric-cicd/latest/)

### Deployement pipelines

Support for Spark Job Definition. The links to lakehouses are configurable through deployment rules.

### Branch-out to new workspace

New option to create a new Workspace linked to the new feature branch. It can also be linked to an existing workspace.

⚠️ Need to check if the Contributor role is sufficient and if all the parameters of the worksapce are replicated (default configuration, caoacity, ...)

### Pureview and Data Loss Prevention feature

New sources for Purview Data Governance

Data Loss Prevention policies for Fabric (Lakehouses, KQL Databases, Mirrored Databases) and Power BI.

More information: [Get started with Data loss prevention policies for Fabric and Power BI](https://learn.microsoft.com/en-gb/purview/dlp-powerbi-get-started)

### Fabric domain and tags

Tags are generally availables
Enhancements to domain, like dedicated image gallery.
📢 Soon tags at the domain level.

### Folder REST APIs

Adding support for Workspace Folder management with a new REST API and the following features: dreate, delete, get, list, move or update folders.
The Item API also support the Workspace Folder management.

### 🎉🎉 Microsoft Fabric SKU estimator

Estimate the rigt size for the Fabric SKU and the Power BI licences for a Fabric Data Platform: [Link to Microsoft Fabric SKU Estimator](https://www.microsoft.com/en-us/microsoft-fabric/capacity-estimator)

### Other

- 🎉🎉 Fabric CLI [documentation](http://aka.ms/Fabric-CLI)

    ```powershell
    pip install ms-fabric-cli
    fab auth login
    fab ls
    ```

- Fabric Terraform (GA)
- Fabric ci-cd Python library
- Fabric VS Code extension, for User Data Functions, Notebooks, Lakehouses (does not yet manage GIT integration)
- April 2025: use of Azure Key Vault references in data connections [Azure Key Vault Reference – Overview](https://learn.microsoft.com/fabric/data-factory/azure-key-vault-reference-overview)
- Build 2025: Full support for SPN with Fabric REST API
- Build 2025: Cross-Tenant support for Azure DevOps 

### Workloads

Workload hub
Workload Development Kit enhencement

## Security

### Private link

- Ability to use Private Link at the workspace level, avoiding to activate at the tenant level. Preview available in early summer [Connect to your most sensitive data with end-to-end network security in Fabric](https://blog.fabric.microsoft.com/en-us/blog/connect-to-your-most-sensitive-data-with-end-to-end-network-security-in-fabric)
- Outbound access protection for Spark
- Customer managed keys in Fabric

[Security in Fabric](https://learn.microsoft.com/en-gb/fabric/security/security-overview)

## OneLake

### 🎉🎉 OneLake Security

OneLake security replaces the OneLake data access roles preview feature.

Capabilities:

- Security roles,
- Grant precise permissions
- RLS / CLS
- Restrict acces to Personal Identifiable Information

Applied to OneLake and spread to all other Fabric engines and tools, includinf SQL Endpoints (Lakehouse and Warehouse).

👉 [Sign-up for early access](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR_BIbobSVbtGoFFUDM3gfGJUNlBWWVpMNDU5NzY5U1NBQVFHOUJPNE5CNS4u)

Two modes for identification:

- User Identity Mode
- Delegated Identity Mode (identity of the workspace or artifact owner)

  |Capability|User Identity Mode|Delegated Identity Mode|
  |---|---|---|
  |Access Context|Signed-in User|Datawarehouse Owner|
  |OneLake RLS/CLS/OLS|Enforced|Not Enforced|
  |SQL GRANT on Tables|Not Allowed|Allowed|
  |SQL GRANT on Views/Procedures|Allowed|Allowed|
  |Dynamic Data Masking|Not Supported|Supported|
  |Custom SQL Roles|Not Supported|Supported|

More information: [The next evolution of OneLake security (Preview)](https://blog.fabric.microsoft.com/en-us/blog/the-next-evolution-of-onelake-security-enters-early-preview)

### Shorcuts

- Shortcut definitions are now saved to the Git repository: [Lakehouse deployment pipelines and git integration (Preview)](https://learn.microsoft.com/en-gb/fabric/data-engineering/lakehouse-git-deployment-pipelines)
- Use of KeyVault references for securing accesses to data behind shortcuts
- Shortcuts are now updatable
- Support for Fabric SQL Databases
- CI/CD and batch creation operations
- External data sharing: share data behind the shortcuts hrough Fabric Datashare
- SPN support for OneLake shortcuts using Trusted Access
- April 2025: Shortcut connections and management from a lakehouse
- April 2025: Shortcyt cache (limit the egress for external cloud providers)
- Build 2025: [Shortcuts transformation](https://aka.ms/ShortcutTransformations) (invalid link)

## Data Engineering

### Spark connector fro Fabric Datawarehouse

New capabilities, like read and write data to the Fabric Warehouse directly with the Spark connector: [Spark connector for Microsoft Fabric Data Warehouse](https://learn.microsoft.com/en-gb/fabric/data-engineering/spark-data-warehouse-connector?tabs=pyspark). Does not work with private links and restricted public access.

### 🎉🎉 Fabric User Data Functions

Serverless platform to build and run functions. Custom logic is embedded in functions, with native integration with Fabric data sources, Notebooks and Data pipelines.

[What is Fabric User data functions (Preview)?](https://learn.microsoft.com/en-gb/fabric/data-engineering/user-data-functions/user-data-functions-overview)

Youtube video: <https://go.microsoft.com/fwlink/?linkid=2307709>

UDF can be called using `Notebookutils`

April 2025: use of custom libraries and SPN
Build 2025: 14 new regions availale, including France Central and West Europe
Build 2025: [SPN support for User data functions](https://blog.fabric.microsoft.com/en-us/blog/21638)
Build 2025: Private libraries support for User data functions

### UDF in Warehouse

- User Data Functions in private preview: call the User Data Functions (Pyhton) from the SQL Endpoints
- Scalar-value and Table-value User Defined Functions: regular T-SQL reusable code, like in SQL Server. Scalar-value functions are available in preview. Table-value functions will come later. Three types of functions are available:
  - SQL: classical UDF functions written in T-SQL,
  - Fabric: Python code / Fabric User Data Functions,
  - AI: leverage advanced AI capabilities bqsed on large language models (LLMs).

👉 [Forms to access preview](https://aka.ms/FabricDWFunctionsPreviewForm)

June 2025: AI Functions are available directly in Fabric Runtime 1.3. Copilot helps to scaffold the code. [Documentation](https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas)

### Warehouse

- SQL audit logs (Preview) in Data Warehouse: Detailed record of warehouse activity, such as when events occur, which triggered them, and the T-SQL statement behind the event.
- Support for HINTS in joins and queries: [Hints in Fabric Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/20036)
- [Query insights in Fabric Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/unlock-the-power-of-query-insights-and-become-a-fabric-data-warehouse-performance-detective)
- [SHOWPLAN_XML in Fabric Data Warehouse (Preview)](https://blog.fabric.microsoft.com/en-us/blog/query-plans-in-fabric-data-warehouse)
- Migration tool to migrate from Azure Synapse Datawarehouse: [Fabric Migration Assistant for Data Warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/migration-assistant) / [Migrate with the Fabric Migration Assistant for Data Warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/migrate-with-migration-assistant)
- April 2025: use of #temp tables in SQL scripts (for distribution, add `WITH (DISTRIBUTION=ROUND_ROBIN);` to the table definition)
- Migrate Azure Synapse Warehouse to Fabric with the migration assistant: [how-to](https://learn.microsoft.com/fabric/data-warehouse/migrate-with-migration-assistant)
- Build 2025: Warehouse Snapshots (Preview)

### Lakeshouse

- 🎉🎉🎉🎉 Build 2025: [Materialized Lake Views](https://blog.fabric.microsoft.com/en-us/blog/announcing-materialized-lake-views-at-build-2025)

  - Simplify complex ETL to process data from Bronze to Gold, with SQL Statements, and incremental by design.
  - Built-in data quality with constraints

June 2025 [Documentation & preview](https://learn.microsoft.com/en-gb/fabric/data-engineering/materialized-lake-views/overview-materialized-lake-view)

### Data Factory

- VNET Data Gateway support in Fabric Pipeline Copy and Copy Jobs: [What is a virtual network (VNet) data gateway?](https://learn.microsoft.com/en-gb/data-integration/vnet/overview)
- Copy Job GA
- Upsert in Copy Jobs for Azure SQL Db and SQL Server
- Overwrite in Copy Jobs for Lakehouse
- Trigger Data Pipelines based on a OneLake event*
- Run Spark Jobs from Data Pipelines
- Parameters for Azure Databricks jobs and Dataflows
- Build 2025: Native change data capture (CDC) support in Copy Job (Preview) [Link](https://learn.microsoft.com/fabric/data-factory/what-is-copy-job)
- June 2025: connect to Azure Function, User Data Function via OPDG or VNetDG.

### Fabric SQL Databases

- Backup billing, starting April 1st: [Automatic backups in SQL database in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/database/sql/backup)
- Performance Dashboard: lead blocking query
- Terraform CRUD Support: manage Fabric SQL database ***service*** with Terraform. To deploy the *content*, a DAC PAC file can be used: [SqlPackage for SQL database in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/database/sql/sqlpackage)
- Data pipeline enhancements: create a table from an activity, call a stored procedure, or script...

### Mirroring

- Mirroring for Azure SQL DB behind a firewall, with VNET Data Gateway or On-Premise Data Gateway
- Mirroring for Azure Database for PostgreSQL Flexible Server
- Open Mirroring UI: quickstart on CSV or Parquet files: [Tutorial: Configure Microsoft Fabric open mirrored databases](https://learn.microsoft.com/en-gb/fabric/database/mirrored-database/open-mirroring-tutorial)
- Build 2025: Preview of SQL Server and SQL Server 2025 Mirroring
- Build 2025: GA of Open Mirroring
- Build 2025: Connect to Azure SQL MI behind a firewall with VNet Data Gateway or OPDG
- Build 2025: customize data retention period

### Dataflows

- VNET Data Gateway support in Fast Copy in Dataflow Gen 2: [What is a virtual network (VNet) data gateway?](https://learn.microsoft.com/en-gb/data-integration/vnet/overview)
- Save as Dataflow Gen 2 for Dataflow Gen 1, Gen 2 or Gen 2 (CI/CD)
- [Incremental refresh for Dataflow Gen 2](https://blog.fabric.microsoft.com/blog/fabric-march-2025-feature-summary#post-20656-_Toc193974256)
- Use of public parameters in Dataflow Gen 2 CI/CD ([source](https://blog.fabric.microsoft.com/en-us/blog/passing-parameter-values-to-refresh-a-dataflow-gen2-preview))
- Build 2025: Dataflow Gen 2 CI/CD GA
- Build 2025: Dataflow Gen2 Public APIs (Preview)
- Build 2025: Dataflow Gen2 parameterization (Preview)
- Build 2025: SharePoint files as a destination in Dataflow Gen2 (Preview)

### Notebooks

- [High concurrency mode in Apache Spark for Fabric](https://learn.microsoft.com/en-us/fabric/data-engineering/high-concurrency-overview)
- June 2025:  `%%tsql` magi command to interact with SQL Database, Warehouse and Lakehouse (readonly), with 3 parameters:
  - `-artifact`: the name of the source
  - `-type`: the type of the source
  - `-bind`: the name of the variable for the resulting dataset
  - `-workspace`: the name of the workspace, if the artifact is located in another workspace

## Real Time Intelligence

### New sources for Event Stream

MQTT, Solace, ADX, weather & Azure Event Grid

### Azure and Fabric Events (GA)

Type of events:

- [Onelake events](https://aka.ms/FE-onelake-overview),
- [Azure blob storage events](https://aka.ms/FE-blob-overview),
- [Job events](https://aka.ms/FE-jobs-overview),
- [Workspace item events](https://aka.ms/FE-item-overview)

Filter events

Connect to Activator, for real time action, or Event Stream to stream the events to other destinations.

### Other

- Managed private endpoints
- Automated schema optimization. automatic type inferrence, with change recommandations
- Eventhouse OneLake availability now supports backfill
- Redesigned alerts (Activator) in Power BI reports
- Migrate Azure Synapse Data Explorer to Eventhouse
- Leverage RTI capabilities for monitoring, based on Fabric events, or KQL queries alerts

## AI & Copilot

Copilot and AI Capabilities will be accessible to all paid SKUs in Microsoft Fabric

### Fabric data agent

Fabric data agent is the new name of AI skill

It is integrated with Azure AI Agent Service from Azure AI Foundry. This allows the agent to query the unstructured data from Azure AI Search or SharePoint but also the structure data from OneLake.

Build 2025: Fabric Data Agent Integration with Microsoft Copilot Studio (Preview)

### AI functions in Data Warehouse (private preview)

Summarize content, translate text, extract key data, analyze sentiment, and more with T-SQL language

## Power BI

- Power BI Desktop performance improvment
- Get the reference of the object in a PBIR file structure: `Go to File > Options and settings > Report settings > Report objects and check the box next to ‘Copy object names when right clicking on report objects’`.
- 🎉🎉🎉 Create semantic models in Direct Lake storage mode from one or more Fabric artifacts in Power BI Desktop: `With the preview feature turned on, select a Lakehouse or Warehouse from the OneLake catalog then Connect.`
- TMDL view support for Direct Lake semantic models (Preview): [Work with TMDL view in Power BI Desktop (preview)](https://learn.microsoft.com/power-bi/transform-model/desktop-tmdl-view)
- Use notebooks with your semantic model (Preview)
- Build 2025: Copilot in Power BI now supports Fabric data agents
- Build 2025: [Translytical preview](https://powerbi.microsoft.com/en-us/blog/announcing-translytical-task-flows-preview/) 

## General

- Build 2025: [Fabric Roadmap](https://roadmap.fabric.microsoft.com/)

## Links

- [x] [Fabric March 2025 Feature Summary](https://powerbi.microsoft.com/en-gb/blog/power-bi-march-2025-feature-summary/)
- [x] [DataOps in Fabric Data Factory](https://blog.fabric.microsoft.com/en-us/blog/data-operations-in-fabric-data-factory)
- [x] [Best-in-class connectivity and data movement with Data Factory in Fabric](https://blog.fabric.microsoft.com/en-us/blog/best-in-class-connectivity-and-data-movement-with-data-factory-in-microsoft-fabric)
- [x] [Folder REST API (Preview)](https://blog.fabric.microsoft.com/en-us/blog/announcing-the-public-preview-of-folder-rest-api)
- [x] [New Eventstream sources: MQTT, Solace PubSub+, Azure Data Explorer, Weather & Azure Event Grid](https://blog.fabric.microsoft.com/en-us/blog/new-eventstream-sources-mqtt-solace-pubsub-azure-data-explorer-weather-event-grid)
- [x] [Workload Development Kit – OneLake support and Developer Experience enhancements](https://blog.fabric.microsoft.com/en-us/blog/workload-development-kit-announcing-onelake-support-and-developer-experience-enhancements)
- [x] [Announcing Fabric User Data Functions (Preview)](https://blog.fabric.microsoft.com/en-us/blog/announcing-fabric-user-data-functions-in-public-preview)
- [x] [Utilize User Data Functions in Data pipelines with the Functions activity (Preview)](https://blog.fabric.microsoft.com/en-us/blog/utilize-user-data-functions-in-data-pipelines-with-the-functions-activity)
- [x] [What’s new with OneLake shortcuts](https://blog.fabric.microsoft.com/en-us/blog/whats-new-with-onelake-shortcuts)
- [x] [Hints in Fabric Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/20036)
- [x] [Unlock the Power of Query insights and become a Fabric Data Warehouse performance detective](https://blog.fabric.microsoft.com/en-us/blog/unlock-the-power-of-query-insights-and-become-a-fabric-data-warehouse-performance-detective)
- [x] [SHOWPLAN_XML in Fabric Data Warehouse (Preview)](https://blog.fabric.microsoft.com/en-us/blog/query-plans-in-fabric-data-warehouse)
- [x] [Playbook for metadata driven Lakehouse implementation in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/playbook-for-metadata-driven-lakehouse-implementation-in-microsoft-fabric)
- [x] [Secure, comply, collaborate: Item Permissions in Fabric Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/secure-comply-collaborate-item-permissions-on-fabric-data-warehouse)
- [x] [Introducing SQL Audit Logs for Fabric Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/introducing-sql-audit-logs-for-fabric-datawarehouse)
- [x] [Introducing the Fabric CLI (Preview)](https://blog.fabric.microsoft.com/en-us/blog/introducing-the-fabric-cli-preview)
- [x] [CI/CD and REST APIs for Fabric Eventstream (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/announcing-the-general-availability-of-ci-cd-and-rest-apis-for-fabric-eventstream)
- [x] [Build event-driven workflows with Azure and Fabric Events (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/build-event-driven-workflows-with-azure-and-fabric-events-now-generally-available)
- [x] [Seamlessly connect Azure Logic Apps to Fabric Eventstream using Managed Identity](https://blog.fabric.microsoft.com/en-us/blog/seamlessly-connect-azure-logic-apps-to-fabric-eventstream-using-managed-identity)
- [x] [Another dimension of Functions in Data Warehouse](https://blog.fabric.microsoft.com/en-us/blog/functions-in-data-warehouse)
- [x] [Exciting New Features for Mirroring for Azure SQL in Fabric](https://blog.fabric.microsoft.com/en-us/blog/exciting-new-features-for-mirroring-for-azure-sql-in-fabric)
- [x] [Revolutionizing Enterprise Network Security: support for VNET Data Gateway in Data pipeline and more (Preview)](https://blog.fabric.microsoft.com/en-us/blog/revolutionizing-enterprise-network-security-support-for-vnet-data-gateway-in-data-pipeline-and-more)
- [x] [High Concurrency mode for notebooks in pipelines (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/announcing-general-availability-of-high-concurrency-mode-for-notebooks-in-pipelines)
- [x] [Supercharge your workloads: write-optimized default Spark configurations in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/supercharge-your-workloads-write-optimized-default-spark-configurations-in-microsoft-fabric)
- [x] [Supporting Database Mirroring sources behind a firewall](https://blog.fabric.microsoft.com/en-us/blog/supporting-database-mirroring-sources-behind-a-firewall)
- [x] [Open Mirroring UI enhancements and CSV support to help you get started today](https://blog.fabric.microsoft.com/en-us/blog/open-mirroring-ui-enhancements-and-csv-support-to-help-you-get-started-today)
- [x] [What’s new for SQL database in Fabric?](https://blog.fabric.microsoft.com/en-us/blog/whats-new-for-sql-database-in-fabric)
- [x] [Terraform Provider for Microsoft Fabric (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/terraform-provider-for-microsoft-fabric-now-generally-available)
- [x] [Simplify Your Data Ingestion with Copy Job (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/simplify-your-data-ingestion-with-copy-job-general-availability-announcement)
- [x] [Simplify your Warehouse ALM with DacFx integration in Git and Deployment pipelines for Fabric Warehouse](https://blog.fabric.microsoft.com/en-us/blog/simplify-your-warehouse-alm-with-dacfx-integration-in-git-and-deployment-pipelines-for-fabric-warehouse)
- [x] [AI Ready Apps: build RAG Data pipeline from Azure Blob Storage to SQL Database in Microsoft Fabric within minutes](https://blog.fabric.microsoft.com/en-us/blog/ai-ready-apps-build-rag-data-pipeline-from-azure-blob-storage-to-sql-database-in-microsoft-fabric-within-minutes)
- [x] [Mirroring in Fabric – What’s new](https://blog.fabric.microsoft.com/en-us/blog/whats-new-with-mirroring-in-microsoft-fabric)
- [x] [Copilot and AI Capabilities will be accessible to all paid SKUs in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/copilot-and-ai-capabilities-now-accessible-to-all-paid-skus-in-microsoft-fabric)
- [x] [Fabric Data Factory: What’s New and Latest Roadmap](https://blog.fabric.microsoft.com/en-us/blog/whats-new-with-fabric-data-factory-and-roadmap)
- [x] [The next evolution of OneLake security (Preview)](https://blog.fabric.microsoft.com/en-us/blog/the-next-evolution-of-onelake-security-enters-early-preview)
- [x] [Migration Assistant for Fabric Data Warehouse (Preview)](https://blog.fabric.microsoft.com/en-us/blog/public-preview-of-migration-assistant-for-fabric-data-warehouse)
- [x] [Empowering agentic AI by integrating Fabric with Azure AI Foundry](https://blog.fabric.microsoft.com/en-us/blog/empowering-agentic-ai-by-integrating-fabric-with-azure-ai-foundry)
- [x] [Introducing Autoscale Billing for Spark in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/introducing-autoscale-billing-for-data-engineering-in-microsoft-fabric)
- [x] [Unlock the power of Real-Time Intelligence in the Era of AI: why Fabric Real-Time Intelligence is a game-changer](https://blog.fabric.microsoft.com/en-us/blog/unlock-the-power-of-real-time-intelligence-in-the-era-of-ai-why-fabric-real-time-intelligence-is-a-game-changer)
- [x] [Optimizing for CI/CD in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/optimizing-for-ci-cd-in-microsoft-fabric)
- [x] [Power BI March 2025 Feature Summary](https://powerbi.microsoft.com/en-gb/blog/power-bi-march-2025-feature-summary/)
- [x] [Empowering businesses with smart capacity planning: Introducing the Microsoft Fabric SKU estimator (Preview)](https://blog.fabric.microsoft.com/en-us/blog/empowering-businesses-with-smart-capacity-planning-introducing-the-microsoft-fabric-sku-estimator)
- [x] [Purview DLP Policies with Restrict Access for Fabric Lakehouses (Preview)](https://blog.fabric.microsoft.com/en-us/blog/purview-dlp-policies-with-restrict-access-for-fabric-lakehouses-a-new-era-of-data-security)
- [x] [Microsoft Purview Data Loss Prevention policies for Fabric have been extended to KQL and Mirrored Databases (Preview)](https://blog.fabric.microsoft.com/en-us/blog/announcement-microsoft-purview-data-loss-prevention-policies-for-fabric-have-been-extended-to-kql-and-mirrored-databases)
- [x] [Boost your development with Microsoft Fabric extensions for Visual Studio Code](https://blog.fabric.microsoft.com/en-us/blog/boost-your-development-with-microsoft-fabric-extensions-for-visual-studio-code)
- [x] [Recap of Data Factory Announcements at Fabric Conference US 2025](https://blog.fabric.microsoft.com/en-us/blog/recap-of-data-factory-announcements-at-fabric-conference-us-2025)
- [x] [Use Service Principals to create shortcuts to ADLS Gen2 storage accounts with trusted access](https://blog.fabric.microsoft.com/en-us/blog/service-principals-can-now-create-shortcuts-to-adls-gen-2-storage-accounts-with-trusted-access)
- [x] [Implementing proactive monitoring with KQL query alerts with Activator](https://blog.fabric.microsoft.com/en-us/blog/implementing-proactive-monitoring-with-kql-query-alerts-with-activator)
- [x] [Passing parameter values to refresh a Dataflow Gen2 (Preview)](https://blog.fabric.microsoft.com/en-us/blog/passing-parameter-values-to-refresh-a-dataflow-gen2-preview)

April 2025:

- [x] [Evaluate your Fabric Data Agents programmatically with the Python SDK (Preview)](https://blog.fabric.microsoft.com/en-us/blog/evaluate-your-fabric-data-agents-programmatically-with-the-python-sdk)
- [x] [Announcing Copilot for SQL Analytics Endpoint in Microsoft Fabric (Preview)](https://blog.fabric.microsoft.com/en-us/blog/announcing-copilot-for-sql-analytics-endpoint-in-microsoft-fabric)
- [x] [Shortcut cache and on-prem gateway support (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/shortcut-cache-and-on-prem-gateway-support-now-generally-available)
- [x] [Manage connections for shortcuts](https://blog.fabric.microsoft.com/en-us/blog/manage-connections-for-shortcuts)
- [x] [Enabling broader adoption of XMLA-based tools and scenarios](https://blog.fabric.microsoft.com/en-us/blog/enabling-broader-adoption-of-xmla-based-tools-and-scenarios)
- [x] [Activator as an Orchestrator of the Fabric Event Driven flows](https://blog.fabric.microsoft.com/en-us/blog/21865)
- [x] [Task flows in Microsoft Fabric (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/announcing-the-general-availability-ga-of-task-flows-in-microsoft-fabric)
- [x] [Authenticate to Fabric data connections using Azure Key Vault stored secrets (Preview)](https://blog.fabric.microsoft.com/en-us/blog/authenticate-to-fabric-data-connections-using-azure-key-vault-stored-secrets-preview)
- [x] [Improving productivity in Fabric Notebooks with Inline Code Completion (Public Preview)](https://blog.fabric.microsoft.com/en-us/blog/improving-productivity-in-fabric-notebooks-with-inline-code-completion)
- [x] [Updates to Fabric Copilot Capacity](https://blog.fabric.microsoft.com/en-us/blog/updates-to-fabric-copilot-capacity)
- [x] [Query vs. Mutation in API for GraphQL – Understanding the difference](https://blog.fabric.microsoft.com/en-us/blog/understanding-differences-between-query-vs-mutation-in-api-for-graphql)
- [x] [Introducing new OpenAI Plugins for Eventhouse (Preview)](https://blog.fabric.microsoft.com/en-us/blog/introducing-new-openai-plugins-for-eventhouse-preview)
- [-] [Medallion Architecture in Fabric Real-Time Intelligence](https://blog.fabric.microsoft.com/en-us/blog/21597)
- [x] [Fabric April 2025 Feature Summary](https://blog.fabric.microsoft.com/en-us/blog/fabric-april-2025-feature-summary)
- [x] [Fabric SQL Database Integration: Unlocking New Possibilities with Power BI desktop](https://blog.fabric.microsoft.com/en-us/blog/fabric-sql-database-integration-unlocking-new-possibilities-with-power-bi-desktop)
- [x] [Service principal and private library support for Fabric User data functions](https://blog.fabric.microsoft.com/en-us/blog/service-principal-and-private-library-support-for-fabric-user-data-functions)
- [x] [Introduction of item limits in a Fabric workspace](https://blog.fabric.microsoft.com/en-us/blog/introduction-of-item-limits-in-a-fabric-workspace)

Build 2025

- [x] [Get to insights faster with SaaS databases and “chat with your data”](https://blog.fabric.microsoft.com/en-us/blog/get-to-insights-faster-with-saas-databases-and-chat-with-your-data-experiences)
- [x] [Fabric May 2025 Feature Summary](https://blog.fabric.microsoft.com/en-us/blog/fabric-may-2025-feature-summary)
- [x] [Mirroring for SQL Server in Microsoft Fabric (Preview)](https://blog.fabric.microsoft.com/en-us/blog/22820)
- [x] [Simplifying Medallion Implementation with Materialized Lake Views in Fabric](https://blog.fabric.microsoft.com/en-us/blog/announcing-materialized-lake-views-at-build-2025)
- [x] [Announcing the General Availability of Open Mirroring](https://blog.fabric.microsoft.com/en-us/blog/announcing-the-general-availability-of-open-mirroring)
- [x] [Connect to your most sensitive data with end-to-end network security in Fabric](https://blog.fabric.microsoft.com/en-us/blog/connect-to-your-most-sensitive-data-with-end-to-end-network-security-in-fabric)
- [x] [Announcing Cosmos DB in Microsoft Fabric (Preview)](https://blog.fabric.microsoft.com/en-us/blog/22987)
- [x] [New Shortcut Type for Azure Blob Storage in OneLake shortcuts](https://blog.fabric.microsoft.com/en-us/blog/new-shortcut-type-for-azure-blob-storage-in-onelake-shortcuts)
- [x] [Warehouse Snapshots in Microsoft Fabric (Preview)](https://blog.fabric.microsoft.com/en-us/blog/warehouse-snapshots-in-microsoft-fabric-public-preview)
- [x] [Power BI April 2025 Feature Summary](https://powerbi.microsoft.com/en-gb/blog/power-bi-april-2025-feature-summary/)
- [x] [Power BI May 2025 Feature Summary](https://powerbi.microsoft.com/en-gb/blog/power-bi-may-2025-feature-summary/)
- [x] [Mirroring in Microsoft Fabric explained: benefits, use cases, and pricing demystified](https://blog.fabric.microsoft.com/en-us/blog/mirroring-in-microsoft-fabric-explained-benefits-use-cases-and-pricing-demystified/)
- [x] [Power BI June 2025 Feature Summary](https://powerbi.microsoft.com/en-gb/blog/power-bi-june-2025-feature-summary/)
- [x] [Translytical task flows (Preview)](https://powerbi.microsoft.com/en-gb/blog/announcing-translytical-task-flows-preview/)
- [x] [How to debug user data functions locally in VS Code](https://blog.fabric.microsoft.com/en-us/blog/how-to-debug-user-data-functions-locally-in-vs-code)
- [x] [Azure Synapse Runtime for Apache Spark 3.5 (Preview)](https://blog.fabric.microsoft.com/en-us/blog/public-preview-azure-synapse-runtime-for-apache-spark-3-5)
- [x] [New pipeline Activities Now Support OPDG and VNET](https://blog.fabric.microsoft.com/en-us/blog/new-pipeline-activities-now-support-opdg-and-vnet)
- [x] [Integrating Fabric with Databricks using private network](https://blog.fabric.microsoft.com/en-us/blog/integrating-fabric-with-databricks-using-private-network)
- [x] [How to create a SQL database in Fabric using Fabric CLI](https://blog.fabric.microsoft.com/en-us/blog/how-to-create-a-sql-database-in-fabric-using-fabric-cli)
- [x] [Boost performance effortlessly with Automated Table Statistics in Microsoft Fabric](https://blog.fabric.microsoft.com/en-us/blog/boost-performance-effortlessly-with-automated-table-statistics-in-microsoft-fabric)
- [x] [Understanding OneLake Security with Shortcuts](https://blog.fabric.microsoft.com/en-us/blog/understanding-onelake-security-with-shortcuts)
- [x] [New regions supported for Fabric User Data Functions](https://blog.fabric.microsoft.com/en-us/blog/announcing-new-regions-supported-for-fabric-user-data-functions)
- [x] [Creating SQL database workload in Fabric with Terraform: A Step-by-Step Guide (Preview)](https://blog.fabric.microsoft.com/en-us/blog/streamline-sql-database-workload-creation-with-terraform)
- [x] [Introducing FinOps Toolkit in Fabric](https://blog.fabric.microsoft.com/en-us/blog/introducing-finops-toolkit-in-fabric)
- [x] [Introducing Aggregations in Fabric API for GraphQL: Query Smarter, Not Harder](https://blog.fabric.microsoft.com/en-us/blog/introducing-aggregations-in-fabric-api-for-graphql-query-smarter-not-harder)
- [x] [That's a wrap for Build 2025!](https://blog.fabric.microsoft.com/en-us/blog/thats-a-wrap-on-build-2025)
- [x] [Updates to database development tools for SQL database in Fabric](https://blog.fabric.microsoft.com/en-us/blog/updates-to-database-development-tools-for-sql-database-in-fabric)

- [x] [Fabric June 2025 Feature Summary](https://blog.fabric.microsoft.com/en-us/blog/fabric-june-2025-feature-summary)
- [x] [Announcing Shortcut Transformations: from files to Delta tables. Always in sync, no pipelines required.](https://blog.fabric.microsoft.com/en-us/blog/announcing-shortcut-transformations-from-files-to-delta-tables-always-in-sync-no-pipelines-required)
- [x] [On-premises data gateway June 2025 release](https://blog.fabric.microsoft.com/en-us/blog/on-premises-data-gateway-june-2025-release)
- [x] [Announcing new features for Microsoft Fabric Extension in VS Code](https://blog.fabric.microsoft.com/en-us/blog/announcing-new-features-for-microsoft-fabric-extension-in-vs-code)
- [x][Customer Managed Keys in OneLake: Strengthening Data Protection and Control](https://blog.fabric.microsoft.com/en-us/blog/customer-managed-keys-in-onelake-strengthening-data-protection-and-control)
- [x] [OneLake security – updates and news](https://blog.fabric.microsoft.com/en-us/blog/publish-date-6-26-2025)
- [x] [Integrating Azure API Management with Fabric API for GraphQL](https://blog.fabric.microsoft.com/en-us/blog/how-to-make-your-sql-scalar-user-defined-function-udf-inlineable-in-microsoft-fabric-warehouse)
- [x] [How to make your SQL scalar user-defined function (UDF) inlineable in Microsoft Fabric Warehouse ](https://blog.fabric.microsoft.com/en-us/blog/inline-scalar-user-defined-functions-udfs-in-microsoft-fabric-warehouse-preview)
- [x] [Inline Scalar user-defined functions (UDFs) in Microsoft Fabric Warehouse (Preview)](https://blog.fabric.microsoft.com/en-us/blog/fabric-eventhouse-now-supports-eventstream-derived-streams-in-direct-ingestion-mode-preview)
- [x] [Fabric Eventhouse now supports Eventstream Derived Streams in Direct Ingestion mode (Preview)](https://blog.fabric.microsoft.com/en-us/blog/announcing-surge-protection-for-background-operation-is-generally-available-ga)
- [x] [Surge Protection for Background Operation (Generally Available)](https://blog.fabric.microsoft.com/en-us/blog/introducing-new-item-creation-experience-in-fabric)
- [x] [Introducing new item creation experience in Fabric](https://blog.fabric.microsoft.com/en-us/blog/integrating-azure-api-management-with-fabric-api-for-graphql)

Links:

- [Get Started with GraphQL](https://learn.microsoft.com/fabric/data-engineering/get-started-api-graphql)
- [Notebook Orchestration in Microsoft Fabric](https://thatfabricguy.com/notebook-orchestration-in-microsoft-fabric/)

---

[Back](./README.md)
