# Customize the Intune User Experience (Company Portal Customization)

This guide explains how to customize the **end-user experience** in Microsoft Intune, most notably by customizing the **Company Portal** (app + web) experience that users see on their devices. By branding and configuring it properly, your users will have a clearer, more supportive and informative interface for enrollment, app installation, support, and device actions. :contentReference[oaicite:1]{index=1}

## Prerequisites

Before you begin:

- You must have one of these Intune roles:
  - **Intune Administrator**
  - **Global Administrator**
- You need the appropriate licenses assigned to the tenant.
- You should gather organizational branding assets (logo, color codes, support contact info). :contentReference[oaicite:2]{index=2}

These customizations apply in the **Microsoft Intune admin center** under “Tenant administration > Customization.” :contentReference[oaicite:3]{index=3}

## Why This Matters

Customizing the Intune user experience:

1. **Reinforces company branding** in the Company Portal apps and website. :contentReference[oaicite:4]{index=4}  
2. Helps users **recognize official content and support channels**. :contentReference[oaicite:5]{index=5}  
3. Improves clarity around device actions, support, and device management choices. :contentReference[oaicite:6]{index=6}  
4. Reduces confusion when users enroll devices or install apps. :contentReference[oaicite:7]{index=7}

---

## Steps to Customize the Intune (Company Portal) Experience

### 1. Sign In to the Microsoft Intune Admin Center

- Go to **https://endpoint.microsoft.com**
- Sign in with an account that has appropriate Intune admin rights.

**Why:** Only administrators with the right permissions can make tenant-wide customizations. :contentReference[oaicite:8]{index=8}

---

### 2. Open the Customization Blade

1. In the left navigation pane, select **Tenant administration**.
2. Choose **Customization**.

**Why:** This is the central place where you can change branding, support info, colors, and portal behavior for end users. :contentReference[oaicite:9]{index=9}

---

### 3. Edit or Create a Customization Policy

You can either:

- **Edit the default customization policy**  
or  
- **Create one or more targeted policies** (up to 10 based on user groups).

**Why:** Group targeting lets you provide different experiences for different user groups (e.g., departments). :contentReference[oaicite:10]{index=10}

---

### 4. Configure Branding

Within the customization settings:

1. **Organization name** — appears across the portal UI. :contentReference[oaicite:11]{index=11}  
2. **Color / Theme color** — choose either a standard preset or input a custom hex code. :contentReference[oaicite:12]{index=12}  
3. **Show in header** — enable this to show the org name or logo in portal headers. :contentReference[oaicite:13]{index=13}  
4. **Upload logos**:
   - Logo for dark backgrounds
   - Logo for light backgrounds
   - Optional brand image (displayed on portal screens) :contentReference[oaicite:14]{index=14}

**Why:** These visual elements make the user interface consistent with your organization’s identity and help users trust the portal. :contentReference[oaicite:15]{index=15}

---

### 5. Add Support and Privacy Information

Within the same customization blade:

- **Support phone number**
- **Support email**
- **Support website URL**
- **Privacy statement URL**  
Some platforms (like iOS) also let you include an in-app privacy message. :contentReference[oaicite:16]{index=16}

**Why:** Users often look here first when they have questions about enrollment, apps, or devices. Clear support info reduces helpdesk calls. :contentReference[oaicite:17]{index=17}

---

### 6. Configure App Sources (Optional)

You can control which app types appear in the Company Portal app:

- Microsoft 365 apps
- Enterprise applications
- Configuration Manager apps

These show up in the portal app and web portal for users. :contentReference[oaicite:18]{index=18}

**Why:** Being selective about app sources helps simplify the user’s view and reduce confusion. :contentReference[oaicite:19]{index=19}

---

### 7. Customize Device Actions

Still in the customization blade:

- Choose whether to show or hide actions like **Remove device** or **Reset device** for Windows and iOS devices. :contentReference[oaicite:20]{index=20}

**Why:** Restricting these actions can prevent end users from accidentally removing or resetting company devices without IT involvement. :contentReference[oaicite:21]{index=21}

---

## Validate the End-User Experience

After saving customization changes:

1. Open the **Company Portal app** (mobile or desktop), or the **Company Portal website**.
2. Verify that:
   - The logo and organization name appear.
   - The theme color is applied.
   - Support information is visible.
   - Optional device actions behave as intended.

**Why:** Validation ensures that users see the experience you intended and can access support if needed. :contentReference[oaicite:22]{index=22}

---

## Troubleshooting

- If changes don’t appear immediately, wait a few minutes and refresh the apps. Compliance caching may apply. :contentReference[oaicite:23]{index=23}  
- Make sure that the policy is assigned to the intended user group. :contentReference[oaicite:24]{index=24}

---

## Sources

- Customize the Microsoft Intune Company Portal Apps, Company Portal website and Intune app, Microsoft Learn. :contentReference[oaicite:25]{index=25}  
- Step 1. Customize and configure the Company Portal, Microsoft Docs. :contentReference[oaicite:26]{index=26}
