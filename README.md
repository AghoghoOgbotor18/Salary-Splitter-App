# 💰 Salary Splitter

A simple salary budgeting web app that helps users split their salary into main expenses, savings, emergency funds, and miscellaneous allocations.

This project allows users to:

- Input their salary.  
- Add main recurring expenses with duration in months.  
- Add miscellaneous expenses (like entertainment, gifts, etc.).  
- Automatically calculate how much can go into savings and emergency funds (based on user-defined percentages).  
- Get a budget breakdown showing whether their expenses fit into their salary.  

---

## 🚀 Live Demo  
Check out the project here: [Smart Budget Planner](https://aghoghoogbotor18.github.io/Salary-Splitter-App/)

---

## 🚀 Features

### Dynamic Input Fields
- Add multiple main expenses with custom names, amounts, and durations.  
- Add miscellaneous expenses dynamically.  

### Number Formatting
- Automatically formats numbers with commas as you type (e.g., `10000 → 10,000`).  

### Smart Budget Allocation
- Calculates monthly share of each main expense.  
- Splits remaining balance into savings, emergency funds, and miscellaneous allocations.  
- If main expenses exceed salary, warns the user.  
- If total expenses exceed salary, suggests cutting down.  

### Interactive Workflow
- Uses prompts to collect savings/emergency fund percentages.  
- Provides feedback and tips if the budget isn’t feasible.  

### Reset Functionality
- Resets the form when user clicks OK after viewing results.  
- Removes dynamically added inputs and restores the default state.  

---

## 🛠️ How It Works

1. Enter your salary.  
2. Add one or more main expenses with name, amount, and duration.  

   Example:  
   `Rent = ₦120,000 over 12 months → ₦10,000/month`.  

3. Add miscellaneous expenses (like “Transport”, “Entertainment”).  
4. Enter savings % and emergency fund % when prompted.  
5. The system splits your salary and shows:  
   - Main expenses  
   - Savings allocation  
   - Emergency fund allocation  
   - Miscellaneous breakdown  

---

## 📂 File Structure
/salary-splitter
│── index.html # Main page
│── style.css # Styling
│── script.js # JavaScript logic (salary splitting + form handling)
│── README.md # Documentation

---

## 🧑‍💻 Challenges Faced

### Handling Dynamic Inputs
- Adding/removing multiple expenses dynamically required careful event handling.  
- Fixed by appending new input fields programmatically with `document.createElement()`.  

### Number Formatting Issues
- Initially, parsing numbers failed because commas weren’t removed.  
- Solved by stripping commas using `.replace(/,/g, "")` before calculations.  

### Main Expenses Exceeding Salary
- Challenge: How to gracefully handle when fixed expenses alone are greater than the salary.  
- Fixed by alerting the user and showing only the fixed expense breakdown without savings/emergency/misc.  

### User Experience & Resetting Form
- Resetting the form wasn’t removing dynamically added inputs.  
- Solved by restoring the container’s HTML back to its default structure on reset.  

### Balancing Remaining Salary
- Splitting between savings, emergency funds, and miscellaneous fairly was tricky.  
- Used percentage-based prompts + equal distribution for miscellaneous items.  

---

## 🔮 Future Improvements

- Add local storage so users don’t lose their data on refresh.  
- Use sliders instead of prompts for entering percentages.  
- Add visual charts/graphs (pie chart for expenses).  
- Allow users to prioritize miscellaneous items (some may get more allocation than others).  
- Support currency selection beyond Naira.  

---

## ✅ Tech Stack

- **HTML5** – Structure  
- **CSS3** – Styling  
- **Vanilla JavaScript (ES6+)** – Core logic 
