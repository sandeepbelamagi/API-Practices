# 🚀 Mini Project — Step 3: Build Your First Router

## 🧠 1. Explain Like You’re 10

Imagine your office now has a front desk 🧾

People come and ask:

- “Show users”  
- “Create user”  

👉 The front desk handles requests  
👉 That is your **router**

---

## 🌍 2. Real-Life Mapping

**Router = receptionist**

It doesn’t do the work.  
It just:

- receives request  
- sends it to service  

---

## 💻 3. Tiny Code (`routers/user.py`)

```python
from fastapi import APIRouter

router = APIRouter()

@router.get("/")
def get_users():
    return [{"name": "Arun"}, {"name": "John"}]

@router.post("/")
def create_user():
    return {"message": "User created"}
```

---

## 🤯 What’s happening?

- `GET /users/` → returns users  
- `POST /users/` → creates user  
- Router handles endpoints only  

---

## 📝 4. Notes (Write This ✍️)

- Router defines API endpoints  
- Uses `APIRouter()`  
- Each function = one endpoint  
- Should **NOT** contain heavy logic  

---

## 🎤 5. Interview Q&A

**Q: What is APIRouter?**  
👉 A tool to group related API endpoints.

**Q: Should business logic be inside router?**  
👉 No, it should be in service layer.

---

## 🧩 6. Your Turn (Important)

If your `main.py` has:

```python
prefix="/users"
```

and your router has:

```python
@router.get("/")
```

👉 What is the full API URL?

**Answer:** `/users/`

---

## 💡 Key Idea

Final URL = **prefix + route path**

---

## 🔁 Quick Check (Your Turn)

If:

- `prefix = /users`
- `route = /list`

👉 What is the full URL?

**(Just write it)**
