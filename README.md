# Assignment-2-Cryptography

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
