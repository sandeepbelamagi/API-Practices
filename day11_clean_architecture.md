# 🚀 DAY 11 — Routers vs Services vs Schemas (Clean Architecture)

## 🧠 1. Explain Like You’re 10

Imagine a pizza shop 🍕

There are 3 roles:

- 🧾 Order taker → takes your order  
- 👨‍🍳 Chef → cooks pizza  
- 📋 Recipe book → defines how pizza should look  

### Map to FastAPI:

- Router → takes request (like order taker)  
- Service → does work (like chef)  
- Schema → defines data (like recipe)  

---

## 🌍 2. Real-Life Example

### User creation 👤

- Router:  
  👉 “Create user request received”  

- Schema:  
  👉 “User must have name and age”  

- Service:  
  👉 “Save user to database”  

---

## 💻 3. Tiny Code Example

### schemas/user.py
```python
from pydantic import BaseModel

class User(BaseModel):
    name: str
```

### services/user_service.py
```python
def create_user_service(user):
    return {"message": f"User {user.name} created"}
```

### routers/user.py
```python
from fastapi import APIRouter
from schemas.user import User
from services.user_service import create_user_service

router = APIRouter()

@router.post("/users")
def create_user(user: User):
    return create_user_service(user)
```

---

## 🤯 What’s happening?

- Router → receives request  
- Schema → validates data  
- Service → processes logic  

👉 Clean separation = enterprise code  

---

## 📝 4. Notes (Write This ✍️)

- Router → handles API endpoints  
- Schema → defines request/response data  
- Service → contains business logic  

👉 Separation improves:

- readability  
- testing  
- scalability  

---

## 🎤 5. Interview Q&A

**Q1: What is the role of a router?**  
👉 To define API endpoints and handle requests.

**Q2: What is a service layer?**  
👉 It contains business logic separate from API routes.

**Q3: Why separate service from router?**  
👉 To keep code clean and reusable.

---

## 🧩 6. Your Turn (Important)

If you need to:

👉 “Save user to database”

Should that go in:

- Router  
- Schema  
- Service  

**(Choose one + why in one line)**
