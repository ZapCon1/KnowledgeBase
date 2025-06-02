## [Table of Contents](https://github.com/ZapCon1/KnowledgeBase.git)

### Macro Call Arguments 

| Argument | Variable# |
|----------|-----------|
|A         | #1        |
|B         | #2        |
|C         | #3        |
|D         | #7        |
|E         | #8        |
|F         | #9        |
|G         | -         |
|H         | #11       |
|I         |           |
|J         | #4        |
|K         | #6        |
|L         | -         |
|M         | 13        |
|N         | -         |
|O         | -         |
|P         | -         |
|Q         | #17       |
|R         | #18       |
|S         | #19       |
|T         | #20       |
|U         | #21       |
|V         | #22       |
|W         | #23       |
|X         | #24       |
|Y         | #25       |
|Z         | #26       |

### WCS Parameters 


| WCS              |  Parameters   |
|------------------|---------------|
| G54              | #5221 - #5226 |
| G55              | #5241 - #5246 |
| G56              | #5261 - #5266 |
| G57              | #5281 - #5286 |
| G58              | #5301 - #5206 |
| G59              | #5321 - #5226 |

To compute the register value in a macro, use this equation (where W is the WCS number): 

```
parameter# = 5221 + (W-54)*20 
```

### Extended WCS Parameteres 

The extended WCS start at #7000 - #7006 and increment by 20 for each new WCS value. 

| WCS              |  Parameters   |
|------------------|---------------|
| G54.1P1          | #7001 - #7006 |
| G54.1P2          | #7021 - #7026 |


Note: Most Brother macros expect a negative value when passing in an extended WCS offset number. 
So `G54.1P1` is referenced by `W-1` in a macro call. 

To compute the register value in a macro, use this equation (where W is the WCS number): 

```
parameter# = 7001 + (-W-1 * 20)
```


### Sample WCS Register Calculation in MACRO

``` 
(W - WCS OFFSET #23)

(FIND THE CORRECT WCS REGISTERS)


IF[#23GT0] GOTO1 (NORMAL WORK OFFSETS)
IF[#23LT0] GOTO2 (EXTENDED WORK OFFSETS)
#3000 = 6(BAD WORK OFFSET VALUE)

(NORMAL WORK OFFSETS)
N1 #100 = #[5221+[#23-54]*20]
#101 = #[5222+[#23-54]*20]
#102 = #[5223+[#23-54]*20]
GOTO3

(EXTENDED WORK OFFSETS)
N2 #100 = #[5221+[#23-54]*20] 
#101 = #[5222+[#23-54]*20]
#102 = #[5223+[#23-54]*20]
GOTO3

N3
```