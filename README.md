Sure, here’s a draft for your README file for the “Hacking the Admins” OSINT challenge in the KPMG CTF 2024. I’ve included sections for the challenge description, steps taken, and your solution, with a touch of emoji to make it engaging!

---

# KPMG CTF 2024: Hacking the Admins 🕵️‍♂️🔍

Welcome to my write-up for the **Hacking the Admins** OSINT challenge in the KPMG CTF 2024! 🚀 This challenge was a test of our open-source intelligence skills and was both exhilarating and challenging. Here’s a detailed walkthrough of how I cracked the challenge and secured the 200 points. 🏆

## Challenge Overview

**Challenge Name:** Hacking the Admins  
**Points:** 200  
**Category:** OSINT (Open-Source Intelligence)  

**Clue Provided:**  
```
Raghava Sai Sarvan really likes cats!!
```

## Solution Walkthrough 🧩

### 1. Initial Clue and Search 🕵️

The first clue pointed to Raghava Sai Sarvan. A quick Google search led me to his personal page. In his about section, I found a Base64 encoded message.

### 2. Decoding the Base64 Message 📜

Decoded Base64 message:
```
Never gonna give you up
Never gonna let you down
Never gonna run around and desert you
Never gonna make you cry
Never gonna say goodbye
Never gonna tell a lie and hurt you
```

This decoded message was a classic Rickroll, leading me to a Pastebin link.

### 3. Pastebin Exploration 🗂️

The Pastebin link required the password “meow” to access. Upon opening, it revealed a LinkedIn profile link:
```
https://www.linkedin.com/in/saurabh-bhatt-cybersecurity/
```

### 4. Finding the Next Clue 🔍

On the LinkedIn profile, I discovered a string of characters:
```
5k2tWE6P7gjtw4iCUSTTeNFaxbTu4WVfoGHgfE73
```

I also found a Discord account with the username **eren_meow**. In the bio of this Discord profile, there was another string:
```
44WkWTAaTZM1pKThjQk2c
```

### 5. Decoding the Base58 Strings 🔑

I used CyberChef to decode these Base58 strings. For the first string, I got another Pastebin link:
```
https://pastebin.com/KM65Tw0R
```

This Pastebin also required a password, which I found by decoding the Base58 string from the Discord bio:
```
meowsaurabh123!
```

### 6. Accessing the Final Pastebin 📎

Using the password, I accessed the Pastebin link which provided a LinkedIn profile:
```
https://www.linkedin.com/in/aditya-kashinath-4042a1186/
```

### 7. The Final Challenge 🏁

On this LinkedIn profile, there was another Pastebin link:
```
https://pastebin.com/KVn2Y9uk
```

This Pastebin required a password generated from a Brainfuck code. I decoded the Brainfuck code to get the password:
```
kitty.olly.chan
```

Using this password, I accessed the final Pastebin, which revealed the flag:

```
KPMG_CTF{71f920fa275127a7b60fa4d4d41432a3}
```

## Conclusion 🎉

After several trials and challenges, I managed to solve the OSINT challenge and secure the flag. It was a rewarding experience to crack the clues and decode the various layers of encryption. 🧠🔓

Feel free to explore the repository for more write-ups and solutions from the KPMG CTF 2024! 🚀
