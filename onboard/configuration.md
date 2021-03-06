## Setting up the Environments

Once the agent has been installed (typically this would be the Exchange On-premises server which would act as the PowerShell host where the exchange management shell is located), you will be presented with various tabs.

**Agent notes**: When installing the agent, it's important to highlight that you must have one agent per datacentre. The agent is also forest specific i.e. if you have more than one Exchange server in different forests in different locations, then each one will need its own agent. A cross domain scenario this would also require multiple agents.

### Configuring Active Directory environment

The Active Directory tab is where you will find all the settings and configuration required with regards to the on-premises Active Directory.

**Agent -** This is the server where the agent is installed.

**Credentials -** The credentials are those of either the Exchange admin or domain admin account.

### Scheduled jobs

Within the configuration section you can edit the list of scheduled jobs, and configure their settings as required.

At the bottom of this tab you will see the scheduled jobs list, which are as follows:

**GetAdGroupsAndMembers -** Gets all AD groups and members in a Domain.

**GetSitesInDomain -** Fetches AD Sites for a Domain (admin required).

**GetSubnetsInDomain -** Fetches IP Subnets for a Domain (admin required).

**GetUsersInDomains -** Gets all users in a Domain.

### Configuring Exchange environment

The Exchange tab is where you will find all the settings and configuration required with regards to the on-premises Exchange server.

**Environment name -** This will be a memorable label / name that helps you to distinguish the environment being referenced.

**Exchange PowerShell Host -** This should be set to the server that contains the Exchange management shell and contains the PowerShell host for the environment.

**Agent -** This is the server where the agent is installed.

**Credentials -** The credentials are those of either the Exchange admin or domain admin account.

### Scheduled jobs

Within the configuration section you can edit the list of scheduled jobs, and configure their settings as required.

At the bottom of this tab you will see the scheduled jobs list, which are as follows:

**TestMRSHealth -** This tests / checks the MRS health of an instance of the Microsoft Exchange Mailbox Replication service.

**GetMigrationEndpoints -** GetMigrationEndpoints will retrieve all available migration endpoints within a Hybrid Environment.

**GetRemoteMailbox -** The GetRemoteMailbox job will run PowerShell commands in order to establish which mailboxes are in O365.

**GetExchangeServers -** This job will get all the On-premises Exchange servers.

**GetOnPremMailbox -** When this job runs it will fetch all information related to the On-premises mailboxes.

**GetOnPremMailboxStatistics -** This job will get all On-premises Mailbox Statistics of the On-premises Mailboxes.

**GetOnPremPersonalArchiveStatistics -** This job will fetch all On-premises Personal Archive Statistics (for example number of items and how many folders etc).

### Configuring TransVault environment

In this tab you can configure the required settings for any TransVault Migration server along with the scheduled jobs that relate to it. These jobs can be run at any time from the scheduled jobs window.

**Environment name -** This will be a memorable label / name that helps you to distinguish the environment being referenced.

**SQL Server -** This should be set to the SQL Server that hosts the TransVault database.

**Database name -** The TransVault database name. e.g. TransVault

**Agent -** This is the server where the OnBoard Agent is installed.

**Credentials -** The credentials are those of either the Exchange admin or domain admin account.

### Scheduled jobs

Within the configuration section you can edit the list of scheduled jobs, and configure their settings as required.

At the bottom of this tab you will see the scheduled jobs list, which are as follows:

**GetTVConnections -** This job fetches the configured connections in a TransVault Environment.

**GetTVErrorReport -** Fetches the error report from the configured TransVault environment.

**GetTVMailboxes -** Fetches the mailboxes/archives seen in a TransVault Environment.

**GetTVQueues -** Fetches the configured queues in a TransVault Environment.

**GetTVQueueStatus -** Fetches the current status of the configured queues in a TransVault Environment.

**MigrationReport -** Fetches the Migration Report from the configured TransVault environment.

### Configuring Enterprise Vault environment

The Enterprise Vault tab is where you will find all the settings and configuration required with regards to the source Enterprise Vault servers.

**Environment name -** This will be a memorable label / name that helps you to distinguish the environment being referenced.

**SQL Server -** This should be set to the SQL Server that hosts the EV Directory database.

**Database name -** The EV Directory database name. e.g. EnterpriseVaultDirectory

**Agent -** This is the server where the OnBoard Agent is installed.

**Credentials -** The credentials are those of the Exchange admin, domain admin, or appropriate EV Vault Store account.

### Scheduled jobs

Within the configuration section you can edit the list of scheduled jobs, and configure their settings as required.

At the bottom of this tab you will see the scheduled jobs list, which are as follows:

**GetArchives -** Reads all Mail Archives from EV.

**GetEVComputersAndServices -** Reads all EV Computers in a VaultSite and their installed EV Services.

**GetEVServicesAndTaskStatus -** Gets the current status of all EV Services and Tasks.

**GetRetentionCategories -** Gets list of the defined RetentionCategories from EV.

**GetVaultSites -** Get all VaultSites in a VaultDirectory.

**GetVaultStorage -** Gets the VaultStorage details.

**GetVaultStorePartitions -** Gets the Vault Store Partitions.

## Additional columns for data grid on the Mappings screen

You can modify which columns are displayed in the Mappings screen.  To add in additional columns, go to Settings --> On-Boarding (this is only accessible with the OnBoard admin permission)

Select which columns you would like to add from the available list on the right hand panel, Extended Properties i.e. add in fields from AD, Exchange, the TransVault mailbox table etc

Click Save when you are happy with your selection, then go back to the Mapping screen.  Onboard > Mapping.

Click on the Select columns icon to see your new list of available fields ![Seed](images/dt-04.png)

You should now see the new columns available in the dropdown and can select/de-select them as required
![Seed](images/dt-05.png)
