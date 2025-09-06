
 Minjoy Food Chatbot

The Minjoy Food Chatbot is a conversational AI application that enables users to place, modify, and track food delivery orders.  
It is built with **FastAPI** and **MySQL**, and provides a lightweight web interface for interaction.

---

## ✨ Features
- Add food items with quantities to an order  
- Remove or modify items in an existing order  
- Complete an order and receive a unique order ID  
- Track an order’s status in real time using the order ID  
- Simple web interface (`chat.html`) for demo purposes  

---
## App demo and Screenshot:
Included in Frontend Dialogflow folder feel free to check them.


## 🛠️ Tech Stack
- **Backend**: FastAPI + Uvicorn  
- **Database**: MySQL  
- **Frontend**: HTML/CSS (lightweight demo UI)  
- **Language**: Python 3.10  

---

## 📂 Project Structure
```

Minjoy-Food-Chatbot/
│── backend/
│   ├── main.py            # FastAPI application
│   ├── db\_helper.py       # Database functions
│   ├── generic\_helper.py  # Utility functions
│   ├── chat.html          # Simple frontend chat UI
│── database/              # SQL schema and setup scripts

````

---

## ⚡ Getting Started

### 1️⃣ Clone the repository
```bash
git clone https://github.com/mirnabadr/Minjoy-Food-Chatbot.git
cd Minjoy-Food-Chatbot/backend
````

### 2️⃣ Install dependencies

```bash
pip install fastapi uvicorn mysql-connector-python
```

### 3️⃣ Set up the database

* Install and run MySQL locally
* Create a database (e.g., `food_orders`)
* Import the schema from the `database/` folder

Update `db_helper.py` with your MySQL credentials.

### 4️⃣ Run the server

```bash
uvicorn main:app --reload
```

The API will be available at **[http://127.0.0.1:8000](http://127.0.0.1:8000)**

### 5️⃣ Open the web demo

* Navigate to: **[http://127.0.0.1:8000/](http://127.0.0.1:8000/)**
* Use the chatbot to add, remove, and track orders

---

## 📌 Example Request (API)

**POST /**

```json
{
  "queryResult": {
    "intent": {"displayName": "order.add - context: ongoing-order"},
    "parameters": {"food-item": ["pizza"], "number": [2]},
    "outputContexts": [{"name": "session-1"}]
  }
}
```

Response

  json
{
  "fulfillmentText": "So far you have: 2 pizza. Do you need anything else?"
}


 🤝 Contribution

Contributions, issues, and feature requests are welcome!
Feel free to fork this repo and submit pull requests.

📧 Author

👩‍💻 Mirna Badr
🔗 GitHub: [mirnabadr](https://github.com/mirnabadr)
🔗 Project Repo: [Minjoy-Food-Chatbot](https://github.com/mirnabadr/Minjoy-Food-Chatbot.git)

```






