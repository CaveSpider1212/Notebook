---
tags: ENEE_244
created: 2026-1-28
description: 1/26, 1/28 notes (Slide set 1)
---

### Base 2 numbers and conversion to base 10

Numbers in daily use are base 10 (called **decimal numbers**), where each digit represents a different power of 10.

For example, 53 can be represented as $5 \times 10^1 + 3 \times 10^0$.

Numbers can also be represented in base 2, called **binary numbers**, where each digit represents a different power of 2.

For example, $110101_2$ can be written as $1 \times 2^5 + 1 \times 2^4 + 0 \times 2^3 + 1 \times 2^2 + 0 \times 2^1 + 1 \times 2^0 = 32 + 16 + 4 + 1 = 53_{10}$.

### Hexadecimal numbers

If the base is greater than 10 (for example, 16), then we would need symbols to represent all the numbers from 10 up to (but not including) 16.

In this case, 10 would be A, 11 would be B, all the way to 15, which would be F.

For example, $(1FF)_{16}$ can be expressed as $1 \times 16^2 + 15 \times 16^1 + 15 \times 16^0 = 256 + 240 + 15 = (511)_{10}$.

Also, $(15)_{16}$ can be written as $0x15$. The $0x$ prefix denotes hexadecimal numbers.

### Special case of hexadecimal and octal conversion

**Hexadecimal numbers** are very useful for representing binary numbers. They yield very simple conversion without the need for arithmetic.

Groups of 4 consecutive bits (short for *binary digits*) from the *right* in a binary number can just be written down in hex.

For example, $(11010011)_2$ can be written as $0xD3$. $1101$ (which is 13) represents $D$, and $0011$ represents $3$.

Hexadecimal numbers are useful for humans to write down binary numbers in short hand, which is shorter and less error-prone (but not very useful for computers).

This is often used to show memory dumps (contents of memory).

**Octal numbers** are also similarly useful. Groups of 3 bits can be written in octal.

For example, $(101010)_2$ can be separated as $(101)_2$ and $(010)_2$, which equal $5$ and $2$, so the answer is $52_8$

### Binary arithmetic

> [!info] Binary Addition
> Similar to addition of decimal numbers, where carrying over is involved.
> 
> Write the last digit of the sum on the bottom and carry over the remaining digit(s) on the top.

^facd10

> [!info] Binary Subtraction
> Similar to subtraction of decimal numbers, where borrowing is involved.
> 
> When you need to borrow from the digit on the left, make the digit on the left the next lowest *binary* number.

> [!info] Binary Multiplication
> Exactly the same as multiplication of decimal numbers, with the only difference being doing [[Binary Representations and Arithmetic#^facd10|binary addition]] in the end.

### Convert decimal and non-decimal

> [!info] Base Numbers
> Numbers in base $x$ means each digit represents a different power of $x$ ($x^0, x^1, x^2, ...x^n$).

Take the decimal number, and divide repeatedly by the base. Repeat with each quotient until we get a quotient of 0.

Write the remainders in reverse order (starting from the last quotient all the way to the original decimal number). This is the number is non-decimal form.

To write numbers in decimal form, multiply each digit by the corresponding base and add them together (see the above note).

### Converting fractions

To convert decimal fractions to binary, it is a similar method as above, but keep multiplying (until the fractional part is 0) instead of dividing. Write the remainders in the order that you did the calculations (opposite of non-fractions).

Multiply the fractional number by the base. You will likely get a number that is a fraction, so take either 0 or 1 and add the fractional part to it. Repeat with the fractional part, and keep going until the carry-over fraction is zero. Finally, read out the 0 or 1 from top to bottom.

(see slides)

To convert from binary to decimal fractions, convert the whole part as normal and for each digit in the fractional part, multiply it by $2^x$, where $x$ starts from $-1$ (the tenths digit) and goes down.

### Complements of numbers

There are two kinds of complements of a number $N$ for a radix (base) $r$:
- Radix complement: $r^n - N$ (where $n$ is the number of digits in $N$)
- Diminished radix complement: $r^n - 1 - N$
	- Easier to complement, since we don't need to borrow when subtracting

### Radix complements

The radix complement is simply the diminished radix complement + 1.

> [!tip] Radix and Diminished Radix Complements (Easy)
> Diminished Radix Complement: $(r - 1)^n - N$, where $n$ is the number of times to repeat $(r - 1)$ and $N$ is the original number, which we are subtracting normally from $(r - 1)^n$
> 
> Radix Complement: $(r - 1)^n - N + 1$, which is the diminished radix complement + 1

If the number is a fraction, then remove the radix point, convert, then restore the fraction point.

> [!info]
> Two's complement of two's complement gives back the number.
> 
> This is important because all computers represent negative integers as their two's complement of their magnitude (absolute value). This changes the representation of negative numbers and allows much simpler circuits for arithmetic, since subtraction can be performed using a circuit for addition.
> 
> The first bit (most significant bit) of a two's complement tells us if the number is positive (first bit is 0) or negative (first bit is 1).

### Subtraction with complements

Do subtraction by replacing negative numbers with their two's complement, then just do addition.

If we wanted to compute $M - N$, the steps are as follows:
1. Represent as $M + (-N)$
2. Replace by radix complement: $M + r^n - N$
3. Discard any carry out of the most significant digit (which represents $r^n$)

There are two cases (both of which are correct);
- If $M \geq N$, then $r^n$ is a carry-out of the most significant bit, so the answer is $M - N$
- If $M < N$, then the answer is negative, so $r^n - (N - M)$ is correct (since it is the two's complement of $M - N$)

> [!example] Subtraction Example #1 (Binary)
> **Question**:
> Compute $11110 - 01001$ (on a 6-bit computer).
> 
> **Solution**:
> Represent the negative number ($01101$) as two's complement by flipping the bit and adding 1.
> $01001$ is actually $001001$ in this case since it is a 6-bit computer. Flipping the bits would get $110110$ and adding 1 would get $110111$.
> Likewise, $11110$ is actually $011110$.
> 
> $011110 + 110111$ using binary addition would get us $1010101$, but since this is a 6-bit computer (and the answer is 7 bits), the most significant bit needs to be discarded, so the final answer is $010101$ or $10101$, or 21.

> [!example] Subtraction Example #2 (Binary)
> **Question**:
> Compute $10001 - 10111$ (on a 6-bit computer).
> 
> **Solution**:
> The complement of the second number (which becomes $010111$) is $101000$, and adding 1 to that gets us $101001$.
> 
> $010001 + 101001$ gets us $111010$. Since the first bit is 1, the number is negative, so we need to take the two's complement of this number to get the absolute value of the answer.
> 
> The two's complement of $111010$ is $000110$, or $00110$, so the answer is $-00110$ (which equals -6).

### Representation of numbers in computers (2's complement representation)

All modern computers use 2's complement representation, so all negative numbers are represented by the 2's complement of their absolute values.

For numbers with $n$-bit absolute values, use $n + 1$ bits int he computer. The most significant bit (MSB) functions as a sign bit.
- If the MSB is 0, then the number is positive
- If the MSB is 1, the number is negative (because the complement of the positive part is stored)

Overflow check: If the carry-in to the $n+1$th bit $\neq$ carry-out, then there is overflow.

In an $n$-bit computer, 2's complement numbers represent the number range $[-2^{n-1} ... 2^{n-1} - 1]$.

### Signed magnitude representation

The first bit on the left is the sign bit, while the remaining bits are the magnitude bits.

Disadvantages:
- Need separate subtraction hardware
- Two zeros: 00000 and 10000
- One less number ($-(2^{n - 1} - 1)$ to $2^{n - 1} - 1$)

Not used in computers due to these drawbacks.