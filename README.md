Here’s a well-structured `README.md` content for your GitHub repository where you demonstrate **CSRF** and **Basic SQL Injection** attacks using **OWASP WebGoat**. You can adjust project-specific details as needed:

---

````markdown
# WebGoat Vulnerability Demonstration: CSRF and SQL Injection

This repository documents a security testing project using [OWASP WebGoat](https://owasp.org/www-project-webgoat/) to demonstrate two common web application vulnerabilities:
- Cross-Site Request Forgery (CSRF)
- Basic SQL Injection

The goal is to simulate real-world attacks in a safe, legal environment for educational and testing purposes.

---

## 🧰 Tools & Environment

- **WebGoat Version**: 8.x
- **Testing Tool**: OWASP ZAP / Burp Suite (optional)
- **Platform**: Docker or Java (manual setup)
- **Language**: N/A (WebGoat is a Java web app)
- **Browser**: Chrome / Firefox

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/webgoat-csrf-sql-demo.git
cd webgoat-csrf-sql-demo
````

### 2. Run WebGoat Using Docker (Recommended)

```bash
docker pull webgoat/webgoat
docker run -p 8080:8080 webgoat/webgoat
```

Access WebGoat in your browser:

```
http://localhost:8080/WebGoat
```

---

## 🔐 Vulnerabilities Demonstrated

### 1. Cross-Site Request Forgery (CSRF)

#### 📌 Description:

CSRF is an attack that tricks a user into performing actions on a web application without their consent or knowledge.

#### ✅ Objective:

Simulate a CSRF attack by crafting a malicious request that modifies user data (e.g., changing a password) when the victim is authenticated.

#### 🛠️ Steps:

* Navigate to **General > CSRF** lesson in WebGoat.
* Observe the form being submitted.
* Create a malicious HTML page with an auto-submitting form.
* Host the file and simulate a user clicking the link while logged into WebGoat.
* Observe the state change (e.g., password update).

---

### 2. Basic SQL Injection

#### 📌 Description:

SQL Injection occurs when user input is improperly sanitized, allowing attackers to inject malicious SQL code.

#### ✅ Objective:

Use SQL injection to bypass login or extract data from the database.

#### 🛠️ Steps:

* Navigate to **Injection Flaws > SQL Injection (Basic)** in WebGoat.
* Test inputs like:

  ```sql
  ' OR '1'='1
  ```
* Observe successful authentication or unauthorized data access.

---

## 📸 Screenshots

| Vulnerability | Screenshot                                 |
| ------------- | ------------------------------------------ |
| CSRF Attack   | ![csrf](screenshots/csrf-demo.png)         |
| SQL Injection | ![sql](screenshots/sql-injection-demo.png) |

---

## 📝 Recommendations

### CSRF Mitigation:

* Use CSRF tokens for all state-changing operations.
* Validate `Origin` and `Referer` headers.

### SQL Injection Mitigation:

* Use prepared statements (parameterized queries).
* Input validation and sanitation.
* Use ORM frameworks where applicable.

---

## 📚 References

* [OWASP WebGoat Documentation](https://owasp.org/www-project-webgoat/)
* [OWASP CSRF Guide](https://owasp.org/www-community/attacks/csrf)
* [OWASP SQL Injection](https://owasp.org/www-community/attacks/SQL_Injection)

---

## ⚠️ Disclaimer

> This project is for educational purposes only. Do **NOT** use these techniques on systems you don’t own or have permission to test.

---

## 👨‍💻 Author

* **Jannatul Ferdous Katha**
* GitHub: [@Katha-Sikdar](https://github.com/Katha-Sikdar)
* Email: [ferdouskatha@gmail.com]

```

```
