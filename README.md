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
Database Setup:

CREATE DATABASE quiz_app;
USE quiz_app;

Users Table:
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100) UNIQUE
);

Scores Table:
CREATE TABLE scores (
  id INT AUTO_INCREMENT PRIMARY KEY,
  user_id VARCHAR(100),
  user_email VARCHAR(100),
  correct_score INT,
  wrong_score INT
);

