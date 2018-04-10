---
layout: post
title: Securing your personal documents/will for use after you die
---

### Shamir's secret algorithm

In simple words, Shami'r algorithm will take a secret (in my case, a password) and break it down into 'n' different fragments with a threshold 't'. The threshold signifies how many fragments are necessary to reconstuct the secret.

Example:
Secret is 'password'

For n=3 and t=2, I can get fragments like,

1-uasdasdasf

2-87uba5823n

3-98ujab16jk

When you combine say 1 & 3 fragments, you get back the original secret.

### How I do it?
1. Put down my documents/will as text files.

2. Encrypt the files with a master password (symmetric - SHA256) and transfer to a thumb drive.

3. Break the password into 3 pieces with threshold as 2.

4. E-mail those 3 pieces to 3 different friends living in different countries. They don't know that they are getting a password fragment, it's just a random string to them.

5. Keep the thumb drive as a secure location and let a family member know what to do if they need to access that data.

### What happens in case of an event?

The 2 of the 3 friends will definitely attend the last rights.

Family member will take the fragments from them and get the master secret.

Family member will decrypt the files using the master secret.

### Reference
* [Online demo of Shamir's algorithm](http://www.point-at-infinity.org/ssss/demo.html)