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

1. Single quotes vs double quotes
  - ''
  - "" 
  - both are fine, there is little to no difference
  - You cannot use one of each in one line ('What the?";)
  - The browser will think the string has not been closed because the other type of quote you are not using to contain your strings can appear in the string. For example (let sglDbl = 'Would you eat a "fish supper"?';)
2. Escaping characters in a string
  - let bigMouth = 'I\'ve got no right to take my place...';
  - We put a backsplash just before the character.
3. Concatenating strings
  - Fancy way for saying "join together"
  - You can join as many strings as you'd like 
  - You can also use a mix of variables and actual strings 
    - (let response = one + 'I am fine - ' + two;)
    - This is called a string literal
4. Concatenation in context 
  - Example:
    // <button>Press me</button>
    // const button = document.querySelector('button');
    // button.onclick = function() {
    //   let name = prompt('What is your name?');
    //   alert('Hello ' + name + ', nice to see you!');
       }
5. Numbers vs. strings 
  - You can add (concatenate) a string and a number. ("front" + 242;)
  - Trying to represent a string as a number doesn't really make sense, but representing a number as a string does, so the browser rather cleverly converts the number to a string and adds the two strings. 
  - You can do this with two numbers (force a number to become a string by wrapping it in quote marks)
    - let myDate = "19" + "50";
      typeof myDate; //would return "string"
  - If you have a numeric value that you want to convert to a string but not change otherwise, or a string variable that you want to convert to a number but not change otherwise, you can use the following two constructs: 
    - The Number object converst anything passed to it into a number, if it can. 
      - let myString = "123";
        let myNum = Number(myString);
        typeof myNum;
