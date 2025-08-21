# postman-gorest-tests
# GoRest API Test Collection (Postman)

This repository contains a **Postman collection and environment** for testing the [GoRest API](https://gorest.co.in/).  
It automates two scenarios as part of an API testing assignment.

---

## 🚀 Scenarios Covered
1. **Create User**  
   - Sends a `POST` request to create a new user.  
   - Validates that the response contains a numeric `id`.  

2. **Verify First User Status**  
   - Sends a `GET` request to fetch users.  
   - Validates that the first user’s `status` is either `active` or `inactive`.  

---

## 📂 Files in this Repository
- `GoRest_API_Test.postman_collection.json` → Postman collection with 2 requests.  
- `GoRest_Environment.postman_environment.json` → Postman environment with variables (`token`, `timestamp`).  

---

## 🛠 How to Use
1. Download or clone this repository.  
2. Open **Postman**.  
3. Click **Import** and upload both JSON files:  
   - Collection: `GoRest_API_Test.postman_collection.json`  
   - Environment: `GoRest_Environment.postman_environment.json`  
4. Select the **GoRest Environment** in the top-right corner of Postman.  

---

## 🔑 Generate Your Token
1. Go to [GoRest Access Tokens](https://gorest.co.in/consumer/login).  
2. Login and generate a **Personal Access Token**.  
3. Copy the token and update it in Postman:  
   - In **Environments → GoRest Environment → token** → Paste your token.  
   - Save changes.  

---

## ▶️ Run the Tests
- **Create User** → Should return `201 Created` and a numeric `id`.  
- **Verify First User Status** → Should pass the test ✅ *"First user's status is active or inactive"*.  

You can also run the whole collection via **Collection Runner** in Postman.  

---

## 📌 Notes
- Each run requires a **unique email**. The collection already uses `{{timestamp}}` to avoid duplicates.  
- If you get `401 Unauthorized`, regenerate your token and update it in the environment.  

---

## ✅ Example Test Result
- Create User → `201 Created`  
- Verify First User Status → Test Passed ✅ 
