This project is just to practice the basics of Javascript. 




There are seven basic data types in Javascript:
1. A number 
  - integers (whole numbers)
  - floating point numbers (decimals)
  - Special numeric values 
    - Infinity ( console.log(1 / 0); //Infinity )
    - -Infinity 
    - NaN (Not a number)
2. A string 
  - ""
  - ''
  - ` ${} `
3. A boolean (logical type)
  - true (yes)
  - false (no, incorrect)
4. The "null" value
  - Nothing 
  - Empty 
  - Value unknown 
5. The "undefined" value 
  - Value is not assigned 
  - Normally, we use null to assign an "empty" or "unknown" value to a variable, and we use undefined for checks like seeing if a variable has been assigned. 
6. Objects and Symbols (all OTHER data types are primitive)
  - Special (used to store collections of data)
  - Symbol type (used to create unique identifiers for objects)
  - Objects are used to store collections of data and more complex entities.
7. The typeof operator 
  - Returns the type of argument 
  - As an operator (typeof x)
  - As a function (typeof (x))
  Example:
    - typeof undefined // "undefined"
    - typeof 0 // "number"
    - typeof true // "boolean"
    - typeof "foo" // "string"
    - typeof Symbol("id") // "symbol"
    - typeof Math // "object" (1)
    - typeof null // "object" (2)
    - typeof alert // "function" (3)
  - Math is a built-in object that provides mathematical operations. 
  - The result of typeof null is "object". That's wrong. It is an officially recognized error in "typeof", keep for compatibility. null is not an object. It is a special value with a seperate type of its own. So, again,this is an error in language. 
  - The result of typeof alert is "function", because alert is a function. 


Strings In Javascript:

