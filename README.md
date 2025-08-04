# 🧠 CS101 – Unit 3 - Advanced Programming Concepts Overview

This unit dives deeper into Python programming with a focus on file input/output and GUI development using Tkinter. 
You'll explore real-world applications and enhance your coding fluency through hands-on labs and demos.
---
### ✅ What to Complete
- 1 Python Labs
    * [ ] Lab05: File I/O Basics:
        ##### 📌 Lab 5 ModulesInPython Instructions: [Lab 5: GUI Modules](Lab_05/GUI_README.md)
- Using Tkinter GUI Lab
+ Practice Exercises/Examples from tKinterGUI_Examples_Demos
  ---
### 📂 Where to Submit
- Python Labs & Homework → Submit .py files via GitHub Classroom
- GUI screenshots (if required) → Upload to Canvas with your .py file
---
# Important Note about Usage of Tkinter Module in CodeSpaces/GitHub

   ## 🐍 Tkinter GUI Projects – Coding in GitHub, Running in the Browser

Welcome to your Tkinter GUI lab!  
In this assignment, you'll write Python code using **Tkinter**, Python’s built-in library for creating graphical user interfaces (GUIs).

---

## 💻 Coding in GitHub Codespaces

You’ll use **GitHub Codespaces** to:
- ✅ Write and edit your Python code
- ✅ Save and commit your work to GitHub
- ✅ Use version control and submit your project

> ⚠️ **Important:** Tkinter GUI windows cannot be displayed in Codespaces because it runs in a cloud container without a graphical interface.

---

## 🌐 Running Your Tkinter Code in the Browser

To run and test your GUI, we’ll use a free browser-based IDE called **Trinket**.

### ✅ Why Trinket?

- No installation required
- Runs in any browser
- Supports Python and Tkinter
- Perfect for final projects and GUI demos

---

## 🚀 Steps to Run Your Tkinter Code in Trinket

### 1. Go to [https://trinket.io](https://trinket.io)

- Click **“Sign Up”** (or **“Log In”** if you already have an account)
- Choose **“Python 3”** as your language

### 2. Create a New Trinket

- Click **“New Trinket” → “Python”**
- Delete the starter code and paste your Tkinter script

### 3. Run Your Code

- Click the **“Run”** button
- Your GUI window will appear inside the browser!

### 4. Save and Share (Optional)

- Click **“Share”** to copy a link to your project
- You can include this link in your final submission or project README

---

## 🧪 Example Tkinter Code to Try

```python
from tkinter import *

root = Tk()
root.title("My First GUI")
root.geometry("300x150")

label = Label(root, text="Hello, Tkinter!")
label.pack(pady=20)

root.mainloop()
