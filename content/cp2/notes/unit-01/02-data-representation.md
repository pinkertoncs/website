---
title: "Lesson 02 - Data Representation"
---

## Review

- Please review the [Computers and Code](/cp1/notes/unit-01/02-computers-and-code/) notes from Programming 1

## References

- [Number Systems, Base Conversions, and Computer Data Representation](http://www.eecs.wsu.edu/~ee314/handouts/numsys.pdf)

## Number Systems

### Decimal (base-10)

- We use a base-10 number system
  - base 10 has 10 **digits** with the values 0-9
  - each position represents a power of 10
- Moving left from the **decimal point**
  - "Ones place"
      - $$10^0 = 1$$
  - "Tens place"
      - $$10^1 = 10$$
  - "Hundreds place"
      - $$10^2 = 100$$
  - etc...
- A number's value is given by the sum of (digit value * place value)
  - 1,234
    - $$1 \cdot 10^3 + 2 \cdot 10^2 + 3 \cdot 10^1 + 4 \cdot 10^0$$

### Binary (base-2)

- Binary is a base-2 number system
  - base-2 has 2 **bits** with the values 0 or 1
  - each position represents a power of 2
- Moving left from the **radix point**
  - $$2^0 = 1$$
  - $$2^1 = 2$$
  - $$2^2 = 4$$
  - $$2^3 = 8$$
  - etc...
- A number's value is given by the sum of (bit value * place value)
  - 1101
  - $$1 \cdot 2^3 + 1 \cdot 2^2 + 0 \cdot 2^1 + 1 \cdot 2^0$$
  - $$ 8 + 4 + 1 = 13$$

### Octal (base-8)

- Octal is a base-8 system

### Hexadecimal (base-16)

- Hexadecimal is a base-16 number system
  - there are 16 hex codes with decimal values 0-15
  - The values 10-15 are represented by using the letters A-F
  - each position represents a power of 16
- Hexadecimal is useful as a shorthand representation of binary, since each hex symbol can
represent **4 bits (one nibble)**. Two hex symbols can thus represent **8-bits (one bytes)**
- Moving left from the radix point
  - $$16^0 = 1$$
  - $$16^1 = 16$$
  - $$16^2 = 256$$
  - etc...
- A number's value is given by the sum of (hex code * place value)
  - 2E
  - $$2 \cdot 16^1 + 14 \cdot 16^0$$
  - $$32 + 14 = 46$$


## Conversions

### Decimal to binary

- For each bit, starting from the left
  - if the number is greater that or equal to the place value
      - set bit to 1
      - subtract the place value from the number
  - if the number is less than place value
      - set the bit to 0 and move on

- Consider the number 7
  - $$2^3 = 8$$
      - is 7 >= 8, no set bit to 0
  - $$2^2 = 4$$
      - is 7 >= 4, yes, set bit to 1, then subtract 4
  - $$2^1 = 2$$
      - is 3 >= 2, yes, set bit to 1 then subtract 2
  - $$2^0 = 1$$
      - is 1 >= 1, yes, set bit to 1, stop
- 7 is 0111 in binary

### Binary to Hex

- Break the binary string into groups of 4, starting from the right
- Convert each group to decimal and then to hex
- Examples
  - $$1011 \to 11 \to \mathrm{B}$$
  - $$0100\;1011 \to 4\;11 \to \mathrm{4B}$$
  - $$11\;1111 \to 3\;15 \to \mathrm{3F}$$




<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<script>
MathJax.Hub.Config({
    jax: ["input/TeX","output/HTML-CSS"],
    displayAlign: "left"
});
</script>
