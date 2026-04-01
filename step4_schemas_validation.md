# 🚀 Mini Project — Step 4: Add Schemas (Real Validation)

## 🧠 1. Explain Like You’re 10

Imagine your office has a form checker 📝

Before accepting any form, it checks:

- Name is filled ✅  
- Age is a number ✅  

If something is wrong:  
👉 “Form rejected” ❌  

👉 That checker = **Schema (Pydantic)**

---

## 🌍 2. Real-Life Example

User submits:

```json
{
  "name": "Arun",
  "age": 25
}
```

👉 Accepted ✅  

But:

```json
{
  "name": "Arun",
  "age": "twenty five"
}
```

👉 Rejected ❌  

---

## 💻 3. Tiny Code (`schemas/user.py`)

```python
from pydantic import BaseModel

class UserCreate(BaseModel):
    name: str
    age: int
```

---

## 💻 Update Router (Important)

```python
from fastapi import APIRouter
from app.schemas.user import UserCreate

router = APIRouter()

@router.post("/")
def create_user(user: UserCreate):
    return {
        "message": "User created",
        "user": user
    }
```

---

## 🤯 What’s happening?

FastAPI automatically:

- Reads JSON request  
- Validates using schema  
- Converts to Python object  

---

## 📝 4. Notes (Write This ✍️)

- Schemas use **Pydantic**  
- Define structure of request data  
- Enforce types (str, int, etc.)  
- Automatically validate input  
- Prevent invalid data  

---

## 🎤 5. Interview Q&A

**Q: What is a schema in FastAPI?**  
👉 A Pydantic model used to validate request/response data.

**Q: What happens if validation fails?**  
👉 FastAPI automatically returns an error (422).

**Q: Why use schemas?**  
👉 To ensure clean and correct data enters the system.

---

## 🧠 Key Concepts (Very Important)

- Pydantic does **type coercion (conversion)**  
- Validation fails only if conversion is **not possible or not safe**

### Examples:

- `"25"` → ✅ PASS (converted to int)  
- `"abc"` → ❌ FAIL (cannot convert)  
- `"30.5"` → ❌ FAIL (float, not valid int)  

---

## 🧩 Final Quick Check 🔐

Will this pass?

```json
{
  "age": 25.0
}
```

**Answer: FAIL — because 25.0 is a float, not a valid integer type.**
