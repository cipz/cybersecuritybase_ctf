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

> More secrets in the [image](02_Steganography_II/bamboozled.jpg). Can you find it?

The description given for this exercise only links to the following `jpg` file:

![](02_Steganography_II/bamboozled.jpg)

To solve this challenge I used again [stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve).
Again, I opened the File format report (`Analyze > File Format`), where I found some additional data appended to the file:

![](02_Steganography_II/solution/sol_1.png)

By decoding the ascii string with an [online base64 decoder](www.base64decode.org), I was able to capture get the flag:

![](02_Steganography_II/solution/sol_2.png)

## 3. Dr. Strangelove
## 4. Cyber monkeys
## 5. Emma's secret
## 6. Password checker
## 7. DiamondHands Bank I
## 8. Two time pad
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