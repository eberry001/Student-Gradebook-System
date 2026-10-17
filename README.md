# Student Grade Book System

[![Python](https://img.shields.io/badge/Python-3.12.13-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![pandas](https://img.shields.io/badge/pandas-Data_Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)

**Author:** Eberechi Bessie Donalds

---

## Executive Summary

The **Student Grade Book System** (also referred to as the **AltSchool Gradebook System**) is a Python application developed in a Jupyter Notebook environment for managing student academic records. The project implements in-memory database storage using Python lists and dictionaries, coupled with `pandas` for structured tabular presentation.

The system handles core record management through a terminal-driven menu interface, automating test score averaging and letter grade determinations based on established academic grading thresholds.

### Key Features

- **Automated Grade Calculation**: Evaluates average scores across two test assessments (`Test 1` and `Test 2`) and assigns grades according to the following scale:
  - **A**: Score $\ge$ 70
  - **B**: Score $\ge$ 60 and < 70
  - **C**: Score $\ge$ 50 and < 60
  - **D**: Score $\ge$ 40 and < 50
  - **F**: Score < 40
- **Student Record Management (CRUD)**:
  - **Add Student**: Prompts for student name and scores (0–100) for Test 1 and Test 2, auto-computes the average and grade, assigns an incremental ID, and stores the record.
  - **View All Students**: Formats and displays records in a clean tabular view using a `pandas.DataFrame` (`to_string(index=False)`).
  - **Update Student Information**: Locates records by student ID and enables updating the student's Name, Test 1 score, or Test 2 score, with automatic re-calculation of the average score and letter grade.
  - **Delete Student**: Searches and removes a student entry from the database using their unique ID.
- **Interactive Menu Loop**: A continuous console loop (`while True`) providing numerical selection (options 1 to 5) with input validation.
- **Preloaded Sample Data**: Contains 5 pre-configured student records with initialized IDs (1 through 5) and sets the subsequent ID tracker to 6.

---

## Repository Structure

```text
.
├── gradebook-eberechibessiedonalds-ipynb (1).ipynb  # Primary Jupyter notebook containing the application logic
└── README.md                                       # Project documentation
```

---

## Tech Stack

- **Programming Language:** Python 3.12.13
- **Libraries & Frameworks:**
  - `pandas` (for tabular DataFrame representation and display)
- **Environment & Tools:**
  - Jupyter Notebook / IPython Kernel (`python3`)
  - Kaggle Notebook Environment

---

## How to Reproduce

### 1. Prerequisites

Ensure you have Python 3 installed (developed with Python `3.12.13`). You will also need `pandas` and a Jupyter Notebook runner installed in your Python environment.

Install the required dependency:

```bash
pip install pandas notebook
```

### 2. Launching the Notebook

1. Open a terminal in the project directory:
   ```bash
   cd "c:\Users\Eberechi B. Donalds\Documents\DATA SCIENCE PROJECTS\Gradebook"
   ```
2. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `gradebook-eberechibessiedonalds-ipynb (1).ipynb` in the Jupyter interface.

### 3. Execution Order

Run the notebook cells sequentially from top to bottom:

1. **Step 1 — Storage Setup:** Imports `pandas` and initializes storage variables (`students = []`, `next_id = 1`).
2. **Step 2 — Grade Calculator:** Defines the `calculate_grade(average)` function.
3. **Step 3 — Add Student Function:** Defines `add_student()` to prompt for user input and append records.
4. **Step 4 — View Students Function:** Defines `view_students()` to render records as a `pandas.DataFrame`.
5. **Step 5 — Update Student Function:** Defines `update_student()` for editing existing records by ID.
6. **Step 6 — Delete Student Function:** Defines `delete_student()` to remove records by ID.
7. **Step 7 — Menu System & Sample Data:** Loads the 5 default student records and starts the interactive loop:
   ```text
   ++++++++++++++++++++++++++++++++++++++++
   STUDENT GRADE BOOK SYSTEM
   ========================================
   1. Add Student
   2. View All Students
   3. Update Student Information
   4. Delete Student From List
   5. Exit
   ========================================
   ```
8. Select an option from `1` to `5` in the input prompt to interact with the grade book. Select option `5` to exit the loop.

---

## Author Info

- **Author:** Eberechi Bessie Donalds
- **Project:** Student Grade Book System (AltSchool Gradebook System)
