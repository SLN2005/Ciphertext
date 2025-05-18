

📜 Custom Transposition Cipher with Hash-based Integrity Check
This project implements a Transposition Cipher for encryption and decryption of alphabetic plaintext using a custom hash-based integrity verification. The hash ensures the correctness of the decrypted text, and a brute-force attack is supported to demonstrate key discovery via property checking.

🔐 Features
Custom Hash Generator: Generates an 8-character hash using character-wise XOR and left-shifting logic.

Transposition Cipher:

Encryption with columnar transposition.

Decryption using the inverse key.

Integrity Check: Ensures decryption validity using a computed hash check.

Brute-Force Attack: Tries all possible key permutations up to a given length and checks for valid plaintext.

🛠️ Project Structure
custom_hash(plainText, hash_length=8): Generates a fixed-length hash for a plaintext.

Encryptor(plainText, key_vect): Encrypts plaintext using a transposition cipher.

Decryptor(cipherText, key_vect): Decrypts ciphertext using a transposition cipher.

preprocess(string): Filters input to include only lowercase a-z characters.

padding(plainText, key_length, hash_code_length=8): Pads the text so its length + hash is divisible by key length.

propertyCheck(plainText, hash_code_length=8): Checks if the hash is valid for given text.

bruteForce(cipherText, key_set): Attempts all keys and returns the ones passing the hash check.

🧪 Sample Run
🔁 Encryption Flow
Preprocess input: remove non-alphabetic characters.

Pad the text to align with the matrix formed by the key length.

Generate a hash and append it to the padded text.

Encrypt using transposition cipher.

🔓 Decryption + Check
Decrypt using the same key.

Use propertyCheck() to verify integrity via the hash.

💥 Brute Force
Try permutations of keys from length 1 to key_length.

Decrypt each with Decryptor.

Pass each output to propertyCheck.

▶️ Usage
🔧 Requirements
Python 3.x

NumPy

💻 Run the Script
bash
Copy
Edit
python script_name.py
✍️ Example Input
css
Copy
Edit
Enter the plaintext you want to encrypt: Hello World!
🖥️ Example Output
vbnet
Copy
Edit
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

📄 License
This project is open-source and free to use for educational and academic purposes.
