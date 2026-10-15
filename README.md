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
    git clone https://github.com/Ashin-06/secure-password-manager.git
    cd secure-password-manager
    ```

2.  **Install Dependencies:**
    This project requires the `bcrypt` and `cryptography` libraries.
    ```bash
    pip install bcrypt cryptography
    ```

3.  **Run the Code:**
    Install Jupyter Notebook and open the notebook included in this repository:
    ```bash
    pip install notebook
    jupyter notebook secpassmanager.ipynb
    ```
    Run the cells from top to bottom in one kernel session. No standalone Python script is included.

## ⚠️ Security Warning

This is an educational project and should **NOT** be used to store real, sensitive passwords. The encryption key is generated in memory and is not saved. Restarting the kernel or rerunning the key-generation cell loses access to passwords encrypted with the previous key. The CSV contains encrypted password values, but service names, usernames, and password hashes remain visible. It is not a persistent password vault.

**DO NOT** commit the `passwords.csv` file to GitHub. The provided `.gitignore` file is configured to prevent this.
