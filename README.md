

# Langchain Streamlit Chatbot for Data Exploration and Analysis using LLMs

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Langchain](https://img.shields.io/badge/Langchain-Enabled-green) ![Streamlit](https://img.shields.io/badge/Streamlit-App-red)

---

## 📌 Project Overview

This project demonstrates how to build an **LLM-powered chatbot** using **Streamlit**, **Langchain**, and **OpenAI** to allow **natural language interaction** with a SQL database. The chatbot interprets user prompts in plain English, translates them to SQL queries, fetches the data, and generates real-time visualizations. It empowers non-technical users to explore data and derive insights without writing code.

---

## 🎯 What You’ll Learn

* Understand how LLMs (like GPT-4) generate SQL queries and Python code
* Use Langchain to integrate LLMs with external tools
* Apply prompt engineering to interact with LLMs effectively
* Use Streamlit to create a chatbot UI
* Visualize data using auto-generated Matplotlib and Plotly code
* Access and query SQL databases using natural language

---

## 📁 Repository Structure

```
.
├── agent.py               # Langchain agents for SQL and Python generation
├── chat_app.py           # Main Streamlit chatbot app
├── helper.py             # Prompt templates and helper logic
├── Query_To_Dashboard-2.ipynb  # Jupyter notebook version
├── requirements.txt      # Python dependencies
├── stream_lit_demo.py    # Alternative Streamlit demo file
└── README.md             # Project documentation
```

---

## 🛠️ Tech Stack

* **Language**: Python 3.10.4
* **LLM Provider**: OpenAI GPT-4 / GPT-3.5 Turbo
* **Frameworks**: Langchain, Streamlit
* **Database**: MySQL
* **Visualization**: Matplotlib, Plotly

---

## 🧩 Step-by-Step Project Execution

### ✅ Step 1: Set Up the Environment

1. Clone the repo:

   ```bash
   git clone https://github.com/sathvik6198/LLM-SQL-Chatbot.git
   cd LLM-SQL-Chatbot
   ```

2. (Optional) Create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   venv\Scripts\activate     # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

### ✅ Step 2: Prepare the Database

1. Install MySQL and MySQL Workbench.

2. Create a new database called `ecommerce`.

3. Import the provided 7 CSV files into 7 tables:

   * `distribution_centers`
   * `events`
   * `inventory_items`
   * `order_items`
   * `orders`
   * `products`
   * `users`

4. Verify the schema using:

   ```sql
   SHOW TABLES;
   ```

---

### ✅ Step 3: Prompt Engineering & Langchain Agents

1. Define prompt templates in `helper.py` for:

   * SQL generation (e.g., “What are top-selling products last month?”)
   * Visualization code (e.g., “Bar chart of orders by city”)

2. Set up agents in `agent.py` using Langchain:

   * SQL Agent: Converts user query to SQL
   * Python Agent: Converts user intent to Python visualization code

3. Chain agents for multi-step tasks:

   * Natural Language → SQL → Python → Visualization

---

### ✅ Step 4: Build the Streamlit Chatbot

Run the chatbot:

```bash
streamlit run chat_app.py
```

Features:

* Accepts user input in plain English
* Displays auto-generated SQL code
* Runs SQL and retrieves data
* Generates Python visualization code using LLM
* Renders chart output in real-time

---

## 📊 Dataset Description

This project uses an **e-commerce dataset** with 7 interconnected tables:

| Table                  | Description                     |
| ---------------------- | ------------------------------- |
| `distribution_centers` | Center details (name, location) |
| `events`               | User session activity logs      |
| `inventory_items`      | Product inventory per center    |
| `order_items`          | Items per order                 |
| `orders`               | Order details (status, time)    |
| `products`             | SKU details and pricing         |
| `users`                | User demographics and source    |

---

## 💡 Sample Prompts

Try these in the chatbot:

* “Show me the number of orders by city”
* “Visualize user signups by month”
* “Top 5 selling products by revenue”
* “Bar chart of canceled orders by browser”

---

## 💰 OpenAI Cost Info

| Model         | Cost per 1K Tokens                  | Use Case                         |
| ------------- | ----------------------------------- | -------------------------------- |
| GPT-3.5 Turbo | \$0.0015 (input) / \$0.002 (output) | Basic queries & visualizations   |
| GPT-4 Turbo   | \$0.01 (input) / \$0.03 (output)    | Advanced analytics and reasoning |

**Tip:** Set `model_name = "gpt-3.5-turbo"` in `agent.py` to reduce cost.

> ⚠️ You must have an [OpenAI account](https://platform.openai.com/account/api-keys) with available quota or billing enabled.

---

## 📌 Final Outcome

You’ll have an **interactive dashboard agent** that:

* Accepts natural language input
* Generates insights from a SQL database
* Creates data visualizations automatically
* Makes analytics accessible to non-technical users

---

## 📌 Future Enhancements

* Add authentication to restrict access
* Support multi-database connections
* Deploy on AWS or GCP
* Add support for CSV uploads

---

## 🧠 Credits

Project inspired by educational use cases from:

* Langchain documentation
* Streamlit community
* ProjectPro’s “EDA using LLMs” guide
