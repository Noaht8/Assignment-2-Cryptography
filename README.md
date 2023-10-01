# Assignment-2-Cryptography

# Playfair Cipher using [Playfair.java](Playfair.java)

This repository contains a Java implementation of the Playfair cipher algorithm. The Playfair cipher is a symmetric encryption technique that operates on pairs of letters (digraphs) instead of individual letters. It was invented by Charles Wheatstone in 1854 and was later popularized by Lord Playfair.

## Features

- Encryption and decryption of messages using the Playfair cipher algorithm.
- Support for handling digraphs and special cases.
- User-friendly command-line interface for input and output.

## Usage

1. Clone the repository: `git clone https://github.com/Noaht8/Assignment-2-Cryptography.git`
2. Compile the Java source code: `javac Playfair.java`
3. Run the program: `java Playfair`

## How it works

1. The `Playfair` class defines methods for encryption and decryption using the Playfair cipher algorithm.
2. The `cipher` method takes an input message and applies the Playfair cipher rules to encode it.
3. The `encodeDigraph` method encodes the digraphs of the input message based on the cipher's specifications.
4. The `decode` method decodes the output from the cipher and reverses the encoding process.
5. The `getPoint` method returns the row and column indices of a given letter in the cipher table.



# RSA Encryption and Decryption for [RSA.py](RSA.py)

This is a Python code snippet that demonstrates the RSA encryption and decryption algorithm. The code defines a function `RSA` that takes three parameters: `p`, `q`, and `message`. It performs the RSA encryption and decryption process using the given parameters.

## Prerequisites
- Python 3.x

## Usage
1. Import the `gcd` function from the `math` module.
2. Define the `RSA` function with the following parameters:
   - `p`: A prime number.
   - `q`: Another prime number.
   - `message`: An integer to be encrypted and decrypted.
3. Inside the `RSA` function:
   - Calculate the value of `n` by multiplying `p` and `q`.
   - Calculate the value of `t` (totient) by multiplying `(p - 1)` and `(q - 1)`.
   - Select the public key `e` by iterating from 2 to `t` and finding a number that is coprime with `t`.
   - Select the private key `d` by finding a number `j` such that `(j * e) % t == 1`.
   - Perform encryption by calculating `ct` as `(message ** e) % n`.
   - Perform decryption by calculating `mes` as `(ct ** d) % n`.
   - Print the encrypted and decrypted messages.
4. Call the `RSA` function with appropriate values for `p`, `q`, and `message` to see the encryption and decryption in action.

## Example

```python
RSA(p=7, q=11, message=9)

Encrypted message is 37
Decrypted message is 9
```
In this example, the message 9 is encrypted using the RSA algorithm with prime numbers 7 and 11. The resulting encrypted message is 37, which is then decrypted back to the original message 9.
