---
layout: post
title: Securing your personal documents/will for use after you die
---

### Shamir's secret algorithm

In simple words, Shami'r algorithm will take a secret (in my case, a password) and break it down into 'n' different fragments with a threshold 't'. The threshold signifies how many fragments are necessary to reconstuct the secret.

Example:
Secret is 'password'

For n=3 and t=2, I can get fragments like
1-uasdasdasf
2-87uba5823n
3-98ujab16jk

### How I do it?
1. Put all my documents/will as a text file on a thumb drive.

2. Encrypt the files with a master password (symmetric - SHA256).

3. Break the password into 3 pieces with threshold as 2.

4. E-mail those 3 pieces to 3 different friends living in different countries.

5. Keep the thumb drive as a secure location and let a family member know what to do if they need to access that data.

### References
Online demo of Shamir's algorithm.
