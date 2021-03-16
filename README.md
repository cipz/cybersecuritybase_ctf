# Cybersecurity Base 2020 / 2021 CTF

## 1. Steganography I

> *You see a large wolf as you are crossing a field. Can you figure out her [name](01_Steganography_I/doggy.jpg)?*

The description given for this exercise only links to the following `jpg` file:
![](01_Steganography_I/doggy.jpg)

To solve this exercise I have used the [stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve) tool, which I started with the command:

    java -jar stegsolve.jar

I opened the File format report (`Analyze > File Format`), where I found the flag (LilSif) under the ascii dump of data:

![](01_Steganography_I/solution/sol_1.png)

## 2. Steganography II

> *More secrets in the [image](02_Steganography_II/bamboozled.jpg). Can you find it?*

The description given for this exercise only links to the following `jpg` file:

![](02_Steganography_II/bamboozled.jpg)

To solve this challenge I used again [stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve).
Again, I opened the File format report (`Analyze > File Format`), where I found some additional data appended to the file:

![](02_Steganography_II/solution/sol_1.png)

By decoding the ascii string with an [online base64 decoder](https://www.base64decode.org), I was able to capture get the flag:

![](02_Steganography_II/solution/sol_2.png)

## 3. Dr. Strangelove

> *You have lost your key to Dr. Strangelove software and he is refusing to help you since he believes that those who are foolish enough to lose their keys don't deserve to use his products. Dr. Strangelove has suggested that you try to figure out what your key was. You can use his key validation service that is available [here](https://csb-capture-the-flag.cs.helsinki.fi/challenge-files/sites/strangelove/).*

The description redirects to this website:

![](03_Dr_Strangelove/solution/sol_1.png)

By viewing the source code of the webpage I saw the only JavaScript file was `test.js`, in which I found the password, hidden in plain sight:

![](03_Dr_Strangelove/solution/sol_2.png)

## 4. Cyber monkeys

> *A troop of cyber monkeys decided to start a security consultancy. They claim that they invented a new unbreakable encryption scheme. Can you break the code: Jub xrrc fgrnyvat bhe onananf? Jr obhtug n arj fnsr naq gur cnffjbeq vf ZbaxrlObbmr.*

For capturing this flag I used an [online Caesar cipher encoder and decoder](https://cryptii.com/pipes/caesar-cipher) to decipher the given string:

![](04_Cyber_monkeys/solution/sol_1.png)

## 5. Emma's secret
## 6. Password checker

> *A merchant named Oswald has forgotten password for his proprietary [software](06_Password_checker/register). Can you help him out?*

The description provides us with a binary file.
By analyzing this with an [online file viewer tool](https://www.percederberg.net/tools/file_info.html), I was able to get the flag:

![](06_Password_checker/solution/sol_1.png)

## 7. DiamondHands Bank I
## 8. Two time pad

> *A shady man named Patches sends a message to Petrus using XOR and a one-time pad. You find out that the plain text message 'riches' encrypted is 'vjeomr'. Patches being stingy sends a new message 'glqfze' and reuses the pad. Decrypt the message.*

To solve this challenge I used and [online XOR calculator](http://xor.pw/), since the description explicitly says *using XOR and a one-time pad*.

First, I extracted the the pad by calculating the XOR between the cleartext and the encrypted string.

![](08_Two_time_pad/solution/sol_1.png)

Then, I got the cleartext of the second string by calculating the XOR between the previous result and the encrypted string:

![](08_Two_time_pad/solution/sol_2.png)

## 9. DiamondHands Bank II
## 10. Logs logs logs
## 11. Password II
## 12. Monkeys are back
## 13. Dr. Strangelove Mk II
## 14. Dawn of the monkeys
## 15. Lazy passwords
## 16. Password III
## 17. Rise of the monkeys
## 18. Cyber crime does pay
## 19. Dr. Strangelove strikes back!
## 20. Steganography III
## 21. Password IV
## 22. Country roads

# Personal considerations