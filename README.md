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
      - let myNum = Number(myString);
      - typeof myNum;
    - Conversely, every number has a method called toString() that converts it to the equivalent string. 
      - let myNum = 123;
      - let myString = myNum.toString();
      - typeof myString; 
  - If a use enters a number into a form's text field, it's a string. However, if you want to add this number to something, you'll need it to be a number, so you could pass it through Number() to handle this. 
6. String Methos and Properties 
  - String .length; returns the length of the string
    - let txt = "Zamir";
    - let sln = txt.length;
  - Finding a String in a String 
    - indexOf() method returns the index of (the position of) the first ocurrence of a specified text in a string
      - let str = "Please locate where 'locate' occurs!"
      - let pos = str.indexOf("locate"); // should output 7
    - lastIndexOf() method returns the index of the last occurance of a specified text in a string. 
      - let str = "Please locate where 'locate' occurs!";
      - let posLast = str.lastIndexOf("locate"); // should output 21 
    - Both indexOf(), and lastIndexOf() return -1 if the text is not found. 
    - Both methods accept a second parameter as the starting position for the search. 
      - let str = "Please locate where 'locate' occurs!";
      - let pos = str.indexOf("locate", 15);
    - The lastIndexOf() methods searched backwards (from the end to the beginning), meaning: if the second parameter is 15, the search starts at position 15, and searches to the beginning of the string. 
      - let str = "Please locate where 'locate' occurs!";
      - let pos = str.lastIndexOf("locate", 15); // 7 
  - Searching for a String in a String 
    - The search() method searches a string for a specified value and returns the position of the match. 
      - let str = "Please locate where 'location' occurs!";
      - let pos = str.search("locate");
  - The two methos, indexOf() and search() are NOT equal. 
    - The search() method cannot take a second start position argument 
    - The indexOf() method cannot take powerful search values (regular expressions)
  - Extracting String Parts 
    - slice(start, end) extracts a part of a string and returns the extracted part in a new string. 
        - let str = "Apple, Banana, Kiwi";
        - let res = str.slice(7, 13); //cuts out "Banana"
      - End number is NOT included
      - If a parameter is negative, the position is counted from the end of the string. 
      - If you omit the second parameter, the method will slice out the rest of the string
      - Or, counting from the end (one parameter and negative)
    - substring(start, end) is similar to slice(), the difference is that substring() cannot accept negative indexes. 
    - substr(start, length) is similar to slice(), the difference being that the second parameter specifies the length of the extracted part. 
      - let str = "Apple, Banana, Kiwi"; 
      - let res = str.substr(7, 6); //output is Banana
  - Replacing String Content 
    - The replace() method replaces a specified value with another value in a string. 
      - str = "Please visit Microsoft!";
      - let n = str.replace("Microsoft", "W3Schools");
    - The method does not change the strng it is called on. It returns a new string. 
    - The replace() method replaces only the FIRST match; 
    - The method is case sensitive
    - To replace case insensitive, use a regular expression with an /i flag(insensitive).
    - To replace all matches, use a regular expression with a /g flag (global match)
      - let n = str.replace(/Microsoft/g, "W3Schools");
  - Converting to Upper and Lower Case 
    - A string is converted to upper case with toUpperCase()
      - let text1 = "Hello World!"; //String 
      - let text2 = text1.toUpperCase(); //text2 is text1 converted to upper (HELLO WORLD!)
    - A string is converted to upper case wth toLowerCase()
  - The concat() method
    - concat() joins two or more strings
      - let text1 = "Hello";
      - let text2 = "World";
      - let text3 = text1.concat(" ", text2);
    - The concat() method can be used instead of the plus operator. These two lines do the same:
      - "Hello" + " " + "World!"
      - "Hello".concat(" ", "World!")
    - NOTE: All string methods return a new string. They don't modify the original string. Formally said - Strings are immutable - Strings cannot be changed, only replaced. 
  - String.trim() method removes whitespace from both sides of a string
    - let str = "        Hello World!        "
    - alert(str.trim());
  - The charAt() Method
    - The charAt() method returns the character at a specified index (position) in a string
      - let str = "HELLO WORLD";
      - str.charAt(0); //returns H
  - Converting a String to an Array 
    - A string can be converted to an array with the split() method
      - let txt = "a,b,c,d,e";  // String
      - txt.split(",");  // Split on commas
      - txt.split(" ");  // Split on spaces
      - txt.split("|");  // Split on pipe
    - If the seperator is omitted, the returned array will contain the whole string index [0]. 
    - If the seperator is "", the returned array will be an array of single characters
      - let text = "Hello";  // String
      - txt.split("");  // Split in characters
        - // Output ["H", "e", "l", "l", "o"] (5)

