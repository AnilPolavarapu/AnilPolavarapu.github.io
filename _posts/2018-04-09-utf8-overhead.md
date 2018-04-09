---
layout: post
title: Unicode overhead for Indian languages
---

Unicode defines a gigantic mapping scheme for written characters in all languages. This post will examine the overhead of using Unicode for 2 major Indian languages.

-----

We are going to work with UTF-8 as that represents the most compact encoding for English and Latin characters. 

Let's start a simple sentence.

<code>How are you?

The 12 characters above (space is a also a character) will result in 13 bytes.

Hindi translation of that sentense.

<code>क्या हाल है?

That's 14 characters in Hindi but after encoding we have 32 bytes (2.5 times)

Telugu translation of that sentence.

<code>మీరు ఎలా ఉన్నారు?

That's 18 characters in Telugu but after encoding we have 46 bytes (3.5 times).

### Conclusion

For the same semantic sentence, Unicode can produce a more verbose representation because of that the fact the basic code plane is biased towards English.

### Further experiment

Run this experiment for a list of common phrases and see how much of overhead we pad when using Unicode.

### Reference
* [Byte counter](https://mothereff.in/byte-counter)