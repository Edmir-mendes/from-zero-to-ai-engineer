# 📝 Boarding Log - Lesson 1

**Date:** June 30, 2026  
**Module:** 0 — Computer Science Fundamentals & Environment  
**Subtopic:** 0.1 — Hardware Basics: CPU, RAM, SSD/HDD, GPU, Processes, and Threads  

---

## 🧠 What I Learned Today (In my own words)

* **The Kitchen Analogy:** A computer operates exactly like a restaurant kitchen when running our code and AI models.
    * **CPU (The Chef):** Handles complex, logical calculations. Highly intelligent and fast, but handles few tasks at a time (sequential processing). It must work in lockstep with the GPU to avoid performance bottlenecks.
    * **RAM (The Workbench):** The live workspace where anything actively running *right now* must live. Attempting to load data larger than this workbench capacity crashes the system.
    * **SSD/HDD (The Pantry):** Permanent storage for large files and datasets. SSDs act as an easily accessible cabinet; HDDs act like a slow warehouse down the hall.
    * **GPU (The Prep Cooks):** Thousands of simple cores working in parallel. Indispensable for Computer Vision and AI because it handles billions of simultaneous matrix operations.

* **Processes vs. Threads:** A **Process** is an isolated application allocated its own space on the RAM (e.g., an active Python interpreter instance). A **Thread** is a smaller sub-task running inside that process, sharing its memory space.

* **Data Engineering Strategy (Divide and Conquer):** If faced with a massive dataset (e.g., 50 GB) and limited RAM (e.g., 16 GB), loading it entirely at once triggers an *Out of Memory* (OOM) crash. The industry-standard solution is to read and process the file in smaller **chunks** (batches).

* **Local AI Scaling:** Large-weights models (like Llama 3 8B) require massive working memory (8 Billion parameters $\times$ 2 Bytes per parameter = 16 GB). To make them viable on consumer edge hardware, we use **Quantization** to shrink the parameter file size without breaking the underlying capabilities.