# 📚 Library Management System — Dynamics 365 CRM

A fully managed **Microsoft Dynamics 365 CRM solution** built to handle end-to-end library operations including book inventory, member management, borrowing lifecycle, and automated notifications.
<img width="1920" height="1080" alt="Screenshot 2025-02-05 130639" src="https://github.com/user-attachments/assets/94b39c9d-c83c-41d9-aec5-4c5e76873cee" />
<img width="1920" height="1080" alt="Screenshot 2025-01-31 144434" src="https://github.com/user-attachments/assets/25a90db2-16f3-468a-814f-8dd5c184f8c8" />
<img width="1920" height="1080" alt="Screenshot 2025-01-31 143917" src="https://github.com/user-attachments/assets/4d2507c4-f7db-4e3f-b71d-685c2e26c9a3" />
<img width="1920" height="1080" alt="Screenshot 2025-01-31 143615" src="https://github.com/user-attachments/assets/3530db2f-80da-463f-970c-ef27478fc0d1" />
<img width="1920" height="1080" alt="Screenshot 2025-01-31 143205" src="https://github.com/user-attachments/assets/5124bcf2-e7c4-4eb4-8443-164659012f77" />
<img width="1920" height="1080" alt="Screenshot 2025-01-29 190715" src="https://github.com/user-attachments/assets/94a1defb-1b07-4299-b412-fd403b1836d4" />
<img width="1920" height="1080" alt="Screenshot 2025-01-29 190638" src="https://github.com/user-attachments/assets/e9ca1b60-e37b-4e64-95f2-8bf79f8915d4" />



---

## 🏗️ Solution Details

| Property | Details |
|---|---|
| Platform | Microsoft Dynamics 365 / Power Platform |
| Solution Type | Managed Solution |
| Version | 1.0.0.2 |
| Publisher | Library |
| Customization Prefix | `library_` |

---

## 📦 Custom Entities (Dataverse Tables)

| Entity | Purpose |
|---|---|
| `library_books` | Stores all book records with genre, copies, and supplier info |
| `library_members` | Manages member profiles and membership types |
| `library_borrowingrecords` | Tracks borrowing lifecycle — issue date, due date, return date, status |
| `library_suppliers` | Manages book vendor and supplier information |

---

## ⚙️ Automated Workflows (Power Automate / Classic Workflows)

| Workflow | Trigger | Action |
|---|---|---|
| Decrease Copies on Borrow | Borrowing record created | Reduces available copies by 1 |
| Increase Copies on Return | Book marked as returned | Increases available copies by 1 |
| Alert on Low Copies | Copies fall below threshold | Sends stock alert notification |
| Update Due Date | Borrowing date set | Auto-calculates and sets return due date |
| Return Date Validation | Record save | Prevents return date before borrowing date |
| Set Overdue Status | Daily / on update | Marks record as Overdue if not returned in time |
| Notify Overdue Members | Overdue status set | Sends email notification to member |
| Business Rules (×2) | Form load / field change | Form-level validations and field visibility logic |

---

## 🧮 Calculated Fields

- **Copies Available** — auto-computed from total copies minus active borrowing records

---

## 🌐 JavaScript Web Resource

- **`crf1f_Availablebook`** — Custom JavaScript for dynamic form behavior including real-time availability display on the Books form

---

## 📱 Model-Driven App

- Built a complete **Library Management System** Model-Driven App with custom sitemap, views, and forms for all 4 entities

---

## 🚀 Solution Type — Why Managed?

This solution is packaged as a **Managed Solution**, which means:
- ✅ Production-deployment ready
- ✅ Components are locked from unintended edits in target environments
- ✅ Follows enterprise-grade ALM (Application Lifecycle Management) practices
- ✅ Can be cleanly uninstalled without leaving orphaned components

---

## 🛠️ Technologies Used

- Microsoft Dynamics 365 CRM
- Microsoft Dataverse
- Power Automate (Classic Workflows)
- JavaScript (Web Resources)
- Business Rules
- Model-Driven Power Apps
- Solution Packaging & Deployment

---


## 📁 Repository Contents
```
├── LibraryManagementSystem_1_0_0_1_managed.zip   # Importable managed solution file
└── README.md
```

---

## 📥 How to Import This Solution

1. Go to **make.powerapps.com**
2. Select your target **Environment**
3. Navigate to **Solutions → Import Solution**
4. Upload `LibraryManagementSystem_1_0_0_1_managed.zip`
5. Follow the import wizard and click **Publish All Customizations**

---

## 👨‍💻 Author

**Keyrun** — Microsoft Dynamics 365 CRM Developer  
Associate Software Engineer @ Tech Mahindra  
Certified: MB-910 | PL-900
