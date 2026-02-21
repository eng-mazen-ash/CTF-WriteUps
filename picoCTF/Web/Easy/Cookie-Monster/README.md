# 🍪 Cookie Monster - picoCTF

## 🧾 Challenge Information

- Platform: picoCTF
- Category: Web Exploitation
- Difficulty: Easy
- Points: (noun)

---

## 📝 Description

> Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. Can you uncover the hidden recipe?

---

## 🎯 Goal

Find and retrieve the hidden flag from the web application.

---

## 🔍 Enumeration

Based on the challenge title "Cookie Monster", the first assumption was that the flag might be stored in:

- HTTP Cookies
- Client-side storage
- Encoded values

Therefore, browser Developer Tools were used for further inspection.

---

## 🛠 Investigation

1- Opened Developer Tools: [F12 → Application → Cookies]

2- A cookie named: [secret_recipe]

3- was discovered with the following value: 
**cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0IzQUQ5NEMyfQ%3D%3D**

---

## 🔓 Decoding Process

### Step 1: URL Decode

The string ends with: [%3D%3D]


This indicates URL encoding (`%3D` = `=`).

After URL decoding:  [cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0IzQUQ5NEMyfQ==]

---

### Step 2: Base64 Decode

The decoded string appears to be Base64 encoded.

After decoding:  [picoCTF{c00k1e_m0nster_l0ves_c00kies_B3AD94C2}]

---

## 🏁 Final Flag 
picoCTF{c00k1e_m0nster_l0ves_c00kies_B3AD94C2

---

## 🧠 Lessons Learned

- Always inspect browser cookies in web challenges.
- Encoded values may be layered (URL encoding + Base64).
- Challenge titles often contain useful hints.
- Client-side storage is a common place to hide flags in beginner web CTFs.

---

## 📌 Key Takeaway

When solving Web CTF challenges:

1. Check Cookies  
2. Check Local and Session Storage  
3. View Page Source  
4. Inspect Network Requests  
5. Try common decoding techniques  

---

🔐 This writeup is for educational purposes only.




