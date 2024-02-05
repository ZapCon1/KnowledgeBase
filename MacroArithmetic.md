# Macro Arithmetic

## [Table of Contents](https://github.com/ZapCon1/KnowledgeBase.git)

|      Group     |  Expression  |                    Purpose                    |                  |       |     |   | Defined Variables |   |     |
|:--------------:|:------------:|:---------------------------------------------:|------------------|-------|-----|---|:-----------------:|---|-----|
|     Define     |     #i=#j    | Define or substitute one variable for another | #100=#103        | #100= | 2   |   |        #101       | = |  0  |
|      -----     |   #i=#j+#k   | Sum                                           | #100=#101+#102   | #100= | 1   |   |        #102       | = |  1  |
|                |   #i=#j-#k   | Subtract                                      | #100=#101-#102   | #100= | -1  |   |        #103       | = |  2  |
|                |              |                                               | #100=#101OR#102  | #100= | 1   |   |        #104       | = |  0  |
|                |   #i=#jOR#k  | Logical Sum                                   | #100=#102OR#103  | #100= | 1   |   |        #105       | = |  5  |
|    Addition    |              |                                               | #100=#101OR#104  | #100= | 0   |   |        #106       | = |  -9 |
|                |              |                                               |                  | #100= |     |   |        #107       | = | 1.2 |
|                |  #i=#jXOR#k  | Exclusive OR                                  |                  | #100= |     |   |                   |   |     |
|      -----     |              |                                               |                  | #100= |     |   |                   |   |     |
|      -----     |   #i=#j*#k   | Product                                       | #100=#103*#105   | #100= | 10  |   |                   |   |     |
|                |   #i=#j/#k   | Quotient                                      | #100=#105/#103   | #100= | 2.5 |   |                   |   |     |
| Multiplication |              |                                               | #100=#101AND#102 | #100= | 0   |   |                   |   |     |
|                |  #i=#jAND#k  | Logical Product                               | #100=#102AND#103 | #100= | 1   |   |                   |   |     |
|      -----     |              |                                               | #100=#101AND#104 | #100= | 0   |   |                   |   |     |
|      -----     |  #i=SIN[#j]  | Sine                                          | #100=SINE[#105]  | #100= |     |   |                   |   |     |
|                |  #i=ASIN[#j] | Arcsine                                       | #100=ASIN[#105]  | #100= |     |   |                   |   |     |
|                |  #i=COS[#j]  | Cosine                                        | #100=COS[#105]   | #100= |     |   |                   |   |     |
|                |  #i=ACOS[#j] | Arccosine                                     | #100=ACOS[#105]  | #100= |     |   |                   |   |     |
|                |  #i=TAN[#j]  | Tangent                                       | #100=TAN[#105]   | #100= |     |   |                   |   |     |
|                |  #i=ATAN[#j] | Arctangent                                    | #100=ATAN[#105]  | #100= |     |   |                   |   |     |
|                |  #i=SQRT[#j] | Square Root                                   | #100=SQRT[#106]  | #100= | 3   |   |                   |   |     |
|                |  #i=ABS[#j]  | Absolute Value                                | #100=ABS[#106]   | #100= | 9   |   |                   |   |     |
|    Functions   |  #i=BIN[#j]  | Convert BCD to Bin                            | #100=BIN[#105]   | #100= |     |   |                   |   |     |
|                |  #i=BCD[#j]  | Convert Bin to BCD                            | #100=BCD[#105]   | #100= |     |   |                   |   |     |
|                | #i=ROUND[#j] | Round off value                               | #100=ROUND[#107] | #100= | 1   |   |                   |   |     |
|                |  #i=FIX[#j]  | Discard fractions less than 1                 | #100=FIX[#107]   | #100= |     |   |                   |   |     |
|                |  #i=FUP[#j]  | Add 1 to fractions less than 1                | #100=FUP[#107]   | #100= |     |   |                   |   |     |
|                |   #i=LN[#j]  | Logarithm                                     | #100=LN[#105]    | #100= |     |   |                   |   |     |
|                |  #i=EXP[#j]  | index                                         | #100=EXP[#105]   | #100= |     |   |                   |   |     |
|      -----     |  #i=ADP[#j]  | add decimal point                             | #100=ADP[#102]   | #100= | 1.  |   |                   |   |     |

## [Table of Contents](https://github.com/ZapCon1/KnowledgeBase.git)
