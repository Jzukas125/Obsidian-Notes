Introduction
Purpose of this is to introduce us to basic concepts such as: Symmetric encryption, Asymmetric encryption, Diffie-Hellman Key Exchange, Hashing, PKI.
First example is obivously the ceasar cipher which shifts letters by a fixed interval
Ceasar cipher is considered a subsitiution cipher becasue each letter in the alphabet is substituted with another. 
Transposition cipher - encrypts messages by changing the order of the letters. Ie the message would be "THIS ALPHA BRAVO CONTACTING TANGO HOTEL MIKE" and the key would be 42351. After filling the columns in with the letters the key would be used to move them around
For an encryption to be considered secure it needs a feasibly impossible time to crack 


Symmetric Encryption
Cryptographic algorithm - an algorithm that defines the encryption and decryption processes
Key - the cryptographic algorithm needs a key to convert the plain text into cipher text and vice verse
Plain text - the original message that needs to be encrypted
cipher text - message in its encrypted form
A symmetric encryption algorithm uses the same key for encryption and decryption hence the name. A secret key needs to be agreed upon by both parties.
	AES is the advanced encryption standard, and it follows four transformations of multiple types, of which are:
-  SubByte(state) - this transformation looks up each byte in a given substitution table and substitutes it with the respective value. The state is 16 bytes saved in a 4 by 4 array.
 - ShiftRows(state) - The second row is shifted by one place, the third row is shifted by two places, and the fourth row is shifted by three places. 
- MixColumns(state) - the second row is shifted by one place, the third row is shifted by two places, and the fourth row is shifted by three places.
- AddRoundKey(state) - a round key is added to the state using the XOR operation