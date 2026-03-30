# 🚀 DAY 4 — JSON + Status Codes

## 🧠 1. Explain Like You’re 10

Imagine you send a message to a robot 🤖:

👉 **“What’s the weather?”**

The robot replies:

👉 **“Temperature: 28, Condition: Sunny”**

But… computers don’t speak English like us.  
They use a structured format.

That format is called **JSON**

---

## 🌍 2. Real-Life Example

Think of a parcel box 📦

Instead of random stuff, everything is neatly labeled:

- name → Arun  
- age → 25  

👉 JSON is like a **labeled box of data**

---

## 💻 3. Tiny Python Example

```python
data = {
    "city": "Bangalore",
    "temperature": 28,
    "condition": "Sunny"
}

print(data)
```

👉 This looks exactly like JSON (Python dictionary ≈ JSON)

---

## 🧠 Status Codes (Very Important)

When you order food 🍕

- If order is successful → 👍  
- If item not found → ❌  
- If server down → 😵  

APIs also send a **status code** to tell what happened.

---

## 🌍 Real-Life Mapping

| Situation        | Meaning            | Status Code |
|-----------------|------------------|------------|
| Everything OK   | Success          | 200        |
| Something created | New data added  | 201        |
| Wrong request   | You made mistake | 400        |
| Not allowed     | No permission    | 401/403    |
| Not found       | Data missing     | 404        |
| Server error    | Backend failed   | 500        |

---

## 💻 FastAPI Example

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/weather")
def get_weather():
    return {
        "city": "Bangalore",
        "temperature": 28
    }
```

👉 By default, this returns:

- JSON data  
- Status code **200**

---

## 📝 4. Notes (Write This ✍️)

### JSON
- JSON = JavaScript Object Notation  
- Used to send data in APIs  
- Format = key : value  
- Looks like Python dictionary  

### Status Codes
- 200 → Success  
- 201 → Created  
- 400 → Bad request  
- 401/403 → Unauthorized/Forbidden  
- 404 → Not found  
- 500 → Server error  

---

## 🎤 5. Interview Q&A

**Q1: What is JSON?**  
👉 A format used to exchange data between client and server.

**Q2: Why JSON?**  
👉 It is lightweight, easy to read, and widely supported.

**Q3: What is status code 200?**  
👉 Request successful.

**Q4: What is 404?**  
👉 Resource not found.

---

## 🧩 6. Your Turn (Important)

If you try to open a user profile that doesn’t exist:

👉 **Which status code should be returned?**
