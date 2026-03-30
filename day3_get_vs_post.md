# 🚀 DAY 3 — GET vs POST (VERY IMPORTANT)

## 🧠 1. Explain Like You’re 10

Imagine a library 📚

### Case 1: You ask

👉 **“Can I see the book Harry Potter?”**

- You are just getting information  
- You don’t change anything  

👉 This is **GET**

---

### Case 2: You say

👉 **“I want to add a new book to the library”**

- You are sending new data  
- You are changing something  

👉 This is **POST**

---

## 🌍 2. Real-Life Examples

### ✅ GET examples:

- Open Instagram → see posts  
- Check weather  
- View your profile  

👉 Only **reading data**

---

### ✅ POST examples:

- Create account  
- Upload photo  
- Place an order  

👉 Sending **new data**

---

## 💻 3. Tiny FastAPI Code

```python
from fastapi import FastAPI

app = FastAPI()

# GET → fetch data
@app.get("/get-user")
def get_user():
    return {"name": "Arun"}

# POST → send data
@app.post("/create-user")
def create_user():
    return {"message": "User created"}
```

---

## 📝 4. Notes (Write This ✍️)

### GET
- Used to **retrieve data**  
- Does **NOT** change server data  

### POST
- Used to **send/create data**  
- **Changes** server data  

👉 **GET = Read**  
👉 **POST = Create**

---

## 🎤 5. Interview Q&A

**Q1: Difference between GET and POST?**  
👉 GET is used to retrieve data, POST is used to send/create data.

**Q2: Does GET change data?**  
👉 No, GET should not modify data.

**Q3: Give examples of POST**  
👉 Creating user, uploading file, placing order.

---

## 🧩 6. Your Turn (Important)

Tell me:

👉 When you log in to a website, is it:

**GET or POST?**

*(Just answer one word + why in one line)*  
