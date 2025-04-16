
# 🔐 Flask File Encryptor & Decryptor

This is a simple web application built with Flask that allows users to upload files and either **encrypt** or **decrypt** them using **Fernet symmetric encryption** from the `cryptography` library.

---

## 🚀 Features

- 🔒 Encrypt any file with a newly generated Fernet key.
- 🔓 Decrypt files using the previously generated key or any other encrypted format.
- 📁 Upload files securely via a web interface.
- 📥 Download encrypted/decrypted files.
- 🧠 Flash messages for feedback and alerts.
- 📦 Key management using local `.key` file.

---

## 📂 Project Structure

```
.
├── app.py
├── uploads/
├── Secret.key
├── templates/
│   └── index.html
├── static/ (optional for CSS/JS)
└── README.md
```

---

## 🛠 Requirements

Make sure you have **Python 3.x** installed. Then, install the required packages:

```bash
pip install Flask cryptography

check code for other libraries
```

---

## 🚧 How It Works

1. The user uploads a file via the browser.
2. They choose whether to **Encrypt** or **Decrypt** the file.
3. For encryption:
   - A new key (`Secret.key`) is generated and saved.
   - The file is encrypted using this key.
4. For decryption:
   - The app uses the `Secret.key` file to attempt decryption.
   - If successful, the decrypted file is made available for download.

---

## 🧪 Running the App

```bash
set FLASK_APP=app.py
set FLASK_ENV=development
python -m flask run
```

Then open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## 📌 Important Notes

- Each encryption generates a new `Secret.key`. Previous keys will be **overwritten**, so store old keys securely if needed.
- Decryption will **fail** if the key doesn't match the file's encryption key.
- Encrypted files will have the `.enc` extension.
- The `uploads/` directory is used to store all files temporarily.

---

