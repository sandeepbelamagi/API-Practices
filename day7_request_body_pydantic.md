# 🚀 DAY 7 — Request Body + Pydantic (VERY IMPORTANT)

## 🧠 1. Explain Like You’re 10

Imagine you are filling a school admission form 📝

You write:

- Name  
- Age  
- Class  

Then submit it.

👉 That full form = **Request Body**

But what if:

- You forget name ❌  
- You write age as “abc” ❌  

👉 School rejects it

This checking is done by **Pydantic**

💡 **Simple idea:**

- Request Body = data you send  
- Pydantic = data checker/validator  

---

## 🌍 2. Real-Life Example

### Creating a user 👤

You send:

```json
{
  "name": "Arun",
  "age": 25
}
```

👉 API checks:

- name is present ✅  
- age is number ✅  

Then:  
👉 “User created”

---

## 💻 3. Tiny FastAPI Code

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

# Pydantic model (data structure)
class User(BaseModel):
    name: str
    age: int

# POST API
@app.post("/create-user")
def create_user(user: User):
    return {
        "message": "User created",
        "data": user
    }
```

---

## 🤯 What’s happening?

- `User` class = data format  
- FastAPI automatically:
  - Reads request body  
  - Validates it  
  - Converts it to Python object  

---

## 📝 4. Notes (Write This ✍️)

### Request Body
- Data sent in POST/PUT requests  
- Usually in JSON format  

### Pydantic
- Used for data validation  
- Ensures correct types (str, int, etc.)  
- Rejects invalid data automatically  

---

## 🎤 5. Interview Q&A

**Q1: What is request body?**  
👉 Data sent by client to server (usually JSON).

**Q2: What is Pydantic?**  
👉 A library used in FastAPI for data validation and parsing.

**Q3: Why use Pydantic?**  
👉 To ensure correct data types and structure before processing.

---

## 🧩 6. Your Turn (Very Important)

Look at this model:

```python
class Product(BaseModel):
    name: str
    price: int
```

👉 If user sends:

```json
{
  "name": "Laptop",
  "price": "ten thousand"
}
```

👉 Will this pass or fail validation?

👉 **Answer: Pass / Fail + why (one line)**
