# 🚀 DAY 14 — Error Handling, Logging, Config (Enterprise Level 💼)

## 🧠 1. Explain Like You’re 10

Imagine a school system 🏫

### Situation 1:
Student enters wrong ID  
👉 Teacher says: “Invalid ID” ❌  
👉 That’s **error handling**

### Situation 2:
School writes in a notebook:  
👉 “Student tried wrong ID at 10 AM”  
👉 That’s **logging**

### Situation 3:
School rules:

- Opening time = 9 AM  
- Closing time = 5 PM  

👉 That’s **config (settings)**

---

## 🌍 2. Real-Life Example (App)

- Error → “User not found”  
- Log → “User login failed at 3:00 PM”  
- Config → API keys, database URL  

---

## 💻 3. Tiny FastAPI Example

```python
from fastapi import FastAPI, HTTPException

app = FastAPI()

@app.get("/user/{id}")
def get_user(id: int):
    if id != 1:
        raise HTTPException(status_code=404, detail="User not found")
    return {"name": "Arun"}
```

---

## 🤯 What’s happening?

- Wrong ID → error raised  
- Proper message returned  
- Status code = **404**  

👉 This is clean error handling  

---

## 📝 4. Notes (Write This ✍️)

### Error Handling
- Use `HTTPException`  
- Always return proper status codes  

### Logging
- Records system activity  
- Helps debugging  

### Config
- Stores settings (API keys, DB URL)  
- Should not hardcode values  

---

## 🎤 5. Interview Q&A

**Q1: How do you handle errors in FastAPI?**  
👉 Using HTTPException with status codes.

**Q2: Why is logging important?**  
👉 Helps track issues and debug problems.

**Q3: What is configuration in backend apps?**  
👉 External settings like DB URL, API keys.

---

## 🧩 6. Your Turn (Important)

If user requests data that doesn’t exist:

👉 **Which status code should you return?**
