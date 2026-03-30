# 🚀 DAY 1 — What is an API (Foundation)

## 🧠 1. Explain Like You’re 10

Imagine you are using a food delivery app 🍕

You click:  
👉 **“Show me pizza”**

But…

- The app doesn’t have pizza data inside it  
- The restaurant has the data  

So how does the app get it?

👉 It sends a message to the restaurant system  
👉 That message goes through a helper  

That helper is called an **API**

💡 **Simple definition:**

> API = a messenger that takes your request and brings back a response

---

## 🌍 2. Real-Life Example

### 🏫 School Office Example

- You = student  
- Office = school database  
- Clerk at window = API  

You ask:  
👉 **“What are my marks?”**

Clerk:

- Takes your request  
- Checks system  
- Gives answer  

You don’t access the database directly  
👉 You always go through the clerk (**API**)

---

## 💻 3. Tiny Python Code (Concept Connection)

We simulate an API response:

```python
def get_student_marks(name):
    return {"name": name, "marks": 95}

response = get_student_marks("Arun")
print(response)
```

👉 Here:

- Function = API (pretend)  
- Input = request  
- Output = response  

---

## 📝 4. Notes (Write This ✍️)

- API stands for **Application Programming Interface**  
- API acts as a **middleman**  
- It connects:
  - Client (app/user)  
  - Server (data/system)  
- API follows:
  - **Request → Response model**  
- We never directly access the server/database  

---

## 🎤 5. Interview Q&A

**Q1: What is an API?**  
👉 API is a system that allows two applications to communicate using requests and responses.

**Q2: Why do we need APIs?**  
👉 To safely access data without directly exposing the backend.

**Q3: Give a real-life example of an API**  
👉 Food delivery app fetching restaurant data.

---

## 🧩 6. Your Turn (Very Important)

Answer this in your own words:

👉 In a **weather app**, what is:

- **Client?**  
- **API?**  
- **Server?**  
