---
tags: ENEE_244
created: 2026-1-28
description: 1/26 notes (Slide set 1)
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

Groups of 4 consecutive bits (short for *binary digits*) in a binary number can just be written down in hex.

For example, $(11010011)_2$ can be written as $0xD3$. $1101$ represents $D$, and $0011$ represents $3$.

Hexadecimal numbers are useful for humans to write down binary numbers in short hand, which is shorter and less error-prone (but not very useful for computers).

This is often used to show memory dumps (contents of memory).

**Octal numbers** are also similarly useful. Groups of 3 bits can be written in octal.

For example, $(101010)_2 = 52_8$

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

### Convert decimal to non-decimal

Take the decimal number, and divide repeatedly by the base. Repeat with each quotient until we get a quotient of 0.

Write the remainders in reverse order (starting from the last quotient all the way to the original decimal number). This is the number is non-decimal form.

### Converting fractions

Similar method as above, but keep multiplying.

Multiply the fractional number by the base. You will likely get a number that is a fraction, so take either 0 or 1 and add the fractional part to it. Repeat with the fractional part, and keep going until the carry-over fraction is zero. Finally, read out the 0 or 1 from top to bottom.

(see slides)