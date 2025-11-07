# Word Counter WebApp

## Overview

**Word Counter WebApp** is a simple and interactive Flask-based web application that enables users to upload `.txt` files and receive a word count of the uploaded document instantly. It’s designed for educational purposes, demonstrating file upload handling, Flask session management, and basic rendering logic.

---

## Features

- **File Upload:** Securely upload `.txt` files for word counting.
- **Word Counting:** Automatically counts words in the uploaded file and displays the result.
- **User Feedback:** Error notifications (flash messages) for invalid uploads.
- **Simple Interface:** Clean, minimal HTML interface for ease of use.

---

## Architecture

### `app.py`
- Flask application setup and route definitions.
- Handles GET (page render) and POST (file upload and processing) requests at `'/'`.
- Manages session, file validation, and word counting logic.
- Displays flash messages for errors or results.

### `templates/index.html`
- HTML form for file upload.
- Displays results and error/success messages.
- Dynamically shows word count or upload feedback.

---

## Getting Started

### Prerequisites

- **Python 3.7+**
- **Flask** (Install with `pip install flask`)
- **A modern web browser**

### Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/kavyashri-as/word_counter_webappForked.git
    cd word_counter_webappForked
    ```

2. **Install dependencies:**
    ```sh
    pip install flask
    ```

3. **Run the application:**
    ```sh
    python app.py
    ```
    The app will start on `localhost:5000` by default.

4. **Open in browser:**
    Navigate to `http://127.0.0.1:5000/` in your web browser.

---

## Exercise: Identifying & Fixing Vulnerabilities

> **Note:** The provided code intentionally introduces security vulnerabilities for educational exercises.  
> You are encouraged to identify and remediate these vulnerabilities.

### Vulnerabilities Introduced

1. **Hardcoded Secret Key:** Sensitive configuration should never be hardcoded in production.
2. **Reflective Cross-Site Scripting (XSS):** User input directly rendered in output.
3. **Command Injection:** Unsanitized user input passed to system commands.
4. **Insecure Deserialization:** `eval` used on untrusted data.

### Challenge Steps

1. **Branch Creation:**  
   Create a branch called `XSS-and-command-injection-fix`.

2. **Code Replacement:**  
   Replace all code in `app.py` with the [provided vulnerable code](#).

3. **Pull Request:**  
   Raise a pull request from your new branch to `main`, describing your fixes for these vulnerabilities.

---

## Contributing

Contributions and fixes are welcome!  
*Please ensure your pull requests address code correctness, security, and maintainability.*

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Acknowledgements

- Inspired by learning activities on web application security using Flask.
- Thanks to all contributors and reviewers.

---

## Contact

For queries or suggestions, please open an issue in this repository.
