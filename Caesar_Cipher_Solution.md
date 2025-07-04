# Caesar Cipher Worksheet Solution
## Information Security Assignment

### What is Caesar Cipher?
Caesar cipher is a simple encryption technique where each letter in the message is shifted by a fixed number of positions in the alphabet. It's named after Julius Caesar, who used it to protect his military messages.

**How it works:**
- **Encryption**: Shift each letter forward by the key number
- **Decryption**: Shift each letter backward by the key number
- **Example**: With key = 3, A becomes D, B becomes E, C becomes F, etc.

---

## Task Solutions

### Task 1: Decrypt with Key = 3
**Encrypted Message:** `Whfkqrfdpsv lv ehwwhu wkdq vfkrro zrun`

**Complete step-by-step decryption:**
- W → T (shift back 3 positions)
- h → e
- f → c
- k → h
- q → n
- r → o
- f → c
- d → a
- p → m
- s → p
- v → s
- (space) → (space)
- l → i
- v → s
- (space) → (space)
- e → b
- h → e
- w → t
- w → t
- h → e
- u → r
- (space) → (space)
- w → t
- k → h
- d → a
- q → n
- (space) → (space)
- v → s
- f → c
- k → h
- r → o
- r → o
- o → l
- (space) → (space)
- z → w
- r → o
- u → r
- n → k

**Decrypted Message:** `Technocamps is better than school work`

---

### Task 2: Decrypt with Key = 3
**Encrypted Message:** `Brx'uh jrqqd qhhg d eljjhu erdw`

**Complete step-by-step decryption:**
- B → Y (shift back 3 positions)
- r → o
- x → u
- ' → ' (punctuation stays the same)
- u → r
- h → e
- (space) → (space)
- j → g
- r → o
- q → n
- q → n
- d → a
- (space) → (space)
- q → n
- h → e
- h → e
- g → d
- (space) → (space)
- d → a
- (space) → (space)
- e → b
- l → i
- j → g
- j → g
- h → e
- u → r
- (space) → (space)
- e → b
- r → o
- d → a
- w → t

**Decrypted Message:** `You're gonna need a bigger boat`

---

### Task 3: Decrypt with Key = 9
**Encrypted Message:** `Cxcx r'en j onnurwp fn'an wxc rw tjwbjb jwhvxan`

**Complete step-by-step decryption:**
- C → T (shift back 9 positions)
- x → o
- c → t
- x → o
- (space) → (space)
- r → i
- ' → ' (punctuation stays the same)
- e → v
- n → e
- (space) → (space)
- j → a
- (space) → (space)
- o → f
- n → e
- n → e
- u → l
- r → i
- w → n
- p → g
- (space) → (space)
- f → w
- n → e
- ' → ' (punctuation stays the same)
- a → r
- n → e
- (space) → (space)
- w → n
- x → o
- c → t
- (space) → (space)
- r → i
- w → n
- (space) → (space)
- t → k
- j → a
- w → n
- b → s
- j → a
- b → s
- (space) → (space)
- j → a
- w → n
- h → y
- v → m
- x → o
- a → r
- n → e

**Decrypted Message:** `Toto i've a feeling we're not in kansas anymore`

---

### Task 4: Decrypt with Key = 21
**Encrypted Message:** `Yj jm yj ijo. Oczmz dn ij omt`

**Complete step-by-step decryption:**
- Y → D (shift back 21 positions)
- j → o
- (space) → (space)
- j → o
- m → r
- (space) → (space)
- y → d
- j → o
- (space) → (space)
- i → n
- j → o
- o → t
- . → . (punctuation stays the same)
- (space) → (space)
- O → T (shift back 21 positions)
- c → h
- z → e
- m → r
- z → e
- (space) → (space)
- d → i
- n → s
- (space) → (space)
- i → n
- j → o
- (space) → (space)
- o → t
- m → r
- t → y

**Decrypted Message:** `Do or do not. There is no try`

---

### Task 5: Decrypt WITHOUT Given Key (Advanced)
**Encrypted Message:** `Z druv r gifdzjv di wifuf. R gifdzjv. "Ufe'k pfl cvrmv yzd jrdnzjv xrdxvv" reu z ufe'k dvre kf`

**How to solve without a key:**
1. **Look for patterns**: Single letters like "Z" and "R" are likely "I" and "A"
2. **Try frequency analysis**: Most common letters in English are E, T, A, O, I, N
3. **Test different keys**: Try keys 1-25 systematically
4. **Look for common words**: "the", "and", "are", "for", "not"

**Solution process:**
- Single letter "Z" appears twice - likely "I" 
- Single letter "R" appears once - likely "A"
- If Z = I, then shift = 17 (Z is position 26, I is position 9, difference = 17)
- Testing key = 17...

**Complete step-by-step decryption with Key = 17:**
- Z → I (shift back 17 positions)
- (space) → (space)
- d → m
- r → a
- u → d
- v → e
- (space) → (space)
- r → a
- (space) → (space)
- g → p
- i → r
- f → o
- d → m
- z → i
- j → s
- v → e
- (space) → (space)
- d → t
- i → o
- (space) → (space)
- w → f
- i → r
- f → o
- u → d
- f → o
- . → . (punctuation stays the same)
- (space) → (space)
- R → A (shift back 17 positions)
- (space) → (space)
- g → p
- i → r
- f → o
- d → m
- z → i
- j → s
- v → e
- . → . (punctuation stays the same)
- (space) → (space)
- " → " (punctuation stays the same)
- U → D (shift back 17 positions)
- f → o
- e → n
- ' → ' (punctuation stays the same)
- k → t
- (space) → (space)
- p → y
- f → o
- l → u
- (space) → (space)
- c → l
- v → e
- r → a
- m → v
- v → e
- (space) → (space)
- y → h
- z → i
- d → m
- (space) → (space)
- j → s
- r → a
- d → m
- n → w
- z → i
- j → s
- v → e
- (space) → (space)
- x → g
- r → a
- d → m
- x → g
- v → e
- v → e
- " → " (punctuation stays the same)
- (space) → (space)
- r → a
- e → n
- u → d
- (space) → (space)
- z → i
- (space) → (space)
- u → d
- f → o
- e → n
- ' → ' (punctuation stays the same)
- k → t
- (space) → (space)
- d → m
- v → e
- r → a
- e → n
- (space) → (space)
- k → t
- f → o

**Decrypted Message:** `I made a promise to frodo. A promise. "Don't you leave him samwise gamgee" and i don't mean to`

---

### Extension Task: Create Your Own Message
**My chosen key:** `8`

**Original Message:** `Meet me at the library after school`

**Complete encryption process:**
- M → U (shift forward 8 positions)
- e → m
- e → m
- t → b
- (space) → (space)
- m → u
- e → m
- (space) → (space)
- a → i
- t → b
- (space) → (space)
- t → b
- h → p
- e → m
- (space) → (space)
- l → t
- i → q
- b → j
- r → z
- a → i
- r → z
- y → g
- (space) → (space)
- a → i
- f → n
- t → b
- e → m
- r → z
- (space) → (space)
- s → a
- c → k
- h → p
- o → w
- o → w
- l → t

**Encrypted Message:** `Umml um il bpm tojtizg ijlmz kknwwt`

---

## Summary of Techniques Used

### 1. **Direct Decryption (When Key is Given)**
- Simply shift each letter backward by the key number
- Keep punctuation and spaces unchanged
- Wrap around the alphabet (A comes after Z when going backward)

### 2. **Frequency Analysis (When Key is Unknown)**
- Look for single letters (usually A or I)
- Check for common short words (the, and, are)
- Try different keys systematically
- Look for recognizable patterns or phrases

### 3. **Tips for Beginners**
- Always work letter by letter
- Keep track of your alphabet positions
- Remember: A=1, B=2, C=3, ..., Z=26
- When going backward, if you get a negative number, add 26
- Practice with simple messages first

---

## Why Caesar Cipher is Important in Information Security

1. **Historical significance**: One of the first encryption methods
2. **Educational value**: Teaches basic cryptography concepts
3. **Foundation knowledge**: Understanding simple ciphers helps learn complex ones
4. **Security awareness**: Shows how easily simple encryption can be broken

**Note**: Caesar cipher is NOT secure for real-world use today because:
- Only 25 possible keys (easy to brute force)
- Vulnerable to frequency analysis
- Pattern recognition makes it breakable
- Modern computers can crack it instantly

---

*This solution demonstrates the basics of cryptanalysis (code-breaking) which is fundamental to information security.* 