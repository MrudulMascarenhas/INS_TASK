# INS_TASK
## Hybrid Cipher Encryption-Decryption

This repository contains implementations of a hybrid encryption-decryption algorithm combining the Hill Cipher and Columnar Transposition Cipher to enhance security. The programs demonstrate encryption, decryption, and secure text transformation methods.

---


### 1. Cryptographic Techniques  

#### Hill Cipher:  
- Encrypts plaintext using a matrix-based key.  
- Decrypts ciphertext using the modular inverse of the key matrix.  

#### Columnar Transposition Cipher:  
- Rearranges text in a grid based on a given key.  
- Reads columns in a defined order to produce encrypted text.  

### 2. Hybrid Encryption-Decryption  
- Combines Hill Cipher and Columnar Transposition for enhanced security.  
- Encrypts plaintext using Hill Cipher first and then applies Columnar Transposition Cipher.  
- Decrypts by reversing the order.

---

## Getting Started  

### Prerequisites  
Ensure you have Python 3.x installed along with NumPy:
```sh
pip install numpy
```

### Clone the Repository  
```sh
git clone https://github.com/MrudulMascarenhas/INS_TASK.git
```

---

## Usage  

### Encryption  
```python
plaintext = "HELLO WORLD"
hill_key = np.array([[3, 3],
                     [2, 5]])
transposition_key = "3142"

encrypted_text = hybrid_encrypt(plaintext, hill_key, transposition_key)
print("Encrypted:", encrypted_text)
```

### Decryption  
```python
decrypted_text = hybrid_decrypt(encrypted_text, hill_key, transposition_key)
print("Decrypted:", decrypted_text)
```

---

## Example Output  
```
Encrypted: XYZABC...
Decrypted: HELLOWORLD
```

---

## Notes  
- The Hill Cipher key must be a square matrix with an invertible determinant mod 26.  
- The transposition key must be a permutation of numbers representing column order.  


