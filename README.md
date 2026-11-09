# Awesome-Billing-User-Roles-Permissions

I can't create the file, commit, or push—I have no filesystem, no shell, and no Git credentials. Everything I produce is text. You will need to save and push it yourself.

I also have to flag what the search results actually support, because **Chargebee's RBAC is a platform feature, not a standalone product**, and the open-source side is a library, not a platform.

## The data problems

**Chargebee User Management is a feature of its billing platform, not a standalone SKU.** The documentation describes seven predefined roles plus custom roles . **Custom roles require the Performance plan or above** . There is no separate "Chargebee User Management" product or price.

**The list mixes billing-specific RBAC with general identity platforms.** Okta, Entra ID, Google Workspace, JumpCloud, OneLogin, Ping, CyberArk, Auth0, and AWS IAM all provide user management and roles as a core identity capability. They are not billing RBAC tools. Listing them alongside Chargebee misleads readers looking for billing-specific access control.

**No standalone RBAC pricing surfaced for any of these platforms.** The prices shown are for the broader identity platform, not a role-management add-on.

## What the search results actually contain

**Chargebee (billing platform with native RBAC):**
- **7 predefined roles**: Tech Support, Analyst, Sales Agent, Customer Support, Sales Manager, Finance Executive, Owner 
- **Custom roles**: only on **Performance plan and above** 
- **Starter plan**: max **3 users** 
- **Password policy**: must update every 90 days, cannot match last 4 

**Identity platforms (proprietary, platform pricing not RBAC-specific):**

| Platform | Entry pricing | Verified detail |
|---|---|---|
| **Okta** | **Starter $6/user/mo**; **Essentials $17/user/mo**; Professional/Enterprise quote  | Workforce Identity sold as suites, billed annually; $1,500 annual minimum  |
| **Microsoft Entra ID** | **P1 $6/user/mo**; **P2 $9/user/mo**; Free with Azure/M365  | P1 adds Conditional Access, SSPR, dynamic groups; P2 adds PIM and Identity Protection  |
| **Google Workspace** | **Business Starter $7–$8.40/user/mo**; Standard $14–$16.80; Plus $22–$26.40  | Flexible vs. annual plans; annual commits to license count  |
| **OneLogin** | **Basic $3/user/mo**; **Essentials $6**; **Business $10**  | Vendr notes 3–5% annual escalators and implementation fees  |
| **Ping Identity** | **PingOne for Workforce $3/user/mo** (5,000 user minimum, annual)  | Customers starts $35K–$50K  |
| **JumpCloud** | **$3 add-on** per ITAM pricing source  | Limited detail surfaced |
| **CyberArk, Auth0, AWS IAM** | **No pricing surfaced in these results** | Do not fabricate |

**Open-source: what actually exists**

**Casbin** is the only open-source RBAC library surfaced in prior research in this conversation: **Go, 13K+ GitHub stars**, supports **ACL, RBAC, and ABAC**, with implementations in Go, Java, Node.js, Python, PHP, .NET, Rust. It is an **access control library you embed in your application**, not a billing RBAC platform. **No new open-source project surfaced in these results.**

## What I recommend

**Split into three honest categories:**

**1. Billing Platform with Native RBAC** (proprietary):
- **Chargebee** — 7 predefined roles; custom roles require **Performance plan+** 

**2. Identity Platforms with User Management & Roles** (proprietary, not billing-specific):
- **Okta** — $6–$17/user/mo 
- **Entra ID** — $6–$9/user/mo 
- **Google Workspace** — $7–$26.40/user/mo 
- **OneLogin** — $3–$10/user/mo 
- **Ping** — $3/user/mo workforce 
- **JumpCloud** — $3 add-on 
- **CyberArk, Auth0, AWS IAM** — **pricing not surfaced**

**3. Open-Source RBAC Library:**
- **Casbin** — 13K+ stars, ACL/RBAC/ABAC, multi-language (from prior research in this conversation)

**Flag the Chargebee custom-role gate explicitly:** custom roles are **Performance plan and above only** . Starter is capped at **3 users** .

If you paste your current `README.md` and confirm you want this framing, I will produce the complete file as text for you to save. I will not present Chargebee RBAC as a standalone product, list identity platforms as billing-specific tools, or fabricate CyberArk/Auth0/AWS IAM pricing that the results do not contain.
