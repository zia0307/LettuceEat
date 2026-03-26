# LettuceEat

LettuceEat is a diet planner app designed to provide personalised meal recommendations based on user health data, dietary preferences, and calorie requirements. It helps users make informed food choices by suggesting suitable recipes while considering ingredients, allergies, and dietary restrictions.

## Overview

The application follows a hybrid architecture:

* Core logic is implemented in C for performance and efficiency
* Compiled into a shared library (dietplanner.dll)
* A Python-based GUI is built using Tkinter
* Python interacts with the C backend using ctypes

## Key Features

* Calorie calculation based on user inputs (age, weight, height, goal)
* Recipe suggestions based on available ingredients
* Filtering based on dietary restrictions (Vegetarian, Vegan, Jain, Halal)
* Allergy-aware recommendations
* Graph-based recipe connections for smarter suggestions

## Tech Stack

* C (core logic and algorithms)
* Python (Tkinter GUI)
* ctypes (C-Python integration)

## Architecture

```
User Input (GUI - Tkinter)
        ↓
Python Layer (ctypes interface)
        ↓
C Backend (dietplanner.dll)
        ↓
Processing (calorie + graph traversal)
        ↓
Results returned to the GUI
```

## Notes

* All computation and filtering logic resides in the C backend
* Python is used only for user interaction and display
* Ensure the DLL is correctly linked before running the application
