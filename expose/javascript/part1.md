1. What is printed by line 9? If the code returns an error, explain why.
 Ans : 20 is printed because we are adding 10 + 10 and in this context var does not effecct.

2. What is printed by line 13? If the code returns an error, explain why.
 Ans : Line 9 prints values added: 20 because 10 + 10 is 20 and the if statement is true.
Line 13 also prints final result: 20. Even though the code gets out of the if statement, it doesn't stop there. It keeps going to the next line. Since we used var, the 20 is still stored in result and it doesn't return an error.

3. Why should you not use var? Explain why
Ans: We should not use var because regardless of the block it is defined in, it can be accessed anywhere inside the function it is defined in. Using var to declare your variables in your programs led to naming conflicts and scoping issues.

4. What is printed by line 9? If the code returns an error, explain why
Ans :  20 is printed because we are adding 10 + 10 and in this context let is variable decleration and result will add the nums and line 9 will print it .

5. What is printed by line 13? If the code returns an error, explain why.
Ans : Line 13 will return an error because eventhough the code moves to next line, Let is blocked scoped, so the variable "dies" as soon as it leaves the if statement. Line 13 tries to print a varaiable that does not exits anymore.

6. What is printed by line 9? If the code returns an error, explain why. ^^^^^
Ans : Line 9 will not print anything because the code returns an error on Line 7 because in line 7, it is trying to change the const result value which is not allowed and you cannot reassigned it after the first time.

7. What is printed by line 13? If the code returns an error, explain why.
Ans ; Line 13 will not print anything because the code returns an error on Line 7 because in line 7, it is trying to change the const result value which is not allowed and you cannot reassigned it after the first time.
