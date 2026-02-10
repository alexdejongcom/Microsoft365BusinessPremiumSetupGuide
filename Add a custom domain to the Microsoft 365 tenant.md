# Add a Custom Domain to a Microsoft 365 Tenant

This guide explains how to add your own domain name (like `yourcompany.com`) to a Microsoft 365 tenant so you can use professional email addresses and align Microsoft 365 services with your branded domain. :contentReference[oaicite:1]{index=1}

## Prerequisites

Before you begin:

- You must be signed in with a **Global Administrator** or **Domain Name Administrator** account. :contentReference[oaicite:2]{index=2}  
- You must *own* the domain you intend to add.  
- You’ll need access to your **domain registrar** (DNS host) to add DNS records for verification.

## Why This Matters

Adding a custom domain:

1. Lets you use professional email addresses (`@yourcompany.com`) rather than the default `@yourtenant.onmicrosoft.com`. :contentReference[oaicite:3]{index=3}  
2. Aligns Microsoft 365 identities across email, Teams, SharePoint, and other services. :contentReference[oaicite:4]{index=4}  
3. Is required before you can assign user email addresses with your domain. :contentReference[oaicite:5]{index=5}

---

## Steps

### 1. Sign in to the Microsoft 365 Admin Center

1. Open your web browser and go to **https://admin.microsoft.com**
2. Sign in with your administrative credentials.

**Why**: Adding or modifying domains requires elevated permissions. (Standard users won’t see the right controls.) :contentReference[oaicite:6]{index=6}

---

### 2. Open the Domains Page

![Domains page in Microsoft 365 Admin Center](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/media/add-domain/domains-page.png)

1. In the left navigation pane, select **Settings**.
2. Choose **Domains**.

**Why**: All domain-related tasks (add, verify, manage DNS) are found on this page. :contentReference[oaicite:7]{index=7}

---

### 3. Start the Add Domain Wizard

![Add domain button in Microsoft 365 Admin Center](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/media/add-domain/add-domain-button.png)

1. On the **Domains** page, select **Add domain**.
2. Enter the custom domain name you want to add (e.g., `yourcompany.com`).
3. Click **Next**.

**Why**: This initiates Microsoft’s guided setup, which helps both verify ownership and configure DNS. :contentReference[oaicite:8]{index=8}

---

### 4. Choose a Verification Method

You’ll be prompted to prove you own the domain.

![Domain verification options in Microsoft 365](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/media/add-domain/domain-verification-options.png)

Most common options:

- **Domain Connect (automatic)**:  
  If your registrar supports it (e.g., GoDaddy, Cloudflare), sign in and allow Microsoft to manage DNS records automatically. :contentReference[oaicite:9]{index=9}

- **TXT Record (manual)**:  
  Microsoft gives you a **TXT record** value. Go to your DNS host and create a TXT record to verify ownership. :contentReference[oaicite:10]{index=10}

**Why**: Verification proves you *control* the domain and prevents anyone else from hijacking it. :contentReference[oaicite:11]{index=11}

---

### 5. Add DNS Records for Microsoft 365 Services

Once verified, you will be shown DNS records that enable Microsoft 365 services (email, Teams, etc.):

- **MX** record for email routing  
- **CNAME** records for autodiscover and service connections  
- **TXT** records for SPF  
- **SRV** records for Teams and Skype Online

![DNS records list in Microsoft 365 setup](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/media/add-domain/dns-records.png)

Add these records at your **domain registrar’s DNS manager**.

**Why**: These records tell the rest of the internet where to send email and how to connect services for your domain. :contentReference[oaicite:12]{index=12}

---

### 6. Complete the Setup Wizard

After DNS records are added:

1. Return to the Microsoft 365 wizard.
2. Select **Verify** (for manual DNS) or let Domain Connect complete automatically.
3. Click **Finish** when prompted.

**Why**: Completing the wizard finalizes the domain addition and updates Microsoft’s internal directory. :contentReference[oaicite:13]{index=13}

---

## Post-Setup Steps (Optional but Recommended)

### Set the New Domain as Default

After adding your domain:

1. In **Settings > Domains**, select your newly added domain.
2. Click **Set as default**.

**Why**: This means new users (and some services) will use your custom domain by default instead of the `.onmicrosoft.com` domain. :contentReference[oaicite:14]{index=14}

---

## Troubleshooting & Notes

- DNS propagation can take **minutes to hours** depending on your registrar.  
- If verification fails, double-check the TXT/MX record values and ensure they’re published correctly. :contentReference[oaicite:15]{index=15}  
- You can add *multiple domains* (e.g., subsidiaries or brands) to one tenant. :contentReference[oaicite:16]{index=16}

---

## Sources

- Add a domain to Microsoft 365 — Microsoft Learn. :contentReference[oaicite:17]{index=17}  
- Add a custom domain name — Microsoft Support. :contentReference[oaicite:18]{index=18}  
- Add DNS records at any DNS host — Microsoft Learn. :contentReference[oaicite:19]{index=19}  
- Domains FAQ — Microsoft Learn. :contentReference[oaicite:20]{index=20}
