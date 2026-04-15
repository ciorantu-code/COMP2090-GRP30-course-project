# 🎓 Student Lifeline (2090 Version)

**Hong Kong Metropolitan University (HKMU) - COMP2090SEF Course Project** *Data Structures, Algorithms and Problem Solving*

Student Lifeline is a unified, centralized desktop application designed to help university students manage their academic lives. By consolidating academic deadlines, grade monitoring, campus lost-and-found, and course peer-reviews into a single interface, this application minimizes "cognitive load" and helps students stay organized.

---
## 🚀 Installation & Usage

Follow these steps to set up and run the application on your local machine.

### 📋 Prerequisites

Ensure your system meets the following requirements before proceeding:

* **Python 3.10 or higher:** Required to support the advanced type-hinting used in this project. You can download the latest version from [python.org](https://www.python.org/downloads/).
* **Standard Python Libraries:** `os`, `datetime`, `abc`, and `tkinter`. 
  *(Note: These are built into standard Python installations, but Linux users may need to explicitly install the `python3-tk` package depending on their distribution).*

### 📦 Dependencies

The application's modern graphical user interface is built using **CustomTkinter**. You must install this external dependency before running the application.

Install it via pip by running the following command in your terminal or command prompt:

```bash
pip install customtkinter


## ✨ Features

The application acts as a central "command center" with six core modules:

* **🏠 Dashboard:** A high-level overview featuring statistical cards and a dynamic countdown of the nearest upcoming events.
* **📅 Important Dates:** An intelligent calendar system that tracks user-created deadlines and automatically generated recurring academic events.
* **📊 Grade Monitor:** A CGPA tracker that provides instant status evaluations and motivational feedback.
* **🔍 Lost & Found:** A campus registry for reporting and searching lost or found items using a case-insensitive search algorithm.
* **⭐ Course Ratings:** A peer-review system allowing students to rate (1-5 stars) and review university courses.
* **🕐 Office Hours:** An instructor availability tracker that automatically sorts schedules chronologically by the day of the week.

---

## 🛠️ Technical Architecture

This project was evolved from a legacy procedural script into a highly modular, **Model-View-Controller (MVC)**-inspired architecture using strictly Object-Oriented Programming (OOP) principles. 

### Core OOP Concepts Demonstrated:
* **Abstraction:** Utilizes an `AppRecord` Abstract Base Class (ABC) to enforce a strict contract (`serialize`, `deserialize`) for all data types.
* **Encapsulation:** Protects data integrity using private variables and `@property` setters (e.g., preventing invalid CGPA entries directly within the model).
* **Inheritance:** Employs hierarchical class structures to maximize code reuse (e.g., `RecurringDate` inheriting temporal calculation logic from `ImportantDate`).
* **Polymorphism:** Allows the main controller to dynamically switch between different GUI views and seamlessly serialize different object types through shared interfaces.

---

## 📂 Project Structure

```text
student-lifeline-2090/
│
├── main_studentlifeline_2090ver.py   # Entry point & Application Controller
├── gui_views.py                      # UI Layer (Polymorphic view classes)
├── models.py                         # Data Layer (ABCs and Data definitions)
├── data_manager.py                   # Persistence Layer (File I/O operations)
└── README.md                         # Project documentation
