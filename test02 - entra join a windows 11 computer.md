# Install the Microsoft Entra Connect Sync Tool Using the Custom Install Option

This guide walks you through installing **Microsoft Entra Connect Sync** on a server and choosing the **custom installation** path. Custom installation lets you tailor the setup — for example by choosing a custom database, account types, authentication options, and filtering — instead of the default express install. :contentReference[oaicite:1]{index=1}

## Prerequisites

Before you begin:

- **Server Requirements**  
  - A domain-joined Windows Server (supported versions per Microsoft documentation).  
  - Administrative privileges on the server where you install the tool. :contentReference[oaicite:2]{index=2}

- **Accounts and Permissions**  
  - A Microsoft Entra (Azure AD) Global Admin account for connecting to the cloud directory.  
  - Permissions in your on-premises Active Directory to read the directory and, if you're creating accounts, sufficient rights to do so. :contentReference[oaicite:3]{index=3}

- **Domain Verification**  
  - Your on-premises AD domain must be verified in Microsoft Entra ID if you plan to use features like seamless sign-on. :contentReference[oaicite:4]{index=4}

---

## Why This Matters

Installing with **custom settings** gives you control over how synchronization behaves:

1. **Database choice** — use SQL Express (default) or an existing SQL Server instance.  
2. **Service accounts** — pick virtual, managed, or password-based accounts as needed.  
3. **Sync scope and rules** — configure filtering or writeback features.  
4. **Authentication method** — choose password hash sync, pass-through authentication, or federated sign-on, based on your environment.  
These options are necessary in complex scenarios such as multiple forests or advanced filtering. :contentReference[oaicite:5]{index=5}

---

## Steps

### 1. Download Microsoft Entra Connect

1. Go to your Microsoft 365 Tenant / Entra admin center.
2. Search for **Entra Connect** or navigate to the Entra ID → Entra Connect section.
3. Click **Download Microsoft Entra Connect** to get the latest *AzureADConnect.msi* installer. :contentReference[oaicite:6]{index=6}

**Why:** You must use the supported installer to ensure compatibility with current features and security. :contentReference[oaicite:7]{index=7}

---

### 2. Run the Installer

1. Copy *AzureADConnect.msi* to the intended synchronization server.
2. Log in to that server with local administrator rights.
3. Double-click *AzureADConnect.msi* to start setup.

Accept the license agreement when prompted. :contentReference[oaicite:8]{index=8}

**Why:** Running the installer locally lets the tool configure services, database, and sync engine components. :contentReference[oaicite:9]{index=9}

---

### 3. Choose *Customize* on the Installation Type Page

1. On the initial setup screen, you’ll be offered **Express Settings** and **Customize**.
2. Select **Customize** to begin a custom installation. :contentReference[oaicite:10]{index=10}

**Why:** *Express* is the default, general-purpose installation. Choosing *Customize* opens additional options for database placement, service accounts, and authentication choices, which are essential for tailored environments. :contentReference[oaicite:11]{index=11}

---

### 4. Install Required Components

The wizard displays options for required services and components:

- **Custom install location** (optional) — define where Entra Connect will be installed.  
- **Use an existing SQL Server** — specify an existing SQL Server instance and database, if you don’t want the default SQL Express.  
- **Existing service account** — optionally provide a domain account for Entra Connect services.  
- **Custom sync groups** — define your own local groups instead of the defaults.  
- **Import sync settings** — if migrating from another setup, import previous configuration. :contentReference[oaicite:12]{index=12}

Choose options appropriate for your environment, then click **Next**.

**Why:** This step lets you align the installation to your operational policies (DB location, permissions model, and group definitions). :contentReference[oaicite:13]{index=13}

---

### 5. Configure User Sign-In

The wizard will prompt you to select how users authenticate:

- **Password Hash Synchronization** — cloud authentication using synchronized hashes from on-premises AD.  
- **Pass-Through Authentication** — authentication requests are passed to on-premises AD.  
- **Federation** — use AD FS or another provider to federate sign-in. :contentReference[oaicite:14]{index=14}

Pick the method that matches your identity strategy, then **Next**.

**Why:** This determines how users sign in to Microsoft services and whether credentials or validation must traverse your on-premises systems. :contentReference[oaicite:15]{index=15}

---

### 6. Connect to Microsoft Entra ID and Active Directory

1. Enter credentials for a Microsoft Entra Global Administrator account to connect to your cloud directory.  
2. Specify connection details for your on-premises Active Directory (forest name and credentials with adequate rights). :contentReference[oaicite:16]{index=16}

Click **Next** after entry.

**Why:** Entra Connect needs authenticated access to both directories to sync objects between them. :contentReference[oaicite:17]{index=17}

---

### 7. Sync Configuration and Optional Features

Continue through the wizard to specify:

- Optional writeback features (e.g., password, device).  
- Filtering rules (OU or attribute-based).  
- How to handle userPrincipalName and SID history. :contentReference[oaicite:18]{index=18}

Make selections suited to your scenario, then **Next**.

**Why:** Sync scope and behavior affect which objects and attributes move to Microsoft Entra ID. Proper filtering helps control what gets synced. :contentReference[oaicite:19]{index=19}

---

### 8. Install and Verify

1. When you reach *Ready to configure*, review your settings.
2. Deselect “Start the synchronization process when configuration completes” if you want to control the first sync manually.
3. Choose **Install**.

When the installer finishes, click **Exit**. :contentReference[oaicite:20]{index=20}

**Why:** Reviewing settings before install ensures accuracy. Manual control of the first sync is useful when you want to validate configuration before users are synced. :contentReference[oaicite:21]{index=21}

---

## Post-Installation Validation

After installation:

1. Verify that the **Synchronization Service Manager** is present on the server.  
2. Check the **Operations** tab for initial sync status.  
3. Confirm user objects and attributes appear in Microsoft Entra ID as expected.

**Why:** These checks confirm that the service is running and syncing your directory. Not validating can conceal issues until users experience sign-in problems. :contentReference[oaicite:22]{index=22}

---

## Troubleshooting & Notes

- If the custom options are confusing, review the Microsoft Entra Connect documentation for detailed descriptions of each feature.  
- Ensure domain verification in Microsoft Entra ID before custom sign-in configuration.  
- Filtering and optional feature selection must align with your AD topology. :contentReference[oaicite:23]{index=23}

---

## Sources

- Custom installation of Microsoft Entra Connect — Microsoft Learn. :contentReference[oaicite:24]{index=24}
- Install your synchronization tool (overview page) — Microsoft Learn. :contentReference[oaicite:25]{index=25}
