# JavaScript Data Types

## 1. Strings
JavaScript strings are sequences of characters, represented using either single quotes (''), double quotes ("") or backticks (``). 
They are immutable, meaning once created, their values cannot be changed. However, we can create new strings based on existing ones.

### Creating Strings
```
// Using single quotes
let singleQuotedString = 'Hello, World!';

// Using double quotes
let doubleQuotedString = "Hello, World!";

// Using backticks for template literals (allowing interpolation and multiline strings)
let templateLiteral = `Hello,
World!`;
```
### String Properties and Methods

#### a.) Length 
Property that returns the length of the string.
```
let str = "Hello";
console.log(str.length); // Outputs: 5
```
#### b.) charAt()
Returns the character at a specified index in the string.
```
let str = "Hello";
console.log(str.charAt(0)); // Outputs: H
```
#### c.) concat() 
Combines two or more strings and returns a new string.
```
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(", ", str2)); // Outputs: Hello, World
```
#### d.) indexOf()
Returns the index within the calling string of the first occurrence of the specified value, starting the search at fromIndex. 
*Returns -1 if the value is not found.*
```
let str = "Hello, World!";
console.log(str.indexOf("World")); // Outputs: 7
```
#### e.) slice()
This method is used to extract a section of a string and returns it as a new string, without modifying the original string. It takes two parameters: 

1. **start:** The index at which to begin extraction. If negative, it is treated as str.length + start. If start is omitted, slice begins from index 0.
2. **end (optional):** The index at which to end extraction (up to, but not including the index specified). If negative, it is treated as str.length + end. If end is omitted, slice extracts to the end of the string.

Here's a more detailed explanation:

##### Example 1: Basic Usage

```
let str = "Hello, World!";
let slicedStr = str.slice(7);
console.log(slicedStr); // Outputs: World!
```

*In this example, `slice(7)` extracts the portion of the string starting from index 7 ("W") to the end of the string. So, the output is "World!".*

##### Example 2: Specifying Start and End Index

```
let str = "Hello, World!";
let slicedStr = str.slice(7, 12);
console.log(slicedStr); // Outputs: World
```

*Here, `slice(7, 12)` extracts the portion of the string starting from index 7 ("W") up to index 12 (not including index 12), which is the space before the exclamation mark. So, the output is "World".*

##### Example 3: Negative Indices

```
let str = "Hello, World!";
let slicedStr = str.slice(-6, -1);
console.log(slicedStr); // Outputs: World
```

*Negative indices count from the end of the string. So, `slice(-6, -1)` extracts the portion of the string starting from the 6th character from the end ("W") up to the 2nd character from the end (not including index -1), which is "d". So, the output is "World".*

##### Example 4: Omitting End Index

```
let str = "Hello, World!";
let slicedStr = str.slice(7);
console.log(slicedStr); // Outputs: World!
```

*If the end parameter is omitted, `slice()` extracts characters to the end of the string, starting from the specified start index.*

##### Example 5: Using Negative Start Index

```
let str = "Hello, World!";
let slicedStr = str.slice(-6);
console.log(slicedStr); // Outputs: World!
```

*If the start parameter is negative, it is treated as str.length + start. So, `slice(-6)` extracts characters from the 6th character from the end ("W") to the end of the string.*

#### f.) toUpperCase() and toLowerCase()
Returns the string with all characters converted to uppercase or lowercase.
```
let str = "Hello";
console.log(str.toUpperCase()); // Outputs: HELLO
console.log(str.toLowerCase()); // Outputs: hello
```
#### g.) trim()
Removes whitespace from both ends of the string.
```
let str = "   Hello   ";
console.log(str.trim()); // Outputs: Hello
```

### String Interpolation:
With ES6, we can use template literals for string interpolation. This allows us to embed expressions within strings.
```
let name = "John";
let age = 30;
console.log(`My name is ${name} and I am ${age} years old.`); // Outputs: My name is John and I am 30 years old.
```

## 2. Boolean

This data type represents a logical value, which can be either `true` or `false`. Booleans are fundamental to decision-making and control flow in programming, as they determine the conditions under which certain code blocks execute. Here's a comprehensive overview:

### Boolean Values:
   - **true**: Represents the logical value of true.
   - **false**: Represents the logical value of false.

### Usage:
**a.) Conditionals**: Booleans are frequently used in conditional statements, such as `if`, `else if`, and `else`, to control the flow of execution based on whether a condition evaluates to true or false.
   ```
   let x = 10;
   if (x > 5) {
       console.log("x is greater than 5"); // This block will execute
   } else {
       console.log("x is not greater than 5");
   }
   ```
**b.) Logical Operators**: Booleans are also used with logical operators (`&&`, `||`, `!`) to create compound conditions and perform logical operations.
   ```
   let temperature = 25;
   let isSummer = true;
   if (temperature > 30 && isSummer) {
       console.log("It's a hot day!"); // This block will not execute
   }
   ```

### Boolean Functions:
**Boolean()**: The Boolean() function can be used to explicitly convert any JavaScript value to a Boolean. The conversion rules are straightforward: empty strings, `0`, `NaN`, `null`, `undefined`, and `false` all convert to `false`, while all other values convert to `true`.
   ```
   console.log(Boolean("Hello")); // true
   console.log(Boolean(0)); // false
   console.log(Boolean({})); // true
   ```

### Boolean Object:
JavaScript has a Boolean object that represents a wrapper around a primitive Boolean data type. However, it's rarely used in practice because it's not necessary to create Boolean objects explicitly, and it can introduce unexpected behavior due to its object nature.
   ```
   let boolObject = new Boolean(true);
   console.log(boolObject.valueOf()); // true
   ```

### 5. Comparison Operators:
Comparison operators (e.g., `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `>=`) return Boolean values based on the comparison between two operands.
   ```
   console.log(5 > 3); // true
   console.log(10 === "10"); // false (strict equality)
   ```

### 6. Truthy and Falsy Values:
In JavaScript, values other than `true` and `false` can be evaluated as either "truthy" or "falsy" in Boolean contexts. For example, an empty string (`""`), zero (`0`), `null`, `undefined`, `NaN`, and `false` are all falsy, while all other values are considered truthy.
   ```
   if ("Hello") {
       console.log("Truthy value"); // This block will execute
   }
   ```
