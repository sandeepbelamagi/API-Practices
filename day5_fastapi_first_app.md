# 🚀 DAY 5 — Your First Real FastAPI App

## 🧠 1. Explain Like You’re 10

Until now, we were just talking about APIs.

Now imagine:

👉 You build your own mini shop counter 🏪  
Where people can come and ask:

- “Hello?”  
- “Give me data”  

👉 FastAPI helps you open that counter in real life

---

## 🌍 2. Real-Life Example

Think of opening a customer service desk

### Before:
- You only imagined how it works  

### Now:
- You actually open the desk  
- People can come and ask questions  

👉 That’s what we do today

---

## 💻 3. Tiny FastAPI App (Run This)

### Step 1: Install FastAPI + server
```bash
pip install fastapi uvicorn
```

### Step 2: Create file → `main.py`
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "My first API is running 🚀"}
```

### Step 3: Run server
```bash
uvicorn main:app --reload
```

### Step 4: Open browser

👉 Go to:

- http://127.0.0.1:8000  
- http://127.0.0.1:8000/docs  

⭐ **(VERY IMPORTANT)**

---

## 🤯 Magic (Important Insight)

That `/docs` page is:

👉 **Auto-generated API documentation**

This is why FastAPI is loved in companies 💼

---

## 📝 4. Notes (Write This ✍️)

- FastAPI app is created using:
  ```python
  app = FastAPI()
  ```
- `@app.get("/")` defines an endpoint  
- `uvicorn` runs the server  
- `--reload` = auto restart on changes  
- `/docs` gives interactive API UI  

---

## 🎤 5. Interview Q&A

**Q1: How do you run a FastAPI app?**  
👉 Using `uvicorn main:app --reload`

**Q2: What is Uvicorn?**  
👉 An ASGI server used to run FastAPI applications.

**Q3: What is /docs in FastAPI?**  
👉 Automatically generated interactive API documentation.

---

## 🧩 6. Your Turn (Very Important Step)

Do this on your system:

- Run the code  
- Open `/docs`  

Then answer:

👉 **What do you see on the /docs page?**
