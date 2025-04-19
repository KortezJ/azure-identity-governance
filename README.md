**Azure Identity Governance Implementation**

This project demonstrates an end-to-end implementation of **Microsoft Entra ID Governance (formerly Azure AD)**, showcasing how to configure access controls, monitor identities, enforce least privilege, and visualize audits in an enterprise cloud environment.

---

### 🔖 Objectives
- Establish enterprise-grade identity access control using Microsoft Entra ID.
- Configure **Access Packages** for HR, Finance, and IT with time-bound permissions.
- Enforce secure access through **Conditional Access Policies** (e.g., MFA).
- Manage elevated permissions using **Privileged Identity Management (PIM)**.
- Conduct recurring **Access Reviews** with auto-removal for stale access.
- Collect audit and sign-in logs, then visualize insights via **Power BI**.

---

### 🛠️ Tools & Services Used
- **Microsoft Azure Portal**  
- **Entra ID Governance**  
  - Access Packages  
  - Conditional Access  
  - PIM (Privileged Identity Management)  
  - Access Reviews  
- **Microsoft Authenticator (MFA)**
- **Power BI Desktop** (data visualization)
- **GitHub** (project repository, documentation)
- **CSV Export Tools** (Azure Portal exports)

---

### 🔐 Step 1: User + Group Creation
Provisioned 5 users for role simulation:
- Alice HR
- Bob Finance
- Carol IT
- Dave Contractor
- Erin Manager

Created 3 groups:
- HR-Access
- Finance-Access
- IT-Access

**📸 Screenshots:**
- Users: `/images/step1_users.png`
- Groups: `/images/step1_groups.png`

---

### 🎫 Step 2: Access Packages Setup
Built 3 Access Packages:
- **HR Tools**
- **Finance Apps**
- **IT Admin JIT Access**

Configured approval workflows, access expiration, lifecycle policies.

**📸 Screenshot:** `/images/step2_access_packages.png`

---

### ⚠️ Step 3: Conditional Access & PIM
**Policies Created:**
- `Require MFA for High Risk Sign-ins`
- `Block Legacy Authentication`

**PIM Configuration:**
- Assigned `Global Reader` role to Carol IT.
- Activation time: 1 hour

**📸 Screenshots:**
- MFA Policy: `/images/step3_mfa_policy.png`
- PIM Activation: `/images/step3_pim_activation.png`

---

### 🔄 Step 4: Access Reviews
**Setup:**
- Reviewer: Erin Manager
- HR & Finance groups
- Frequency: Weekly
- Auto-remove if no action in 30 days

**📸 Screenshots:**
- Configuration: `/images/step4_review_config.png`
- Decision History: `/images/step4_decision_log.png`

---

### 📁 Step 5: Log Export & Audits
Exported logs from Azure:
- `Access Reviews`  
- `Group Membership`  
- `Sign-in Activity`

Stored in `/data/` as `.csv` files.

---

### 📊 Step 6: Power BI Dashboard
Loaded data into Power BI Desktop and created:
- **Bar Chart**: Review Approvals vs Denials
- **Line Graph**: Sign-ins over time
- **Matrix**: Membership churn by user/role

**📸 Screenshot:** `/images/step6_powerbi_dashboard.png`

---

### 🧠 Key Takeaways
- Mastery of Azure Identity Governance and lifecycle automation
- Secure access enforcement with MFA + Conditional Access
- Role-based and just-in-time elevation using PIM
- Real-world access auditing and review strategy
- Audit compliance readiness with Power BI integration

---

### 🔄 Reproduce This Project
1. Spin up a free Entra ID tenant in the Azure Portal
2. Add users, groups, and packages as shown
3. Export logs from:
   - Azure AD > Audit Logs
   - Azure AD > Sign-in Logs
   - Identity Governance > Access Reviews
4. Visualize using Power BI Desktop (`Get Data > CSV`)

---

### 📢 Recruiter Tip
This project mimics a real enterprise governance model in the cloud—perfect for roles in **Cloud Security**, **Identity & Access Management (IAM)**, or **Compliance Engineering**. It proves hands-on experience with **Microsoft Entra ID**, **zero trust**, and **lifecycle automation**.

---

### 💬 Feedback or Questions?
Open an issue or connect with me on GitHub. Always improving.

