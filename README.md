# 🎓 EduBot — AI Student Assistant Chatbot

An intelligent, AI-powered chatbot designed to assist students with subject queries, timetable management, exam schedules, and study guidance.

---

## 📸 Preview

> Add a screenshot of your chatbot here after uploading.
> `![EduBot Preview](screenshot.png)`

---

## 🚀 Features

- 🤖 **AI-Powered Chat** — Real-time responses using Claude (Anthropic API)
- 📅 **Timetable Management** — View full weekly class schedule
- 📋 **Exam Schedule & Countdown** — Track upcoming exams with urgency alerts
- 💬 **Interactive Chat Interface** — Clean, responsive chat UI
- ⚡ **Quick Actions** — One-click prompts for common student queries
- 🧠 **Study Assistance** — Get help with subjects, concepts, and study tips
- 🗑️ **Clear Chat** — Reset conversation anytime

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure and layout |
| CSS3 | Styling and animations |
| JavaScript (ES6+) | Logic and interactivity |
| Anthropic Claude API | AI-powered responses |
| Google Fonts | Typography (Sora, Space Mono) |

> **Note:** MySQL integration can be added for storing chat history, user profiles, and dynamic timetable/exam data.

---

## 📁 Project Structure

```
student-ai-chatbot/
│
├── student-ai-chatbot.html   # Main application file
├── README.md                 # Project documentation
└── screenshot.png            # Preview image (add yours)
```

---

## ⚙️ Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/student-ai-chatbot.git
cd student-ai-chatbot
```

### 2. Get Your Anthropic API Key
- Go to [console.anthropic.com](https://console.anthropic.com)
- Sign up / Log in
- Navigate to **API Keys** → Create a new key

### 3. Add Your API Key
Open `student-ai-chatbot.html` and find this line:
```javascript
headers: { 'Content-Type': 'application/json' },
```
Add your key:
```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_API_KEY_HERE',
  'anthropic-version': '2023-06-01'
},
```

### 4. Open in Browser
Simply open `student-ai-chatbot.html` in any modern browser — no server needed!

---

## 💬 How to Use

1. Open the chatbot in your browser
2. Type any question in the input box
3. Press **Enter** or click the send button
4. Use **Quick Action** buttons in the sidebar for common queries
5. Click **📅 Timetable** or **📋 Exams** in the navbar for schedule details
6. Click **🗑 Clear** to reset the conversation

### Example Questions You Can Ask
- *"What are my classes today?"*
- *"When is my next exam?"*
- *"Explain Newton's laws of motion"*
- *"Give me tips to study for Math"*
- *"Help me write an essay introduction"*

---

## 🗄️ MySQL Integration (Optional)

To connect a database for dynamic data, create the following tables:

```sql
CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100)
);

CREATE TABLE timetable (
  id INT AUTO_INCREMENT PRIMARY KEY,
  student_id INT,
  day VARCHAR(20),
  time VARCHAR(20),
  subject VARCHAR(100),
  room VARCHAR(50),
  teacher VARCHAR(100)
);

CREATE TABLE exams (
  id INT AUTO_INCREMENT PRIMARY KEY,
  student_id INT,
  subject VARCHAR(100),
  exam_date DATE,
  exam_time TIME,
  room VARCHAR(50)
);

CREATE TABLE chat_history (
  id INT AUTO_INCREMENT PRIMARY KEY,
  student_id INT,
  role VARCHAR(20),
  message TEXT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🌐 Live Demo

Hosted via GitHub Pages:
👉 `https://YOUR_USERNAME.github.io/student-ai-chatbot/student-ai-chatbot.html`

---

## 👨‍💻 Author

**Your Name**
- GitHub: [@YOUR_USERNAME](https://github.com/Lavanya3118)
- Email: your@email.com

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙏 Acknowledgements

- [Anthropic](https://anthropic.com) — Claude AI API
- [Google Fonts](https://fonts.google.com) — Sora & Space Mono fonts
- [GitHub Pages](https://pages.github.com) — Free hosting

