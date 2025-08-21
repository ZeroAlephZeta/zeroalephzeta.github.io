---
date: 14-8-25
duration: 2 hr
prev: "[[FCP day 6]]"
next: "[[FCP day 8]]"
---
#### Signed and unsigned integers
Integers are stored in 8-bit, 16-bit, and 32-bit sizes. If it is *signed*, it is stored with one less bit and the leftmost bit is used for the sign, using `0` for positive numbers and `1` for negative numbers. C by default makes `int` signed. It could be changed to the unsigned ones by declaring the variables as `unsigned int`.   
- The `int` type has 32 bits. 
- The `short` and `long` specifiers are kind of useless, except when extra effort is required for too large values or maybe too fast calculations. 
- There are even more useless `long long int` and `unsigned long long int` take it to 64-bit stuff.
- **Standard signed integer types:** `int`, `short`, `long`, `long long`.
- **Standard unsigned integer types:** `unsigned int`, `unsigned short`, `unsigned long`, `unsigned long long`, `_Bool`.

#### Octal and hexadecimal
- Decimal constants contain digits `0-9` but cannot start with a `0`.
- Octals **must** start with a `0`.
- Hexadecimals start with `0x`.

#### Conversion specifiers
After the `%`,
**Unsigned**
- Decimal takes `d`,
- Octal takes `o`,
- Hexadecimal takes `x`.
**Signed**
some `hd`, `ld`, `lld` business I missed.

#### Floats
The `float` memory comes in single precision `32-bit` and double precision `64-bit`formats. 
- Single precision has `1` sign bit, `8` exponent bits but one digit is used for some NAN or something, and `23` fraction bits. Highest value is around `10^38`.
- Double precision has `1` sign bit, `15` exponents and `48` fraction bits. 

EVERYTHING CRASHED
