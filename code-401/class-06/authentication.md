# Authentication 

## Securing Passwords

1. Explain to a non-technical friend how you would safely hash and store a password.

    Imagineyour password is like a secret message. Instead of keeping this message in its original form (which can be easily read if someone fids it), we use a special tool to scramble it into a unique code. This scrambled code is called a "hash". Even if someone gets a hold of this code, they can't easily turn it back into the original message. When you want to log in, we scramble your entered password in the same way and check if the codes match. This way, we never have to look at or store your actual password, just the scrambled code. 

2. What is Bcrypt?

    Bcrypt is a tool that helps us scramble passwords into these unique codes. It's based on a special mathematical method called the Blowfish algorithm. What makes Bcrypt special is that it can make the scrambling process slow on purpose. This might sound odd, but it's actually a good thing. If someone tries to guess your password by trying lots of different codes quickly, Bcrypt slows them down, making it much harder for them to succeed. 


3. Why might you use something like Bcrypt?

    We would use Bcrypt because it's strong and secure. Unlike some other tools, Bycript is designed to adapt over time. As computers get faster and better at guessing passwords, Bcrypt can be adjusted to be even slower, keeping passwords safe. It's like having a lock that gets tougher to pick as thieves get smarter. Using Bcrypt ensures that even if someone steals the scrambled codes, they would have a very hard time figuring out the original passwords. 