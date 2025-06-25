

# Langchain Streamlit Chatbot for Data Exploration and Analysis using LLMs

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Langchain](https://img.shields.io/badge/Langchain-Enabled-green) ![Streamlit](https://img.shields.io/badge/Streamlit-App-red)

## 📌 Project Overview

This project demonstrates how to build a **Streamlit-based chatbot** integrated with **Langchain** and **OpenAI LLMs** to enable natural language interaction with a **MySQL database**. The chatbot interprets user queries in plain English, translates them into SQL queries, fetches the data, and visualizes the results — streamlining the data exploration process for non-technical users.

## 🎯 What You'll Learn

* Understand LLMs, attention mechanisms, and transformer architecture
* Explore use cases of LLMs in real-world applications
* Get started with Langchain and prompt engineering
* Connect LLMs to SQL databases for query generation
* Automatically generate and run Python code for data visualization
* Build a fully functional Streamlit chatbot application

## 📦 Repository Contents

```
.
├── agent.py               # Langchain agents for SQL and Python code generation
├── chat_app.py           # Streamlit-based chatbot UI
├── helper.py             # Utility functions for prompt formatting and query parsing
├── requirements.txt      # All required dependencies
├── stream_lit_demo.py    # Alternate Streamlit launcher
├── Query_To_Dashboard-2.ipynb  # Notebook version for debugging and experimentation
└── README.md             # Project documentation
```

## 🧠 Tech Stack

* **Programming Language**: Python 3.10.4
* **Frontend**: Streamlit
* **Backend**: MySQL (via `mysql-connector-python` and `mysqlclient`)
* **LLM Framework**: Langchain
* **Visualization**: Matplotlib, Plotly
* **Model**: OpenAI GPT-3.5 Turbo / GPT-4 Turbo

## 🗂️ Dataset Description

The e-commerce dataset consists of 7 interconnected tables:

* `distribution_centers`: IDs, names, and coordinates of distribution centers
* `events`: User events including timestamps and actions
* `inventory_items`: Product inventory across centers
* `order_items`: Detailed order breakdown
* `orders`: Master order metadata
* `products`: Product attributes and pricing
* `users`: User profile and traffic information

## 🛠️ Setup Instructions

1. **Clone this repository**

   ```bash
   git clone https://github.com/sathvik6198/LLM-SQL-Chatbot.git
   cd LLM-SQL-Chatbot
   ```

2. **Create virtual environment (optional but recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   venv\Scripts\activate     # Windows
   ```

3. **Install required packages**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up MySQL**

   * Install MySQL and MySQL Workbench
   * Create a database and import the 7 CSV files

5. **Run the Streamlit App**

   ```bash
   streamlit run chat_app.py
   ```

## 💡 Project Highlights

* Converts natural language to SQL using Langchain
* Visualizes results with auto-generated Python code
* Includes guardrails and memory for consistent responses
* Easy to extend for new datasets or visualizations

## 💰 Cost Estimation (OpenAI API)

| Model         | Cost per 1K tokens                  | Est. Total Cost for 100 queries |
| ------------- | ----------------------------------- | ------------------------------- |
| GPT-3.5 Turbo | \$0.0015 (input) / \$0.002 (output) | \~\$0.35–\$0.50                 |
| GPT-4 Turbo   | \$0.01 (input) / \$0.03 (output)    | \~\$5.00–\$10.00                |

Use GPT-3.5 for most interactions to save cost, and GPT-4 for complex logic.

> Note: Ensure your OpenAI account has available quota or free credits.

## 🚀 Future Enhancements

* Add role-based access for different user types
* Expand to support NoSQL databases
* Deploy on AWS/GCP/Azure for broader accessibility
