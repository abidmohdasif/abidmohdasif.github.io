```mermaid
flowchart TD
     id2([Start])-->Computer_Generates_A_Numeber
    Computer_Generates_A_Numeber --> id1{User_Input_A_Number}
    id1{User_Input_A_Number}--> id4[/User_Input_Greater_Than_Random_Number/]
    id1{User_Input_A_Number}--> id5[/User_Input_Less_Than_Random_Number/]
    id1{User_Input_A_Number}--> id6[/User_Input_Is_Random_Number/]
    id5[/User_Input_Less_Than_Random_Number/]--> Wrong
    id4[/User_Input_Greater_Than_Random_Number/] --> Wrong
    id6[/User_Input_Is_Random_Number/] --> Correct
    Wrong --> id1{User_Input_A_Number}
    id1{User_Input_A_Number} --> id7[/Input_Is_Not_A_Number/]
   id7[/Input_Is_Not_A_Number/] --> Try_Again
    Try_Again --> id1{User_Input_A_Number}
    Correct --> id3([End])

```
## Documentation
First the computer generates a number

Then the user is asked to guess what they think the number is 

Based on the users input it goes to either input is greater than, input is less than, input is the same or input is not a number

If the input is greater than or input is less than it goes to wrong

Wrong then goes back to user intputs a number

If input is not a number it goes to try again

Try again then goes back to user inputs a number

If input is the same then it goes to correct

Correct then goes to end and ends the cycle