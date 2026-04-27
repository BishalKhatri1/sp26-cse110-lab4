1. ^^^ What will happen at line 12 and why? If the code causes an error, explain why. ^^^
Ans : Line 12 prints 3 because the loop runs through the array which has a length of 3. Even though i was defined inside the for loop, we used var. Since var is function-scoped and doesn't care about blocks, the variable i survives outside the loop. By the time the loop finishes, i has reached 3, so that's what gets printed.

2. ^^^ What will happen at line 13 and why? If the code causes an error, explain why. ^^^
ANs : At line 13, the code will log **150** to the console without any errors. This happens because the variable `discountedPrice` is declared with **`var`**, which has "function scope." This means the variable isn't trapped inside the loop's curly braces; instead, it stays alive throughout the entire function. Since the loop just finished processing the last item in the array ($300 \times 0.5 = 150$), that final value remains stored in the variable for line 13 to read and print.

3. ^^^ What will happen at line 14 and why? If the code causes an error, explain why. ^^^
Ans : At line 14, the code will log **150** to the console. It does not cause an error.

This happens because `finalPrice` was created with **`var`**, meaning it is a single "container" that stays alive for the whole function. During the final round of the loop, the code calculates the discount for the last price ($300 \times 0.5 = 150$) and saves it to that container. When the loop ends, the container doesn't disappear; it just holds onto that last value of 150, which is what gets printed at line 14.

4. ^^^ What will this function return? Give a brief explanation why. If the code causes an error, explain why. ^^^
Ans : The function will return the array **`[50, 100, 150]`**. It works by looping through the original prices and applying a 50% discount to each one. During the first round, it calculates half of 100 (**50**); in the second, half of 200 (**100**); and in the third, half of 300 (**150**). Each of these results is saved into the `discounted` list one by one. Once the loop finishes, the function sends back that final list containing all the new, lower prices.

5. ^^^ What will happen at line 12 and why?  If the code causes an error, explain why. ^^^ (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5)).
Ans : At line 12, the code will **cause an error** and stop running. Specifically, it will say that `i` is not defined.

The reason this happens is because of how the word `let` works in JavaScript. When you create a variable using `let` inside a loop, that variable is "trapped" inside the curly brackets of that loop. It only exists while the loop is running.

Because line 12 is outside of the loop's curly brackets, the computer no longer knows what `i` is. It is like trying to use a key that was locked inside a room you just walked out of. Since the computer can't find the variable, it crashes instead of printing a number.


6. ^^^ What will happen at line 13 and why? If the code causes an error, explain why. ^^^
Ans : At line 13, the code will crash and cause a **ReferenceError**.

This happens because the variable `discountedPrice` was created using `let` inside the `for` loop.

In JavaScript, variables declared with `let` are **block-scoped**, meaning they only exist within their own curly braces.

Since line 13 is outside of the loop's braces, the computer no longer recognizes that variable.

The program stops because it cannot print something that is officially "not defined" in that area.


7. ^^^ What will happen at line 14 and why? If the code causes an error, explain why. ^^^
Ans :  Line 14 will log **150** to the console. Although `finalPrice` is updated inside the `for` loop, it is declared with `let` on **line 4**, which gives it **function scope** (accessible anywhere within `discountPrices`). After the final iteration (where the price is 300 and the discount is 0.5), the variable retains its last assigned value. There is **no error** because the variable is still within its valid scope when called.


8. ^^^ What will this function return? Give a brief explanation. If the code causes an error, explain why. ^^^
Ans ; The function will return the array **`[50, 100, 150]`**. 

It iterates through the input `prices` ($100, 200, 300$), applying a $50\%$ discount ($0.5$) to each. The line `Math.round(discountedPrice * 100) / 100` ensures each price is rounded to two decimal places before being pushed to the `discounted` array. Although `let` is used for block-scoping, the `return` statement is inside the function and correctly accesses the `discounted` variable.

9. ^^^ What will happen at line 11 and why? If the code causes an error, explain why. ^^^
Ans : Line 11 will cause a **ReferenceError** stating that `i` is not defined. This happens because `i` is declared using **`let`** inside the `for` loop, making it **block-scoped**. Consequently, `i` exists only within the loop's curly braces and is inaccessible to the `console.log(i)` call outside that block. If `var` had been used instead, the code would have worked due to function-scoping.

10. ^^^ What will happen at line 12 and why? If the code causes an error, explain why. ^^^
Ans : Line 12 will successfully print **3** to the console without causing an error. This is because `length` is declared with **`const`** on line 4, which makes it available throughout the entire function's scope. Since the `console.log` is located within those same function boundaries, it has full access to the variable. Unlike the previous question's `i`, `length` is not confined to the `for` loop's block.

11. ^^^ What will this function return? Give a brief explanation. If the code causes an error, explain why. ^^^
Ans : The function will return the array **`[50, 100, 150]`**. 

Inside the loop, the code calculates each discounted price by multiplying the original price by $1 - 0.5$ (which is $0.5$). Since the inputs are `100`, `200`, and `300`, the loop pushes `50`, `100`, and `150` into the `discounted` array. Even though `discounted` is declared with `const`, JavaScript allows you to mutate the contents of an array (like using `.push()`) as long as you don't reassign the variable itself to a new value.

12. Given the above Object, write the notation for:  (These should be in your part2.md)
Accessing the value of the name property in the student object
Accessing the value of the Grad Year property in the student object
Calling the function for the greeting property in the student object
Accessing the name property of the object in the Favorite Teacher property in student
Access index zero in the array of the courseLoad property of the student object
Ans : A. `student.name`
B. `student['Grad Year']`
C. `student.greeting()`
D. `student['Favorite Teacher'].name`
E. `student.courseLoad[0]`


 ### 13. Arithmetic

**A. `'3' + 2`**
**Answer:** `'32'`
**Explanation:** The `+` operator triggers string concatenation when one operand is a string. The number `2` is coerced into a string and joined with `'3'`.

**B. `'3' - 2`**
**Answer:** `1`
**Explanation:** The subtraction operator `-` only works with numeric values. JavaScript converts the string `'3'` into the number `3` to perform the mathematical operation.

**C. `3 + null`**
**Answer:** `3`
**Explanation:** In a numeric context, `null` is converted to `0`. Therefore, 3 + 0 = 3.

**D. `'3' + null`**
**Answer:** `'3null'`
**Explanation:** Because the first operand is a string, the `+` operator performs concatenation, converting the value `null` into the string `"null"`.

**E. `true + 3`**
**Answer:** `4`
**Explanation:** The boolean `true` is converted to its numeric equivalent, which is `1`. Then, 1 + 3 = 4.

**F. `false + null`**
**Answer:** `0`
**Explanation:** Both values are converted to numbers for addition: `false` becomes `0` and `null` becomes `0`. 0 + 0 = 0.

**G. `'3' + undefined`**
**Answer:** `'3undefined'`
**Explanation:** The string `'3'` forces concatenation, which converts the value `undefined` into the string `"undefined"`.

**H. `'3' - undefined`**
**Answer:** `NaN`
**Explanation:** The `-` operator attempts to convert both to numbers. While `'3'` becomes `3`, `undefined` converts to `NaN` (Not a Number). Any arithmetic operation involving `NaN` results in `NaN`.

---

### 14. Comparison

**A. `'2' > 1`**
**Answer:** `true`
**Explanation:** When comparing a string and a number, JavaScript converts the string `'2'` to the number `2`. Since 2 > 1, it returns true.

**B. `'2' < '12'`**
**Answer:** `false`
**Explanation:** When comparing two strings, JavaScript uses lexicographical (alphabetical) order. It compares the first characters: `'2'` is greater than `'1'`, so `'2'` is considered "larger" than `'12'`.

**C. `2 == '2'`**
**Answer:** `true`
**Explanation:** The loose equality operator `==` performs type coercion. It converts the string `'2'` to the number `2` before checking equality.

**D. `2 === '2'`**
**Answer:** `false`
**Explanation:** The strict equality operator `===` checks both value and type. Since one is a number and the other is a string, they are not strictly equal.

**E. `true == 2`**
**Answer:** `false`
**Explanation:** JavaScript converts the boolean `true` to the number `1`. Since 1 does not equal 2, the comparison is false.

**F. `true === Boolean(2)`**
**Answer:** `true`
**Explanation:** The `Boolean(2)` function converts the "truthy" number `2` into the boolean value `true`. The expression then becomes `true === true`, which is true in both value and type.

---

### 15. Explain the difference between the == and === operators.

**Answer:** The **`==` (Loose Equality)** operator compares two values for equality after performing **type coercion**. If the types are different, JavaScript will attempt to convert them to a common type before comparing. 

The **`===` (Strict Equality)** operator compares both the **value** and the **data type**. It does not perform type coercion; if the types are different (e.g., a number vs. a string), it immediately returns `false`.


17. If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result. (This should be in your part2.md). Here we are passing in a function as a parameter, however we can also return a function from another function just as easily, you're encouraged to play around with callbacks as they are used heavily in frontend JS development. 
Ans : ### 17. Function Call Result

**Result:** `[2, 4, 6]`

**Step-by-step Walkthrough:**

1.  **Function Invocation:** The function `modifyArray` is called with the array `[1, 2, 3]` and the function `doSomething` as the `callback`.
2.  **Initialization:** Inside `modifyArray`, an empty array `newArr` is created.
3.  **Iteration 1:** The loop starts at `i = 0`. It takes `array[0]` (which is `1`) and passes it to the callback: `doSomething(1)`. This returns `1 * 2 = 2`. The value `2` is pushed into `newArr`.
4.  **Iteration 2:** At `i = 1`, it takes `array[1]` (which is `2`) and calls `doSomething(2)`. This returns `2 * 2 = 4`. The value `4` is pushed into `newArr`.
5.  **Iteration 3:** At `i = 2`, it takes `array[2]` (which is `3`) and calls `doSomething(3)`. This returns `3 * 2 = 6`. The value `6` is pushed into `newArr`.
6.  **Return:** The loop finishes, and the function returns `newArr`, which is now `[2, 4, 6]`.

19. What is the output of the above code? 
Ans :1
4
3
2

**Explanation:** JavaScript executes synchronous code first, printing **1** and **4** immediately. Even with a `0`ms delay, `setTimeout` is asynchronous and moves to the task queue, meaning **3** prints only after the main script finishes. Finally, **2** prints after its specified 1-second (1000ms) delay.
