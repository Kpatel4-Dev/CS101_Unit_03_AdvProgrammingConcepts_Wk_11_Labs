# 🐍 Tkinter GUI Projects – Coding in GitHub, Running in the Browser

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
