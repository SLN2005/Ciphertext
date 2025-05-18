

# Custom Transposition Cipher with Hash-based Integrity Check
This project implements a Transposition Cipher for encryption and decryption of alphabetic plaintext using a custom hash-based integrity verification. The hash ensures the correctness of the decrypted text, and a brute-force attack is supported to demonstrate key discovery via property checking.

🔐 Features
Custom Hash Generator: Generates an 8-character hash using character-wise XOR and left-shifting logic.

Transposition Cipher:

Encryption with columnar transposition.

Decryption using the inverse key.

Integrity Check: Ensures decryption validity using a computed hash check.

Brute-Force Attack: Tries all possible key permutations up to a given length and checks for valid plaintext.



🔓 Decryption + Check
Decrypt using the same key.

Use propertyCheck() to verify integrity via the hash.


💥 Brute Force
Try permutations of keys from length 1 to key_length.

Decrypt each with Decryptor.

Pass each output to propertyCheck.




🖥️ Example Output

Using a fixed key length of: 9
Using a randomly generated key for demonstration: [3, 5, 1, 9, 4, 7, 6, 8, 2]

Plaintext: Hello World!
Processed Text (a-z only): helloworld
Padded Text: helloworldxyz
Hash Value: avbsdgye
Hashed Text (padded + hash): helloworldxyzavbsdgye
Ciphertext: ...
Deciphered Text: helloworldxyzavbsdgye
Property Check on Deciphered Text: True

Launching brute force attack on the generated ciphertext...
...
Found potential key(s) of length 9: [[3, 5, 1, 9, 4, 7, 6, 8, 2]]


🧠 Concepts Covered
Transposition cipher logic.

XOR-based hashing.

Matrix manipulation.

Brute-force key search.

Integrity verification through deterministic hashing.


