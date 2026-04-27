### **Part 3: Debugging Questions**

**1. What was the bug?**
The bug was **Type Coercion**. In JavaScript, the values retrieved from HTML input fields are always treated as **Strings**. When the `+` operator is used with strings, it performs **concatenation** (joining them together) instead of mathematical addition. For example, instead of $2 + 3 = 5$, the code was doing `"2" + "3" = "23"`.

**2. How would you fix it?**
I would fix it by wrapping the input variables in the `Number()` function. This converts the strings into actual numbers before the addition happens. 

**Fixed Code:**
```javascript
function calculateSum(num1, num2) {
  let result = Number(num1) + Number(num2);
  return result;
}
