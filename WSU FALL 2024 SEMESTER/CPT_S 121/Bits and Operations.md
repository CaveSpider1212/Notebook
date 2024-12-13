---
tags: CPT_S_121
created: 2024-11-15
description: Lesson 13.1
---

### Basic Memory Concepts

- When a variable is declared, memory is allocated based on its data type (char, int, double)
	- Char is the smallest, followed by integers, and doubles are the largest
- All information is stored in memory as *bits* of data
	- Bit is derived from binary digit, which can be either 0 or 1
- A sequence of 4-bits is a *nibble*, and a sequence of 8-bits is called a *byte*

### Number Systems

- Decimal and binary systems are called *positional* number systems
- A digit from one of these systems has a *weight* dependent upon its position or location within the string of digits
- Each position is weighted as the *base* of the system to a power
	- Decimal is base 10
	- Binary is base 2
- A *binary number* consists of one or more bits
- To evaluate a number in a positional number system, pick each digit and multiply by its weighted position and compute the sum
	- For example, $123_{10} = 1 * 10^2 + 2 * 10^1 + 3 * 10^0$
		- The 1 is in the hundreds ($10^2$) position, the 2 is in the tens ($10^1$) position, and the 3 is in the ones ($10^0$) position

### Converting from Decimal to Binary

The binary number will be represented by one byte or 8-bits, so there will be 8 digits.

1.  Find the weights $2^x$ for an 8-bit number, starting from x = 7 going all the way to x = 0
2.  Determine if $2^x$ (starting from x = 7) goes into the decimal number
	- If it doesn't, place a 0 there and move on with the same decimal number
	- If it does, place a 1 there and subtract the value (what $2^x$ is equal to) from the current decimal number and move on with the new number as the decimal number
3. Keep going all the way through x = 0

> [!example] Converting from Decimal to Binary
> Convert $123_{10}$ to a binary number represented by one byte or 8-bits.
> 
> 1. We need the following weights for an 8-bit number:
> $$2^7 \hspace{2mm} 2^6 \hspace{2mm} 2^5 \hspace{2mm} 2^4 \hspace{2mm} 2^3 \hspace{2mm} 2^2 \hspace{2mm} 2^1 \hspace{2mm} 2^0$$
> 
> 2. Determine if the largest power of 2 (in this case, $2^7$) goes into $123_{10}$. It doesn't, so place a 0 in the $2^7$ slot.
> $$2^7 = 128_{10} > 123_{10}$$
> 
> 3. Determine if $2^6$ goes into $123_{10}$. It does, so place a 1 in the $2^6$ slot
> $$2^6 = 64_{10} \leq 123_{10}$$
> 
> 4. Subtract $64_{10}$ from $123_{10}$. This is the new decimal number we are using.
> $$123_{10} - 64_{10} = 59_{10}$$
> 
> 5. Determine if $2^5$ goes into $59_{10}$. It does, so place a 1 in the $2^5$ slot.
> $$2^5 = 32_{10} \leq 59_{10}$$
> 
> 6. Subtract $32_{10}$ from $59_{10}$. This is the new decimal number we are using.
> $$59_{10} - 32_{10} = 27_{10}$$
> 
> 7. Determine if $2^4$ goes into $27_{10}$. It does, so place a 1 in the $2^4$ slot.
> $$2^4 = 16_{10} \leq 27_{10}$$
> 
> 8. Subtract $16_{10}$ from $27_{10}$. This is the new decimal number we are using.
> $$27_{10} - 16_{10} = 11_{10}$$
> 
> 9. Determine if $2^3$ goes into $11_{10}$. It does, so place a 1 in the $2^3$ slot.
> $$2^3 = 8_{10} \leq 11_{10}$$
> 
> 10. Subtract $8_{10}$ from $11_{10}$. This is the new decimal number we are using.
> $$11_{10} - 8_{10} = 3_{10}$$
> 
> 11. Determine if $2^2$ goes into $3_{10}$. It doesn't, so place a 0 in the $2^2$ slot.
> $$2^2 = 4_{10} > 3_{10}$$
> 
> 12. Determine if $2^1$ goes into $3_{10}$. It does, so place a 1 in the $2^1$ slot.
> $$2^1 = 2_{10} \leq 3_{10}$$
> 
> 13. Subtract $2_{10}$ from $3_{10}$. This is the new decimal number we are using.
> $$3_{10} - 2_{10} = 1_{10}$$
> 
> 14. Determine if $2^0$ goes into $1_{10}$. It does, so place a 1 in the $2^0$ slot.
> $$2^0 = 1_{10} \leq 1_{10}$$
> 
> Final answer: ${01111011}_2$

Note: If the lsb (least significant bit, the rightmost bit) is 1, the number is odd, and if it's 0, the number is even

### Converting from Binary to Decimal

1. Find the weights $2^x$ for a 4-bit number, starting from x = 3 all the way to x = 0
2. Multiply each digit from the binary number by the corresponding position weight (for example, the digit in the thousandths place will be multiplied by $2^3$, hundredths place by $2^2$, and so on)
3. Sum up each individual digit (the products found above) to get the decimal value

> [!example]
> Convert a nibble ${1010}_2$ to a decimal number.
> 
> 1. We need the following weights for a 4-bit number. Each weight corresponds to an individual digit of the binary number in the same order.
> $$2^3 \hspace{2mm} 2^2 \hspace{2mm} 2^1 \hspace{2mm} 2^0$$
> 
> 2. Pick off each digit from the binary number and multiply by its corresponding positional weight (shown above).
> $$1 \times 2^3 = 8_{10}$$
> $$0 \times 2^2 = 0_{10}$$
> $$1 \times 2^1 = 2_{10}$$
> $$0 \times 2^0 = 0_{10}$$
> 
> 3. Sum up each individual result obtained in the previous step.
> $$8_{10} + 0_{10} + 2_{10} + 0_{10} = 10_{10}$$
> 
> Final answer: $10_{10}$

### Applying Bitwise Operators

- Bitwise operators include
	- **Left shift (<<)**: shift each bit in the number to the left by the set number of positions (the number is next to the bit)
		- Result depends on how much memory is available...if there is a set limit on memory then the digits at the end will shift to the left (and their old positions will be replaced with 0's), otherwise 0's will simply just be added to the end
		- Example: $1011_2$ << 2 becomes $1100_2$ if only a nibble (4 bits) of memory is available, otherwise would be $100100_2$
	- **Right shift (>>)**: shift each bit in the number to the right by the set number of positions (the number is next to the bit)
		- Replaces old spots with 0's, also loses the lsb
		- Example: $1001_2$ >> 1 becomes $0101_2$
	- **Negation (~)**: negate or "flip" each bit (each 1 becomes a 0, and each 0 becomes a 1)
		- Example: ~$1010_2$ becomes $0101_2$
	- **Bitwise AND (&)**: AND each bit in each corresponding position (becomes 1 if both bits are 1's, and 0 if any one of them are 0)
		- Example: $1010_2$ & $0011_2$ becomes  $0010_2$
	- **Bitwise OR (|)**: OR each bit in each corresponding position (becomes 1 if either bit is 1, and 0 if both bits are 0)
		- Example: $1010_2$ | $0011_2$ becomes $1011_2$
	- **Exclusive OR/XOR (^)**: XOR each bit in each corresponding position (1 if the bits are different, and 0 if the bits are the same)
		- Example: $1010_2$ ^ $0011_2$ becomes $1001_2$

### Why Apply Bitwise Operators?

- Each position shifted to the left with a binary number indicates multiplication by 2, and to the right indicates division by 2
- Shift operations are much more efficient than multiplication and division operations
- Bitwise AND operators may be used to clear bits (any bit with a 0 will lead to a result of 0)
- Bitwise OR may be used to set bits (any bit with a 1 will lead to a result of 1)
- XOR may be used to toggle bits (any bit with a 1 results in the negation of the bit)