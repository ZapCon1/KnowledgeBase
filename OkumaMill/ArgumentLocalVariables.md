# Argument\Local Variables

## [Table of Contents](https://github.com/ZapCon1/KnowledgeBase.git)

Okuma arguments use local variables which are created by the user in the program:
A local variable is two alphabetical characters followed by up to two more alphanumeric characters:

##### Example:
AA11=1 : creates a local variable called 'AA11' and assigns it a value of 1.<br>
BB22=.5 : creates a local variable called 'BB22' and assigns it a value of 0.5.<br>
CC33=AA11\*BB22 : creates a local variable called 'BB22' and assigns it the value of the sum of AA11 multiplied by BB22


##### Local variables can be used in subprogram calls.
To check if a variable is null (like Fanuc #0) then it needs to begin with a 'P' e.g. PA12<br>
When 'P' is commanded at the beginning of a local variable, them the input can be interrogated with an EMPTY evaluation to see if it has a null\empty value.

##### Example:<br>

IF\[PA12 EQ EMPTY]N10<br>
M00 (code will stop here if PA12 has been commanded)<br>
N10 (code will jump here if PA12 has not been commanded)<br>

##### Example<br>	

(Program start)<br>
BB22=4.567 (set local variable BB22 to 4.567)<br> 
CALL O1234 AA11=1.234 BB22=BB22 PC33=1 (PC33 is an optional input)<br>
M02 <br>
(Program end)
<br><br>
(sub program O1234)<br>
O1234<br>
VC1=AA11 (This will set Common Variable VC1 to 1.234)<br>
VC2=BB22 (This will set Common Variable VC2 to 4.567)<br>
VC3=PC33 (This will set Common Variable VC3 to 1)<br>	
IF\[PC33 EQ EMPTY]N10 (Check if PC33 has been commanded)<br>	
G0 X=AA11 Y=BB22 Z=PC33 (Move to XYZ position)<br>	
GOTO N20 (Skip XY move)<br>	
N10 (Move to XY position)<br>	
G0 X=AA11 Y=BB22<br>	
N20<br>	
RTS (End of subprogram)<br>