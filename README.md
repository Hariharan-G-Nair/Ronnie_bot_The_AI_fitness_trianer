# 🏋️ Ronnie Bot - The AI Fitness Trainer — Retrieval-Augmented Generation (RAG) Chatbot with Llama 3

Ronnie Bot is a conversational **Retrieval-Augmented Generation (RAG)** chatbot built using **Flask, LangChain, FAISS, and Groq-hosted Llama 3**.

The application answers **fitness, workout, rehabilitation, nutrition, cardio, and supplement-related queries** by retrieving relevant information from multiple structured CSV knowledge bases and generating accurate, context-aware responses using a Large Language Model (LLM).

Unlike traditional chatbots that rely only on pre-trained knowledge, this system dynamically retrieves domain-specific information using **semantic similarity search with FAISS**, injects the retrieved context into the LLM prompt, and maintains conversational memory for coherent multi-turn interactions.

This project demonstrates a practical, end-to-end implementation of a production-style RAG pipeline with a clean web interface and real-world applicability.

---

# 🚀 Features

- 📄 Multiple CSV-based fitness knowledge sources
- 🧠 Conversational memory (context-aware responses)
- 🔍 Semantic similarity search using FAISS
- 🤖 Groq-hosted Llama 3.1 (8B Instant)
- 🌐 Flask REST API
- 💬 Interactive browser-based chat UI
- ⚡ Fast inference using Groq API
- 🏋️ Workout, diet, rehab, supplement, and cardio guidance
- 💾 Automatic FAISS index creation & loading

---

# 🏗️ Tech Stack

| Component | Technology |
|----------|-------------|
| Backend | Flask |
| LLM | Groq — `llama-3.1-8b-instant` |
| Framework | LangChain |
| Vector Store | FAISS |
| Embeddings | `sentence-transformers/all-MiniLM-L6-v2` |
| Frontend | HTML, CSS, Vanilla JavaScript |
| Language | Python 3.11 |

---

# 📁 Project Structure

```bash
Fitness_trainer_app/
│
├── app.py
├── chatbot.py
├── requirements.txt
├── .env
├── .gitignore
├── faiss_index/
│
├── templates/
│   └── index.html
│
├── 1500_workout_routines.csv
├── indian_nutrition_diet_1200_records.csv
├── indian_food_nutrition_520_unique_foods.csv
├── megaGymDataset.csv
├── training_types.csv
├── cardio_hiit_workouts_500_plus.csv
├── workout_theory_nutrition_guide.csv
├── Injury prevention and rehab.csv
├── Supplement guide.csv
└── Warm_up.csv
```

---

# 🔑 Prerequisites

- Python 3.11
- A Groq API Key

Get your API key from:

https://console.groq.com

---

# ⚙️ Setup Instructions

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/fitness-trainer-chatbot.git

cd fitness-trainer-chatbot
```

---

## 2️⃣ Create & Activate Virtual Environment

### Windows (PowerShell)

```bash
python -m venv myenv

myenv\Scripts\Activate.ps1
```

### Windows (CMD)

```bash
python -m venv myenv

myenv\Scripts\activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Create a `.env` File

Create a file named `.env` in the project root directory:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

# 🧠 FAISS Index Creation

The application automatically creates a FAISS vector index during the first run using all CSV knowledge sources.

On subsequent runs:

- Existing FAISS indexes are loaded automatically
- Rebuilding embeddings is skipped for faster startup

Generated FAISS files are stored inside:

```bash
faiss_index/
```

---

## 5️⃣ Run the Application

```bash
python app.py
```

You should see:

```bash
Flask server launching...
⚡ Creating new FAISS index...
```

Or if the index already exists:

```bash
Flask server launching...
✅ Loading existing FAISS index...
```

---

# 🌐 Open in Browser

```bash
http://127.0.0.1:5000
```

---

# ⚠️ Notes

- FAISS index is automatically persisted locally
- Memory resets when the Flask server restarts
- First startup may take longer due to embedding model download
- `favicon.ico` 404 warnings are harmless
- `.env`, `__pycache__`, and `faiss_index/` are excluded using `.gitignore`

---

# 🔮 Future Improvements

- 🧠 Per-user conversational memory
- ⏳ Streaming token responses
- 🌙 Dark mode UI
- 🐳 Full Docker deployment
- 📱 Mobile responsive interface
- ☁️ Cloud vector database support
- 🔐 Authentication & user sessions

---

# 🤝 Contributing

Contributions are welcome!

Feel free to:

- Open issues
- Submit pull requests
- Suggest new fitness datasets
- Improve UI/UX

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

## Hariharan G

- Data Scientist
- AI Developer
- Fitness Analyst/Trainer
