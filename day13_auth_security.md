# 🚀 DAY 13 — Authentication & Security (Login Systems 🔐)

## 🧠 1. Explain Like You’re 10

Imagine a school gate 🚪

- Students must show ID card  
- Only then they can enter  

👉 That checking = **Authentication**

Now imagine:

- Teachers can enter staff room  
- Students cannot  

👉 That permission = **Authorization**

💡 **Simple difference:**

- Authentication → Who are you?  
- Authorization → What can you do?  

---

## 🌍 2. Real-Life Example (Instagram)

- You login → Authentication  
- You edit your post → Allowed  
- You edit someone else’s post → Not allowed ❌  

---

## 💻 3. Tiny FastAPI Example

```python
from fastapi import FastAPI, HTTPException

app = FastAPI()

@app.get("/secure-data")
def secure_data(password: str):
    if password != "admin123":
        raise HTTPException(status_code=401, detail="Unauthorized")
    return {"data": "Secret info"}
```

---

## 🤯 What’s happening?

- User sends password  
- If wrong → **401 error** ❌  
- If correct → access granted ✅  

---

## 📝 4. Notes (Write This ✍️)

### Authentication
- Verifies identity (login)  
- Example: username + password  

### Authorization
- Controls access  
- Example: admin vs user  

### Status Codes
- 401 → Unauthorized  
- 403 → Forbidden  

---

## 🎤 5. Interview Q&A

**Q1: Difference between authentication and authorization?**  
👉 Authentication verifies identity, authorization controls access.

**Q2: What is 401?**  
👉 Unauthorized (not authenticated)

**Q3: What is 403?**  
👉 Forbidden (authenticated but no permission)

---

## 🧩 6. Your Turn (Important)

Scenario:

👉 User logs in correctly  
👉 But tries to access admin panel (not allowed)

Which status code should be returned?

- 401  
- 403  

**(Choose one + why in one line)**
