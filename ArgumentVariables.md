# Argument Variables

## [Table of Contents](https://github.com/ZapCon1/KnowledgeBase.git)

There are two styles of passing arguments: Argument 1 and Argument 2. 

For Argument 1, you can pass letters in sequaltial order. For example `A1 B2 C3 D4 E5`.
Note that not all controllers let you pass every letter of the alphabet,
but the key concept is that you can pass letters past `A`, `B`, and `C` and each one gets its own specific local variable number. 

For Argument 2, you can only pass six letters as arguments `A`, `B`, `C`, and `I`, `J`, `K`.  
But critically, you can pass and abritrary number of of `I`, `J`, `K` arguments into the macro. 
The macro can be coded to account for however many get passed in, which gives a lot of flexibility. 
This is effectively a way you can pass array data into a macro as an argument. 

## Argument 1 vs Argument 2

| Argument 1 | Variable |   | Argument 2 | Variable |
|:----------:|:--------:|---|:----------:|:--------:|
|      A     |    #1    |   |      A     |    #1    |
|      B     |    #2    |   |      B     |    #2    |
|      C     |    #3    |   |      C     |    #3    |
|      D     |    #7    |   |     I1     |    #4    |
|      E     |    #8    |   |     J1     |    #5    |
|      F     |    #9    |   |     K1     |    #6    |
|      G     |    N/A   |   |     I2     |    #7    |
|      H     |    #11   |   |     J2     |    #8    |
|      I     |    #4    |   |     K2     |    #9    |
|      J     |    #5    |   |     I3     |    #10   |
|      K     |    #6    |   |     J3     |    #11   |
|      L     |    N/A   |   |     K3     |    #12   |
|      M     |    #13   |   |     I4     |    #13   |
|      N     |    N/A   |   |     J4     |    #14   |
|      O     |    N/A   |   |     K4     |    #15   |
|      P     |    N/A   |   |     I5     |    #16   |
|      Q     |    #17   |   |     J5     |    #17   |
|      R     |    #18   |   |     K5     |    #18   |
|      S     |    #19   |   |     I6     |    #19   |
|      T     |    #20   |   |     J6     |    #20   |
|      U     |    #21   |   |     K6     |    #21   |
|      V     |    #22   |   |     I7     |    #22   |
|      W     |    #23   |   |     J7     |    #23   |
|      X     |    #24   |   |     K7     |    #24   |
|      Y     |    #25   |   |     I8     |    #25   |
|      Z     |    #26   |   |     J8     |    #26   |
|            |          |   |     K8     |    #27   |
|            |          |   |     I9     |    #28   |
|            |          |   |     J9     |    #29   |
|            |          |   |     K9     |    #30   |
|            |          |   |     I10    |    #31   |
|            |          |   |     J10    |    #32   |
|            |          |   |     K10    |    #33   |


## Examples


|       ARGUMENT 1 EXAMPLE       |   |     |   |   |   |       ARGUMENT 2 EXAMPLE       |   |     |   |   |
|:------------------------------:|:-:|:---:|:-:|:-:|---|:------------------------------:|:-:|:---:|:-:|:-:|
|   G65 P1234 A1 B2 C3 D4 E5 F6  |   |     |   |   |   |   G65 P1234 A1 B2 C3 I4 I5 I6  |   |     |   |   |
|                A               | = |  #1 | = | 1 |   |                A               | = |  #1 | = | 1 |
|                B               | = |  #2 | = | 2 |   |                B               | = |  #2 | = | 2 |
|                C               | = |  #3 | = | 3 |   |                C               | = |  #3 | = | 3 |
|                D               | = |  #7 | = | 4 |   |                I               | = |  #4 | = | 4 |
|                E               | = |  #8 | = | 5 |   |                I               | = |  #7 | = | 5 |
|                F               | = |  #9 | = | 6 |   |                I               | = | #10 | = | 6 |
|                                |   |     |   |   |   |                                |   |     |   |   |
| G65 P1234 A1 D2 H3 K3 M5 V6 Z7 |   |     |   |   |   | G65 P1234 A1 I2 J3 K4 I5 J6 I7 |   |     |   |   |
|                A               | = |  #1 | = | 1 |   |                A               | = |  #1 | = | 1 |
|                D               | = |  #7 | = | 2 |   |                I               | = |  #4 | = | 2 |
|                H               | = | #11 | = | 3 |   |                J               | = |  #5 | = | 3 |
|                K               | = |  #6 | = | 4 |   |                K               | = |  #6 | = | 4 |
|                M               | = | #13 | = | 5 |   |                I               | = |  #7 | = | 5 |
|                V               | = | #22 | = | 6 |   |                J               | = |  #8 | = | 6 |
|                Z               | = | #26 | = | 7 |   |                I               | = | #10 | = | 7 |
|                                |   |     |   |   |   |                                |   |     |   |   |
|   G1234 A1 D2 H3 K3 M5 V6 Z7   |   |     |   |   |   |   G1234 A1 I2 J3 K4 I5 J6 I7   |   |     |   |   |
|                A               | = |  #1 | = | 1 |   |                A               | = |  #1 | = | 1 |
|                D               | = |  #7 | = | 2 |   |                I               | = |  #4 | = | 2 |
|                H               | = | #11 | = | 3 |   |                J               | = |  #5 | = | 3 |
|                K               | = |  #6 | = | 4 |   |                K               | = |  #6 | = | 4 |
|                M               | = | #13 | = | 5 |   |                I               | = |  #7 | = | 5 |
|                V               | = | #22 | = | 6 |   |                J               | = |  #8 | = | 6 |
|                Z               | = | #26 | = | 7 |   |                I               | = | #10 | = | 7 |

