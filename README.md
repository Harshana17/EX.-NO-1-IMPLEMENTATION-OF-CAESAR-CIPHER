# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
def caesar_encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            shift_base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
            result += char 
    return result
def caesar_decrypt(cipher, shift):
    return caesar_encrypt(cipher, -shift)  
plaintext = "Hello World!"
shift = 3
encrypted = caesar_encrypt(plaintext, shift)
decrypted = caesar_decrypt(encrypted, shift)
print("Plaintext :", plaintext)
print("Encrypted :", encrypted)
print("Decrypted :", decrypted)
```

## OUTPUT:

<img width="1161" height="314" alt="image" src="https://github.com/user-attachments/assets/2b5e07e5-2fcd-450c-ba85-49a040b274d8" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
