# JavaScript Data Types

## 1. Strings
JavaScript strings are sequences of characters, represented using either single quotes (''), double quotes ("") or backticks (``). 
They are immutable, meaning once created, their values cannot be changed. However, you can create new strings based on existing ones.

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
