# 🧠 Multi-Agent AI Blog Generation System

An end-to-end multi-agent content generation pipeline built using LangGraph, LLM orchestration, and Stable Diffusion, capable of autonomously generating high-quality technical blogs with structured sections, citations, and contextual images.

---

## 🚀 Overview

This project automates the entire blog creation workflow:

- Topic → Planning → Research → Writing → Image Generation → Final Markdown  
- Uses a graph-based multi-agent architecture to coordinate specialized agents  
- Produces developer-grade technical blogs with structured sections and optional citations  

---

## Workflow
<img width="160" height="630" alt="image" src="https://github.com/user-attachments/assets/5d2020ba-e10e-4f1b-aadc-36312f701859" /> <img width="252" height="432" alt="image" src="https://github.com/user-attachments/assets/4caf0a61-9d88-4432-a420-0dc4fe78c47d" />


---

## 🏗️ Architecture

The system is built as a stateful directed graph:

Router → Research → Orchestrator → Workers (parallel) → Reducer → Image Generator

### Key Components

- Router Agent  
  Decides execution mode: closed_book, hybrid, open_book  

- Research Agent  
  Fetches and filters relevant web results using Tavily API  

- Orchestrator Agent  
  Generates structured blog plan (5–8 sections)  

- Worker Agents  
  Generate sections concurrently (fan-out execution)  

- Reducer + Image Pipeline  
  Merges sections and generates images using Stable Diffusion  

---

## ⚙️ Features

- Multi-agent orchestration using LangGraph  
- Dynamic execution modes  
- Parallel content generation (2–3× faster)  
- Automated research integration  
- Structured blog generation  
- AI-driven image generation (SDXL)  

---

## 🧪 Tech Stack

- LangGraph  
- LangChain  
- Groq LLM (LLaMA 3.3 70B)  
- Tavily API (web search)  
- Hugging Face Inference API  
- Stable Diffusion XL  

---

## 📂 Output

- Markdown blog file  
- Auto-generated images stored locally  
- Structured, production-ready content  

---

## ▶️ Usage

```bash
python main.py
```

```python
run("Your Blog Topic")
```

---

## 📌 Example

```python
run("Self Attention Mechanism")
```

---

## 📈 Performance

- ~80% reduction in manual writing effort  
- 2–3× faster generation via parallel execution  
- 5–8 structured sections per blog  
- Up to 3 contextual images per blog  

---

## 🤝 Contributing

Feel free to fork and improve the system by adding:
- Better agents  
- More tools  
- Improved prompts  

---

## 📜 License

MIT License
