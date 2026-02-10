# Customize the Entra ID Sign-In User Experience

This guide walks you through how to customize the Microsoft Entra ID (formerly Azure AD) sign-in experience for your organization. Custom branding helps users *trust they’re signing in to the right place* and can reduce phishing risk by showing your logo, colors, and helpful text. :contentReference[oaicite:1]{index=1}

> **Note:** These settings apply at the **tenant level** and affect all applications that use Microsoft Entra ID for authentication (such as Microsoft 365 apps). There is no per-application sign-in branding in the core Entra ID branding blade. :contentReference[oaicite:2]{index=2}

## Prerequisites

Before you begin:

- You need one of the following roles:
  - **Organizational Branding Administrator**
  - **Application Administrator**
  - **Global Administrator** (this role also has access)
- Your tenant must be licensed appropriately (Microsoft Entra ID P1, P2, or a qualifying Microsoft 365 Business subscription). :contentReference[oaicite:3]{index=3}
- You should have images ready with correct sizes (e.g., **banner logo**, **background image**). :contentReference[oaicite:4]{index=4}

---

## Why This Matters

Customizing the sign-in experience:

1. **Reinforces trust** by showing your company’s branding during authentication.
2. **Reduces phishing risk** by making it harder for attackers to spoof your login screen.
3. Helps users **recognize official access points** before entering credentials.
4. Allows you to provide **help text or guidance** directly on the screen. :contentReference[oaicite:5]{index=5}

---

## Steps

### 1. Sign In to the Microsoft Entra Admin Center

1. Open a browser and go to: **https://entra.microsoft.com**
2. Sign in with an account that has allowed admin privileges (e.g., Organizational Branding Admin).

**Why:** Only administrators with branding permissions can view and edit tenant branding. :contentReference[oaicite:6]{index=6}

---

### 2. Open Company Branding

1. In the left navigation menu, expand **Identity > Identity providers** or use the search bar to find **Custom Branding** / **Company branding**.
2. Select **Company branding**.

**Why:** This page is where Microsoft exposes the sign-in branding customizations that apply to all user authentication screens. :contentReference[oaicite:7]{index=7}

---

### 3. Begin Customizing the Sign-In Page

#### Basics

1. Click **Configure** (or **Edit** if a default exists).
2. Upload your assets:
   - **Favicon** (32×32 px, <5 KB)
   - **Background image** (1920×1080 px, <300 KB)
   - **Page background color** (fallback if the image doesn’t load) :contentReference[oaicite:8]{index=8}

**Why:** These elements improve the visual identity of your sign-in page and ensure users see your brand instead of Microsoft’s defaults. :contentReference[oaicite:9]{index=9}

---

#### Layout

1. Choose one of the layout templates (e.g., full-screen or partial screen).
2. Optionally enable a **header** or **footer**.

**Why:** Layout affects how your page elements appear spatially and ensures a polished experience across devices. :contentReference[oaicite:10]{index=10}

---

#### Sign-In Form Branding

1. Upload:
   - **Banner logo** (e.g., 245×36 px)
   - **Square logos** (for light and dark themes, ~240×240 px)
2. Enter optional:
   - **Username hint text** (e.g., “Use your company email”)
   - **Sign-in page text** (adds guidance or support info under the login form)

**Why:** These settings make the identity prompt instantly recognizable and can reduce helpdesk calls by giving clearer instructions. :contentReference[oaicite:11]{index=11}

> **Important:** The sign-in page text is public; do *not* include sensitive content. :contentReference[oaicite:12]{index=12}

---

### 4. Preview and Save

1. Use the **Preview** button to review your changes.
2. If it looks correct, choose **Review + Create** (or **Save** / **Apply**).

**Why:** Previewing avoids embarrassing branding mishaps before users see them. :contentReference[oaicite:13]{index=13}

---

## Validate Your Custom Sign-In Experience

After saving your theme:

1. Open a private/incognito browser.
2. Navigate to a Microsoft 365 sign-in page (e.g., **https://login.microsoftonline.com**).
3. Enter your work email and proceed to the branded sign-in screen.
4. Confirm your custom background, logos, and text appear as expected.

**Why:** Sign-in caching can cause delays; testing helps confirm the configuration rolled out correctly. :contentReference[oaicite:14]{index=14}

---

## Notes & Limitations

- **Tenant scope:** Branding applies tenant-wide, not per application. :contentReference[oaicite:15]{index=15}
- **Guest users:** Custom branding may behave differently for B2B external users. :contentReference[oaicite:16]{index=16}
- Some elements (like CSS overrides) are deprecated or limited for new tenants. :contentReference[oaicite:17]{index=17}

---

## Troubleshooting

- If your changes don’t appear immediately, Microsoft global cache replication may take *some time* (minutes to hours). :contentReference[oaicite:18]{index=18}
- Check image sizes and file types (PNG/JPG) if uploads fail. :contentReference[oaicite:19]{index=19}

---

## Sources

- Add company branding to your organization’s Microsoft Entra sign-in experience, Microsoft Learn. :contentReference[oaicite:20]{index=20}
- Customize Microsoft 365 sign-in page branding overview. :contentReference[oaicite:21]{index=21}
