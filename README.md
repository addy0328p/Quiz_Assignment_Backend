# 🧠 Quiz Assignment - MERN Stack

A modern, fully-featured quiz application built using the **MERN stack (MongoDB, Express.js, React, Node.js)**.  
It provides a clean UI, timed quiz functionality, and dynamic questions fetched from the Open Trivia Database API.

---

## 🔗 Repository Links

- **Frontend Repository:** [Quiz Frontend Assignment](https://github.com/addy0328p/Quiz_frontend_assignment)
- **Backend Repository:** [Quiz Assignment Backend](https://github.com/addy0328p/Quiz_Assignment_Backend)
- **GitHub Profile:** [addy0328p](https://github.com/addy0328p)
- **Live Backend API:** [https://quiz-assignment-backend.onrender.com](https://quiz-assignment-backend.onrender.com)

---

## ✨ Features

### Core Functionality
- **📧 Email-based Quiz Start:** Users enter their email to begin the quiz session.
- **⏰ 30-Minute Countdown Timer:** Timer is displayed at the top; quiz auto-submits when time expires.
- **🎯 15 Dynamic Questions:** Pulled in real-time from the OpenTDB API.
- **🧭 Navigation Panel:** Users can jump between questions with clear status (visited/attempted).
- **📊 Result Page:** Displays each question, user’s answer, and the correct answer side by side.

### User Experience
- **🎨 Tech-inspired UI:** Dark theme with smooth transitions and modern layout.
- **📱 Responsive Design:** Works seamlessly across desktop, tablet, and mobile devices.
- **⚡ Smooth Transitions:** Animated navigation between questions.
- **📈 Progress Indicators:** Tracks visited and attempted questions in real-time.

---

## 🧩 Requirements (as per assignment)

### 1. **Layout & Flow**
- A start page where users submit their **email address**.
- **15 questions** are displayed one by one.
- A **30-minute timer** counts down from the top and **auto-submits** upon timeout.

### 2. **Navigation**
- Users can navigate freely to any question.
- Overview panel indicates:
  - Which questions are **visited**.
  - Which ones are **attempted**.

### 3. **End of Quiz**
- When the quiz ends (either manually submitted or timer expires), users are redirected to a **report page**.
- This report shows:
  - Each question.
  - The **user’s answer** and the **correct answer**, displayed side by side for comparison.

### 4. **Data Source**
- Questions are fetched from the [Open Trivia DB API](https://opentdb.com/api.php?amount=15).
- The API provides:
  - `question`, `correct_answer`, and `incorrect_answers`.
- Choices displayed = concatenation of `correct_answer + incorrect_answers`.

---

## ⚙️ Technical Details

### **Frontend**
- **Framework:** React 18  
- **State Management:** React Context API  
- **HTTP Client:** Axios  
- **Styling:** Custom CSS (Dark theme)  
- **Deployment:** Vercel  

### **Backend**
- **Runtime:** Node.js  
- **Framework:** Express.js  
- **Database:** MongoDB (via Mongoose ODM)  
- **API Type:** RESTful  
- **Deployment:** Render  
- **Live URL:** [https://quiz-assignment-backend.onrender.com](https://quiz-assignment-backend.onrender.com)

### **APIs**
- `POST /api/quiz/start` – Start a quiz session  
- `PUT /api/quiz/question/:quizId/:questionId` – Update question progress  
- `POST /api/quiz/submit/:quizId` – Submit the quiz  
- `GET /api/quiz/results/:quizId` – Retrieve result data  
- `GET /api/health` – Health check  

---

## 🧠 Judgment Criteria

### 1. **Functionality**
- All requirements (layout, timer, navigation, and result page) are fully implemented and work correctly.

### 2. **Bug-Free Code**
- The application runs without runtime or logical errors.
- Proper error handling is implemented on both frontend and backend.

### 3. **Code Quality**
- Clean, modular, and well-organized code.
- Consistent naming conventions.
- Comments used **judiciously** for complex or non-intuitive logic.

---

## 🚀 Submission & Hosting

### Hosted On:
- **Frontend:** Vercel  
- **Backend:** Render  

### Included in Repository:
- Clear `README.md` with setup & usage details.
- Instructions to run locally and in production.
- Explanation of challenges, design choices, and assumptions.

---

## 🧾 How to Run Locally

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)
- Git

### Installation
```bash
# Clone both repositories
git clone https://github.com/addy0328p/Quiz_Assignment_Backend.git
git clone https://github.com/addy0328p/Quiz_frontend_assignment.git

# Backend setup
cd Quiz_Assignment_Backend
npm install
npm run dev

# Frontend setup (in a new terminal)
cd ../Quiz_frontend_assignment
npm install
npm start
