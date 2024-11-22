# PRODIGY_-CS_01
def caesar_cipher(text,shift,mode):
    result=""
    for char in text:
        if char.isalpha():
            if mode=='encrypt':
                result+= chr((ord(char)+shift-65)%26+65)
            elif mode=='decrypt':
                result+= chr((ord(char)-shift-65)%26+65)
        else:
            result+= char
    return result
message = input("Enter your Message:")
shift= int(input("Enter shift value:"))
mode=input("Enter mode (encrypt/decrypt) :")
result=caesar_cipher(message,shift,mode)
print(f"The{mode}ed Message is:{result}")
