# fitch style proofs: my tinkering

```
01  (P > Q)           Premise
02  . P                 Assumption
03  . . A                 Assumption
04  . . Q                 1,2  >E
05  . (A > Q)           3-4  >I
06  (P > (A > Q))     2-5  >I
```



Indentation:

```
(¬q → ¬p) → (p → r)                 Premise
    (¬q → ¬p) → (p → r)               Assumption1
        (¬q → ¬p) → (p → r)             Assumption2
            (¬q → ¬p)                     fa
            ¬¬p                           fb
            (p → r)                       fc
        (¬q → ¬p) → (p → r)             discharge ass2
    (¬q → ¬p) → (p → r)               discharge ass1
(¬q → ¬p) → (p → r) → (¬q → ¬p)     conclusion
```



```
1  |  (P > Q)          Premise
2  |  |  P             Assumption
3  |  |  | A           Assumption
4  |  |  | Q           1,2  >E
5  |  |  (A > Q)       3-4  >I
6  |  (P > (A > Q))    2-5  >I
```



# fitch style proofs: proper

```
Problem: (P > Q) |- (P > (A > Q))

1  |_  (P > Q)          Premise
2  | |_  P              Assumption
3  | | |_  A            Assumption
4  | | |   Q            1,2  >E
5  | |   (A > Q)        3-4  >I
6  |   (P > (A > Q))    2-5  >I


Problem: (A v B) |- ~(~A & ~B)

1   |_  (A v B)        Premise
2   | |_  (~A & ~B)    Assumption
3   | | |_  A          Assumption
4   | | |   ~A         2  &E
5   | | |   #          3,4  #I
6   | | |_  B          Assumption
7   | | |   ~B         2  &E
8   | | |   #          6,7  #I
9   | |   #            1,3-5,6-8  vE
10  |   ~(~A & ~B)     2-9  ~I


Problem: (A v (Ex)Fx) |- (Ex)(A v Fx)

1   |_  (A v (Ex)Fx)        Premise
2   | |_  A                 Assumption
3   | |   (A v Fa)          2  vI
4   | |   (Ex)(A v Fx)      3  EI
5   | |_  (Ex)Fx            Assumption
6   | | |_  Fa              Assumption
7   | | |   (A v Fa)        6  vI
8   | | |   (Ex)(A v Fx)    7  EI
9   | |   (Ex)(A v Fx)      5,6-8  EE
10  |   (Ex)(A v Fx)        1,2-4,5-9  vE


Problem:  |- (Ax)(Ay)((Fx & ~Fy) > ~x=y)

1   |_  a                            Flag
2   | |_  b                          Flag
3   | | |_  (Fa & ~Fb)               Assumption
4   | | | |_  a=b                    Assumption
5   | | | |   Fa                     3  &E
6   | | | |   ~Fb                    3  &E
7   | | | |   Fb                     4,5  =E
8   | | | |   #                      6,7  #I
9   | | |   ~a=b                     4-8  ~I
10  | |   ((Fa & ~Fb) > ~a=b)        3-9  >I
11  |   (Ay)((Fa & ~Fy) > ~a=y)      2-10  AI
12    (Ax)(Ay)((Fx & ~Fy) > ~x=y)    1-11  AI
```
