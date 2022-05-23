# ada-info
Some points to improve quality of life when using ADA frequently
## Saving the password
To connect normally, use 
```bash
ssh s.ranjan@ada
```
Add ada to list of known hosts by entering yes (if propmted)
Then enter password.
Login Complete

Painful to enter password each time 

Use [this](https://serverfault.com/questions/241588/how-to-automate-ssh-login-with-password) link to avoid doing that


```bash
# Generate a key
ssh-keygen -t rsa -b 2048
# Might need to hit Enter three times

# Copy key to the Server
ssh-copy-id s.ranjan@ada
#Enter the password

# Login to test if it worked
ssh s.ranjan@ada
# Not prompted for password (hopefully)
```

Add an alias in bashrc to simplify the process of logging in
Open .bashrc using `nano ~/.bashrc` and at the end of the file, append:
```bash
alias ada="ssh s.ranjan@ada"
```
