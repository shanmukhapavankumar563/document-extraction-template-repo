# Internship Challenge: Document Extraction Service

Welcome! This challenge is designed to evaluate your problem-solving skills and your technical ability to work with unstructured data documents. You have **10 days** to complete this task from the moment you accept the invitation link.

## 📅 Challenge Timeline
* **Start Date:** [Insert Date/Time]
* **End Date:** [Insert Date/Time - 10 days later]
* **Submission:** Your final commit must be pushed before the deadline.
* **Branch Policy:** You must perform all work and submit final code on the **`main`** branch only.

---

## 🚀 The Problem Statement
Your task is to build an application (preferably using **Python**) that can process document images or PDFs to achieve the following:

1. **Classification:** Automatically identify if the document is an **Invoice** or a **Packing List**.
2. **Extraction:** Extract key fields and provide the final result in **Excel (.xlsx) or JSON format**:
   * **For Invoices:** Vendor Name, Invoice Number, Invoice Date, and the Table of Contents (Line Items).
   * **For Packing Lists:** Order Number / Purchase Order (PO) Number, Ship-to Address, and the Table of Contents (Line Items).

---

## 🛠️ Technical Constraints (Local-First)
To ensure data privacy and cost-efficiency, we have the following strict requirements:
* **No External/Paid APIs:** You are **not** allowed to use paid or external services (e.g., OpenAI API, AWS Textract, Azure Document Intelligence).
* **Local LLM Hosting:** If you choose an LLM-based solution for extraction or classification, it must be a **lightweight model** (e.g., Llama 3.2-3B, Phi-3, or Mistral-7B) capable of being **hosted locally** (using tools like Ollama, Llama.cpp, or Hugging Face).
* **Tech Stack:** You are responsible for documenting how to set up the local environment to run your solution.

---

## 📂 Repository Structure
* `/app`: Your source code and application files.
* `/samples`: Initial samples provided. Add your own samples here in sub-folders (e.g., `/training`, `/test`).
* `/output`: This is where your **sample outputs** (Excel/JSON files) from the extraction process must be stored.
* `/resumes`: Upload your resume here as a **PDF file**.
* `/design`: Detailed documentation explaining your logic (Images, PDF, or Docx).
* `README.md`: This file.

---

## 🛠️ Design & Documentation Requirements
We will **primarily review your design folder** to evaluate your approach. Your documentation must be detailed and cover:
* **Tech Stack:** Specific versions of local models, libraries (e.g., Tesseract, PaddleOCR), and frameworks used.
* **Component Architecture:** How the data flows from a raw PDF to a structured Excel/JSON file.
* **Logic & Exceptions:** Explain how you arrived at the output and how you handle **exceptions** (e.g., blurred images, missing fields, or classification errors).
* **Validation:** Keep samples of your successful outputs within the `/design` folder as well.
* **Visuals:** Use diagrams, flowcharts, or screenshots to explain your system.

---

## ⚖️ Rules & Evaluation
1. **Multilingual Support:** English documents only for this assessment.
2. **The "10-Day" Rule:** No commits will be accepted after the 10-day window.
3. **Interview Stage:** At the time of the interview, you will be asked to **live-code or walk through your logic** and explain how you handled specific document structures.

---

## ❓ Questions
If you have questions, please open an **Issue** in the [Main Template Repository]. Do not email the recruiters directly.

**Good luck! We are excited to see your local-first, innovative approach.**
