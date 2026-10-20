# CC 101 Activity 4: Number Systems Conversion — Paper Solutions

**Student Name:** Mart Sid D. De Venecia  
**Program & Section:** BSCS 1-1  
**Student ID:** 26117109 ($N = 109$)  

---

## 1. Binary to Decimal: $10011011_2$

| Bit Position ($2^n$) | $2^7$ | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Place Value** | $128$ | $64$ | $32$ | $16$ | $8$ | $4$ | $2$ | $1$ |
| **Binary Digit** | $1$ | $0$ | $0$ | $1$ | $1$ | $0$ | $1$ | $1$ |
| **Calculation** | $128 \times 1$ | $64 \times 0$ | $32 \times 0$ | $16 \times 1$ | $8 \times 1$ | $4 \times 0$ | $2 \times 1$ | $1 \times 1$ |
| **Product** | $128$ | $0$ | $0$ | $16$ | $8$ | $0$ | $2$ | $1$ |

$$128 + 0 + 0 + 16 + 8 + 0 + 2 + 1 = \mathbf{155_{10}}$$

---

## 2. Octal to Decimal: $2737_8$

| Digit Position ($8^n$) | $8^3$ | $8^2$ | $8^1$ | $8^0$ |
| :--- | :---: | :---: | :---: | :---: |
| **Place Value** | $512$ | $64$ | $8$ | $1$ |
| **Octal Digit** | $2$ | $7$ | $3$ | $7$ |
| **Calculation** | $512 \times 2$ | $64 \times 7$ | $8 \times 3$ | $1 \times 7$ |
| **Product** | $1024$ | $448$ | $24$ | $7$ |

$$1024 + 448 + 24 + 7 = \mathbf{1503_{10}}$$

---

## 3. Hexadecimal to Decimal: $\text{CCF}_{16}$

*Hexadecimal equivalents:* $\text{C} = 12$, $\text{F} = 15$

| Digit Position ($16^n$) | $16^2$ | $16^1$ | $16^0$ |
| :--- | :---: | :---: | :---: |
| **Place Value** | $256$ | $16$ | $1$ |
| **Hex Digit** | $\text{C}$ ($12$) | $\text{C}$ ($12$) | $\text{F}$ ($15$) |
| **Calculation** | $256 \times 12$ | $16 \times 12$ | $1 \times 15$ |
| **Product** | $3072$ | $192$ | $15$ |

$$3072 + 192 + 15 = \mathbf{3279_{10}}$$

---

## 4. Decimal to Binary: $112_{10}$

| Division by $2$ | Quotient ($Q$) | Remainder ($R$) |
| :--- | :---: | :---: |
| $112 \div 2$ | $56$ | $0$ |
| $56 \div 2$ | $28$ | $0$ |
| $28 \div 2$ | $14$ | $0$ |
| $14 \div 2$ | $7$ | $0$ |
| $7 \div 2$ | $3$ | $1$ |
| $3 \div 2$ | $1$ | $1$ |
| $1 \div 2$ | $0$ | $1$ |

*Reading remainders from bottom to top:*

$$112_{10} = \mathbf{1110000_2}$$

---

## 5. Decimal to Octal: $2315_{10}$

| Division by $8$ | Quotient ($Q$) | Remainder ($R$) |
| :--- | :---: | :---: |
| $2315 \div 8$ | $289$ | $3$ |
| $289 \div 8$ | $36$ | $1$ |
| $36 \div 8$ | $4$ | $4$ |
| $4 \div 8$ | $0$ | $4$ |

*Reading remainders from bottom to top:*

$$2315_{10} = \mathbf{4413_8}$$

---

## 6. Decimal to Hexadecimal: $1917_{10}$

| Division by $16$ | Quotient ($Q$) | Remainder ($R$) | Hex Digit |
| :--- | :---: | :---: | :---: |
| $1917 \div 16$ | $119$ | $13$ | $\text{D}$ |
| $119 \div 16$ | $7$ | $7$ | $7$ |
| $7 \div 16$ | $0$ | $7$ | $7$ |

*Reading remainders from bottom to top:*

$$1917_{10} = \mathbf{\text{77D}_{16}}$$

---

## 7. Binary to Hexadecimal: $1111100010_2$

*Group bits into sets of 4 from right to left (pad leftmost group with leading zeros):*

| 4-Bit Binary Group | `0011` | `1110` | `0010` |
| :--- | :---: | :---: | :---: |
| **Decimal Value** | $3$ | $14$ | $2$ |
| **Hexadecimal Digit** | $3$ | $\text{E}$ | $2$ |

$$1111100010_2 = \mathbf{\text{3E2}_{16}}$$

---

## 8. Binary to Octal: $1100111011_2$

*Group bits into sets of 3 from right to left (pad leftmost group with leading zeros):*

| 3-Bit Binary Group | `001` | `100` | `111` | `011` |
| :--- | :---: | :---: | :---: | :---: |
| **Octal Digit** | $1$ | $4$ | $7$ | $3$ |

$$1100111011_2 = \mathbf{1473_8}$$

---

## 9. Hexadecimal to Binary: $\text{F80}_{16}$

*Convert each hexadecimal digit into its 4-bit binary equivalent ($\text{F} = 15$):*

| Hexadecimal Digit | $\text{F}$ ($15$) | $8$ | $0$ |
| :--- | :---: | :---: | :---: |
| **4-Bit Binary** | `1111` | `1000` | `0000` |

$$\text{F80}_{16} = \mathbf{111110000000_2}$$

---

## 10. Octal to Hexadecimal: $522_8$

**Step 1: Convert Octal to 3-bit Binary**

| Octal Digit | $5$ | $2$ | $2$ |
| :--- | :---: | :---: | :---: |
| **3-Bit Binary** | `101` | `010` | `010` |

$$522_8 = 101010010_2$$

**Step 2: Regroup Binary into 4-bit Groups (from right to left)**

| 4-Bit Binary Group | `0001` | `0101` | `0010` |
| :--- | :---: | :---: | :---: |
| **Hexadecimal Digit** | $1$ | $5$ | $2$ |

$$522_8 = \mathbf{\text{152}_{16}}$$

---

## 11. IPv4 Address to Binary: `10.18.44.244`

*Convert each decimal octet into an 8-bit binary number:*

| Decimal Octet | $10$ | $18$ | $44$ | $244$ |
| :--- | :---: | :---: | :---: | :---: |
| **8-Bit Binary** | `00001010` | `00010010` | `00101100` | `11110100` |

**Result:** `00001010.00010010.00101100.11110100`

---

## 12. Color Code Conversions (Hexadecimal & RGB)

### a) Hex `#1AF110` to Decimal RGB
*Formula:* $(\text{First Hex Digit} \times 16) + \text{Second Hex Digit}$

* **Red ($\text{1A}_{16}$):** $(1 \times 16) + 10 = 16 + 10 = \mathbf{26}$
* **Green ($\text{F1}_{16}$):** $(15 \times 16) + 1 = 240 + 1 = \mathbf{241}$
* **Blue ($\text{10}_{16}$):** $(1 \times 16) + 0 = 16 + 0 = \mathbf{16}$

$$\text{Result: } \mathbf{\text{rgb}(26, 241, 16)}$$

### b) Decimal `rgb(130, 96, 220)` to Hexadecimal
*Formula:* $\text{Decimal} \div 16 \rightarrow \text{Quotient } (Q) \text{ is the first hex digit, Remainder } (R) \text{ is the second hex digit}$

| Channel | Decimal | Division by $16$ | Quotient ($Q$) | Remainder ($R$) | Hex Pair |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Red ($R$)** | $130$ | $130 \div 16$ | $8$ | $2$ | `82` |
| **Green ($G$)** | $96$ | $96 \div 16$ | $6$ | $0$ | `60` |
| **Blue ($B$)** | $220$ | $220 \div 16$ | $13$ ($\text{D}$) | $12$ ($\text{C}$) | `DC` |

$$\text{Result: } \mathbf{\#\text{8260DC}}$$

---

## 13. Unix / Linux File Permissions: `664`

| Permission Group | Owner | Group | Others |
| :--- | :---: | :---: | :---: |
| **Octal Digit** | $6$ | $6$ | $4$ |
| **3-Bit Binary** | `110` | `110` | `100` |
| **Symbolic (`rwx`)** | `rw-` | `rw-` | `r--` |

**Result:** `rw-rw-r--`

---

## 14. 4-Bit Unsigned Integer Limit

* **Total Values ($2^4$):** $2^4 = 16$ values ($0$ to $15$)
* **Largest Decimal:** $15_{10}$
* **Binary:** $1111_2$
* **Hexadecimal:** $\text{F}_{16}$

---

## 15. Student ID Number Conversion ($N = 109$)

### a) Decimal to Binary ($109_{10} \rightarrow \text{Base } 2$)

| Division by $2$ | Quotient ($Q$) | Remainder ($R$) |
| :--- | :---: | :---: |
| $109 \div 2$ | $54$ | $1$ |
| $54 \div 2$ | $27$ | $0$ |
| $27 \div 2$ | $13$ | $1$ |
| $13 \div 2$ | $6$ | $1$ |
| $6 \div 2$ | $3$ | $0$ |
| $3 \div 2$ | $1$ | $1$ |
| $1 \div 2$ | $0$ | $1$ |

$$\text{Binary: } \mathbf{1101101_2}$$

### b) Decimal to Octal ($109_{10} \rightarrow \text{Base } 8$)

| Division by $8$ | Quotient ($Q$) | Remainder ($R$) |
| :--- | :---: | :---: |
| $109 \div 8$ | $13$ | $5$ |
| $13 \div 8$ | $1$ | $5$ |
| $1 \div 8$ | $0$ | $1$ |

$$\text{Octal: } \mathbf{155_8}$$

### c) Decimal to Hexadecimal ($109_{10} \rightarrow \text{Base } 16$)

| Division by $16$ | Quotient ($Q$) | Remainder ($R$) | Hex Digit |
| :--- | :---: | :---: | :---: |
| $109 \div 16$ | $6$ | $13$ | $\text{D}$ |
| $6 \div 16$ | $0$ | $6$ | $6$ |

$$\text{Hexadecimal: } \mathbf{\text{6D}_{16}}$$