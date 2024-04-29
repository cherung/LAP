# Introduction (with ChatGPT)
Error correction codes (ECC) are techniques used in digital communication and data storage to detect and correct errors that occur during transmission or storage. These errors can be caused by various factors such as noise, interference, or physical defects in the medium.  

One of famous ECC is Hamming code, used in digital communication and data storage systems. Named after its inventor, Richard Hamming, it adds extra parity bits to transmitted data, enabling the detection and correction of errors that occur during transmission or storage. By assigning parity bits to cover specific combinations of data bits, Hamming code can identify and correct single-bit errors and detect some multiple-bit errors. 


For example, the Hamming (7, 4) code uses 7 bits to encode a 4 bit message.  As shown in the following figure, the original message are placed in position 1 to 4.  Next, we add bits to area 5 to 7, so that each circle has even number of 1s. For example: the original data is 1101.  The filled in data is $b_5=0, b_6 = 1, b_7 = 0$.
  
<img src="Hamming.png" alt="Hamming" width="200px">

# 0-1 Vector space
In this project, we will learn how to use 0-1 vector space to design an ECC.

A 0-1 vector space is a specific type of vector space where the vectors consist of elements that are either 0 or 1. In other words, each component of the vectors can take only one of two possible values: 0 or 1.

Formally, a 0-1 vector space can be defined as follows:

Let F be a field, typically $F = \{ 0, 1 \}$ with addition and multiplication modulo 2 (also known as the binary field).
For addition, the definition is 
| + | 0 | 1 |
|---|---|---|
| 0 | 0 | 1 |
| 1 | 1 | 0 |

For multiplication, the definition is 
| * | 0 | 1 |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 1 |

For a message with $n$ bits, we can make it a $n$-vector of elements in $F$.  For example, when $n=4$, a message  $1011$ can be formulate as 

$$ m=\begin{bmatrix} 1 \\ 
                     0 \\ 
                     1 \\ 
                     1 \end{bmatrix}. $$

# Hamming code


