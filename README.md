# Feistel-Cipher-Python

Python program to implement Feistel encryption and decryption. Feistel Cipher is a symmetric structure used in the construction of block ciphers. It involves multiple applications of two primary applications: substitutions and permutations. The encryption algorithm applies multiple rounds of both. 

![Picture1](https://user-images.githubusercontent.com/68347909/115645110-c91cf880-a2ed-11eb-9e9f-7958ff6cc797.png)

A Feistel network uses a round function, a function which takes two inputs, a data block and a subkey, and returns one output the same size as the data block. In each round, the round function is run on half of the data to be encrypted and its output is XORed with the other half of the data as shown above. This is repeated a fixed number of times, and the final output is the encrypted data. 

 ![image](https://user-images.githubusercontent.com/68347909/115645355-3761bb00-a2ee-11eb-87f3-c35ea5f41373.png)

An important advantage of Feistel networks compared to other cipher designs such as substitution–permutation networks is the entire operation is guaranteed to be invertible (that is, encrypted data can be decrypted), even if the round function is not itself invertible. 

In this repository, a feistel program is written in Python. There are 6 functions: 
xor: to perform XOR operations between two byte sequences
F: the round function
gen_keylist: to generate keys
feistel_block: The building block of the feistel cipher (see the first image)
feistel_enc: The actual encoder
feistel_dec: The decoder
