# Huffman-Shannon_fano

# Aim:

Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 

Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.

# Tools Required:

Google colab

# Program:
```
import numpy as np

import math

L = 0

hs = 0

p = []

lk = []

n = int(input("Enter the number of Samples : "))

for i in range (n): pr = float(input(f"Enter the probability of sample values {i + 1}: "))

p.append(pr)

for j in range (n):

l = float(input(f"Enter the length of the sample values {j + 1}: "))

lk.append(l)# Avg length of the code word

for k in range (n):

Avg1 = p[k] * lk[k]

L = L + Avg1

for k in range (n):

e = p[k] * math.log(1 / p[k], 2)

hs = hs + e

hs = round(hs,3)

eff = hs / L

eff = round(eff,3)

red = round(1 - eff,3)

for k in range(n):

var1 = p[k] * (lk[k]-L)**2

var = var + var1

var = round(var,3)

print(f"Average Codeword Length is : {L}")

print(f"Entropy is : {hs}")

print(f"Efficiency is : {eff}")

print(f"Redudancy is : {red}")

print(f"Variance is : {var}")
```
# Calculation:

![image](https://github.com/user-attachments/assets/64a8b73c-3f13-4abb-a282-bb41bcc4618b)

# Results:

Here the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25

Average Codeword Length is : 2.625 Entropy is : 2.625 Efficiency is : 100.0 % Redudancy is : 0.0 Variance is : 0.484
