# 🚀 DAY 8 — Response Models (Clean APIs like companies)

## 🧠 1. Explain Like You’re 10

Imagine a school report card system 🏫

Teacher has:

- Name  
- Marks  
- Internal notes (secret)  

But student should only see:

- Name  
- Marks  

👉 You hide some data before sending

This is what **Response Models** do.

---

## 🌍 2. Real-Life Example

### User system 👤

Database has:

- name  
- email  
- password 🔒  

But API response should **NOT** send password

👉 Response Model controls what is returned

---

## 💻 3. Tiny FastAPI Code

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

# Request model
class UserIn(BaseModel):
    name: str
    password: str

# Response model
class UserOut(BaseModel):
    name: str

@app.post("/user", response_model=UserOut)
def create_user(user: UserIn):
    return user
```

---

## 🤯 What happens here?

- Client sends: **name + password**  
- Server returns: **only name**  

👉 Password is automatically hidden 🚫

---

## 📝 4. Notes (Write This ✍️)

- Response Model defines what API returns  
- Helps:
  - Hide sensitive data  
  - Keep response clean  
- Defined using `response_model=...`  
- Uses **Pydantic**  

---

## 🎤 5. Interview Q&A

**Q1: What is a response model?**  
👉 A schema that defines what data is returned from an API.

**Q2: Why use response models?**  
👉 To hide sensitive data and ensure consistent API responses.

**Q3: Can request and response models be different?**  
👉 Yes, and they should be in most cases.

---

## 🧩 6. Your Turn (Important)

If your database has:

- name  
- email  
- password  

👉 Which field should NOT be returned in API response?

**(One word answer)**
