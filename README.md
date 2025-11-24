🔐 Caesar Cipher Encryption & Decryption Tool

This project provides a simple yet reliable implementation of the Caesar Cipher, one of the oldest classical encryption algorithms.
Users can easily encrypt and decrypt text by choosing a custom shift value.

📌 Features
✔ Encrypt Messages

Shift each alphabetic character by a user-defined number.

✔ Decrypt Messages

Reverse the shift to recover the original message.

✔ Input Validation

Ensures safe and error-free input handling for shift values.

✔ Case-Sensitive Support

Uppercase and lowercase letters are processed correctly

Non-alphabetic characters remain unchanged

📂 Project Structure
Caesar-Cipher/
│
├── caesar_cipher.py     # Main Python program
└── README.md            # Documentation

🛠 How the Caesar Cipher Works

The algorithm shifts each letter by a fixed amount within the alphabet.

Example:

Plain Text : HELLO
Shift      : 3
Encrypted  : KHOOR


Decryption simply applies the negative shift.

▶️ Usage
Run the Program
python caesar_cipher.py

Menu Options
1 → Encrypt a message
2 → Decrypt a message
3 → Exit

💻 Code Snippet (Core Logic)
def caesar_shift(char, shift):
    if not char.isalpha():
        return char
    shift %= 26
    base = 65 if char.isupper() else 97
    return chr((ord(char) - base + shift) % 26 + base)


def encrypt(text, shift):
    return "".join(caesar_shift(c, shift) for c in text)


def decrypt(text, shift):
    return encrypt(text, -shift)

📘 Example Program Output
=== Caesar Cipher Tool ===
1. Encrypt a message
2. Decrypt a message
3. Exit

Enter your choice: 1
Enter your message: hello world
Enter shift value: 5

Encrypted Message: mjqqt btwqi

🏆 Author

C Asmitha 
This project was created as part of academic and training tasks focusing on cryptography basics.

📄 License

This project is free to use for learning and educational purposes.
