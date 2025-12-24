# FastAPI-Project
# Patient Management System API

A lightweight RESTful API built with **FastAPI** to manage patient records. This application handles data persistence using a local JSON file and features automatic calculation of BMI (Body Mass Index) and health verdicts based on patient data.

## Features

- **CRUD Operations:** Create, Read, Update, and Delete patient records.
- **Automatic Calculations:** automatically computes `bmi` and a health `verdict` (Underweight, Normal, Obese) whenever a patient is created or updated.
- **Sorting:** Sort patients by height, weight, or BMI in ascending or descending order.
- **Validation:** Robust data validation using Pydantic models (e.g., age limits, positive height/weight).
- **Persistence:** Data is saved locally in `patients.json`.

## Prerequisites

* Python 3.7+
* pip (Python Package Manager)

## Installation

1.  **Clone the repository** (or save the code file):
    ```bash
    git clone <repository-url>
    cd <project-folder>
    ```

2.  **Install dependencies:**
    You will need `fastapi` and `uvicorn` (for the server).
    ```bash
    pip install fastapi uvicorn
    ```

3.  **Initialize Data File:**
    Before running the app for the first time, create an empty JSON file named `patients.json` in the same directory, containing an empty object:
    ```json
    {}
    ```

## Usage

### 1. Run the Server
Assuming your python file is named `main.py`:

```bash
uvicorn main:app --reload
