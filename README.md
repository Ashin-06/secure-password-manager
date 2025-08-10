# Secure Password Manager

This is a simple, educational command-line password manager created in Python. The tool uses the `bcrypt` library for robust password hashing and the `cryptography` (Fernet) library for symmetric encryption to securely store credentials.

## Features

* **Strong Hashing:** Uses `bcrypt` to generate a unique salt for each password before hashing.
* **Symmetric Encryption:** Employs `Fernet` to encrypt and decrypt passwords for storage.
* **Local Storage:** Saves credentials, including the service name, username, hashed password, and encrypted password, into a local `passwords.csv` file.
* **Credential Retrieval:** Includes a function to read from the CSV file and decrypt the passwords for display.

## Technologies Used

* Python
* `bcrypt`
* `cryptography`

## Setup and Usage

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/secure-password-manager.git](https://github.com/your-username/secure-password-manager.git)
    cd secure-password-manager
    ```

2.  **Install Dependencies:**
    This project requires the `bcrypt` and `cryptography` libraries.
    ```bash
    pip install bcrypt cryptography
    ```

3.  **Run the Code:**
    Open the `Day1.ipynb` notebook in a Jupyter environment or run the equivalent Python script to save and retrieve passwords.

## ⚠️ Security Warning

This is an educational project and should **NOT** be used to store real, sensitive passwords. The encryption key is generated and used within the same session, and the `passwords.csv` file is stored unencrypted on your disk.

**DO NOT** commit the `passwords.csv` file to GitHub. The provided `.gitignore` file is configured to prevent this.