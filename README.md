# 🗂️ Amazon S3 Storage Classes & Lifecycle Management

## 📌 Overview

- This document explains:
- What S3 Storage Classes are
- How to check and change the storage class of an object
- How to configure S3 Lifecycle Rules to transition or delete objects automatically
---

## 📦 S3 Storage Classes
### 🔹 What are S3 Storage Classes?
- Amazon S3 Storage Classes allow you to store data at different cost levels based on access frequency and data retention needs.
- Common storage classes:
- Standard
- Standard-IA (Infrequent Access)
- Intelligent-Tiering
- One Zone-IA
- Glacier / Glacier Deep Archive
---

## 🔍 How to Check and Edit Storage Class of a File
- Go to AWS Management Console → S3
- Open your bucket
- Select the file (example: index.html)
- Click on Properties
- Scroll to Storage class
- Click Edit
- Select your preferred storage class
- Click Save changes
- ✅ The storage class of the object is now updated.
---

## 🔄 S3 Lifecycle Management
#### 📖 Definition

- S3 Lifecycle policies allow you to automatically:
- Move objects between different storage classes
- Expire (delete) objects after a specific time
  based on conditions such as object age or inactivity.
- This helps in cost optimization and data management.
---

## ⚙️ Create an S3 Lifecycle Rule
#### Step 1: Open Lifecycle Rules
- Go to S3
- Open your bucket
- Navigate to Management
- Click Lifecycle rules
- Click Create lifecycle rule
#### Step 2: Rule Details
- Rule name: kurrebucket-lc-rule
- Scope: Apply to all objects in the bucket
---

#### Step 3: Lifecycle Rule Actions
#### ✅ Action 1: Transition Objects Between Storage Classes
- Transition 1:
- Storage class: Standard-IA
- Days after object creation: 30 days
- Transition 2:
- Storage class: Intelligent-Tiering
- Days after object creation: 60 days
- Click Add transition to add multiple transitions.
#### ✅ Action 2: Expire Current Versions of Objects
- Delete objects after: 90 days
- Next
- Review all settings
- Click Create rule
- ✅ Lifecycle rule is now active.
---

## 📝 Important Notes
- Lifecycle rules apply automatically once enabled
- Transitions must follow a valid order (earlier → cheaper storage)
- Lifecycle policies are cost-effective for long-term storage
- Rules work only on existing and future objects, depending on configuration
---

## 🎯 Use Cases
-Reduce storage cost
- Archive unused data
- Automatic data cleanup
- Long-term compliance storage
---

## 📚 Related AWS Services
- Amazon S3
- S3 Lifecycle Rules
- S3 Storage Classes
- AWS Cost Optimization
---
  ## 👨‍💻 Author

**Kumlesh Kurre**
💼 IT Support & Network Engineer

⭐ If you find this guide helpful, don’t forget to star ⭐ the GitHub repository!
