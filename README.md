# 🛡️ SQL Injection Vulnerability Scanner (Web-Based)

A web-based SQL injection vulnerability scanner designed for ethical security testing. This tool allows users to input a target URL and test parameters, and then sends a series of predefined SQL payloads to detect potential injection vulnerabilities.

## 🌐 Live Web Interface

This scanner uses a clean HTML, CSS, and JavaScript interface to help security researchers and developers identify potential weak points in web forms or APIs.

---

## 📸 Features

- 🖥️ **Web UI**: Intuitive user interface with tabbed views
- 🎯 **Targeted Scanning**: Input specific URLs and parameters to test
- 💥 **Predefined Test Payloads**: Includes basic, advanced, and time-based SQLi test cases
- 📊 **Result Analysis**: Displays response analysis for each test
- ⚠️ **Warning Highlights**: Flags potentially vulnerable responses
- 🧠 **Recommendations**: Provides security suggestions when vulnerabilities are detected

---
sql-injection-scanner/
│
├── index.html # The main HTML UI file (contains all logic)
└── README.md # Project documentation

---

## 🚀 How to Use

1. Open `index.html` in a browser (Chrome, Firefox, etc.)
2. Enter:
   - **Target URL** (must accept `POST` requests)
   - **Parameter to test** (e.g., `username`, `email`)
3. Select a test case or manually input your own
4. Click **Start Scan**
5. View scan results below, including:
   - Payload used
   - Vulnerability status
   - Recommendation for mitigation

> ⚠️ This scanner sends test payloads using `POST` requests with `FormData`.

---

## 🧪 Sample Payloads Used

- `' OR '1'='1' --`
- `" OR 1=1 --`
- `admin'--`
- `1' ORDER BY 1--`
- `1' AND 1=CONVERT(int,(SELECT table_name FROM information_schema.tables))--`
- `1'; WAITFOR DELAY '0:0:5'--`

---

## 🛡️ Ethical Disclaimer

This tool is intended **for educational purposes and authorized testing only**.  
**Do not use it on systems you do not own or have explicit permission to test.** Unauthorized use may violate laws and terms of service.

---

## 🧰 Requirements

- A modern web browser
- Target URL must accept `POST` requests with form data

---

## 📦 Deployment (Optional)

You can host this on a local or remote server:

```bash
python -m http.server

## 📁 Project Structure
Then visit: http://localhost:8000/index.html

📚 References
OWASP - SQL Injection

PayloadAllTheThings - SQLi

🙋‍♂️ Author
Sourav 
jhin47wick47@gmail.com

📝 License
This project is licensed under the MIT License – see the LICENSE file for details.


---

Let me know if you’d like to separate the HTML, CSS, and JS into different files, or if you want a Python/Flask backend to go with it.
