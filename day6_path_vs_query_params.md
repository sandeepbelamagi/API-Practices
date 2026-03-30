# 🚀 DAY 6 — Path Params vs Query Params

## 🧠 1. Explain Like You’re 10

Imagine a school office 🏫

### Case 1: You say

👉 **“Give marks of student 101”**

Here:

- 101 is part of the path  

👉 This is a **Path Parameter**

---

### Case 2: You say

👉 **“Give marks of student 101 for subject Math”**

Here:

- subject = extra detail  

👉 This is a **Query Parameter**

---

## 🌍 2. Real-Life Example (Instagram)

### Path param:

👉 `/user/123`  
→ You are saying: “Give user with ID 123”

---

### Query param:

👉 `/posts?limit=10`  
→ You are saying: “Give posts, but only 10”

---

## 💻 3. Tiny FastAPI Code

### Path Parameter
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/user/{user_id}")
def get_user(user_id: int):
    return {"user_id": user_id}
```

### Query Parameter
```python
@app.get("/items")
def get_items(limit: int = 10):
    return {"limit": limit}
```

---

## 📝 4. Notes (Write This ✍️)

### Path Parameters
- Part of URL path  
- Used to identify a specific resource  
- Example: `/user/123`  

### Query Parameters
- Added after `?`  
- Used for filtering/sorting/options  
- Example: `/items?limit=10`  

---

## 🎤 5. Interview Q&A

**Q1: Difference between path and query parameters?**  
👉 Path parameters identify a resource, query parameters modify/filter the request.

**Q2: Give example of path param**  
👉 `/user/123`

**Q3: Give example of query param**  
👉 `/products?limit=5`

---

## 🧩 6. Your Turn (Important)

Tell me:

👉 In this URL:

`/products/45?category=electronics`

- What is the **path parameter**?  
- What is the **query parameter**?  
