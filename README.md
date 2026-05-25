# Medical Cost & Loan Data Visualization Dashboard

An interactive, web-based data visualization dashboard built with PHP, 
JavaScript, and Google Charts that allows users to explore and analyze 
two real-world datasets: US Medical Costs and Loan Approval Predictions.

**Course:** CPS 4745 — Data Visualization, Fall 2024
**Team:** Dahana Moz Ruiz & Samantha Gonzalez — Kean University

---

## Features:

### Loan Approval Dataset
- **Grouped Bar Chart** — Visualizes loan approval status by home ownership 
  type (Mortgage, Rent, Own, Other) and credit history length 
  (Short: 0–5 yrs, Medium: 6–15 yrs, Long: 15+ yrs)
- **Scatter Plot** — Plots applicant income vs. loan amount requested, with 
  a real-time income range slider filter
- **Filter by Home Ownership** — Dropdown filter dynamically updates charts 
  via AJAX without page reload
- **Paginated Data Table** — Browse the full dataset 10 records at a time 
  with Next/Back navigation

### Medical Costs Dataset
- **Dynamic Chart Builder** — Select any combination of attributes 
  (Region, Smoker, Age, Sex, Children) and chart type (Bar, Line, Pie) 
  to generate a custom average medical charges visualization
- **Dataset Viewer** — Toggle the full dataset table inline
- **User Manual** — Embedded Google Docs manual accessible within the app

### Authentication
- Session-based login/logout system built with PHP
- Protected dashboard routes — unauthenticated users are redirected to login

---

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript, Google Charts API, jQuery (AJAX)
- **Backend:** PHP (session management, data fetching, routing)
- **Data:** 
  - [Loan Approval Prediction Dataset (Kaggle)](https://www.kaggle.com/)
  - [Medical Cost Personal Dataset (Kaggle)](https://www.kaggle.com/)

---

## Project Structure

| File | Description |
|------|-------------|
| `index.html` | Landing / login page |
| `login.php` | Authentication logic |
| `logout.php` | Session destruction and redirect |
| `dashboard.php` | Main dashboard — charts, filters, data table |
| `fetch_data.php` | AJAX endpoint for loan dataset queries |
| `medcostsdata.php` | AJAX endpoint for medical costs queries |
| `loanstyle.css` | Styles for loan visualization section |
| `medstyle.css` | Styles for medical costs section |

---

## Setup

This project requires a PHP server with MySQL. To run locally:

1. Clone the repository
```bash
git clone https://github.com/dahanam/Medical-Cost-Loan-Data-Visualization-Dashboard.git
```

2. Place the project folder in your local server directory 
   (e.g. `htdocs` for XAMPP)

3. Import the datasets into your MySQL database and update the 
   connection credentials in `fetch_data.php` and `medcostsdata.php`

4. Start your PHP server and navigate to `index.html`

---

## Authors

Dahana Moz Ruiz & Samantha Gonzalez — Kean University, Fall 2024
