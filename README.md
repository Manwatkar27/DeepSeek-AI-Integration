# 🤖 DeepSeek AI Integration

A lightweight web application that integrates with the **DeepSeek AI model** using **Ollama** for smart and contextual AI responses. Built with a Spring Boot backend and a simple HTML + CSS frontend, this project demonstrates how to interact with LLMs without any database or complex front-end frameworks.

---

## 📌 Features

- 🧠 Ask questions and get responses from DeepSeek AI via Ollama
- 🛠️ Spring Boot-powered backend
- 🌐 Simple and stylish HTML + CSS frontend
- 🔗 Fast communication via REST API
- 🧪 Includes basic test cases

---

## 🛠 Tech Stack

| Layer        | Technology         |
|--------------|--------------------|
| Frontend     | HTML, CSS          |
| Backend      | Spring Boot (Java) |
| AI Model     | DeepSeek via Ollama |
| API Format   | REST               |

---

## 📁 Project Structure

deepseek-integration/
├── .mvn/
├── src/
│ └── main/
│ ├── java/com/deepseek_java/deepseek/
│ │ └── DeepseekSpringbootApplication.java
│ └── resources/
│ └── static/ ← HTML + CSS
├── test/
│ └── java/com/deepseek_java/
├── target/
├── pom.xml
├── HELP.md
└── README.md



---

## ⚙️ How to Run

### 1. Start Ollama with DeepSeek

Make sure you have [Ollama](https://ollama.com/) installed and the DeepSeek model pulled.

```bash
ollama run deepseek

2. Run Spring Boot Application
Use Maven wrapper to start the backend:

bash
Copy
Edit
./mvnw spring-boot:run
The application will be available at:
http://localhost:8080

3. Access Frontend
Open your browser and go to:

bash
Copy
Edit
http://localhost:8080/index.html
Ask your questions and receive replies from DeepSeek AI in real-time.

📦 API (Backend to Ollama)

Spring Boot sends a POST request like:

json
Copy
Edit
POST http://localhost:11434/api/generate
{
  "model": "deepseek",
  "prompt": "Your message here"
}
Receives response:

json
Copy
Edit
{
  "response": "AI-generated answer here"
}

🧪 Testing
Basic test classes are under:

swift
Copy
Edit
src/test/java/com/deepseek_java/
Run tests with:

bash
Copy
Edit
./mvnw test

🔒 Notes

API key is not required as Ollama runs locally.
No database used — replies are not stored.
