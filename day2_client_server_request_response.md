# 🚀 DAY 2 — Client, Server, Request, Response

## 🧠 1. Explain Like You’re 10

Let’s go back to the restaurant 🍔

You say: **“I want a burger”** → this is a **request**  
Kitchen makes it → **processing**  
Waiter brings burger → **response**

So:

👉 **Request** = asking for something  
👉 **Response** = getting the answer  

---

## 🌍 2. Real-Life Example (Instagram ❤️)

When you like a post:

Client (**Instagram app**) sends:  
👉 **“User liked post 123”** → Request  

Server processes it  

Server sends back:  
👉 **“Like added successfully”** → Response  

---

## 💻 3. Tiny FastAPI Code

Now we start real API thinking 👇

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/hello")
def say_hello():
    return {"message": "Hello user"}
```

### What’s happening here?

- `/hello` → API endpoint  
- When client calls it → request  
- Function runs → server logic  
- Returns JSON → response  

---

## 📝 4. Notes (Write This ✍️)

- **Client** → sends request (app)  
- **Server** → processes request  
- **Request** → input sent to server  
- **Response** → output from server  
- APIs work on **request → response cycle**  

---

## 🎤 5. Interview Q&A

**Q1: What is a request?**  
👉 A request is a message sent from client to server asking for data or action.

**Q2: What is a response?**  
👉 A response is the data returned by the server after processing the request.

**Q3: What is client-server architecture?**  
👉 A system where the client sends requests and the server processes and responds.

---

## 🧩 6. Your Turn (Think Carefully)

If you open a weather app and search:

👉 **“Weather in Bangalore”**

Tell me:

- What is the **request**?  
- What is the **response**?  
