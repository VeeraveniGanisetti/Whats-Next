# What’s Next — Project Plan

## 1. Problem Statement

Students often feel confused while choosing their education and career path because they may not have enough information about available courses, careers, entrance exams, required skills, higher-study options, and job opportunities.

Information is also scattered across different websites and sources, making it difficult for students to understand which path is suitable for them.

**What’s Next** aims to provide students with a clear and structured platform to explore education and career pathways in one place.

---

## 2. Objective

The main objective of **What’s Next** is to help students understand and explore different education and career opportunities through a simple and structured web application.

The application will help students:

* Understand different education pathways.
* Explore courses and streams.
* Explore career options.
* Find relevant entrance and competitive exams.
* Understand required skills.
* Explore higher-study opportunities.
* View step-by-step career roadmaps.
* Compare different education and career options.
* Make informed career decisions based on available information.

---

## 3. Target Users

The application is designed for **students at different stages of education**.

The initial version will focus on students following the **Indian education system**.

The application should be designed in a way that allows support for other countries and education systems to be added in the future without significantly changing the existing architecture.

---

## 4. Proposed Solution

**What’s Next** will be a web-based career guidance application.

Students will be able to create an account, provide their education details, and explore different career-related information.

The application will organize information into structured categories such as:

* Education levels
* Streams
* Courses
* Careers
* Skills
* Entrance exams
* Higher studies
* Job opportunities
* Career roadmaps

The system will initially provide **information-based career exploration**, while advanced AI-based personalized guidance can be added in future versions.

---

# 5. MVP Features

The Minimum Viable Product (MVP) will contain the following features:

### 5.1 Student Registration

Students can create an account using basic details such as:

* Name
* Email
* Password

### 5.2 Student Login

Registered students can securely log in to their accounts.

### 5.3 Student Profile

Students can maintain their basic profile information.

### 5.4 Education Details

Students can enter relevant education information such as:

* Education level
* Stream
* Course
* Other required academic details

### 5.5 Explore Careers

Students can explore different careers and view information such as:

* Career description
* Required education
* Required skills
* Related courses
* Job opportunities
* Higher-study options

### 5.6 Explore Courses

Students can explore courses and understand:

* Course name
* Education level
* Stream
* Course description
* Related careers
* Entrance exams

### 5.7 Explore Entrance Exams

Students can explore relevant entrance and competitive examinations associated with education and career pathways.

### 5.8 Career Roadmaps

Students can view a structured step-by-step roadmap for reaching a particular career.

Example:

**Intermediate → Entrance Exam → Degree → Skills → Internship → Job**

### 5.9 Search

Students can search for:

* Careers
* Courses
* Exams
* Skills
* Other relevant information

### 5.10 Compare Options

Students can compare different courses or career options based on available information.

---

# 6. Technology Stack

| Layer           | Technology            |
| --------------- | --------------------- |
| Frontend        | HTML, CSS, JavaScript |
| Backend         | Python, Django        |
| Database        | SQLite                |
| Version Control | Git                   |
| Repository      | GitHub                |

The application will initially be developed as a web application.

---

# 7. User Flow

The basic user flow will be:

**Home**

↓

**Register / Login**

↓

**Student Profile**

↓

**Education Details**

↓

**Explore**

↓

**Careers / Courses / Entrance Exams**

↓

**Career Roadmap**

↓

**Compare Options**

The navigation should remain simple so that students can easily move between different sections.

---

# 8. Future Enhancements

The following features will **not be included in the initial MVP** but can be added after the basic application is working successfully:

### 8.1 AI Chatbot

An AI-based chatbot can answer students' career-related questions.

### 8.2 RAG-Based Career Guidance

Retrieval-Augmented Generation (RAG) can be used to provide answers based on verified career and education information stored in the system.

### 8.3 Personalized Recommendations

The system can recommend courses and careers based on a student's:

* Education
* Interests
* Skills
* Preferences
* Goals

### 8.4 International Education Systems

Support can be added for education systems of other countries.

The architecture will use country and education-system entities so that international support can be added without redesigning the entire application.

### 8.5 Mobile Application

A mobile application can be developed in the future.

### 8.6 Advanced Analytics

Analytics can be added to understand how students use the platform.

### 8.7 Multilingual Support

Multiple Indian and international languages can be supported in future versions.

---

# 9. System Architecture

The high-level architecture of the application is:

**Student**

↓

**Frontend**

HTML + CSS + JavaScript

↓

**Django Backend**

↓

**SQLite Database**

↓

**Django Backend**

↓

**Frontend**

↓

**Student**

### Architecture Responsibilities

**Frontend**

* Displays the user interface.
* Collects user input.
* Sends requests to the backend.
* Displays responses.

**Django Backend**

* Handles business logic.
* Manages authentication.
* Processes user requests.
* Communicates with the database.
* Provides required information to the frontend.

**SQLite Database**

* Stores user information.
* Stores education data.
* Stores courses, careers, exams, skills, and roadmap information.

---

# 10. Initial Database Entities

The initial database design contains the following entities:

1. **User**
2. **StudentProfile**
3. **Country**
4. **EducationSystem**
5. **EducationLevel**
6. **Stream**
7. **Course**
8. **Career**
9. **Skill**
10. **EntranceExam**
11. **Roadmap**
12. **RoadmapStep**

### Entity Purpose

**User**
Stores authentication-related information.

**StudentProfile**
Stores additional information about a student.

**Country**
Stores countries supported by the application.

**EducationSystem**
Represents the education system of a particular country.

**EducationLevel**
Represents levels such as school, intermediate, undergraduate, postgraduate, etc.

**Stream**
Represents educational streams such as MPC, BiPC, Commerce, Arts, etc.

**Course**
Stores information about educational courses and programs.

**Career**
Stores information about career options.

**Skill**
Stores skills associated with different careers.

**EntranceExam**
Stores information about entrance and competitive examinations.

**Roadmap**
Represents the pathway toward a particular career.

**RoadmapStep**
Stores individual steps within a career roadmap.

---

# 11. Database Relationships

The major relationships between the entities are:

### User ↔ StudentProfile

**One-to-One**

One user has one student profile.

---

### Country → EducationSystem

**One-to-Many**

One country can have multiple education systems.

---

### EducationSystem → EducationLevel

**One-to-Many**

One education system can contain multiple education levels.

---

### EducationLevel → Stream

**One-to-Many**

One education level can contain multiple streams.

---

### Stream → Course

**One-to-Many**

A stream can contain multiple courses.

---

### Course ↔ Career

**Many-to-Many**

A course can lead to multiple careers, and a career can be associated with multiple courses.

---

### Course ↔ EntranceExam

**Many-to-Many**

A course can have multiple relevant entrance exams, and an entrance exam can be relevant to multiple courses.

---

### Career ↔ Skill

**Many-to-Many**

A career can require multiple skills, and the same skill can be useful for multiple careers.

Example:

**Skill: Python**

can be associated with:

* Software Developer
* Data Analyst
* Machine Learning Engineer
* Backend Developer

---

### Career → Roadmap

**One-to-Many**

A career can have one or more roadmaps depending on the pathway.

---

### Roadmap → RoadmapStep

**One-to-Many**

A roadmap contains multiple individual steps.

Example:

**Roadmap: Software Developer**

1. Complete relevant education
2. Learn programming
3. Learn databases
4. Build projects
5. Complete internships
6. Apply for jobs

Keeping roadmap steps as separate records makes them easier to manage, search, reorder, and modify.

---

# 12. MVP Development Scope

The first working version of **What’s Next** will focus only on the core functionality.

### Phase 1 — Foundation

* Project setup
* Django setup
* Database configuration
* Git/GitHub setup

### Phase 2 — Authentication

* Registration
* Login
* Logout
* Student profile

### Phase 3 — Education Data

* Education levels
* Streams
* Courses
* Entrance exams

### Phase 4 — Career Data

* Careers
* Skills
* Career-course relationships
* Career information

### Phase 5 — Guidance

* Career roadmaps
* Roadmap steps
* Search
* Compare options

### Phase 6 — Testing & Integration

* Test all features
* Fix bugs
* Improve UI
* Connect all modules
* Validate the complete user flow

---

# 13. Development Approach

The project will be developed incrementally.

The development process will follow:

**Plan → Build → Test → Fix → Review → Continue**

The application will not attempt to implement all advanced features at once.

The core MVP will be completed first. After the MVP becomes stable, advanced features such as AI chatbot, RAG, personalized recommendations, and international education systems can be considered.

---

# 14. Project Success Criteria

The MVP will be considered successful when a student can:

1. Register an account.
2. Log in.
3. Create/update a profile.
4. Enter education details.
5. Explore courses.
6. Explore careers.
7. Find relevant entrance exams.
8. View career roadmaps.
9. Search for relevant information.
10. Compare available options.

The application should provide this information through a **simple, clear, and easy-to-use interface**.

---

# 15. Project Development Principle

**Build the basic system first. Add intelligence later.**

The project will first establish a reliable foundation for student, education, course, career, exam, skill, and roadmap data.

Once the foundation is stable, AI and advanced guidance features can be integrated without disrupting the core application.
