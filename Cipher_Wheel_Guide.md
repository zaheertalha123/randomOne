# Cipher Wheel Guide
## How to Use Caesar Cipher Wheels

### Understanding the Cipher Wheels

From the images provided, we can see two types of cipher wheels:

1. **Numbered Cipher Wheel**: Has letters A-Z on the outer ring and numbers 0-25 on the inner ring
2. **Letter-Only Cipher Wheel**: Has only letters A-Z arranged in a circle

### How Cipher Wheels Work

A cipher wheel is a mechanical tool that makes Caesar cipher encryption and decryption easier by providing a visual reference for letter shifts.

#### **Basic Principle:**
- The **outer ring** contains the **plaintext** alphabet (normal letters)
- The **inner ring** contains the **ciphertext** alphabet (shifted letters)
- By rotating the inner ring, you can set different keys (shift values)

---

## Using the Numbered Cipher Wheel

### **For Encryption:**

1. **Set your key**: Rotate the inner ring so that the number corresponding to your key aligns with letter A on the outer ring
   - Example: For key = 3, align number 3 with letter A

2. **Encrypt each letter**: 
   - Find your plaintext letter on the outer ring
   - Read the corresponding number on the inner ring
   - Convert that number back to a letter (A=0, B=1, C=2, etc.)

### **For Decryption:**

1. **Set your key**: Same as encryption - align the key number with letter A
2. **Decrypt each letter**:
   - Find your ciphertext letter on the outer ring
   - Read the corresponding number on the inner ring
   - Subtract the key value from this number
   - Convert the result back to a letter

---

## Using the Letter-Only Cipher Wheel

### **For Encryption:**

1. **Set your key**: Rotate the inner ring so that the letter that is 'key positions' after A aligns with letter A on the outer ring
   - Example: For key = 3, align letter D with letter A (A→B→C→D = 3 shifts)

2. **Encrypt each letter**:
   - Find your plaintext letter on the outer ring
   - Read the corresponding letter directly below it on the inner ring

### **For Decryption:**

1. **Set your key**: Same as encryption setup
2. **Decrypt each letter**:
   - Find your ciphertext letter on the inner ring
   - Read the corresponding letter directly above it on the outer ring

---

## Practical Examples Using the Cipher Wheels

### **Example 1: Encrypt "HELLO" with Key = 3**

**Setup**: Align D (3 positions from A) with A on outer ring, or align number 3 with A.

**Encryption Process**:
- H (outer) → K (inner) 
- E (outer) → H (inner)
- L (outer) → O (inner)
- L (outer) → O (inner)
- O (outer) → R (inner)

**Result**: "HELLO" becomes "KHOOR"

### **Example 2: Decrypt "KHOOR" with Key = 3**

**Setup**: Same alignment as encryption

**Decryption Process**:
- K (inner) → H (outer)
- H (inner) → E (outer)
- O (inner) → L (outer)
- O (inner) → L (outer)
- R (inner) → O (outer)

**Result**: "KHOOR" becomes "HELLO"

---

## Step-by-Step Instructions for Each Worksheet Task

### **Task 1: "Whfkqrfdpsv lv ehwwhu wkdq vfkrro zrun" (Key = 3)**

**Cipher Wheel Setup**:
1. Align number 3 with letter A (or align D with A)
2. For each encrypted letter, find it on the outer ring and read the inner ring
3. Subtract 3 from the position value to get the original letter

**Using the wheel to decrypt**:
- W (outer) → find position 22 → subtract 3 → position 19 → T
- h (outer) → find position 7 → subtract 3 → position 4 → e
- f (outer) → find position 5 → subtract 3 → position 2 → c
- Continue this process...

### **Task 2: "Brx'uh jrqqd qhhg d eljjhu erdw" (Key = 3)**

**Same setup as Task 1**
- B → position 1 → subtract 3 → position 24 (wrapping around) → Y
- r → position 17 → subtract 3 → position 14 → o
- x → position 23 → subtract 3 → position 20 → u
- Continue...

### **Task 3: Key = 9**

**Cipher Wheel Setup**:
1. Align number 9 with letter A (or align J with A)
2. Apply the same process with 9-position shifts

### **Task 4: Key = 21**

**Cipher Wheel Setup**:
1. Align number 21 with letter A (or align V with A)
2. Apply the same process with 21-position shifts

---

## Advantages of Using Cipher Wheels

1. **Visual Reference**: Easy to see letter relationships
2. **Reduced Errors**: Less mental math required
3. **Quick Setup**: Once aligned, encryption/decryption is straightforward
4. **Educational**: Helps understand the shifting concept visually
5. **Reusable**: Can be used for any Caesar cipher key

---

## Creating Your Own Cipher Wheel

### **Materials Needed**:
- Two circular pieces of cardboard/paper
- Brad fastener or pin
- Ruler and compass
- Marker

### **Steps**:
1. **Create outer ring**: Draw a large circle and divide into 26 equal sections
2. **Label outer ring**: Write A-Z in alphabetical order
3. **Create inner ring**: Draw a smaller circle and divide into 26 equal sections
4. **Label inner ring**: Write A-Z in alphabetical order
5. **Assemble**: Attach with brad fastener in the center
6. **Optional**: Add numbers 0-25 for easier reference

---

## Security Note

While cipher wheels make Caesar ciphers easier to use, remember that Caesar ciphers are:
- **Easily breakable** with modern computers
- **Vulnerable** to frequency analysis
- **Not secure** for real-world applications
- **Educational tools** for learning cryptography basics

The cipher wheel is an excellent learning tool for understanding substitution ciphers and the foundations of cryptography!

---

*This guide demonstrates how to use cipher wheels effectively for Caesar cipher encryption and decryption, making the process more visual and less error-prone.* 