# Truth table


A truth table is used in logic to presents the values of logical expressions for each of their arguments.

## Unary operations
4 unary operations:
- Logical false (unary falsum): the output value is always false
- Logical negation (unary negation): the output is the opposite of input.
- Logical identity (unary identity): the output value is the same as input.
- Logical true: the output value is always true

p|F|N|I|T
-|-|-|-|-
1|0|0|1|1
0|0|1|0|1


## Binary operations
16 possible truth functions of two binary variables

1|2|3|4|#|  op
-|-|-|-|-|-----------
⊤|⊤|⊥|⊥| | p
⊤|⊥|⊤|⊥| | q
o|o|o|o|0| ⊥
o|o|o|x|1| p ↓ q ≡ ¬(p ∨ q) ≡ ¬p ∧ ¬q
o|o|x|o|2| ¬(q → p) ≡ q ∧ ¬p
o|o|x|x|3| ¬p
o|x|o|o|4| ¬(p → q) ≡ p ∧ ¬q
o|x|o|x|5| ¬q
o|x|x|o|6| p ⊕ q ≡ ¬(p ↔ q)
o|x|x|x|7| p ↑ q ≡ ¬(p ∧ q) ≡ ¬p ∨ ¬q
x|o|o|o|8| p ∧ q
x|o|o|x|9| p ↔ q ≡ ¬(p⊕q)
x|o|x|o|a| q
x|o|x|x|b| p → q ≡ ¬p ∨ q
x|x|o|o|c| p
x|x|o|x|d| q → p ≡ ¬q ∨ p
x|x|x|o|e| p ∨ q
x|x|x|x|f| ⊤


¬(p ∧ q) ≡ ¬p ∨ ¬q
¬(p ∨ q) ≡ ¬p ∧ ¬q
¬(p → q) ≡  p ∧ ¬q
¬(p ↔ q) ≡  p ⊕ q  ≡ (p ∧ ¬q) ∨ (¬p ∧ q)



p|q|⊥| ↓ |¬← |¬p|¬→ |¬q|^|↑  |∧  |↔|q|→  |p|←  |∨  |⊤
-|-|-|---|---|--|---|--|-|---|---|-|-|---|-|---|---|-
1|1|0| 0 |0  |0 |0  |0 |0|`0`|`1`|1|1|1  |1|1  |1  |1
1|0|0| 0 |0  |0 |`1`|1 |1|1  |0  |0|0|`0`|1|1  |1  |1
0|1|0| 0 |`1`|1 |0  |0 |1|1  |0  |0|1|1  |0|`0`|1  |1
0|0|0|`1`|0  |1 |0  |1 |0|1  |0  |1|0|1  |0|1  |`0`|1


---

0|1  |2  |3 |4  |5 |6|7  |8  |9|a|b  |c|d  |e  |f
-|---|---|--|---|--|-|---|---|-|-|---|-|---|---|-
0|0  |0  |0 |0  |0 |0|`0`|`1`|1|1|1  |1|1  |1  |1
0|0  |0  |0 |`1`|1 |1|1  |0  |0|0|`0`|1|1  |1  |1
0|0  |`1`|1 |0  |0 |1|1  |0  |0|1|1  |0|`0`|1  |1
0|`1`|0  |1 |0  |1 |0|1  |0  |1|0|1  |0|1  |`0`|1
⊥|↓  |¬← |¬p|¬→ |¬q|^|↑  |∧  |↔|q|→  |p|←  |∨  |⊤


- NAND (7) p ↑ q ≡ ¬(p ∧ q)
- OR       p ∨ q
- NOR  (1) p ↓ q ≡ ¬(p ∨ q)
- XOR    p ⊕ q
- XNOR ¬(p ⊕ q)



NOT   = ¬
AND   = ∧
NAND  = ↑ = ¬(p ∧ q)
OR    = ∨
NOR   = ↓
IMPLY = →
IFF   = ↔ =  (p → q) ∧ (q → p)
XOR   = ^ =  (p ∨ q) ∧ ¬(p ∧ q) = ⊕
XNOR  = 

∨ ∧ ¬ → ← ↔ ⊕ ↓ ↑

p|q|r|p∧q|p∨q|p→q|
-|-|-|-|-|-|
1|1|1|1|0|0|
1|1|0| | |0|
1|0|1|0|1|0|
1|0|0| | |0|
0|1|1|0|1|0|
0|1|0| | |0|
0|0|1|0|1|0|
0|0|0| | |0|
