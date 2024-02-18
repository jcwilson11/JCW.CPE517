# Decimal numbers
- the decimal system has 10 digits: 0 to 9
- you need two or more digits to represent a number greater than 9
- foe example. 23 needs the digit 2 and the digit 3; 2*10 + 3*1 = 23
- The decimal number system has a base 10
- from right to left, the position of a digit in a number represents a power of 10 10^5, 10^4, 10^3, 10^2, 10^1, 10^0
    - for example, decimal digit: 2     3
    -                   position: 10^1 10^0
    -                   value:    2*10^1 + 3*10^0 = 23

# Binary numbers
- the base 2 number system has base 2; only two digits: 0 and 1
- the value of digit is determined by its position in the number
- weight is based on powers of 2
    - example of a binary full number: 101
    - example of a binary fraction: 101.01 
- weight structure of a binary number is:
    - 2^5, 2^4, 2^3, 2^2, 2^1, 2^0, (binary point) 2^-1, 2^-2, 2^-3, 2^-4, 2^-5
- Ex1 convert 1101 to decimal
    - whole number: weights are 2^3, 2^2, 2^1, 2^0
    -                           8,   4,   2,   1
    -            binary digits: 1,   1,   0,   1
    -            value: 1*8 + 1*4 + 0*2 + 1*1 = 13
- Ex2 convert 10.111 to decimal
    - 2^1...2^-3 : 1*2 + 0*1 = 2
    - 1*0.5 + 1*.25 + 1*.125 = .875
    - value = 2.875

# Decimal to Binary Coversion
1. Sum of weights: convert decimal number to binary
2. repeated division by 2 method: use to convert a decimal whole number to binary
3. repeated multiplication by 2 method: used to convert decimal fraction to binary

## Sum of weights
- converting 9 to binary number
- weights: 64   32   16   8   4   2   1
- 8 and 1 are the only weights that add up to 9
- step one, find the largest weight that is less than or equal to the number
- step two, subtract the weight from the number
- step three, repeat steps one and two until the number is zero
- 9 - 8 = 1
- 1 - 1 = 0
- step four, plsce a 1 in the weights that were used and a 0 in the weights that were not used
- 64 32  16  8  4  2  1
- 0  0   0   1  0  0  1
- 9 in binary is 1001

### example 1: convert 25 to binary using sum of weights
25 -> 16 + 8 + 1
- 64 32  16  8  4  2  1
- 0  0   1   1  0  0  1
- 25 in binary is 11001
### example 2: convert 58 to binary using sum of weights
58 -> 32 + 16 + 8 + 2
- 64 32  16  8  4  2  1
- 0  1   1   1  0  1  0
- 58 in binary is 111010
### example 3: convert 0.625 to binary using sum of weights
- 0.5 0.25 0.125 0.0625
- 1   0    1     0
- 0.625 in binary is 0.101
### example 4: convert 0.75 to binary using sum of weights
- 0.5 0.25 0.125 0.0625
- 1   1    0     0
- 0.75 in binary is 0.11
### example 5: convert 0.125 to binary using sum of weights
- 0.5 0.25 0.125 0.0625
- 0   0    1     0
- 0.125 in binary is 0.001

# Binary arithmetic
## Addition
- four basic rules of binary addition
    - 0 + 0 = 0; sum = 0, carry = 0
    - 0 + 1 = 1; sum = 1, carry = 0
    - 1 + 0 = 1; sum = 1, carry = 0
    - 1 + 1 = 10; sum = 0, carry = 1
    - example: 1+1 = 10
    - example: 1+1+1 = 11

- ex1: 110 + 100
    - 110
    - 100
    - 1010
- ex2: 111 + 11
    - 111
    - 11
    - 1010

## Subtraction
- four basic rules of binary subtraction
    - 0 - 0 = 0; difference = 0, borrow = 0
    - 1 - 1 = 0; difference = 0, borrow = 0
    - 1 - 0 = 1; difference = 1, borrow = 0
    - 0 - 1 = 1; difference = 1, borrow = 1; 10-1 = 1
    - 11 - 01 = 10

- ex1: 101 - 011
    - 101
    - 011
    - 010
- ex2: 110 - 101
    - 110
    - 101
    - 001

