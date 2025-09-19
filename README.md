# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.25,0.25,0.125,0.125,0.125,0.0625,0.0625} for its output. 
Apply the Huffman to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
  Co-Lab
# Program:
```
p = [0.30,0.25,0.20,0.12,0.08,0.05];

# Code lengths
lk = [2,2,2,3,4,4];

n = len(p);

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n));

# Entropy
import math
hs = 0;
for k in range(n):
    hs = hs + p[k] * math.log2(1/p[k]);
hs = round(hs*1000)/1000;

# Efficiency & Redundancy
eff = round((hs / L)*1000)/1000;
red = round((1 - eff)*1000)/1000;

# Variance of codeword length
var = sum(p[k] * (lk[k] - L)**2 for k in range(n));
var = round(var*1000)/1000;

print("Average Codeword Length is : " + str(L));
print("Entropy is : " + str(hs));
print("Efficiency is : " + str(eff*100) + "%");
print("Redundancy is : " + str(red));
print("Variance is : " + str(var));
```
# Calculation:

![WhatsApp Image 2025-09-19 at 10 57 33_86549d9c](https://github.com/user-attachments/assets/4d5c1248-0da9-4cb5-b62e-f2ed7da890fc)


# Output
```
Average Codeword Length is : 1.78
Entropy is : 1.896
Efficiency is : 100.0%
Redundancy is : 0.0
Variance is : 0.398
``` 
# Results:
```
Thus,the Huffman-Shannon_fano is verified both theoretically and practically
```
