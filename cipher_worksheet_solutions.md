# Cryptography Worksheet Solutions

## Introduction to Cryptography

This worksheet covers fundamental concepts of cryptography including:
- Caesar Shift Cipher
- Modular Arithmetic
- Affine Ciphers
- Transposition Cipher

---

## Caesar Shift Cipher

### Problem 1: Encrypt THE QUICK BROWN FOX using Caesar Shift of 1

**Solution:**
- Original alphabet: ABCDEFGHIJKLMNOPQRSTUVWXYZ
- Shifted alphabet:  BCDEFGHIJKLMNOPQRSTUVWXYZA

**Step-by-step encryption:**
- T → U
- H → I
- E → F
- (space remains space)
- Q → R
- U → V
- I → J
- C → D
- K → L
- (space remains space)
- B → C
- R → S
- O → P
- W → X
- N → O
- (space remains space)
- F → G
- O → P
- X → Y

**Answer:** UIF RVJDL CSPXO GPY

### Problem 2: Encrypt MATH IS FUN using a Caesar Shift of 5

**Solution:**
- Original alphabet: ABCDEFGHIJKLMNOPQRSTUVWXYZ
- Shifted alphabet:  FGHIJKLMNOPQRSTUVWXYZABCDE

**Step-by-step encryption:**
- M → R
- A → F
- T → Y
- H → M
- (space remains space)
- I → N
- S → X
- (space remains space)
- F → K
- U → Z
- N → S

**Answer:** RFYM NX KZS

### Problem 3: Decrypt NBSI JT GVO using Caesar Shift of 1

**Solution:**
With shift of 1, to decrypt we shift backwards by 1:
- Original alphabet: ABCDEFGHIJKLMNOPQRSTUVWXYZ
- Shifted alphabet:  BCDEFGHIJKLMNOPQRSTUVWXYZA

**Step-by-step decryption:**
- N → M
- B → A
- S → R
- I → H
- (space remains space)
- J → I
- T → S
- (space remains space)
- G → F
- V → U
- O → N

**Answer:** MATH IS FUN

### Problem 4: Decrypt N QNPJ HNUMJWX (Break the cipher)

**Solution:**
To break this cipher, we try different shift values systematically:

**Testing different shifts:**
- Shift 1: M POMI GMZLIVW (not meaningful)
- Shift 2: L ONLH FLYKHAV (not meaningful)
- Shift 3: K NMKG EKXJGZU (not meaningful)
- Shift 4: J MLJF DJWIFYT (not meaningful)
- Shift 5: I LIKE CIPHERS ✓

**Answer:** The message is "I LIKE CIPHERS" with a Caesar shift of 5.

### Problem 5: What math are we using when encrypting and decrypting the Caesar Shift ciphers?

**Solution:**
We are using **modular arithmetic**. Specifically:
- For encryption: (original_position + shift) mod 26
- For decryption: (encrypted_position - shift) mod 26

The mod 26 operation ensures we "wrap around" the alphabet (A=0, B=1, ..., Z=25).

### Problem 6: How many different Caesar Shift ciphers are there?

**Solution:**
There are **25 different Caesar Shift ciphers**.

**Explanation:**
- We have 26 letters in the alphabet
- A shift of 0 doesn't change the message (not useful for encryption)
- A shift of 26 is the same as a shift of 0
- Therefore, we have shifts 1, 2, 3, ..., 25 = 25 different ciphers

### Problem 7: Alice's 50 different Caesar Shift ciphers

**Solution:**
Alice is **wrong** about having 26^50 different ways.

**Why Alice is wrong:**
- There are only 25 meaningful Caesar shifts (as calculated above)
- Even if using 50 different shifts, she's limited to these 25 possibilities
- The actual number of ways would be much smaller

**Why this is a bad idea:**
1. **Complexity without security**: Using multiple shifts doesn't significantly increase security
2. **Key management**: Difficult to remember and share 50 different shift values
3. **Error-prone**: High chance of making mistakes during encryption/decryption
4. **Still vulnerable**: Each individual shift is still easily breakable

### Final Thought: Should we use this cipher in modern times?

**Answer:** No, we should not use Caesar ciphers in modern times.

**Reasons:**
- **Easily breakable**: Only 25 possible keys to try
- **Frequency analysis**: Can be broken by analyzing letter frequencies
- **Computer power**: Modern computers can try all possibilities in milliseconds
- **Better alternatives**: Modern cryptography offers much stronger security

---

## Modular Arithmetic

### Problem 1: What is 51 (mod 4)?

**Solution:**
51 ÷ 4 = 12 remainder 3
51 = 4 × 12 + 3

**Answer:** 51 (mod 4) = 3

### Problem 2: What is (500 + 160) (mod 2)?

**Solution:**
500 + 160 = 660
660 ÷ 2 = 330 remainder 0
660 = 2 × 330 + 0

**Answer:** (500 + 160) (mod 2) = 0

### Problem 3: What are the only possible solutions for x (mod 4)?

**Solution:**
When working modulo 4, the remainder must be less than 4.

**Answer:** The possible solutions are: 0, 1, 2, 3

### Problem 4: In general, what are the possible solutions for x (mod n)?

**Solution:**
When working modulo n, the remainder must be less than n.

**Answer:** The possible solutions are: 0, 1, 2, 3, ..., (n-1)

### Problem 5: What is the multiplicative inverse of 5 (mod 7)?

**Solution:**
We need to find a number x such that 5x ≡ 1 (mod 7)

**Testing values:**
- 5 × 1 = 5 ≡ 5 (mod 7) ✗
- 5 × 2 = 10 ≡ 3 (mod 7) ✗
- 5 × 3 = 15 ≡ 1 (mod 7) ✓

**Answer:** The multiplicative inverse of 5 (mod 7) is 3

### Problem 6: What is the multiplicative inverse of 4 (mod 9)?

**Solution:**
We need to find a number x such that 4x ≡ 1 (mod 9)

**Testing values:**
- 4 × 1 = 4 ≡ 4 (mod 9) ✗
- 4 × 2 = 8 ≡ 8 (mod 9) ✗
- 4 × 3 = 12 ≡ 3 (mod 9) ✗
- 4 × 4 = 16 ≡ 7 (mod 9) ✗
- 4 × 5 = 20 ≡ 2 (mod 9) ✗
- 4 × 6 = 24 ≡ 6 (mod 9) ✗
- 4 × 7 = 28 ≡ 1 (mod 9) ✓

**Answer:** The multiplicative inverse of 4 (mod 9) is 7

### Problem 7: Does 2 have a multiplicative inverse (mod 4)?

**Solution:**
We need to find a number x such that 2x ≡ 1 (mod 4)

**Testing all possible values:**
- 2 × 0 = 0 ≡ 0 (mod 4) ✗
- 2 × 1 = 2 ≡ 2 (mod 4) ✗
- 2 × 2 = 4 ≡ 0 (mod 4) ✗
- 2 × 3 = 6 ≡ 2 (mod 4) ✗

**Answer:** No, 2 does not have a multiplicative inverse (mod 4)

### Problem 8: What types of numbers n have multiplicative inverses for every number in the set {1, 2, ..., n-1}?

**Solution:**
A number has a multiplicative inverse modulo n if and only if it is coprime to n (i.e., gcd(number, n) = 1).

For every number in {1, 2, ..., n-1} to have a multiplicative inverse modulo n, n must be coprime to all numbers from 1 to n-1.

**Answer:** Prime numbers. Only when n is prime do all numbers from 1 to n-1 have multiplicative inverses modulo n.

---

## Affine Ciphers

### Problem 1: Encrypt HELLO using x = 3, y = 1

**Solution:**
Formula: M = mx + y (mod 26)
Where A=0, B=1, C=2, ..., Z=25

**Step-by-step encryption:**
- H = 7: M = 7×3 + 1 = 22 (mod 26) = 22 → W
- E = 4: M = 4×3 + 1 = 13 (mod 26) = 13 → N
- L = 11: M = 11×3 + 1 = 34 (mod 26) = 8 → I
- L = 11: M = 11×3 + 1 = 34 (mod 26) = 8 → I
- O = 14: M = 14×3 + 1 = 43 (mod 26) = 17 → R

**Answer:** WNIIR

### Problem 2: Decrypt MCHX using x = 3, y = 2

**Solution:**
Formula: m = x^(-1)(M - y) (mod 26)
First, find the multiplicative inverse of 3 (mod 26):
3 × 9 = 27 ≡ 1 (mod 26), so 3^(-1) = 9

**Step-by-step decryption:**
- M = 12: m = 9×(12 - 2) = 9×10 = 90 ≡ 12 (mod 26) → M
- C = 2: m = 9×(2 - 2) = 9×0 = 0 ≡ 0 (mod 26) → A
- H = 7: m = 9×(7 - 2) = 9×5 = 45 ≡ 19 (mod 26) → T
- X = 23: m = 9×(23 - 2) = 9×21 = 189 ≡ 7 (mod 26) → H

**Answer:** MATH

### Problem 3: For what values of x can we use this encryption system?

**Solution:**
For the decryption step to work, we need the multiplicative inverse of x modulo 26 to exist.

This happens when gcd(x, 26) = 1.

Since 26 = 2 × 13, x must not be divisible by 2 or 13.

**Answer:** x must be coprime to 26. The valid values are: 1, 3, 5, 7, 9, 11, 15, 17, 19, 21, 23, 25 (12 values total)

### Problem 4: How many possible ciphers are there?

**Solution:**
- Valid values for x: 12 (from Problem 3)
- Valid values for y: 26 (any value from 0 to 25)
- Total combinations: 12 × 26 = 312

**Answer:** There are 312 possible Affine ciphers.

### Final Thought: Should we use this cipher today?

**Answer:** No, Affine ciphers should not be used in modern cryptography.

**Reasons:**
- **Limited keyspace**: Only 312 possible keys
- **Frequency analysis**: Still vulnerable to statistical attacks
- **Easy to break**: Modern computers can try all possibilities quickly
- **Pattern preservation**: Mathematical structure can be exploited

---

## Transposition Cipher

### Problem 1: Encrypt "BEWARE THE IDES OF MARCH" using length 5

**Solution:**
First, remove spaces: BEWARETHEIDESOFMARCH (20 letters)
Arrange in 5-column matrix:

```
B E W A R
E T H E I
D E S O F
M A R C H
```

Read by columns: BEDME ETEA WHSR AEOC RIFH

**Answer:** BEDME ETEA WHSR AEOC RIFH

### Problem 2: Decrypt "INLRREINVCFIIAOA" using length 4

**Solution:**
Message length: 16 letters
With length 4, we have 16 ÷ 4 = 4 rows

Arrange by columns:
```
I N L R
R E I N
V C F I
I A O A
```

Read by rows: INLR REIN VCFI IAOA

**Answer:** INLR REIN VCFI IAOA → "IN LARGE INOVATION" (likely "IN LARGE INNOVATION")

### Problem 3: Break the message "HYDAMAPOYPNZ"

**Solution:**
Message length: 12 letters
Try different matrix sizes:

**Try 2×6:**
```
H Y D A M A
P O Y P N Z
```
Read by rows: HYDAMA POYPNZ (not meaningful)

**Try 3×4:**
```
H Y D A
M A P O
Y P N Z
```
Read by rows: HYDA MAPO YPNZ (not meaningful)

**Try 4×3:**
```
H Y D
A M A
P O Y
P N Z
```
Read by rows: HYD AMA POY PNZ (not meaningful)

**Try 6×2:**
```
H Y
D A
M A
P O
Y P
N Z
```
Read by rows: HY DA MA PO YP NZ (not meaningful)

**Try reading columns differently for 3×4:**
```
H M Y (column 1)
Y A P (column 2)
D P N (column 3)
A O Z (column 4)
```
Read by rows: HMYAPDPNAOZ (not meaningful)

**Most likely solution with 4×3:**
Reading by rows: HAPPY MONDAY

**Answer:** HAPPY MONDAY

### Problem 4: If Eve intercepts a message with n letters, what techniques do you use to break it?

**Solution:**
**Techniques to break transposition ciphers:**

1. **Try all possible matrix dimensions**: For n letters, try all factor pairs of n
2. **Look for common words**: Search for patterns that form common English words
3. **Frequency analysis**: Check if the result has normal English letter frequencies
4. **Word spacing**: Try different ways to space the decoded text
5. **Anagram solving**: Use anagram solvers for shorter messages

**Answer:** Systematic trial of all possible matrix dimensions and pattern recognition

### Problem 5: How can you make your messages more secure?

**Solution:**
**Ways to improve transposition cipher security:**

1. **Use irregular matrices**: Don't fill the last row completely
2. **Multiple rounds**: Apply transposition multiple times
3. **Combine with substitution**: Use both transposition and substitution ciphers
4. **Random padding**: Add random letters to confuse analysis
5. **Variable block sizes**: Use different matrix sizes for different parts

**Answer:** Use multiple rounds, combine with other ciphers, and add randomness

### Problem 6: What are the maximum number of matrices you need to try to break a message?

**Solution:**
For a message of length n, you need to try all possible ways to arrange n letters in a rectangle.

This equals the number of divisor pairs of n.

**Example:** For n = 12, divisors are 1, 2, 3, 4, 6, 12
Possible matrices: 1×12, 2×6, 3×4, 4×3, 6×2, 12×1 = 6 matrices

**Answer:** The number of divisors of n (including both orientations)

### Final Thought: Should we use this cipher in modern day?

**Answer:** No, transposition ciphers alone should not be used in modern cryptography.

**Reasons:**
- **Limited security**: Vulnerable to systematic analysis
- **Frequency analysis**: Letter frequencies remain unchanged
- **Pattern recognition**: Modern computers can quickly try all possibilities
- **No key complexity**: Simple geometric transformations are easily broken

However, transposition concepts are still used as components in modern cryptographic algorithms.

---

## Bonus Problems

### Bonus Problem 1: Create and exchange encrypted messages

**Example Solution:**
**My cipher:** Caesar shift of 7
**Original message:** "MEET AT DAWN"
**Encrypted message:** "TLLA HA KHDU"

**Partner's challenge:** Try to decrypt this message without knowing the shift value!

### Bonus Problem 2: Create your own cipher

**My Custom Cipher: "Reverse Caesar"**

**How it works:**
1. Write the message backwards
2. Apply Caesar shift of 3
3. Insert random letter after every 2 characters

**Example:**
- Original: "HELLO"
- Reversed: "OLLEH"
- Caesar +3: "ROOHK"
- Add random letters: "ROXOKH"

**Decryption:**
1. Remove every 3rd character
2. Apply Caesar shift of -3
3. Reverse the result

**Partner's message to decrypt:** "ROXOKH"

---

## Summary

This worksheet covers fundamental cryptographic concepts that form the foundation of modern cryptography:

1. **Caesar Cipher**: Simple substitution with mathematical foundation
2. **Modular Arithmetic**: Essential mathematical tool for cryptography
3. **Affine Cipher**: Generalization using linear functions
4. **Transposition Cipher**: Rearrangement-based encryption

While these classical ciphers are not secure enough for modern use, they teach important principles that underlie contemporary cryptographic systems. 