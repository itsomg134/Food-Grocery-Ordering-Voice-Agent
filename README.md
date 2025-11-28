
# 🛒 Voice-Based Food & Grocery Ordering Agent

<div align="center">

![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![Python](https://img.shields.io/badge/Python-3.11-yellow?logo=python)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?logo=javascript)
![JSON](https://img.shields.io/badge/Storage-JSON-orange?logo=json)
![Docker](https://img.shields.io/badge/Docker-Ready-0db7ed?logo=docker)
![License](https://img.shields.io/badge/License-MIT-green)

**A Voice-Enabled Shopping Agent that understands your grocery needs, manages your cart, places orders, and even tracks past orders — fully powered using JSON.
Built for the #MurfAIVoiceAgentsChallenge.**

[Features](#-features) • [Project-Structure](#️-project-structure) • [Quick-Start](#-quick-start) • [Demo](#-demo-video) • [Author](#-author)

</div>

---
<img width="1280" height="720" alt="Brown and Beige Modern AI Features YouTube Thumbnail" src="https://github.com/user-attachments/assets/4974979c-84da-47fe-9e73-7ea7233e761c" />

## 🛍️ Overview

This project is a **voice-controlled grocery and food ordering assistant** that can:

✔ Understand what items the user wants
✔ Handle quantities, substitutions & ingredients
✔ Maintain a live cart during conversation
✔ Save final order as a JSON file
✔ Track previous orders
✔ Provide delivery status (mocked)

Perfect for building **Swiggy / Zomato / Zepto-style voice ordering** workflows.

---


https://github.com/user-attachments/assets/6c717e07-556b-48d4-880f-4fee58c24753


## 🎯 Primary Goal (MVP)

### **Food & Grocery Ordering with Cart → Order JSON**

Your voice agent can:

### 🧾 **1. Read from a Catalog JSON**

You create a structured catalog with:

* Groceries (milk, bread, eggs…)
* Snacks
* Fresh produce
* Prepared food (pizza, sandwiches, biryani…)
* Household essentials

### 🛒 **2. Understand User Intent**

The agent extracts:

* Item names
* Quantities
* Variants (e.g., “brown bread”)
* High-level intents like *“ingredients for pasta”*

### ➕ **3. Add to Cart**

Keeps a running cart as the conversation flows.

### 📦 **4. Place Order**

When the user says *“place order”*, the bot:

* Saves the cart as a JSON file
* Generates `order_id`
* Stores timestamp, total amount, and items

---

## 🚀 Advanced Features

### **📡 Mock Order Tracking**

Each placed order gets a status:

* *Confirmed → Packed → Out for Delivery → Delivered*

When the user asks:

> “Where is my order?”

The agent reads the JSON status.

### **📚 Order History**

All previous orders are saved in an `orders/` directory.

The agent can answer:

* “Show my last order”
* “Repeat my previous order”
* “Order the same snacks again”

---

## ⭐ Features

### ✔ Natural Language Ordering

Understands flexible user phrases:

* “Get me 2 packets of Lays”
* “I need ingredients for Maggie”
* “Add one medium Veg Pizza”
* “Remove eggs from cart”

### ✔ Smart Ingredient Bundles

Example:

> “I want to make pasta”

Bot automatically adds:

* Pasta
* Onion
* Tomato
* Garlic
* Masala

### ✔ JSON-Based Persistence

All data stored locally:

* `catalog.json`
* `orders/order_123.json`
* `history.json`
* `tracking.json`

### ✔ Voice Input + TTS Output

Built using Murf Falcon STT & TTS.

---

## 🛠️ Tech Stack

* **Python** (core agent logic)
* **JSON** for catalog + order storage
* **Murf Falcon Voice Models**
* **Optional Docker Setup**
* **Speech-to-Text + Text-to-Speech Pipeline**

---

## 📁 Project Structure

```
/Food-Grocery-Voice-Agent
│
├── data/
│   ├── catalog.json
│   ├── history.json
│   └── orders/
│       ├── order_001.json
│       └── order_002.json
│
├── src/
│   ├── agent.py
│   ├── cart_manager.py
│   ├── order_manager.py
│   ├── catalog_loader.py
│   └── tracking_engine.py
│
├── logs/
├── requirements.txt
└── README.md
```

---

## ⚙️ Quick Start

### **1. Clone the Repo**

```bash
git clone https://github.com/yourusername/Food-Grocery-Voice-Agent
cd Food-Grocery-Voice-Agent
```

### **2. Install Dependencies**

```bash
pip install -r requirements.txt
```

### **3. Run the Voice Agent**

```bash
python src/agent.py
```

---

## 🧪 Sample Order JSON

```json
{
  "order_id": "ORD-1024",
  "timestamp": "2025-11-28T10:32:00",
  "items": [
    { "name": "Milk", "quantity": 2, "price": 28 },
    { "name": "Bread - Brown", "quantity": 1, "price": 45 }
  ],
  "total_amount": 101,
  "status": "Packed"
}
```

---

## 🎥 Demo Video

📎 https://drive.google.com/file/d/1IKyFaaXQrR7d-tmofOyvjm9-vVBij3i_/view?usp=drive_link

---

## 📌 Future Improvements

* Delivery ETA prediction
* Payment simulation
* Image-based catalog viewer
* Real-time voice interruptions handling
* Integrate with a real backend

---

## 👨‍💻 Author

**Om Gedam**
GitHub: **@itsomg134**
Email: **[omgedam123098@gmail.com](mailto:omgedam123098@gmail.com)**
Twitter (X): **@omgedam**
LinkedIn: **Om Gedam**
Portfolio: **[https://ogworks.lovable.app](https://ogworks.lovable.app)**

Built with ❤️ to simplify everyday shopping.
