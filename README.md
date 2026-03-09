# AI-Property-Assistant

The **AI Property Assistant** is an intelligent property search system that helps users find real estate properties using natural language queries. Instead of manually filtering properties, users can simply ask questions like:

> "Find a 2 bedroom apartment in Karachi with parking."

The assistant processes the query using AI, extracts relevant information such as **city, property type, and amenities**, and then searches the property database to return relevant results.

The system also includes **state management and caching** to make property searches faster and more efficient.

---

#  Project Objectives

The goal of this project is to build an **AI-driven property search assistant** that:

* Understands natural language queries
* Extracts user intent and entities
* Validates property search information
* Searches a property database
* Uses caching to improve performance
* Returns filtered results through an API

This project demonstrates how **AI workflows can automate real estate search systems.**

---

#  System Workflow

The assistant processes requests through several stages:

### 1️⃣ Webhook Request

The system receives a user query through a **webhook API endpoint**.

Example query:

```
Find apartments in Karachi with 2 bedrooms
```

---

### 2️⃣ Intent & Entity Extraction

An AI model analyzes the query and extracts structured data such as:

* city
* property_type
* bedrooms
* amenities

---

### 3️⃣ Search State Management

The extracted information is stored in a **search state object** so the assistant can remember previously provided details.

---

### 4️⃣ Validation

The system validates the extracted entities:

* Property type validation
* City validation

If information is missing, the assistant requests more details.

---

### 5️⃣ Cache Decision

Before searching the database, the system checks whether results for the requested city already exist in the **cache**.

If cached results are available, they are returned immediately.

---

### 6️⃣ Database Search

If no cache is found, the assistant queries the **property database** to retrieve matching properties.

---

### 7️⃣ Result Filtering

The returned properties are filtered based on:

* Property type
* Bedrooms
* Amenities
* Availability

---

### 8️⃣ Cache Storage

The filtered results are stored in cache so that future requests for the same city can be answered faster.

---

### 9️⃣ Response to User

The assistant returns the final list of matching properties through the webhook response.

---


#  Demo Screenshots

### Property Assistant Workflow

<img width="1231" height="414" alt="AI property agent1" src="https://github.com/user-attachments/assets/551408cd-abcc-4391-815f-75d49b2bca47" />


---

### Database Property Search

<img width="1348" height="605" alt="db" src="https://github.com/user-attachments/assets/268c28cf-a8c6-4b93-a46d-e2d160df9df7" />


---

### Final API Response

<img width="1283" height="443" alt="Screenshot 2026-03-01 021107" src="https://github.com/user-attachments/assets/018e4108-049c-4383-8403-3b2a648f6757" />


---

# 🛠️ Technologies Used

This project combines AI and workflow automation tools.

Main technologies used include:

* **AI / LLM** – Intent detection and entity extraction
* **JavaScript** – Workflow logic
* **Webhook API** – User interaction
* **Property Database** – Property storage and retrieval
* **Cache System** – Performance optimization
* **Workflow Automation Platform**

---

# 📦 Example API Request

Example input request:

```json
{
  "query": "Find 2 bedroom apartments in Karachi with parking"
}
```

Example response:

```json
{
  "city": "Karachi",
  "property_type": "Apartment",
  "bedrooms": 2,
  "amenities": ["Parking"],
  "properties": [...]
}
```

---

# 🚀 Future Improvements

Possible improvements for the system include:

* Property recommendation system
* AI chatbot interface
* Price prediction model
* Map-based property search
* Voice-based property assistant

---

# 👨‍💻 Author

**Adeel Naeem**

AI / ML Developer
Focused on building intelligent AI assistants and automation systems.


