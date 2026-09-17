# 🔎 Google Dorking — Quick Notes

### 📌 What Is Google Dorking?

Google Dorking uses advanced search operators to discover publicly indexed information during OSINT and bug bounty reconnaissance.

---

### 1. WordPress API Users

```text
inurl:"/wp-json/wp/v2/users"
```

**Role:** Finds publicly accessible WordPress API user endpoints.

---

### 2. Exposed API Files

```text
intitle:"index.of" intext:"api.txt"
```

**Role:** Finds directory listings containing potential API key files.

---

### 3. API Directories

```text
inurl:"/api/v1" "index of"
```

**Role:** Identifies potentially exposed API directories.

---

### 4. PHP API Endpoints

```text
ext:php inurl:"api.php?action="
```

**Role:** Finds PHP endpoints using action-based API parameters.

---

### 5. Potential API Key Exposure

```text
intitle:"index of" (api_key OR "api key" OR apiKey) -pool
```

**Role:** Searches for directory listings containing API key-related files.

---

### ⚠️ High-Risk Data to Watch For

* 🔑 API Keys
* 🔐 Passwords
* 🎟️ JWT Tokens
* 👤 PII
* 💳 Credit Card Data
* 🗄️ Database Backups
* ⚙️ `.env` Files

> **Note:** Search results are not automatically vulnerabilities. Verify findings only within authorized bug bounty scopes.
