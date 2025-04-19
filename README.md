# Azure Identity Governance

This project demonstrates how to implement **Microsoft Azure Identity Governance** step-by-step using **Access Packages, Conditional Access, PIM, and Access Reviews**. It’s a practical showcase with real configurations, screenshots, and exported audit data—ideal for anyone looking to understand or manage enterprise identity governance in Azure.

---

## 📌 Objectives
- Set up secure **access control** with Azure Identity Governance.
- Implement **Conditional Access** and **Privileged Identity Management (PIM)**.
- Run **Access Reviews** and automate lifecycle cleanup.
- Export **logs for auditing** and create a Power BI-ready dataset.

---

## 🛠️ Tools Used
- Microsoft Azure Portal
- Entra ID Governance
- Power BI (for visualizing exported logs)
- GitHub (project documentation)

---

## 🔐 Step 1: Create Users and Groups
Created the following sample users:
- Alice HR
- Bob Finance
- Carol IT
- Dave Cont
- Erin Manager

And added to:
- `HR-Access`  
- `Finance-Access`  
- `IT-Access`  

📸 *[Screenshot: `images/step1_users.png`](images/step1_users.png)*  
📸 *[Screenshot: `images/step1_groups.png`](images/step1_groups.png)*

---

## 🎫 Step 2: Configure Access Packages
- Built 3 Access Packages to align with business roles:
  - **HR Tools**
  - **Finance Apps**
  - **IT Admin JIT Access**
- Configured request policies, approval flows, and life cycles.

📸 *[Screenshot: `images/step2_access_packages.png`](images/step2_access_packages.png)*

---

## 🚧 Step 3: Conditional Access & PIM
- Created Conditional Access policies:
  - `Require MFA for High Risk Sign-ins`
  - `Block Legacy Authentication`
- Set up PIM for the **Global Reader** role.
- Assigned **Carol IT** as eligible and activated for 1 hour.

📸 *[Screenshot: `images/step3_mfa_policy.png`](images/step3_mfa_policy.png)*  
📸 *[Screenshot: `images/step3_pim_activation.png`](images/step3_pim_activation.png)*

---

## 🔁 Step 4: Access Reviews
- Set up recurring access reviews for:
  - `HR Group` (Package 1)
  - `Finance Group` (Package 2)
- Reviewer: **Erin Manager**
- Auto-remove users if no response in 30 days

📸 *[Screenshot: `images/step4_review_config.png`](images/step4_review_config.png)*  
📸 *[Screenshot: `images/step4_decision_log.png`](images/step4_decision_log.png)*

---

## 📁 Step 5: Audit Logs & Export
Exported and included:
- Access Review Logs  
- Group Membership Logs  
- Sign-in Logs  

📁 *See `data/` folder for .csv files*

---

## 📊 Step 6: Power BI Dashboard *(Optional)*
Created visuals for:
- 📈 Review Approvals vs Denials (Bar Chart)
- 📉 Sign-ins Over Time (Line Graph)
- 🔄 Group Membership Changes (Matrix)

📸 *[Screenshot: `images/step6_powerbi_dashboard.png`](images/step6_powerbi_dashboard.png)*

---

## 🧠 Key Learnings
- How Azure Identity Governance tools secure enterprise identity management.
- Automated lifecycle management and least privilege enforcement.
- Integration between access policies, approvals, and monitoring.

---

## 🔄 Reproduce This Project
1. Spin up a Microsoft Entra ID test tenant.
2. Follow each step using the Azure Portal.
3. Export logs under *Azure AD > Audit Logs / Sign-in logs / Access Reviews*
4. Import to Power BI or Excel for reporting.

---

## 💬 Feedback / Suggestions
Open an issue or message me on GitHub!

---

> 🧠 **Tip for Recruiters:**  
This project showcases hands-on governance implementation and security configuration in a real Azure environment—demonstrating infrastructure readiness, compliance mindset, and cloud access control best practices.
