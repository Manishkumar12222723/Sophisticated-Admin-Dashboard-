# 🤖📊 Power BI Dashboard: Bot Performance Evaluation (Multilingual & RLS)

This repository contains a **Power BI-based interactive dashboard** designed for **admin-level monitoring and analysis of chatbot performance** in a telecom organization. The dashboard offers **role-based access control (RLS)** and supports both **English and Arabic-speaking users**, enabling secure and accessible insights across departments.

---

## 📌 Table of Contents

- [📈 Project Overview](#-project-overview)
- [🎯 Objectives](#-objectives)
- [🔧 Features](#-features)
- [📁 Dataset Description](#-dataset-description)
- [📊 Dashboard Capabilities](#-dashboard-capabilities)
- [🏗 Project Structure](#-project-structure)
- [💡 How to Use](#-how-to-use)
- [🔐 Role-Based Access (RLS)](#-role-based-access-rls)
- [🌐 Multilingual Design](#-multilingual-design)
- [🚀 Future Enhancements](#-future-enhancements)
- [📷 Dashboard Preview](#-dashboard-preview)
- [📜 License](#-license)
- [👨‍💼 Author](#-author)

---

## 📈 Project Overview

This project visualizes bot interactions, performance, response speed, and OpenAI-related cost metrics across multiple departments. The data comes from two primary sources:

- **`OpenAI_Analytics`**: Captures API usage, token consumption, and associated costs.
- **`Response_Analytics`**: Logs chatbot responses, success/failure rates, query types, and response times.

Together, these form the foundation for a **sophisticated Power BI dashboard** that enables **decision-making, optimization, and cost control**.

---

## 🎯 Objectives

- Provide **department-wise visibility** into chatbot performance.
- Analyze **API consumption trends** and **costs** (OpenAI, GPT, ADA).
- Identify **high-performing** and **underperforming bots**.
- Monitor **service availability** and **response quality**.
- Empower stakeholders with **data-driven decisions**.

---

## 🔧 Features

- ✅ Interactive filters for date, department, language, and query category
- ✅ Key KPIs: Total Queries, Success Rate, Cost, API Calls, Avg. Response Time
- ✅ Breakdown of GPT vs ADA usage
- ✅ Service Availability (%) tracking
- ✅ Query-response performance table
- ✅ **Arabic-English toggle** using bookmarks
- ✅ **Role-Based Access Control (RLS)** per department
- ✅ Export-ready visual summaries

---

## 📁 Dataset Description

### 🔹 `Response_Analytics`

| Column Name       | Description                              |
|------------------|------------------------------------------|
| `client_name`     | Department using the bot                 |
| `conversation_id` | Unique session identifier                |
| `datetime`        | Timestamp of the query                   |
| `language`        | Language used in the query (e.g., "en", "ar") |
| `query`           | Input question from user                 |
| `query_category`  | Category of the query                    |
| `response`        | Output response from the chatbot         |
| `response_category` | Valid, Invalid, or Failure category   |
| `response_time`   | Time taken to respond (in seconds)       |
| `user_location`   | Location of the user                     |

---

### 🔹 `OpenAI_Analytics`

| Column Name       | Description                              |
|------------------|------------------------------------------|
| `openai_call`     | Number of OpenAI API calls               |
| `openai_cost`     | Total cost incurred for the API usage    |
| `gpt_call_count`  | GPT-specific call count                  |
| `ada_call_count`  | ADA-specific call count                  |
| `tokens_generated`| Number of tokens generated               |
| `query_tokens`    | Tokens used in input                     |
| `datetime`        | Timestamp of API interaction             |
| `conversation_id` | Link to response data                    |

---

## 📊 Dashboard Capabilities

| Section | Description |
|--------|-------------|
| **KPIs** | Display core indicators: Total Queries, Success Rate, Total Cost, Avg. Response Time, Total Calls |
| **Visuals** | Bar charts for GPT vs ADA usage, pie charts for success/failure, and area charts for cost/time trends |
| **Departmental View** | Filter visualizations by department using slicers and dynamic visuals |
| **Table Reports** | Export-ready tabular view of bot performance for specific filters |
| **Multilingual Design** | English and Arabic versions of dashboards using bookmarks |
| **Quota Monitoring** | OpenAI quota usage and tracking logic (future add-on) |

---

## 🏗 Project Structure

```plaintext
├── CC_Data.xlsx                     # Main dataset (OpenAI + Response logs)
├── Bot_Performance_Dashboard.pbix  # Power BI dashboard file
├── assets/
│   └── dashboard_preview.png       # Dashboard image preview
└── README.md                       # Project documentation
