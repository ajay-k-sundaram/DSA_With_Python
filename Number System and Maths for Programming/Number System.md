## Number System
Base 2 (Binary Number System)
	```0 and 1```
 
Base 10 (Decimal Number System)
	```0 , 1, 2, 3, 4, 5, 6, 7, 8, 9```
 
Base 8 (Octal Number System)
	```0, 1, 2, 3, 4, 5, 6, 7```
 
Base 16 (Hexa-Decimal Number System)
	```0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F```

Number Conversion : It can be done by taking LCM with its base and merging the reminder on reverse.

Example :

```
1. 85 is in decimal number system and convert it to binary.

		2 | 85 |
		-----------
		2  | 42 | 1
		------------
		2  | 21 | 0
		------------
		2  | 10 | 1
		------------
		2  | 5  | 0
		------------
		2  | 2  | 1
		------------
		     1
		     
		So the binary value of 85 is 110101
		
2. 17 is in decimal number system and convert it to octal

		8 | 17 |
		-----------
		8 |  2  | 1
		-----------
		So the octal value of 17 is 21

3. 1001 is a binary digit convert it to decimal

	Multiply and add the power of the base with digits
	
	1 * (2^3) + 0 * (2^2) + 0 * (2^1) + 1 * (2^0) = 9

4. 30 is in Octal number system convert it to decimal

	3 * (8^1) + 0 * (8^0) = 24

5. 1A is in Hexa Decimal and convert it to decimal

	1 * (16^1) + 10 * (16^0) = 26

6. 78 is in Decimal and convert it to Hexa-Decimal

	16 | 78 |
	------------
	16 | 4  | 14 (E)
	------------
		 0    4
	So the hexa decimal value of 78 is 04E == 4E
		
```

## Negative Binary Numbers

![Alt text](https://github.com/ajay-k-sundaram/Notes-for-Computer-Science/blob/master/Number%20System%20and%20Maths%20for%20Programming/Resources/MSB%20and%20LSB.png?raw=true)

Example :
```
1. Take 12 and make it negative 12

	12 in binary is 1100
	In 8 bit it is 00001100

	a = 00001100
	!a = 11110011
	
	x = !a + 1 
		11110011
	   +       1
	   ----------
		11110100

	Note :
		# This is called 2's complement method.
		
		# lets take a number 16 whose binary conversion is 10000 
			what if it is needs to be accomodated in 4 bits ? it can't 
			because 16 needs 5 bits but we can solve this mathematically
			16 = 15 + 1
			   = 1111 + 0001

2. Range of Numbers

	1 byte can store 256 combination of numbers. Which is because 1 byte has 8 bits and each bit can store either 0 or 1 so 2^8 = 256
	but the actual numbers which can be stored is only in 7 bits, that's because MSB is for positive or negative. So 2^7 = 128 
	128 * 2 = 256 [128 numbers in +ve and 128 numbers in -ve]
But from -128 to 128 there are 257 numbers thats because these are integers so it has 0 in the middle.
	let's take it as -128 to 127 because -0 is a +ve number 

	a = 00000000
	!a = 11111111
	x = !a + 1

	 11111111
	+       1
	----------
	100000000

	since it has 8 bits we can neglect 1 in the last bit so negative of 0 is 0

	Algorithm to find the range of numbers with 1 byte memory
		(-2^(n-1)) to (2^(n-1) -1)

	
```


Size of integer is 4bytes which is 32 bits. In that MSB is the reserved to determine weather the integer is negative or positive.
## Bitwise Operators

```
and (&)

	a | b | a and b
	------|--------
	0 | 1 |    0
	1 | 0 |    0
	1 | 1 |    1
	0 | 0 |    0
	T | F |    F
	F | T |    F
	F | F |    F
	T | T |    T

	Note :
		While and with 1 the digits remains same
				1 0 1 0 0 1 0 1
			and 1 1 1 1 1 1 1 1 
			---------------------
				1 0 1 0 0 1 0 1
or (|)

	a | b | a or b
	------|--------
	0 | 1 |   1
	1 | 0 |   1
	1 | 1 |   1
	0 | 0 |   0
	T | F |   T
	F | T |   T
	F | F |   F
	T | T |   T
	
xor (^) Exclusive or

	a | b | a or b
	------|--------
	0 | 1 |   1
	1 | 0 |   1
	1 | 1 |   0
	0 | 0 |   0
	T | F |   T
	F | T |   T
	F | F |   F
	T | T |   F

	Note :
		# xor a number with 1 will gives the compliment of it
			0 xor 1 = 1
			F xor T = T
		# xor a number with 0 will gives the same number
			1 xor 0 = 1
			T xor F = T
		# xor a number with same number will give 0
			1 xor 1 = 0

complement (~)

	It gives opposite
	1 ~ = 0
	0 ~ = 1
	T ~ = F
	F ~ = T

left shift (<<)

	It shifts the digit to its left side

	12 in decimal 1100
	12 << 1 = 11000
	= 24

	Note :
		# Left shifting any number with 1 will double the number
		   x << 1 = 2x
		# Left shifting x with y will give x + 2^y
		   x << y == x + 2^y
		   5 << 6 == 5 + 2^6 = 69

Right shift (>>)

	It shifts the digit to its right side

	1010101 >> 1 = 101010

	Note :
		# x >> y = x / (2^y)
```

## Problems

1. Find 171 is odd or Even
2. Find the unique number in the given array `[5, 2, 3, 1, 5, 3, 1]` the array has repeated numbers in even times.
3. Find the unique number in the given array `[5, 2, 3, 5, 1, 2, 3, 5, 2, 3]` the array has repeated numbers in odd times.
4. All the numbers in the array will have negative of that number and positive of that number except one find what it is? `[5, 2, 3, -3, 6, -5, -2]`
5. Find the ith bit of a number is zero or one. 01011011 and the i is 6
6. Set the ith bit to its complement. 01011011 and the i is 7
7. Find the position of the right most set bit 01011000. 
