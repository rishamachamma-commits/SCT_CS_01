# 📝 Task 01 — Caesar Cipher Program

## 📌 Overview

This project implements a **Caesar Cipher**, one of the simplest and most widely known encryption techniques.
The program allows users to:

* ✔️ Enter a message
* ✔️ Enter a shift value
* ✔️ Encrypt the message
* ✔️ Decrypt the message

The goal is to help users understand the basics of classical cryptography.

---

## 🔐 What is the Caesar Cipher?

The **Caesar Cipher** is a substitution cipher where each letter in the plaintext is shifted by a fixed number of positions down or up the alphabet.

Example (Shift = 3):

* **Plaintext:** HELLO
* **Ciphertext:** KHOOR

Formula:

```
Encrypted Letter = (Original Letter + Shift) mod 26
Decrypted Letter = (Encrypted Letter - Shift) mod 26
```

---

## 🧠 Features

* 🔤 Handles **both uppercase and lowercase** letters
* 🧩 Ignores numbers, spaces, and symbols (keeps them unchanged)
* ⬅️➡️ Supports **both encryption and decryption**
* 🔁 Works with any positive or negative shift value
* 🖥️ Simple and user-friendly CLI interface

---

## 📂 Project Structure

```
Caesar-Cipher/
│── README.md
│── caesar_cipher.py
└── examples/
      └── sample_output.txt
```

---

## 🧪 Example Usage

### **Input:**

```
Enter your message: SkillCraft
Enter shift value: 4
Choose an option:
1. Encrypt
2. Decrypt
Your choice: 1
```

### **Output:**

```
Encrypted message: WmoilGvepx
```

---

## 🧩 Sample Python Code

```python
def encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            base = 65 if char.isupper() else 97
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char
    return result

def decrypt(text, shift):
    return encrypt(text, -shift)

message = input("Enter a message: ")
shift = int(input("Enter shift value: "))

print("1. Encrypt")
print("2. Decrypt")
choice = input("Choose an option: ")

if choice == "1":
    print("Encrypted message:", encrypt(message, shift))
elif choice == "2":
    print("Decrypted message:", decrypt(message, shift))
else:
    print("Invalid choice")
```

---

## 🧾 Learning Outcomes

By completing this task, you will:

* Understand how classical ciphers work
* Learn modular arithmetic usage
* Improve string manipulation and conditional logic skills
* Build a functional Python cryptography tool

---

## 🏷️ Author

SkillCraft Technology — Internship Task 01

---


