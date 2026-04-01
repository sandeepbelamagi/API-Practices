# 🚀 Mini Enterprise Project — Step 2: Build the Skeleton

## 🧠 Explain Like You’re 10

Imagine we are opening a small company office 🏢

We first decide:

- front desk  
- forms desk  
- work desk  

We are not doing the work yet.  
We are just setting up the rooms properly.

👉 That is called the **project skeleton**

---

## 🌍 Real-Life Example

Before a hospital starts treating patients, it first creates:

- reception  
- records room  
- doctor rooms  

Same in FastAPI:

- `main.py` starts the app  
- `routers/` receives requests  
- `schemas/` checks forms  
- `services/` does the work  

---

## 💻 Tiny Code

### Folder structure

```
app/
    main.py
    routers/
        user.py
    schemas/
        user.py
    services/
        user_service.py
```

---

### main.py

```python
from fastapi import FastAPI
from app.routers.user import router as user_router

app = FastAPI()

app.include_router(user_router, prefix="/users", tags=["Users"])
```

---

## 📝 Notes

- `main.py` is the entry point  
- `include_router()` connects route files to the app  
- `prefix="/users"` means all user routes start with `/users`  
- `tags=["Users"]` groups endpoints nicely in `/docs`  

---

## 🎤 Interview Q&A

**Q: Why use include_router()?**  
👉 To keep routes modular and connect them cleanly to the main app.

**Q: What is the purpose of prefix in FastAPI?**  
👉 It adds a common base path to related endpoints.

**Q: Why use tags?**  
👉 To organize endpoints in the API docs.

---

## 🔁 Quick Reinforcement

So if router has:

```python
@router.get("/")
```

and in main.py we use:

```python
prefix="/users"
```

then the final URL becomes:

👉 `/users/`

---

## 🧩 Your Turn

In `main.py`, what does `prefix="/users"` help us do?

**(Answer in one line)**
