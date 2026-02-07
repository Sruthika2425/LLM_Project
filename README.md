# LangChain Enterprise AI System

The **LangChain Enterprise AI System** is an AI-powered decision support platform that enables enterprises to analyze customer risk and financial exposure using **natural language queries**.  
The system combines **LangChain orchestration**, **LLM reasoning**, and **structured enterprise data** to generate intelligent, actionable business decisions.

---

## 📌 Project Overview

Enterprises handle large volumes of customer-related data such as usage metrics, billing records, and support interactions. Extracting meaningful insights and making timely decisions from this data is challenging.

This project solves that problem by allowing business users to:
- Ask questions in **natural language**
- Automatically analyze customer churn and risk
- Generate AI-driven business decisions using LangChain agents and tools

---

## 🎯 Objectives

- Enable business decision-making using natural language input  
- Analyze customer churn and risk factors  
- Integrate structured enterprise data with LLM reasoning  
- Demonstrate enterprise-grade LangChain architecture  
- Provide a modular and scalable AI system design  

---

## 🚀 Key Features

- Natural Language Business Query Interface  
- LangChain-based Orchestration Layer  
- Intent Detection for Query Classification  
- Domain-Specific Chains (Customer & Finance)  
- SQL Tool Integration for Structured Data Access  
- Customer Risk Analysis (Churn, Usage, Support)  
- Financial Exposure Analysis  
- AI-Generated Final Decision Output  
- Web-Based Interactive Interface  

---

## 🧠 How the System Works

1. User enters a natural language business query  
2. The query is routed through the LangChain orchestration layer  
3. Intent detection identifies the domain of the query  
4. Relevant domain-specific chains are executed  
5. SQL tools retrieve enterprise data from the database  
6. The LLM reasons over retrieved data  
7. A final structured business decision is generated  

---

## 🏗️ System Architecture

```mermaid
flowchart TD

U[User Interface<br/>Streamlit UI]
U --> Q[Natural Language Query]

Q --> O[LangChain Orchestration Layer]

O --> I[Intent Detection Chain]
I -->|Customer Intent| C[Customer Chain]
I -->|Finance Intent| F[Finance Chain]

C --> T[SQL Tools]
F --> T

T --> DB[(Enterprise Intelligence DB<br/>SQLite)]

DB --> T
T --> O

O --> LLM[LLM Reasoning Engine]
LLM --> R[Final Business Decision]

R --> U
