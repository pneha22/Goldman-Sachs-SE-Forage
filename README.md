# Goldman-Sachs-SE-Forage
- Understand the techniques used by hackers to circumvent controls
- Learn a variety of techniques for cracking passwords
two variables: the website's unfortunate and irresponsible use of MD5 and the use of non-randomized passwords by the account holders.
Like SHA1, SHA3, and most other algorithms, MD5 was designed to convert plaintext into hashes, also known as "message digests," quickly and with a minimal amount of computation
the SHA512crypt function included by default in Mac OS X and most Unix-based operating systems passes text through 5,000 hashing iterations.
And because I can brute-force this really quickly, I have all of my wordlists filtered to only include words that are at least six chars long. This helps to save disk space and also speeds up wordlist-based attacks. Same thing with digits. I can just brute-force numerical passwords very quickly, so there are no digits in any of my wordlists. Then I go straight to my wordlists + best64.rule since those are the most probable patterns, and larger rule sets take much longer to run. Our goal is to find the most plains in the least amount of time, so we want to find as much low-hanging fruit as possible first.
salting appends random characters to each password before it is hashed. Besides defeating rainbow tables, salting slows down brute-force and dictionary attacks because hashes must be cracked one at a time rather than all of them at once
In cryptography, a salt is random data fed as an additional input to a one-way function that hashes data, a password or passphrase.[1] Salting helps defend against attacks that use precomputed tables (e.g. rainbow tables), by vastly growing the size of table needed for a successful attack.[2][3][4]
It also helps protect passwords that occur multiple times in a database, as a new salt is used for each password instance.[5] Additionally, salting does not place any burden on users.
Without a salt, identical passwords will map to identical hash values, which could make it easier for a hacker to guess the passwords from their hash value.
A cryptographic hash function is a mathematical algorithm that transforms input data into a fixed-size string of bytes, known as a hash value or digest.
The primary purpose of cryptographic hash functions is to provide data integrity and authenticity, ensuring that the data has not been tampered with or altered.
1. Properties:
	- Deterministic: For a given input, a cryptographic hash function always produces the same output.
	- Quick Computation: Hash functions produce output quickly, even for large inputs.
	- Pre-image Resistance: It should be computationally infeasible to find the original input data from its hash value.
	- Second Pre-image Resistance: Given an input, it should be difficult to find another input that produces the same hash value.
	- Collision Resistance: It should be computationally infeasible to find two different inputs that produce the same hash value.
	- Avalanche Effect: A small change in the input should result in a significantly different output.
	- Introduction:
		- Password cracking software refers to tools and programs used to recover passwords from their hashed or encrypted forms.
		- These tools are employed by security professionals, system administrators, and attackers to test and improve the security of password systems.
	- Types of Password Cracking Software:
		- Offline Attack Tools: These tools operate on captured password hashes stored in files or databases.
			- Examples include Hashcat, John the Ripper, and Ophcrack.
		- Online Attack Tools: These tools attempt to guess passwords by sending login attempts to a target system.
			- Examples include Hydra and Medusa.
		- Wireless Network Attack Tools: These tools target Wi-Fi networks to crack passwords used for authentication.
			- Examples include Aircrack-ng and Fern Wi-Fi Cracker.
		- Web Application Attack Tools: These tools target web applications to exploit vulnerabilities and extract passwords.
			- Examples include Burp Suite and OWASP ZAP.
