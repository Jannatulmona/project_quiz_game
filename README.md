
# 🎯 QUIZ APP – JavaFX Based Desktop Application

A modern, interactive desktop **Quiz Application** developed using **JavaFX** and **MySQL**.  
This app is designed to conduct programming quizzes with real-time scoring, timer-based questions, and detailed performance tracking.

---
## 🚀 Features
- 🔐 Secure User Login & Registration
- ⏱️ Time-limited Questions (15 seconds per question)
- 🧠 MCQ-based Programming Quizzes
- 📊 Real-time Score Calculation
- 🏆 Leaderboard System
- 💾 MySQL Database Integration
- 🖥️ User-friendly JavaFX Interface
- ❌ Error Handling & Validation
---

## 🛠️ Technologies Used
- **Java**
- **JavaFX**
- **FXML**
- **MySQL**
- **JDBC**
- **MVC Architecture**

---

## 📁 **Project Structure**
QuizApp/
│
├─ src/
│   └─ main/
│       ├─ java/
│       │   └─ org/example/
│       │       ├─ Main.java
│       │       ├─ WelcomeController.java
│       │       ├─ LoginController.java
│       │       ├─ RulesController.java
│       │       ├─ QuizController.java
│       │       └─ ScoreController.java
│       │
│       └─ resources/
│           ├─ welcome.fxml
│           ├─ login.fxml
│           ├─ rules.fxml
│           ├─ quiz.fxml
│           ├─ score.fxml
│           │
│           └─ images/
│               └─ icon.png
## ⚙️ **Installation & Setup**

### **Prerequisites**
- Java JDK (8 or higher)
- JavaFX SDK
- MySQL Server
- IDE (IntelliJ IDEA / Eclipse / NetBeans)

---

## 🗄️ **Database Setup**

1. Open **MySQL Server**
2. Create a new database
```sql
CREATE DATABASE quiz_app;
3.Select the database
USE quiz_app;
4.Create required tables (example)
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(100)
);

CREATE TABLE questions (
    id INT AUTO_INCREMENT PRIMARY KEY,
    question TEXT,
    option_a VARCHAR(255),
    option_b VARCHAR(255),
    option_c VARCHAR(255),
    option_d VARCHAR(255),
    correct_option VARCHAR(5)
);

CREATE TABLE scores (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    score INT,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
5.Update database credentials in DBConnection.java
String url = "jdbc:mysql://localhost:3306/quiz_app";
String user = "root";
String password = "your_password";

---
## ▶️ **Running the Project**
1.Clone the repository:
**`git clone https://github.com/Jannatulmona/project_quiz_game.git`**
2. Open the project in your IDE  
3. Add **mysql-connector-j.jar** to project libraries  
4. Configure JavaFX VM options (replace with your JavaFX path):
```bash
--module-path /path/to/javafx/lib --add-modules javafx.controls,javafx.fxml
5.Run the application using:
Main.java

---
🧩 Architecture (MVC)

Model – Data classes & database logic

View – JavaFX UI (FXML files)

Controller – Application logic & event handling

---

## 👀 **Preview**
### **Welcome Screen**
![welcome Screen]https://github.com/Jannatulmona/project_quiz_game/blob/main/Screenshot%202025-12-06%20180558.png?raw=true
### **Login Screen**
![Login Screen]https://github.com/Jannatulmona/project_quiz_game/blob/f4f6bfc631510facf6f99869c62add88ad998739/Screenshot%202025-12-06%20180640.png

