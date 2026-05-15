---
tags: ENEE_244
created: 2026-1-31
description: 1/28, 2/2 notes (Slide set 2)
---

### Bits and combinations in binary numbers

A single binary digit in a computer is called a bit.

A collection of $n$ bits encodes $2^n$ combinations. These combinations can be used to represent different pieces of information (numbers, etc.).

To encode $k$ combinations, we need $\lceil \log_2 k \rceil$ bits.

### BCD codes

Some digital systems store numbers in decimal code with binary combinations representing decimal digits. The most common one is **binary coded decimal** (BCD), in which each decimal digit is represented in 4 bits ($\lceil \log_2(10) \rceil$). A common type of BCD code is the **8421 code**.

Advantage of the 8421 code:
- No conversion required for human interface, so useful for small electronics with screen such as an alarm clock or digital thermostat (but not used in CPUs)

Disadvantages of the 8421 code:
- Unused combinations lead to loss of range (for example, 16 bits in binary is 65536 combination, but there are only 10000 in decimal code)
- Diminished complement (9's complement) cannot be computed by bit-flipping, so subtraction is harder
- Simple binary arithmetic circuits cannot be used; decimal circuits are larger

### Self-complementing BCD codes

There are other decimal codes in which a bit-flip *does* yield the 9's complement.

- **2421 code**
	- Digits have weights of 2, 4, 2, 1 respectively
		- More than one way of encoding any single number (meaning 0101 and 1011, for example, are both 5)
		- Just choose one
	- Advantage: self-complementing (bit-flip gives 9's complement)
		- For example, flipping the bits of 1011 (which is 5 in decimal) will get 0100, which is 4 in 2421 code and is also 9's complement of 5 ($9 - 5 = 4$)
- **Excess 3 code**
	- Represent digit $i$ by $i + 3$
		- For example, 0 is 0011 in excess-3, which represents 3 ($0 + 3$) in decimal, and 1 is 0100, which is 4 ($1 + 3$) in decimal
	- NOT a weighted code (unlike 8421 and 2421, which have individual weights for digits)
	- Self-complementing
		- For example, flipping the bits of 1001 (which is 6 in decimal) will get 0110, which is 3 in decimal, and is also 9's complement of 6 ($9 - 6 = 3$)

### Unit distance coding to fix transient errors

This is a type of binary coding in which only one bit changes between successive numbers (for example, the **Gray code**).

Advantage:
- If up-down counting is common, transient states may occur if all the bits don't change at the same time (this means that between changing from one decimal number to the next, we may temporarily get a completely different decimal number by incrementing bits)
	- This is not a problem for synchronous (clocked) circuits
	- Unit-distance codes are especially useful when sensing an analog quantity that changes only incrementally, and representing it in digital.
- Power dissipation is less than other codes, because a component of dynamic power is dissipated when bits flip in circuits

These are used only rarely in special-purpose circuits, and not in CPUs.

### Alphanumeric codes

**Alphanumeric codes** are used to represent alphabets, numbers, special characters on keyboard and monitors. The most common is **ASCII** (American Standard Code for Information Interchange).

ASCII is a 7-bit code coding 128 characters, with uppercase and lowercase characters both included. 'A' is 65 in ASCII, while 'a' is 97, and the remaining letters follow a sequence from these points.

8 bits make a byte, so additional bit can be used for other reasons:
- Unused
- Other symbols
- Parity bits in communication

More recently, the 16-bit Unicode character set has been developed, which encodes English, foreign characters, and a variety of symbols.

### Error detection codes

Sometimes, errors may occur in transmission across a noisy medium. We would like to detect if a received quantity is corrupted. This is possible with **error detection codes**.

If the received quantity is corrupted, then request a re-transmission.

For binary numbers: Add an extra bit to the data word being transmitted, called a **parity bit**.

We can have an odd or even parity:
- Odd parity: Add bit that makes \# of 1's odd before transmission
- Even parity: Add bit that makes \# of 1's even before transmission ^55455f

If the number of 1's in the data bits + the parity bit is even, then the even parity is 1. If it's odd, then the odd parity is 1.

If there are an odd number of 1's in the transmission, then the even parity is 1 while the odd parity is 0. If there are an even number of 1's in the transmission, then the even parity is 0 while the odd parity is 1.

Then the data word along with the parity bit is transmitted.

### Error check with parity bit codes

Upon receipt, if computed parity bit at the destination is not equal to the received parity bit from the medium, then an error is detected.

A single parity bit works only for 1-bit errors.

This is possible for data words of any length.

On error, a retransmit is requested.