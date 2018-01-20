# DB Security and Info Sec - Lecture 4 
Friday 8th December 2017 
H. Dee 

## Symmetric Key Encryption: DES, AES  

### Key Points

- Key is secret 
- Key is known at both ends - needed for Encryption and Decryption. 


## DES 

Data Encyption Standard:

	- US Gov. needed standard for secure computational storage and transmission of documents. 
	- IBM - algorithm on Lucifer cypher. 
	- 1975. Practically broken in the late 1990s. 

	
Broadly speaking: 

	- Shuffle Key around so you get 16 sub keys. 
	- Combine (XOR) these sub keys w/ half of the input text. 
	- Switch halves. 
	- Repeat this 16 times in total. 