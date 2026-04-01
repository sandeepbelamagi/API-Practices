# 🚀 DAY 9 — CRUD APIs (Core of Every Application)

## 🧠 1. Explain Like You’re 10

Imagine a notebook 📓

You can:

- ✍️ Write something → Create  
- 👀 Read what’s written → Read  
- ✏️ Change something → Update  
- ❌ Erase something → Delete  

👉 These 4 actions = **CRUD**

---

## 🌍 2. Real-Life Example (Instagram)

- Create → Post a photo 📸  
- Read → View posts 👀  
- Update → Edit caption ✏️  
- Delete → Remove post ❌  

---

## 💻 3. Tiny FastAPI Code (Basic CRUD)

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

items = []  # fake database

class Item(BaseModel):
    name: str

# CREATE
@app.post("/items")
def create_item(item: Item):
    items.append(item)
    return {"message": "Item added"}

# READ
@app.get("/items")
def get_items():
    return items

# UPDATE
@app.put("/items/{index}")
def update_item(index: int, item: Item):
    items[index] = item
    return {"message": "Item updated"}

# DELETE
@app.delete("/items/{index}")
def delete_item(index: int):
    items.pop(index)
    return {"message": "Item deleted"}
```

---

## 📝 4. Notes (Write This ✍️)

- CRUD = Create, Read, Update, Delete  

### Mapping to HTTP:
- POST → Create  
- GET → Read  
- PUT → Update  
- DELETE → Delete  

👉 Most APIs are built using CRUD operations  

---

## 🎤 5. Interview Q&A

**Q1: What is CRUD?**  
👉 Basic operations: Create, Read, Update, Delete.

**Q2: Which HTTP method is used for update?**  
👉 PUT (or PATCH in some cases)

**Q3: Why is CRUD important?**  
👉 It forms the foundation of most backend systems.

---

## 🧩 6. Your Turn (Important)

Tell me:

👉 If you want to delete a user, which HTTP method will you use?

**(One word answer)**
