# Currency Converter — Real-World Failure Simulation 
# Softawre Bug (Option B)

This project is a **web application** that simulates a **software bug/glitch (Option B)** inside a simple currency conversion tool. It is built using **plain HTML, CSS, and JavaScript**, with no backend required.

---

## Project Overview

The application converts **US Dollars (USD)** to **Euros (EUR)**.

### Features

**Happy Path**
Uses a correct, static conversion rate:
`1 USD = 0.93 EUR`

**Failure Injection**
A toggle in the UI intentionally activates a wrong formula:
`1 USD = 1.25 EUR`

**Error Handling**
When the bug is injected, the app:

* Displays a **crash/anomaly banner**
* Prints a **structured JSON error log** to:

  * The browser console
  * A visible log panel on the page

---

## 🚀 How to Run the Application

This is a **client-side** app. No server is required.

1. Save the HTML file as `index.html`.
2. Double-click the file to open it in any modern browser (**Chrome, Firefox, Edge**, etc.).

---

## 🐞 How to Trigger the Failure

1. Open Developer Tools → **Console** (F12 or Ctrl+Shift+J / Cmd+Option+J).
2. Enter an amount (e.g., `100.00`) into the input field.
3. Check **“⚠️ Inject Software Bug (Wrong Formula)”**.
4. Click **“Convert to EUR”**.

### Expected Behavior When Bug Is Active

* The result box shows an **incorrect** conversion (e.g., `125.00`).
* A banner appears saying **“🚨 Calculation Anomaly Detected”**.
* The **Show Logs** button becomes enabled. Clicking it reveals the structured error log.

---

## Failure Type & Logging

This project uses **Option B — Software Bug / Glitch Simulation**.
The injected bug is a **hardcoded incorrect constant (`1.25`)** replacing the correct conversion rate (`0.93`).

Each time the failure occurs, a **structured log** is produced with the required fields:

* timestamp
* function
* input
* result
* expected
* delta
* errorCode

### Example Log (Input: 100.00 USD)

```json
{
  "timestamp": "2025-11-19T12:45:00.000Z",
  "function": "convertUSDtoEUR",
  "input": 100.00,
  "result": 125.00,
  "expected": 93.00,
  "delta": 32.00,
  "errorCode": "BUG_WRONG_FORMULA"
}
```

This fully satisfies the **Option B** structure and requirements.

Authors:
nna0921 
basim-12
---
