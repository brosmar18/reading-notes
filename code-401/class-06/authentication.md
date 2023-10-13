# Authentication 

## Securing Passwords

1. Explain to a non-technical friend how you would safely hash and store a password.

    Imagineyour password is like a secret message. Instead of keeping this message in its original form (which can be easily read if someone fids it), we use a special tool to scramble it into a unique code. This scrambled code is called a "hash". Even if someone gets a hold of this code, they can't easily turn it back into the original message. When you want to log in, we scramble your entered password in the same way and check if the codes match. This way, we never have to look at or store your actual password, just the scrambled code. 

2. What is Bcrypt?

    Bcrypt is a tool that helps us scramble passwords into these unique codes. It's based on a special mathematical method called the Blowfish algorithm. What makes Bcrypt special is that it can make the scrambling process slow on purpose. This might sound odd, but it's actually a good thing. If someone tries to guess your password by trying lots of different codes quickly, Bcrypt slows them down, making it much harder for them to succeed. 


3. Why might you use something like Bcrypt?

    We would use Bcrypt because it's strong and secure. Unlike some other tools, Bycript is designed to adapt over time. As computers get faster and better at guessing passwords, Bcrypt can be adjusted to be even slower, keeping passwords safe. It's like having a lock that gets tougher to pick as thieves get smarter. Using Bcrypt ensures that even if someone steals the scrambled codes, they would have a very hard time figuring out the original passwords. 

## Basic Auth 

1. What is Basic Authentication?

    Basic authentication is a method used in HTTP transactions that allows an HTTP user agent (like a web browser) to provide a username and password when making a request. It is a straightforward technique for enforcing access controls to web resources without the need for cookies, session identifiers, or login pages. 

2. What properties are necessary in the header of a Basic Auth request?

    In a Basic Auth request, the necessary property in the header is the `Authorization` field. This field contains the word "Basic" followed by a space and then the `<credentials>`. The `<credentials>` is the Base64 encoding of the combired username and password, separated by a colon. 

4. How are `username:password` in Basic Auth encoded?

    In Basic Authentication, the `username:password` combination is first joined by a single colon (`:`). The resulting string is then encoded using Base64. This Base64 encoded string represents the `<credentials>` that are included in the `Authorization` header field of the HTTP request. 

## OWASP auth cheetsheet 

1. Define the authentication process to a non-technical recruiter.

    Authentication is like checking someone's ID at the entrance of a private event. In the online world, when you log into a website or an app, it needs to make sure you are who you say you are. This is done by asking for your username (like your name) and a password (like a secret handshake). If both are correct, the website lets you in. If not, it asks you to try again. It's a way to keep private info safe and ensure only authorized people get access. 

2. How should your error messaging respond (both HTTP and HTML)? Why?

    Error messages should be generic and not give away too much information. For example, instead of saying "Username not found" or "Password is incorrect," the message should simply state "invalid login credentials". This is important for two main reasons: 
    
    - **Security**: By being vague, we don't giuve potential attackers clues about what they got wrong, makig it harder for them to guess the correct credentials. 

    - **User Privacy**: We don't want to inadvertently reveal if a particular username exists or not, as this can be used for malicious purposes or unwanted solicitations. 

    In terms of HTTP responses, a standard "401 Unauthorized" can be used to indicate failed authentication attempts. This keeps it consistent and doesn't provide extra information to potential attackers. 


