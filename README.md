

Caesar Cipher Implementation:

This is a Python implementation of the Caesar Cipher, a simple encryption technique, created as part of my learning journey with Prodigy Infotech.

Project Description:

The Caesar Cipher shifts letters in a text by a fixed number, creating a simple encryption mechanism. This project allows users to:

Encrypt and decrypt messages using a shift value of their choice.

Works with both uppercase and lowercase letters.

Non-alphabetical characters, like spaces or punctuation, remain unchanged.


Features:

Encrypt and decrypt text using a Caesar Cipher.

Handles both uppercase and lowercase letters.

Preserves non-alphabetical characters (spaces, punctuation).


How to Use:

1. Clone the repository:

git clone https://github.com/MUHSINA2006/PRODIGY_-CS_01.git


2. Open the Python script:

caesar_cipher.py


3. Run the script and follow the prompts to:

Input a message.

Enter a shift value (number).

Choose whether to encrypt or decrypt the message.




Code:

Here is the Python code for the Caesar Cipher:

def caesar_cipher(text, shift, mode):
    result = ""
    for char in text:
        if char.isalpha():
            if mode == 'encrypt':
                result += chr((ord(char) + shift - 65) % 26 + 65)
            elif mode == 'decrypt':
                result += chr((ord(char) - shift - 65) % 26 + 65)
        else:
            result += char
    return result

# Example usage
message = input("Enter your Message: ")
shift = int(input("Enter shift value: "))
mode = input("Enter mode (encrypt/decrypt): ")

result = caesar_cipher(message, shift, mode)
print(f"The {mode}ed Message is: {result}")

Example

Input:

Enter your Message: Hello, World!
Enter shift value: 3
Enter mode (encrypt/decrypt): encrypt

Output:

The encrypted Message is: Khoor, Zruog!

Technologies Used

Python for implementation.


Learnings

Basic encryption and decryption methods.

Handling strings and character manipulation in Python.

Introduction to cryptography concepts.


Contributions

Feel free to fork this project, make improvements, or provide feedback!