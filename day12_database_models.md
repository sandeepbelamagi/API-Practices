# 🚀 DAY 12 — Database Thinking + Models

## 🧠 1. Explain Like You’re 10

Imagine a school register book 📘

It stores:

- Student name  
- Age  
- Class  

👉 This book = **Database**

But we don’t write randomly…

We define:

- What fields exist  
- What type they are  

👉 That structure = **Model**

---

## 🌍 2. Real-Life Example

### User system 👤

Database table:

| id | name | age |
|----|------|-----|
| 1  | Arun | 25  |

👉 Model defines:

- id → number  
- name → text  
- age → number  

---

## 💻 3. Tiny Example (Concept Level)

```python
class UserModel:
    def __init__(self, id, name, age):
        self.id = id
        self.name = name
        self.age = age

user = UserModel(1, "Arun", 25)

print(user.name)
```

👉 This represents how data is stored

---

## 🧠 Important Difference (VERY IMPORTANT)

| Concept            | Purpose                      |
|-------------------|-----------------------------|
| Schema (Pydantic) | Validate API data           |
| Model (DB)        | Represent database structure|

👉 **Don’t mix them ❗**

---

## 📝 4. Notes (Write This ✍️)

- Database stores persistent data  
- Model defines structure of database table  
- Each model = one table  

👉 **Schema ≠ Model**

- Schema → API validation  
- Model → Database structure  

---

## 🎤 5. Interview Q&A

**Q1: What is a database model?**  
👉 A representation of a table structure in code.

**Q2: Difference between schema and model?**  
👉 Schema validates data, model defines database structure.

**Q3: Why use models?**  
👉 To maintain consistent and structured data storage.

---

## 🧩 6. Your Turn (Important)

Tell me:

👉 If a user sends data to API, which handles it first?

- Schema  
- Model  

**(Choose one + why in one line)**
