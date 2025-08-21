---
date: 31-7-25
duration: 2 hr
prev: "[[FCP day 2]]"
next: "[[FCP day 4]]"
---
## The `printf` function
The `printf()` function comes with a *format string* which contains the main things to be printed and all the things to be replaced by the values are also included inside it.
The `%` sign is the *conversion specification* and it comes with a *format specifier* `d` or `f`. Mistakes and mismatches in the correspondence between conversion specifications and format specifiers lead to garbage errors and all the usual machine stuff.

The general format of a conversion specifier is `%m.pX` where `X` is the format specifier. The `p` is called the *precision*, and `m` is the minimum field width. There are specifiers other than `d` and `f` as well, such as `e` and `g`. The `e` is the exponential format. There are `p` digits **shown** after the decimal point. The `f` is the fixed length specifier or something. 

**READ THIS PART OF THE BOOK BECAUSE TOO SLEEPY IN CLASS TO TAKE GOOD NOTES. CHAPTER 3 BEGINNING.**

#### Escape sequences
Escape sequences include `\a` (now allegedly obsolete). The `\b` character gives a backspace to the thing already printed. And `\n` and `\t` are new line and horizontal tab respectively. Now to print a `"` character, it does not behave like normal character. One has to give the command `\"` for it to print like a normal character. You print `\` by typing in `\\`.

## The `scanf` function
The `scanf()` takes input from the user and it also has a lot of inputs etc. **READ THE BOOK.**.
