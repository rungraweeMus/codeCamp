# JavaScript Algorithms and Data Structures
## Basic JavaScript
> Introduction to JavaScript    
1. Comment Your JavaScript Code
There are two ways to write comments in JavaScript:  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Using // will tell JavaScript to ignore the remainder of the text on the current line:  
    >// This is an in-line comment.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)You can make a multi-line comment beginning with /* and ending with */:

    >/* This is a multi-line comment */
___
2. Declare JavaScript Variables  

   JavaScript provides eight different data types  
 which are undefined, null, boolean, string,   symbol, bigint, number, and object.  

   ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the **var** keyword to create a variable called myName.
   > var ourName;
___
3. Storing Values with the Assignment Operator  
In JavaScript, you can store a value in a variable with the assignment operator.    
  
   > var ourName = 10;  

   ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)This assigns the Number value 10 to ourName

   >myData = 8;  
    myNew = myData;

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)This assigns 8 to myData and then resolves myData to 8 again and assigns it to myNew.  

        Assign the value 7 to variable a
        a = 7;    

        Assign the contents of a to variable b
        b = a;
___
4. Initializing Variables with the Assignment Operator    

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Creates a new variable called `myVar` and assigns it an initial value of `0`.

    > var  myVar = 0;  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Define a variable `a` with var and initialize it to `a` value of `9`.

     > var a = 9; 

___
5. Understanding Uninitialized Variables  

    When JavaScript variables are declared, they have an initial value of `undefined`. If you do a mathematical operation on an `undefined` variable your result will be `NaN` which means "Not a Number". If you concatenate a string with an `undefined` variable, you will get a literal string of `"undefined"`.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Initialize the three variables `a`, `b`, and `c` with `5`, `10`, and `"I am a"` respectively so that they will not be `undefined.`

    >// Only change code below this line  
    var a = 5;  
    var b = 10;  
    var c = "I am a";  
    // Only change code above this line  
    a = a + 1;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    // a=6   
    b = b + 5;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    // b=15  
    c = c + " String!";

___
6. Understanding Case Sensitivity in Variables  
In JavaScript all variables and function names are case sensitive. This means that capitalization matters.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)`MYVAR` is **not** the same as `MyVar` **nor** `myvar`. It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.     

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Best Practice  
    >Write variable names in JavaScript in camelCase. In camelCase, multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized.   

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Examples:  
    > var someVariable;    
       var anotherVariableName;  
       var thisVariableNameIsSoLong;    

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the existing declarations and assignments so their names use camelCase.
    Do not create any new variables.  
    >`Variable declarations`  
    var studlyCapVar;  
    var properCamelCase;  
    var titleCaseOver;

    >`Variable assignments`  
    studlyCapVar = 10;
    properCamelCase = "A String";
    titleCaseOver = 9000;
___
7. Add Two Numbers with JavaScript  

    >`Number` is a data type in JavaScript which represents numeric data.  

    >Now let's try to add two numbers using JavaScript.  

    >JavaScript uses the `+` symbol as an addition operator when placed between two numbers.  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Example:  
    >myVar = 5 + 10; // assigned 15

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the **0** so that sum will equal **20**.

    >var sum = 10 + 10;
___
8. Subtract One Number from Another with JavaScript  

    >We can also subtract one number from another.  

    >JavaScript uses the <mark>-</mark> symbol for subtraction.  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Example:  

    >myVar = 12 - 6; // assigned 6  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the 0 so the difference is 12.  
    >var difference = 45 - 33;
___
9. Multiply Two Numbers with JavaScript
    We can also multiply one number by another.

    JavaScript uses the * symbol for multiplication of two numbers.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Example

    >myVar = 13 * 13; // assigned 169

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the 0 so that product will equal 80.

    >var product = 8 * 10;
___
10. Divide One Number by Another with JavaScript  

    We can also divide one number by another.

    JavaScript uses the / symbol for division.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Example

    >myVar = 16 / 2; // assigned 8

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the 0 so that the quotient is equal to 2.

    >var quotient = 66 / 33;
___
11. Increment a Number with JavaScript  

    You can easily increment or add one to a variable with the **++** operator.

    <mark>**i++;**</mark>

    *is the equivalent of i = i + 1;*

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Note

    >The entire line becomes i++;, eliminating the need for the equal sign.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the code to use the ++operator on myVar.

    >var myVar = 87;

    // Only change code below this line

    >myVar++;

___
12. Decrement a Number with JavaScript  

    You can easily decrement or decrease a variable by one with the **--** operator.

    **<mark>i--;</mark>**  is the equivalent of **<mark> i = i - 1; </mark>**


    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Note

    >*The entire line becomes i--;, eliminating the need for the equal sign.*

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the code to use the -- operator on myVar.

    > var myVar = 11;

    // Only change code below this line

    >myVar --;
___
13. Create Decimal Numbers with JavaScript  
  
    We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Note

    >*Not all real numbers can accurately be represented in floating point. This can lead to rounding errors.*

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a variable myDecimal and give it a decimal value with a fractional part (e.g. 5.7).

    >var ourDecimal = 5.7;

    // Only change code below this line
    >var myDecimal = 2542.01;
___
14. Multiply Two Decimals with JavaScript  
In JavaScript, you can also perform calculations with decimal numbers, just like whole numbers.

    `Let's multiply two decimals together to get their product.`

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the 0.0 so that product will equal 5.0.

    >var product = 2.0 * 2.5;    
___
15. Divide One Decimal by Another with JavaScript
Now let's divide one decimal by another.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the 0.0 so that quotient will equal to 2.2.

    >var quotient = 4.4 / 2.0; `// Change this line`

___
16. Finding a Remainder in JavaScript
The remainder operator % gives the remainder of the division of two numbers.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Example

    >5 % 2 = 1   
Math.floor(5 / 2) = 2 (Quotient)  
2 * 2 = 4  
5 - 4 = 1 (Remainder)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Usage

    >In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2.

    >17 % 2 = 1 (17 is Odd)  
    >48 % 2 = 0 (48 is Even)

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Note

    The remainder operator is sometimes incorrectly referred to as the "modulus" operator. It is very similar to modulus, but does not work properly with negative numbers.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Set remainder equal to the remainder of 11 divided by 3 using the remainder (%) operator.

    `// Only change code below this line`

    >var remainder = 11 % 3;
___
17. Compound Assignment With Augmented Addition  

    In programming, it is common to use assignments to modify the contents of a variable. Remember that everything to the right of the equals sign is evaluated first, so we can say:

    >myVar = myVar + 5;

    *to add **`5`** to **`myVar`**. Since this is such a common pattern, there are operators which do both a mathematical operation and assignment in one step.*

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) One such operator is the += operator.

    >var myVar = 1;  
    >myVar += 5;  
    >console.log(myVar); `// Returns 6`

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the assignments for a, b, and c to use the += operator.
    >var a = 3;  
var b = 17;  
var c = 12;  

    `// Only change code below this line`  
    >a += 12;  
b += 9;  
c += 7;
___
18. Compound Assignment With Augmented Subtraction  

    Like the <mark>+=</mark> operator, <mark>-=</mark> subtracts a number from a variable.  

    >myVar = myVar - 5;  

    will subtract <mark>5</mark> from <mark>myVar</mark>. This can be rewritten as:  

    >myVar -= 5;    

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the assignments for a, b, and c to use the <mark>-=</mark> operator.

     var a = 11;  
    var b = 9;  
    var c = 3;  

    `// Only change code below this line`  
    a -= 6;  
    b -= 15;  
    c -= 1;
___
19. Compound Assignment With Augmented Multiplication  

    The <mark>*=</mark> operator multiplies a variable by a number.  

    >myVar = myVar * 5;  

    will multiply <mark>myVar</mark> by <mark>5</mark>. This can be rewritten as:  

    >myVar *= 5;      

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the assignments for a, b, and c to use the <mark>*=</mark> operator.

    var a = 5;  
    var b = 12;  
    var c = 4.6;  

    `// Only change code below this line`  
    a *= 5;  
    b *= 3;  
    c *= 10;  
___
20. Compound Assignment With Augmented Division  

    The <mark>/=</mark> operator divides a variable by another number.  

    >myVar = myVar / 5;  

    Will divide <mark>myVar</mark> by <mark>5</mark>. This can be rewritten as:  

    >myVar /= 5;  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the assignments for a, b, and c to use the <mark>/=</mark> operator.
    
    var a = 48;  
    var b = 108;  
    var c = 33;  

    `// Only change code below this line`  
    a /= 12;  
    b /= 4;  
    c /= 11;  
___
21. Declare String Variables  
Previously we have used the code  

    >var myName = `"your name"`;  

    `"your name"` is called a string literal. It is a string because it is a series of zero or more characters enclosed in single or double quotes.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create two new string variables: myFirstName and myLastName and assign them the values of your first and last name, respectively.

    > var myFirstName = `"Rungrawee"`  
    > var myLastName = `"Musignawabut"`
___
22. Escaping Literal Quotes in Strings  

    When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: `"` or `'` inside of your string?

    In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash (&#92;) in front of the quote.

    >var sampleStr = "Alan said, &#92;"Peter is learning JavaScript&#92;".";

    This signals to JavaScript that the following quote is not the end of the string, but should instead appear inside the string. So if you were to print this to the console, you would get:

    >Alan said, "Peter is learning JavaScript".

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use backslashes to assign a string to the myStr variable so that if you were to print it to the console, you would see:

    *`I am a "double quoted" string inside "double quotes".`*

    var myStr = "I am a \"double quoted\" string inside \"double quotes\"."; `// Change this line`
___
23. Quoting Strings with Single Quotes  

    String values in JavaScript may be written with single or double quotes, as long as you start and end with the same type of quote. Unlike some other programming languages, single and double quotes work the same in JavaScript.
    
    >doubleQuoteStr = `"This is a string"`;   
    singleQuoteStr = `'This is also a string'`;

    The reason why you might want to use one type of quote over the other is if you want to use both in a string. This might happen if you want to save a conversation in a string and have the conversation in quotes. Another use for it would be saving an <mark>&#60;a&#62;</mark> tag with various attributes in quotes, all within a string.

    >conversation = 'Finn exclaims to Jake, "Algebraic!"';

    However, this becomes a problem if you need to use the outermost quotes within it. Remember, a string has the same kind of quote at the beginning and end. But if you have that same quote somewhere in the middle, the string will stop early and throw an error.

    >goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"';  
    badStr = 'Finn responds, "Let's go!"'; // Throws an error

    In the goodStr above, you can use both quotes safely by using backslash \ as an escape character.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**`Note`**

    `*backslash \ should not be confused with the forward slash /. They do not do the same thing.*`

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)*Change the provided string to a string with single quotes at the beginning and end and no escape characters.*

    >var myStr = 'Addr';
___
24. Escape Sequences in 
Escape Sequences in Strings    

    Quotes are not the only characters that can be escaped inside a string. There are two reasons to use escaping characters:

    1. To allow you to use characters you may not otherwise be able to type out, such as a carriage return.
    2. To allow you to represent multiple quotes in a string without JavaScript misinterpreting what you mean.

    We learned this in the previous challenge.  
    |Code  |  Output  |  
    |:-----------:|:----------:|
    |&#92;'|single quote|
    |&#92;"|double quote|
    |&#92;&#92;|backslash|
    |&#92;n|newline|
    |&#92;r|carriage return|
    |&#92;t|tab|
    |&#92;b|word boundary|
    |&#92;f|form feed|
    `Note that the backslash itself must be escaped in order to display as a backslash.`

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Assign the following three lines of text into the single variable `myStr` using escape sequences  
    >FirstLine  
       	&nbsp;	&nbsp;	&nbsp;	&nbsp;	&nbsp;\SecondLine  
    ThirdLine

    *You will need to use escape sequences to insert special characters correctly. You will also need to follow the spacing as it looks above, with no spaces between escape sequences or words.*

    Here is the text with the escape sequences written out.

    "FirstLine `newline tab backslash` SecondLine `newline` ThirdLine"

    >var myStr = "FirstLine\n\t\\SecondLine\nThirdLine"; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`// Change this line`

___
25. Concatenating Strings with Plus Operator

    In JavaScript, when the + operator is used with a String value, it is called the concatenation operator. You can build a new string out of other strings by concatenating them together.

    **Example**

    >'My name is Alan,' + ' I concatenate.'  

    **Note**

    Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

    **Example**

    >var ourStr = "I come first. " + "I come second.";  
    // ourStr is "I come first. I come second."

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Build myStr from the strings `"This is the start. "` and `"This is the end."` using the `+` operator.

      >var myStr = "This is the start. " + "This is the end.";  
      *// Only change this line*
___
26. Concatenating Strings with the Plus Equals Operator  

    We can also use the += operator to concatenate a string onto the end of an existing string variable. This can be very helpful to break a long string over several lines.

    **Note**

    Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

    **Example**

    >var ourStr = "I come first. ";  
    ourStr += "I come second.";  
    // ourStr is now "I come first. I come second."

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Build `myStr` over severall lines by concatenating these two strings: `"This is the first sentence. "` and `"This is the second sentence."` using the `+=` operator. Use the `+=` operator similar to how it is shown in the editor. Start by assigning the first string to `myStr`, then add on the second string.  

    >// Only change code below this line   
    var myStr = "This is the first sentence. ";  
    myStr += "This is the second sentence.";
___
27. Constructing Strings with Variables   
Sometimes you will need to build a string, Mad Libs style. By using the concatenation operator (+), you can insert one or more variables into a string you're building.

    **Example:**

    >var ourName = "freeCodeCamp";  
    ourStr = "Hello, our name is " + ourName + ", how are you?";  
    // ourStr is now "Hello, our name is freeCodeCamp, how are you?"  


    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Set `myName` to a string equal to your `name` and build `myStr` with myName between the strings `"My name is "` and `" and I am well!"`

    >// Only change code below this line  
    var myName = "Rungrawee";  
    var myStr = "My name is " + myName + " and I am well!";
___
28. Appending Variables to Strings  

      *Just as we build a string over multiple lines out of string literals, we can also append variables to a string using the plus equals <mark>(+=)</mark> operator.*

    **Example**

    >var anAdjective = "awesome!";  
    var ourStr = "freeCodeCamp is ";  
    ourStr += anAdjective;  
    // ourStr is now "freeCodeCamp is awesome!"    
    
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Set someAdjective and append it to myStr using the += operator.

    >`// Change code below this line`  
var someAdjective = "boring";  
    var myStr = "Learning to code is ";  
    myStr += someAdjective;

___
29. Find the Length of a String  

    *You can find the length of a String value by writing .length after the string variable or string literal.*

    >"Alan Peter".length; // 10

    For example, if we created a variable `var firstName = "Charles"`, we could find out how long the string `"Charles"` is by using the `firstName.length` property.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the `.length` property to count the number of characters in the `lastName` variable and assign it to `lastNameLength.`

    `// Setup`  
    var lastNameLength = 0;  
    var lastName = "Lovelace";  

    `// Only change code below this line`  
    lastNameLength = lastName`.length`;  &nbsp;&nbsp;//8
___
30. Use Bracket Notation to Find the First Character in a String  

    *Bracket notation is a way to get a character at a specific `index` within a string.*

    Most modern programming languages, like JavaScript, don't start counting at 1 like humans do. They start at 0. This is referred to as Zero-based indexing.

    For example, the character at index 0 in the word "Charles" is "C". So if `var firstName = "Charles"`, you can get the value of the first letter of the string by using `firstName[0]`.

    **Example:**

    >var firstName = "Charles";  
    var firstLetter = firstName[0]; // firstLetter is "C"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use bracket notation to find the first character in the `lastName` variable and assign it to `firstLetterOfLastName`.

    `// Setup`  
    var firstLetterOfLastName = "";  
    var lastName = "Lovelace";

    `// Only change code below this line`  
    firstLetterOfLastName = `lastName[0]`;   &nbsp;&nbsp;// "L"
___
31. Understand String Immutability  

    *In JavaScript, `String` values are immutable, which means that they cannot be altered once created.*

    **For example, the following code:**

    >var myStr = "Bob";  
    myStr[0] = "J";

    cannot change the value of `myStr` to "Job", because the contents of `myStr` cannot be altered. Note that this does not mean that `myStr` cannot be changed, just that the individual characters of a string literal cannot be changed. The only way to change `myStr` would be to assign it with a new string, like this:

    >var myStr = "Bob";  
    myStr = "Job";  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Correct the assignment to `myStr` so it contains the string value of `Hello World` using the approach shown in the example above.

    `// Setup`  
    var myStr = "Jello World";

    `// Only change code below this line`  
    myStr = "Hello World"; `// Change this line`  
    `// Only change code above this line`
___
32. Use Bracket Notation to Find the Nth Character in a String  

    *You can also use bracket notation to get the character at other positions within a string.*

    Remember that computers start counting at **0**, so the first character is actually the zeroth character.

    **Example:**

    >var firstName = "Ada";  
    var secondLetterOfFirstName = firstName[1]; // secondLetterOfFirstName is "d"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Let's try to set thirdLetterOfLastName to equal the `third letter` of the `lastName` variable using bracket notation.

    **Hint:** Try looking at the example above if you get stuck.

    `// Setup`  
    var lastName = "Lovelace";

    `// Only change code below this line`  
    var thirdLetterOfLastName = lastName[2]; // Change this line
___
33. Use Bracket Notation to Find the Last Character in a String  

    *In order to get the last letter of a string, you can subtract one from the string's length.*

    For example, if var firstName = "Charles", you can get the value of the last letter of the string by using firstName[firstName.length - 1].

    **Example:**

    >var firstName = "Charles";  
    var lastLetter = firstName[firstName.length - 1]; // lastLetter is "s"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use bracket notation to find the last character in the lastName variable.

    **Hint:** Try looking at the example above if you get stuck.

    `// Setup`  
    var lastName = "Lovelace";

    `// Only change code below this line`  
    var lastLetterOfLastName = lastName[lastName. length - 1]; `// Change this line`
___
34. Use Bracket Notation to Find the Nth-to-Last Character in a String  

    *You can use the same principle we just used to retrieve the last character in a string to retrieve the Nth-to-last character.*

    For example, you can get the value of the third-to-last letter of the `var firstName = "Charles"` string by using `firstName[firstName.length - 3]`

    **Example:**

    >var firstName = "Charles";  
    var thirdToLastLetter = firstName[firstName.length - 3]; `// thirdToLastLetter is "l"`

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use bracket notation to find the second-to-last character in the lastName string.

    **Hint:** Try looking at the example above if you get stuck.

    `// Setup`  
    var lastName = "Lovelace";

    `// Only change code below this line`  
    var secondToLastLetterOfLastName = lastName[lastName.length - 2]; `// Change this line`
___
35. Word Blanks  

    We will now use our knowledge of strings to build a "Mad Libs" style word game we're calling "Word Blanks". You will create an (optionally humorous) "Fill in the Blanks" style sentence.

    In a "Mad Libs" game, you are provided sentences with some missing words, like nouns, verbs, adjectives and adverbs. You then fill in the missing pieces with words of your choice in a way that the completed sentence makes sense.

    Consider this sentence - "It was really ____, and we ____ ourselves ____". This sentence has three missing pieces- an adjective, a verb and an adverb, and we can add words of our choice to complete it. We can then assign the completed sentence to a variable as follows:

    >var sentence = "It was really " + "hot" + ", and we " + "laughed" + " ourselves " + "silly" + ".";

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)In this challenge, we provide you with a noun, a verb, an adjective and an adverb. You need to form a complete sentence using words of your choice, along with the words we provide.

    You will need to use the string concatenation operator `+` to build a new string, using the provided variables: `myNoun`, `myAdjective`, `myVerb`, and `myAdverb`. You will then assign the formed string to the wordBlanks variable. You should not change the words assigned to the variables.

    You will also need to account for spaces in your string, so that the final sentence has spaces between all the words. The result should be a complete sentence.

    >var myNoun = "dog";  
    var myAdjective = "big";  
    var myVerb = "ran";  
    var myAdverb = "quickly";  

    >`// Only change code below this line`  
    var wordBlanks = "My " + myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb + ".";  `// Change this line`  
    `// Only change code above this line`
___
36. Store Multiple Values in one Variable using JavaScript Arrays  

    With JavaScript array variables, we can store several pieces of data in one place.

    You start an array declaration with an opening square bracket, end it with a closing square bracket, and put a comma between each entry, like this:

    >var sandwich = ["peanut butter", "jelly", "bread"].

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the new array myArray so that it contains both a string and a number (in that order).

    **Hint** Refer to the example code in the text editor if you get stuck.

    `// Only change code below this line`
    >var myArray = ["first", 1];
___
37. Nest one Array within Another Array  

    You can also nest arrays within other arrays, like below:

    >[["Bulls", 23], ["White Sox", 45]]  
    This is also called a multi-dimensional array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a nested array called myArray.

    `// Only change code below this line`  
    var myArray = [["first", 1], 2, "third"];
___
38. Access Array Data with Indexes  

    We can access the data inside arrays using indexes.

    Array indexes are written in the same bracket notation that strings use, except that instead of specifying a character, they are specifying an entry in the array. Like strings, arrays use zero-based indexing, so the first element in an array has an index of 0.

    **Example**

    >var array = [50,60,70];  
    array[0]; // equals 50  
    var data = array[1];  // equals 60  

        Note:
        There shouldn't be any spaces between the array name and the square brackets, like array [0]. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a variable called myData and set it to equal the first value of myArray using bracket notation.

    `// Setup`  
    var myArray = [50,60,70];

    `// Only change code below this line`  
    var myData = myArray[0];
___
39. Modify Array Data With Indexes  

    *Unlike strings, the entries of arrays are mutable and can be changed freely.*

    **Example**

    >var ourArray = [50,40,30];  
    ourArray[0] = 15; // equals [15,40,30]  

        Note:
        There shouldn't be any spaces between the array name and the square brackets, like array [0]. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the data stored at index 0 of myArray to a value of 45.

    `// Setup `   
    var myArray = [18,64,99];

    `// Only change code below this line`  
    myArray[0] = 45;
___
40. Access Multi-Dimensional Arrays With Indexes  

    *One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outer-most (the first level) array, and each additional pair of brackets refers to the next level of entries inside.*

    **Example**

    >var arr = [  
         	&nbsp;&nbsp;&nbsp;&nbsp;[1,2,3],  
            &nbsp;&nbsp;&nbsp;&nbsp;[4,5,6],  
            &nbsp;&nbsp;&nbsp;&nbsp;[7,8,9],  
            &nbsp;&nbsp;&nbsp;&nbsp;[[10,11,12], 13, 14]  
    ];  
    &nbsp;&nbsp;&nbsp;&nbsp;arr[3]; // equals [[10,11,12], 13, 14]  
    &nbsp;&nbsp;&nbsp;&nbsp;arr[3][0]; // equals [10,11,12]  
    &nbsp;&nbsp;&nbsp;&nbsp;arr[3][0][1]; // equals 11  

    **Note:**  
    There shouldn't be any spaces between the array name and the square brackets, like `array [0][0]` and even this `array [0] [0]` is not allowed. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Using bracket notation select an element from myArray such that myData is equal to 8.

    `// Setup`   
    var myArray = [[1,2,3], [4,5,6], [7,8,9], [[10,11,12], 13, 14]];

    `// Only change code below this line`  
    var myData = myArray[2][1];
___
41. Manipulate Arrays With push()  
    An easy way to append data to the end of an array is via the **`push()`** function.

    **`.push()`** takes one or more parameters and "pushes" them onto the end of the array.

    **Examples:**

    >var arr1 = [1,2,3];  
    arr1.push(4);  
    // arr1 is now [1,2,3,4]  

    >var arr2 = ["Stimpson", "J", "cat"];  
    arr2.push(["happy", "joy"]);  
    // arr2 now equals ["Stimpson", "J", "cat",  ["happy", "joy"]]

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Push ["dog", 3] onto the end of the myArray variable.

        // Setup  
        var myArray = [["John", 23], ["cat", 2]];

        // Only change code below this line  
        myArray.push(["dog", 3]);
___
42. Manipulate Arrays With pop()  

    *Another way to change the data in an array is with the **`.pop`**() function.*

    **`.pop()`** is used to "pop" a value off of the end of an array. We can store this "popped off" value by assigning it to a variable. In other words, .pop() removes the last element from an array and returns that element.

    *Any type of entry can be "popped" off of an array - numbers, strings, even nested arrays.*

    >var threeArr = [1, 4, 6];  
    var oneDown = threeArr.pop();  
    console.log(oneDown); // Returns 6  
    console.log(threeArr); // Returns [1, 4]  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the .pop() function to remove the last item from myArray, assigning the "popped off" value to removedFromMyArray.

        // Setup
        var myArray = [["John", 23], ["cat", 2]];

        // Only change code below this line
        var removedFromMyArray = myArray.pop();
___
43. Manipulate Arrays With shift()   

    *pop() always removes the last element of an array. What if you want to remove the first?*

    That's where **`.shift()`** comes in. It works just like .pop(), except it removes the first element instead of the last.

    **Example:**

    >var ourArray = ["Stimpson", "J", ["cat"]];  
    var removedFromOurArray = ourArray.shift();  
    // removedFromOurArray now equals "Stimpson" and ourArray now equals ["J", ["cat"]].

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the **`.shift()`** function to remove the first item from myArray, assigning the "shifted off" value to removedFromMyArray.  

        // Setup    
        var myArray = [["John", 23], ["dog", 3]];  

        // Only change code below this line  
        var removedFromMyArray = myArray.shift();
___
44. Manipulate Arrays With unshift() 

    Not only can you shift elements off of the beginning of an array, you can also unshift elements to the beginning of an array i.e. add elements in front of the array.

    **`.unshift()`** works exactly like .push(), but instead of adding the element at the end of the array, **`unshift()`** adds the element at the beginning of the array.

    **Example:**

    >var ourArray = ["Stimpson", "J", "cat"];  
    ourArray.shift(); // ourArray now equals ["J", "cat"]  
    ourArray.unshift("Happy");  
    // ourArray now equals ["Happy", "J", "cat"]  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add ["Paul",35] to the beginning of the myArray variable using unshift().

        // Setup
        var myArray = [["John", 23], ["dog", 3]];
        myArray.shift();

        // Only change code below this line
        myArray.unshift(["Paul",35]);
___
45. Shopping List    

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a shopping list in the variable **`myList`**. The list should be a multi-dimensional array containing several sub-arrays.

    The first element in each sub-array should contain a string with the name of the item. The second element should be a number representing the quantity i.e.

    >["Chocolate Bar", 15]

    There should be at least 5 sub-arrays in the list.

    >var **`myList`** = [["Chocolate Bar", 15],["coffee", 18],["cake", 9],["Salad Bar", 1]];
___
46. Write Reusable JavaScript with Functions

    *In JavaScript, we can divide up our code into reusable parts called functions.*

    Here's an example of a function:

        function functionName() {  
           console.log("Hello World");  
        }  

    You can call or `invoke` this function by using its name followed by parentheses, like this: `functionName();` Each time the function is called it will print out the message `"Hello World"` on the dev console. All of the code between the curly braces will be executed every time the function is called.     


     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a function called reusableFunction which prints "Hi World" to the dev console.  
     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Call the   function.  

        function reusableFunction() {  
            console.log("Hi World");  
        }  

        reusableFunction()
___
47. Passing Values to Functions with Arguments  

    Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)*Here is a function with two parameters, `param1` and `param2`:*

        function testFun(param1, param2) {  
        console.log(param1, param2);  
        }
    
    Then we can call `testFun`: `testFun("Hello", "World");` We have passed two arguments, `"Hello"` and `"World"`. Inside the function, `param1` will equal "Hello" and `param2` will equal "World". Note that you could call `testFun` again with different arguments and the parameters would take on the value of the new arguments.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a function called functionWithArgs that accepts two arguments and outputs their sum to the dev console.  
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Call the function with two numbers as arguments.

        function functionWithArgs(num1, num2){  
             return num1+num2;  
        }  

        functionWithArgs(1, 2)  //call function -> return 3  
        functionWithArgs(7, 9)  //call function -> return 16
___
48. Global Scope and Functions   

    In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.

     *which are used without the **`var`** keyword are automatically created in the **`global`** scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with **`var`**.*

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Using **`var`**, declare a **`global`** variable named myGlobal outside of any function. Initialize it with a value of **`10`**.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Inside function **`fun1`**, assign **`5`** to **`oopsGlobal`** **without** using the **`var`** keyword.

        // Declare the myGlobal variable below this line
        var myGlobal = 10;

        function fun1() {  
            // Assign 5 to oopsGlobal Here  
            oopsGlobal = 5;  
        }  

        // Only change code above this line  

        function fun2() {  
             var output = "";
             if (typeof myGlobal != "undefined") {  
                output += "myGlobal: " + myGlobal;  
             }  
             if (typeof oopsGlobal != "undefined") {  
                output += " oopsGlobal: " + oopsGlobal;  
             }  
            console.log(output);  
        }
___
49. Local Scope and Functions  

    Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

    *Here is a function **`myTest`** with a local variable called **`loc`**.*

        function myTest() {
            var loc = "foo";
            console.log(loc);
        }
        myTest(); // logs "foo"
        console.log(loc); // loc is not defined

    <mark>**loc**</mark> is not defined outside of the function.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)The editor has two console.logs to help you see what is happening. Check the console as you code to see how it changes. Declare a local variable myVar inside myLocalScope and run the tests.

    **`Note:`** The console will still have 'ReferenceError: myVar is not defined', but this will not cause the tests to fail.

        function myLocalScope() {
            'use strict';

        // Only change code below this line
        var myVar = 'use strict';
        console.log('inside myLocalScope', myVar);
        }
        myLocalScope();

        // Run and check the console
        // myVar is not defined outside of myLocalScope
        console.log('outside myLocalScope', myVar);
___
50. Global vs. Local Scope in Functions  

    *It is possible to have both **`local`** and **`global`** variables with the same name. When you do this, the local variable takes precedence over the global variable.*

    **In this example:**

        var someVar = "Hat";
        function myFun() {
            var someVar = "Head";
            return someVar;
        }

    The function **`myFun`** will return **`"Head"`** because the **`local`** version of the variable is present.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)*Add a local variable to **`myOutfit`** function to override the value of **`outerWear`** with **`"sweater"`**.*

        // Setup
        var outerWear = "T-Shirt";

        function myOutfit() {
        // Only change code below this line
         var outerWear = "sweater" ;


        // Only change code above this line
            return outerWear;
        }

        myOutfit();   //return "sweater" in local scope
___
51. Return a Value from a Function with Return  

    *We can pass values into a function with arguments. You can use a **`return`** statement to send a value back out of a function.*

    **Example**

        function plusThree(num) {
            return num + 3;
        }
        var answer = plusThree(5); // 8

    **`plusThree`** takes an argument for **`num`** and returns a value equal to **`num + 3`**.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a function **`timesFive`** that accepts one argument, multiplies it by **`5`**, and returns the new value. See the last line in the editor for an example of how you can test your **`timesFive`** function.

        function timesFive(num) {
             return num*5;
        }

        var answer = timesFive(5); // 25
        var answer = timesFive(2); // 10
___
52. Understanding Undefined Value returned from a Function  

    A function can include the **`return`** statement but it does not have to. In the case that the function doesn't have a **`return`** statement, when you call it, the function processes the inner code but the returned value is **`undefined`**.

    **Example**

        var sum = 0;
        function addSum(num) {
            sum = sum + num;
        }
        addSum(3); // sum will be modified but returned value is undefined
    
    **`addSum`** is a function without a **`return`** statement. The function will change the global **`sum`** variable but the returned value of the function is **`undefined`**.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a function **`addFive`** without any arguments. This function adds 5 to the **`sum`** variable, but its returned value is **`undefined`**.

        // Setup
        var sum = 0;

        function addThree() {
        sum = sum + 3;
        }

        // Only change code below this line
        function addFive() {
        sum = sum + 5;
        }

        // Only change code above this line

        addThree();
        addFive();
___
53. Assignment with a Returned Value  

    If you'll recall from our discussion of <u>Storing Values with the Assignment Operator</u>, everything to the right of the equal sign is resolved before the value is assigned. This means we can take the return value of a function and assign it to a variable.

    *Assume we have pre-defined a function **`sum`** which adds two numbers together, then:*
    
    >ourSum = sum(5, 12);

    will call **`sum`** function, which returns a value of **`17`** and assigns it to **`ourSum`** variable.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Call the processArg function with an argument of 7 and assign its return value to the variable processed.
    // Setup
        var processed = 0;

        function processArg(num) {
            return (num + 3) / 5;
        }       

        // Only change code below this line
        processed = processArg(7);   //2
___
54. Stand in Line  

    In Computer Science a queue is an abstract *Data Structure* where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Write a function **`nextInLine`** which takes an array (**`arr`**) and a number (**`item`**) as arguments.

    *Add the number to the end of the array, then remove the first element of the array.*

    The **`nextInLine`** function should then return the element that was removed.

        function nextInLine(arr, item) {
             // Only change code below this line
             arr.push(item);
  
            return arr.shift();
            // Only change code above this line
        }

        // Setup
        var testArr = [1,2,3,4,5];

        // Display code
        console.log("Before: " + JSON.stringify(testArr));
        console.log(nextInLine(testArr, 6));
        console.log("After: " + JSON.stringify(testArr));
___
55. Understanding Boolean Values  

    *Another data type is the Boolean. Booleans may only be one of two values: true or false. They are basically little on-off switches, where true is "on" and false is "off." These two states are mutually exclusive.*

    **Note**
    **`Boolean`** values are never written with quotes. The **`strings "true"`** and **`"false"`** are not **`Boolean`** and have no special meaning in JavaScript.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the **`welcomeToBooleans`** function so that it returns **`true`** instead of **`false`** when the run button is clicked.

        function welcomeToBooleans() {

            // Only change code below this line

            return true; // Change this line

            // Only change code above this line
        }
___
56. Use Conditional Logic with If Statements  

    **`If`** statements are used to make decisions in code. The keyword if tells JavaScript to execute the code in the curly braces under certain conditions, defined in the parentheses. These conditions are known as **`Boolean`** conditions and they may only be **`true`** or **`false`**.

    *When the condition evaluates to **`true`**, the program executes the statement inside the curly braces. When the Boolean condition evaluates to **`false`**, the statement inside the curly braces will not execute.*

    **Pseudocode**

        if (condition is true) {
             statement is executed
        }
    
    **Example**

        function test (myCondition) {
            if (myCondition) {
                return "It was true";
            }
            return "It was false";
        }
        test(true);  // returns "It was true"
        test(false); // returns "It was false"

    When **`test`** is called with a value of **`true`**, the **`if`** statement evaluates **`myCondition`** to see if it is **`true`** or not. Since it is **`true`**, the function returns **`"It was true"`**. When we call **`test`** with a value of **`false`**, **`myCondition`** is not **`true`** and the statement in the curly braces is not executed and the function returns **`"It was false"`**.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create an **`if`** statement inside the function to return **`"Yes, that was true"`** if the parameter **`wasThatTrue`** is true and return **`"No, that was false" otherwise.`**

        function trueOrFalse(wasThatTrue) {
            // Only change code below this line
  
            if (wasThatTrue) {
            return "Yes, that was true";
            }
            return "No, that was false";

            // Only change code above this line

        }
___
57. Comparison with the Equality Operator  

    There are many comparison operators in JavaScript. All of these operators return a boolean **`true`** or **`false`** value.

    The most basic operator is the equality operator **`==`**. The equality operator compares two values and returns **`true`** if they're equivalent or **`false`** if they are not. Note that equality is different from assignment (**`=`**), which assigns the value on the right of the operator to a variable on the left.

        function equalityTest(myVal) {  
            if (myVal == 10) {  
                return "Equal";  
            }  
            return "Not Equal";  
        } 

    If myVal is equal to 10, the equality operator returns true, so the code in the curly braces will execute, and the function will return "Equal". Otherwise, the function will return "Not Equal". In order for JavaScript to compare two different data types (for example, numbers and strings), it must convert one type to another. This is known as "Type Coercion". Once it does, however, it can compare terms as follows:

        1   ==  1   // true
        1   ==  2   // false
        1   == '1'  // true
        "3" ==  3   // true

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the equality operator to the indicated line so that the function will return "Equal" when val is equivalent to 12.

        // Setup
        function testEqual(val) {
            if (val == 12) { // Change this line
            return "Equal";
            }
            return "Not Equal";
        }

        testEqual(10);
___
58. Comparison with the Strict Equality Operator  

    Strict equality (**===**) is the counterpart to the equality operator (**==**). However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

    *If the values being compared have different types, they are considered unequal, and the strict equality operator will return false.*

    **Examples**

        3 ===  3   // true
        3 === '3'  // false

    In the second example, **`3`** is a **`Number`** type and **`'3'`** is a **`String`** type.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the strict equality operator in the **`if`** statement so the function will return **`"Equal"`** when val is strictly equal to **`7`**

        // Setup
        function testStrict(val) {
            if (val === 7) { // Change this line
            return "Equal";
            }
            return "Not Equal";
        }

        testStrict(10);
___
59. Practice comparing different values  

    *In the last two challenges, we learned about the equality operator (**`==`**) and the strict equality operator (**`===`**). Let's do a quick review and practice using these operators some more.*

    If the values being compared are not of the same type, the equality operator will perform a type conversion, and then evaluate the values. However, the strict equality operator will compare both the data type and value as-is, without converting one type to the other.

    **Examples**

        3 == '3'  // returns true because JavaScript performs type conversion from string to number
        3 === '3' // returns false because the types are different and type conversion is not performed

    **Note**

    In JavaScript, you can determine the type of a variable or a value with the **`typeof`** operator, as follows:

        typeof 3   // returns 'number'
        typeof '3' // returns 'string'
        
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)The **`compareEquality`** function in the editor compares two values using the equality operator. Modify the function so that it returns "Equal" only when the values are strictly equal.

        // Setup
        function compareEquality(a, b) {
            if (a === b) { // Change this line
            return "Equal";
            }
            return "Not Equal";
        }

        compareEquality(10, "10");  //"Not Equal"
___
60. Comparison with the Inequality Operator  

    The inequality operator (**!=**) is the opposite of the equality operator. It means "Not Equal" and returns **`false`** where equality would return **`true`** and vice versa. Like the equality operator, the inequality operator will convert data types of values while comparing.

    **Examples**

        1 !=  2     // true
        1 != "1"    // false
        1 != '1'    // false
        1 != true   // false
        0 != false  // 
        
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the inequality operator **`!=`** in the **`if`** statement so that the function will return "Not Equal" when **`val`** is not equivalent to **`99`**

        // Setup
        function testNotEqual(val) {
            if (val != 99) { // Change this line
            return "Not Equal";
            }
        return "Equal";
        }

        testNotEqual(10);  
___
61. Comparison with the Strict Inequality Operator  

    The strict inequality operator (**!==**) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns **`false`** where strict equality would return **`true`** and vice versa. Strict inequality will not convert data types.

    **Examples**

        3 !==  3   // false
        3 !== '3'  // true
        4 !==  3   // true

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Add the strict inequality operator to the **`if`** statement so the function will return "Not Equal" when **`val`** is not strictly equal to **`17`**

        // Setup
        function testStrictNotEqual(val) {
            if (val !== 17) { // Change this line
            return "Not Equal";
            }
            return "Equal";
        }

        testStrictNotEqual(10);
___
62. Comparison with the Greater Than Operator  

    The greater than operator (**>**) compares the values of two numbers. If the number to the left is greater than the number to the right, it returns **`true`**. Otherwise, it returns **`false`**.

    *Like the equality operator, greater than operator will convert data types of values while comparing.*

    **Examples**

        5   >  3   // true
        7   > '3'  // true
        2   >  3   // false
        '1' >  9   // false

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the greater than operator to the indicated lines so that the return statements make sense.

        function testGreaterThan(val) {
        if (val > 100) {  // Change this line
            return "Over 100";
        }

        if (val > 10) {  // Change this line
            return "Over 10";
        }

        return "10 or Under";
        }

        testGreaterThan(10);
___
63. Comparison with the Greater Than Or Equal To Operator  

    The greater than or equal to operator (**>=**) compares the values of two numbers. If the number to the left is greater than or equal to the number to the right, it returns **`true`**. Otherwise, it returns **`false`**.

    *Like the equality operator, greater than or equal to operator will convert data types while comparing.*

    **Examples**

        6   >=  6   // true
        7   >= '3'  // true
        2   >=  3   // false
        '7' >=  9   // false

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the greater than or equal to operator to the indicated lines so that the return statements make sense.

        function testGreaterOrEqual(val) {
        if (val >= 20) {  // Change this line
            return "20 or Over";
        }

        if (val >= 10) {  // Change this line
            return "10 or Over";
        }

        return "Less than 10";
        }

        testGreaterOrEqual(10);

___
64. Comparison with the Less Than Operator  

    The less than operator (<) compares the values of two numbers. If the number to the left is less than the number to the right, it returns true. Otherwise, it returns false. Like the equality operator, less than operator converts data types while comparing.

    **Examples**

        2 < 5 // true   
        '3' < 7 // true 
        5 < 5 // false 
        3 < 2 // false 
        '8' < 4 // false

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the less than operator to the indicated lines so that the return statements make sense.

        function testLessThan(val) {
            if (val < 25) {  // Change this line
            return "Under 25";
            }

            if (val < 55) {  // Change this line
            return "Under 55";
            }

            return "55 or Over";
        }

        testLessThan(10);
___
65. Comparison with the Less Than Or Equal To Operator   

    The less than or equal to operator (**<=**) compares the values of two numbers. If the number to the left is less than or equal to the number to the right, it returns **`true`**. If the number on the left is greater than the number on the right, it returns **`false`**. Like the equality operator, **`less than or equal`** to converts data types.

    **Examples**

        4   <= 5  // true
        '7' <= 7  // true
        5   <= 5  // true
        3   <= 2  // false
        '8' <= 4  // false
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the less than or equal to operator to the indicated lines so that the return statements make sense.

        function testLessOrEqual(val) {
            if (val <= 12) {  // Change this line
                return "Smaller Than or Equal to 12";
            }

            if (val <= 24) {  // Change this line
                return "Smaller Than or Equal to 24";
            }

            return "More Than 24";
        }

        testLessOrEqual(10);
___
66. Comparisons with the Logical And Operator  

    *Sometimes you will need to test more than one thing at a time. The logical and operator (**&&**) returns true if and only if the operands to the left and right of it are **`true`**.*

    The same effect could be achieved by nesting an if statement inside another if:

        if (num > 5) {
            if (num < 10) {
                return "Yes";
            }
        }
        return "No";
    will only return "Yes" if **`num`** is greater than **`5`** and less than **`10`**. The same logic can be written as:

        if (num > 5 && num < 10) {
            return "Yes";
        }   
        return "No";

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Replace the two if statements with one statement, using the && operator, which will return **`"Yes"`** if **`val`** is less than or equal to **50** and greater than or equal to **25**. Otherwise, will return **`"No"`**.

        function testLogicalAnd(val) {
        // Only change code below this line

            if (val <= 50 && val >= 25) {
                return "Yes";
            }

        // Only change code above this line
            return "No";
        }

        testLogicalAnd(10);

___
67. Comparisons with the Logical Or Operator  

    The logical or operator (**||**) returns **`true`** if either of the operands is **`true`**. Otherwise, it returns **`false`**.

    The logical or operator is composed of two pipe symbols: (**||**). This can typically be found between your Backspace and Enter keys.

    *The pattern below should look familiar from prior waypoints:*

        if (num > 10) {
            return "No";
        }
        if (num < 5) {
            return "No";
        }
            return "Yes";

    will return "Yes" only if **`num`** is between **`5`** and **`10`** (5 and 10 included). The same logic can be written as:

        if (num > 10 || num < 5) {
          return "No";
        }
          return "Yes";
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Combine the two **`if`** statements into one statement which returns **`"Outside"`** if **`val`** is not between **10** and **20**, inclusive. Otherwise, return **`"Inside"`**.

        function testLogicalOr(val) {
            // Only change code below this line

            if (val > 20 || val < 10) {
                return "Outside";
            }


            // Only change code above this line
            return "Inside";
        }

        testLogicalOr(15);
___
68. Introducing Else Statements  

    When a condition for an <mark>if</mark> statement is true, the block of code following it is executed. What about when that condition is false? Normally nothing would happen. With an <mark>else</mark> statement, an alternate block of code can be executed.

        if (num > 10) {
        return "Bigger than 10";
        } else {
        return "10 or Less";
        }

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Combine the **`if`** statements into a single **`if/else`** statement.

        function testElse(val) {
        var result = "";
        // Only change code below this line

            if (val > 5) {
                result = "Bigger than 5";
            } else {
                result = "5 or Smaller";
            }

            // Only change code above this line
            return result;
        }

        testElse(4);
___
69. Introducing Else If Statements  

    If you have multiple conditions that need to be addressed, you can chain **`if`** statements together with **`else if`** statements.

        if (num > 15) {
            return "Bigger than 15";
        } else if (num < 5) {
            return "Smaller than 5";
        } else {
            return "Between 5 and 15";
        }
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the logic to use **`else if`** statements.

        function testElseIf(val) {
            if (val > 10) {
                return "Greater than 10";
            } else if (val < 5) {
                return "Smaller than 5";
            } else {
                return "Between 5 and 10";
            }
        }
        testElseIf(7);
___
70. Logical Order in If Else StatementsPassed  

    Order is important in **`if`**, **`else if`** statements.

    The function is executed from top to bottom so you will want to be careful of what statement comes first.

    Take these two functions as an example.

    **Here's the first:**

        function foo(x) {
        if (x < 1) {
            return "Less than one";
        } else if (x < 2) {
            return "Less than two";
        } else {
            return "Greater than or equal to two";
        }
        }
    And the second just switches the order of the statements:

        function bar(x) {
        if (x < 2) {
            return "Less than two";
        } else if (x < 1) {
            return "Less than one";
        } else {
            return "Greater than or equal to two";
        }
        }
    While these two functions look nearly identical if we pass a number to both we get different outputs.

        foo(0) // "Less than one"  
        bar(0) // "Less than two"  

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the order of logic in the function so that it will return the correct statements in all cases.

        function orderMyLogic(val) {
        if (val < 5) {
            return "Less than 5";
        } else if (val < 10) {
            return "Less than 10";
        } else {
            return "Greater than or equal to 10";
        }
        }

        orderMyLogic(7);
___
71. Chaining If Else Statements  

    **`if/else`** statements can be chained together for complex logic. Here is pseudocode of multiple chained **`if / else if`** statements:

        if (condition1) {
        statement1
        } else if (condition2) {
        statement2
        } else if (condition3) {
        statement3
        . . .
        } else {
        statementN
        }
     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Write chained if/else if statements to fulfill the following conditions:

    **num < 5** - return "Tiny"  
    **num < 10** - return "Small"  
    **num < 15** - return "Medium"  
    **num < 20** - return "Large"  
    **num >= 20** - return "Huge"  

        function testSize(num) {
            // Only change code below this line
            if (num < 5) {
                return "Tiny";
            } else if (num < 10) {
                return "Small";
            } else if (num < 15) {
                return "Medium";
            } else if (num < 20) {
                return "Large";
            } else if (num >= 20) {
                return "Huge";
            } 
            // Only change code above this line
        }

        testSize(7);
___
72. Golf Code  

    In the game of golf each hole has a **`par`** meaning the average number of **`strokes`** a golfer is expected to make in order to sink the ball in a hole to complete the play. Depending on how far above or below **`par`** your **`strokes`** are, there is a different nickname.

    *Your function will be passed **`par`** and **`strokes`** arguments. Return the correct string according to this table which lists the strokes in order of priority; top (highest) to bottom (lowest):*

    |Strokes  |  Return  |  
    |:-----------:|:----------:|
    |1|"Hole-in-one!"|
    |<= par - 2|"Eagle"|
    |par - 1|"Birdie"|
    |par|"Par|
    |par + 1|"Bogey"|
    |par + 2|"Double Bogey"|
    |>= par + 3|"Go Home!"|

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)**`par`** and **`strokes`** will always be numeric and positive. We have added an array of all the names for your convenience.

        var names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

        function golfScore(par, strokes) {

            // Only change code below this line
            if (strokes == 1) {
            return names[0];
            } else if (strokes <= par - 2) {
            return names[1];
            } else if (strokes == par - 1) {
            return names[2];
            } else if (strokes == par) {
            return names[3];
            } else if (strokes == par + 1) {
            return names[4];
            } else if (strokes == par + 2) {
            return names[5];
            } else if (strokes >= par + 3) {
            return names[6];
            }
            // Only change code above this line
        }

        golfScore(5, 4);
 ___
73. Selecting from Many Options with Switch Statements  

    If you have many options to choose from, use a **`switch`** statement. A switch statement tests a value and can have many case statements which define various possible values. Statements are executed from the first matched **`case`** value until a **`break`** is encountered.

    _**Here is an example of a switch statement:**_

        switch(lowercaseLetter) {
            case "a":
                console.log("A");
                break;
            case "b":
                console.log("B");
                break;
        }
    **`case`** values are tested with strict equality (**===**). The **`break`** tells JavaScript to stop executing statements. If the **`break`** is omitted, the next statement will be executed.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Write a switch statement which tests **`val`** and sets **`answer`** for the following conditions:

    <mark> 1 </mark> - "alpha"  
    <mark> 2 </mark> - "beta"  
    <mark> 3 </mark> - "gamma"  
    <mark> 4 </mark> - "delta"  

        function caseInSwitch(val) {
            var answer = "";
            // Only change code below this line
            switch(val) {
                case 1:
                return "alpha";
                break;
                case 2:
                return "beta";
                break;
                case 3:
                return "gamma";
                break;
                case 4:
                return "delta";
                break;
            }
            // Only change code above this line
            return answer;
        }

        caseInSwitch(1);
___
74. Adding a Default Option in Switch Statements  

    In a **`switch`** statement you may not be able to specify all possible values as **`case`** statements. Instead, you can add the **`default`** statement which will be executed if no matching **`case`** statements are found. Think of it like the final **`else`** statement in an **`if/else`** chain.

    *A default statement should be the last case.*

        switch (num) {
            case value1:
                statement1;
                break;
            case value2:
                statement2;
                break;
            ...
            default:
                defaultStatement;
                break;
        }

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Write a switch statement to set answer for the following conditions:

    <mark> "a" </mark> **- "apple"**  
    <mark> "b" </mark> **- "bird"**  
    <mark> "c" </mark> **- "cat"**  
    <mark> default </mark> **- "stuff"**  

        function switchOfStuff(val) {
            var answer = "";
            // Only change code below this line
            switch (val) {
                case "a":
                    return "apple";
                    break;
                case "b":
                    return "bird";
                    break;
                case "c":
                    return "cat";
                    break;
                default:
                    return "stuff";
                    break;
            }
            // Only change code above this line
            return answer;
        }

        switchOfStuff(1);
___
75. Multiple Identical Options in Switch Statements  

    If the **`break`** statement is omitted from a **`switch`** statement's **`case`**, the following **`case`** statement(s) are executed until a **`break`** is encountered. If you have multiple inputs with the same output, you can represent them in a **`switch`** statement like this:

        switch(val) {
            case 1:
            case 2:
            case 3:
                result = "1, 2, or 3";
                break;
            case 4:
                result = "4 alone";
        }

    *Cases for 1, 2, and 3 will all produce the same result.*

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Write a switch statement to set **`answer`** for the following ranges:

    <mark> 1-3 </mark> **- "Low"**  
    <mark> 4-6 </mark> **- "Mid"**  
    <mark> 7-9 </mark> **- "High"**  

    **Note:**  You will need to have a **`case`** statement for each number in the range.

        function sequentialSizes(val) {
            var answer = "";
            // Only change code below this line
            switch(val) {
                case 1:
                case 2:
                case 3:
                    return "Low";
                    break;
                case 4:
                case 5:
                case 6:
                    return "Mid";
                    break;
                case 7:
                case 8:
                case 9:
                    return "High";
                    break;
            }
            // Only change code above this line
            return answer;
        }  
        sequentialSizes(1);
___
76. Replacing If Else Chains with Switch  

    If you have many options to choose from, a **`switch`** statement can be easier to write than many chained **`if/else if`** statements. The following:

        if (val === 1) {
            answer = "a";
            } else if (val === 2) {
                answer = "b";
                } else {
                    answer = "c";
                }

    *can be replaced with:*

        switch(val) {
            case 1:
                answer = "a";
                break;
            case 2:
                answer = "b";
                break;
            default:
                answer = "c";
        }

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the chained **`if/else if`** statements into a **`switch`** statement.

        function chainToSwitch(val) {
            var answer = "";
            // Only change code below this line

            switch(val) {
                case "bob":
                    return "Marley";
                    break;
                case 42:
                    return "The Answer";
                    break;
                case 1: 
                    return "There is no #1";
                    break;
                case 99:
                    return "Missed me by this much!";
                    break;
                case 7:
                    return "Ate Nine";
                    break;
            }
            
            // Only change code above this line
            return answer;
        }

        chainToSwitch(7);
___
77. Returning Boolean Values from Functions  

    You may recall from <u>Comparison with the Equality Operator</u> that all *comparison operators return a boolean **`true`** or **`false`** value.

    *Sometimes people use an if/else statement to do a comparison, like this:*

        function isEqual(a,b) {
            if (a === b) {
                return true;
            } else {
                return false;
            }
        }
    But there's a better way to do this. Since **`===`** returns **`true`** or **`false`**, we can return the result of the comparison:

        function isEqual(a,b) {
            return a === b;
        }

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Fix the function **`isLess`** to remove the **`if/else`** statements.

        function isLess(a, b) {
            // Only change code below this line
                return a<b ;
            
            // Only change code above this line
        }

        isLess(10, 15);
___
78. Return Early Pattern for Functions  

    When a **`return`** statement is reached, the execution of the current function stops and control returns to the calling location.

    **Example**

        function myFun() {
            console.log("Hello");
            return "World";
            console.log("byebye")
        }
        myFun();

    The above outputs "Hello" to the console, returns "World", but **`"byebye"`** is never output, because the function exits at the **`return`** statement.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the function **abTest** so that if **a** or **b** are less than **0** the function will immediately exit with a value of **undefined**.

    **Hint**:
    Remember that <u>**`undefined`** is a keyword</u>, not a string.

        // Setup
        function abTest(a, b) {
            // Only change code below this line

            if (a < 0 || b < 0) {
                return undefined;
            }

            // Only change code above this line

            return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
        }

        abTest(2,2);
___
79. Counting Cards  

    *In the casino game Blackjack, a player can gain an advantage over the house by keeping track of the relative number of high and low cards remaining in the deck. This is called <u>Card Counting</u>.*

    Having more high cards remaining in the deck favors the player. Each card is assigned a value according to the table below. When the count is positive, the player should bet high. When the count is zero or negative, the player should bet low.

    |Count Change	  |  Cards  |  
    |:-----------:|:--------------:|
    |+1|2, 3, 4, 5, 6|
    |0|7, 8, 9|
    |-1|10, 'J', 'Q', 'K', 'A'|

    *You will write a card counting function. It will receive a **`card`** parameter, which can be a number or a string, and increment or decrement the global **`count`** variable according to the card's value (see table). The function will then return a string with the current count and the string **`Bet`** if the count is positive, or **`Hold`** if the count is zero or negative. The current count and the player's decision (Bet or Hold) should be separated by a single space.*

    **Example Output**  
    <mark> -3 Hold </mark>  
    <mark> 5 Bet </mark>

    >**Hint**  
    Do NOT reset <mark>count</mark> to 0 when value is 7, 8, or 9.  
    Do NOT return an array.  
    Do NOT include quotes (single or double) in the output.

        var count = 0;

        function cc(card) {
            // Only change code below this line
            
            switch(card) {
                case 2:
                case 3:
                case 4:
                case 5:
                case 6:
                    count ++;
                    break;
                case 10:
                case "J":
                case "Q":
                case "K":
                case "A":
                    count --;
                    break;
            }
            if (count > 0) {
                return `${count} Bet`;
            } else {
                return `${count} Hold`;
            }

            // Only change code above this line
        }

        cc(2); cc(3); cc(7); cc('K'); cc('A')
___
80. Build JavaScript Objects  

    You may have heard the term **`object`** before.

    Objects are similar to **`arrays`**, except that instead of using indexes to access and modify their data, you access the data in objects through what are called **`properties`**.

    *Objects are useful for storing data in a structured way, and can represent real world objects, like a cat.*

    **Here's a sample cat object:**

        var cat = {
            "name": "Whiskers",
            "legs": 4,
            "tails": 1,
            "enemies": ["Water", "Dogs"]
        };
    In this example, all the properties are stored as strings, such as - **`"name"`**, **`"legs"`**, and **`"tails"`**. However, you can also use numbers as properties. You can even omit the quotes for single-word string properties, as follows:

        var anotherObject = {
            make: "Ford",
            5: "five",
            "model": "focus"
        };
    However, if your object has any non-string properties, JavaScript will automatically typecast them as strings.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Make an object that represents a dog called **`myDog`** which contains the properties **`"name"`** (a string), **`"legs"`**, **`"tails"`** and **`"friends"`**.

    You can set these object properties to whatever values you want, as long as **`"name"`** is a string, **`"legs"`** and **`"tails"`** are numbers, and **`"friends"`** is an array.

        var myDog = {
            // Only change code below this line
            "name": "Choby",
            "legs": 4,
            "tails": 1,
            "friends":  ["Bob", "Lucy", 'Bubu']
            // Only change code above this line
        };
___
81. Accessing Object Properties with Dot Notation  

    There are two ways to access the properties of an object: dot notation (<mark> **.** </mark>) and bracket notation (<mark> **[ ]** </mark>), similar to an array.

    Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

    *Here is a sample of using dot notation (<mark> **.** </mark>) to read an object's property:*

        var myObj = {
            prop1: "val1",
            prop2: "val2"
        };
        var prop1val = myObj.prop1; // val1
        var prop2val = myObj.prop2; // val2

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Read in the property values of **`testObj`** using dot notation. Set the variable **`hatValue`** equal to the object's property **`hat`** and set the variable **`shirtValue`** equal to the object's property **`shirt`**.

        // Setup
            var testObj = {
            "hat": "ballcap",
            "shirt": "jersey",
            "shoes": "cleats"
        };

        // Only change code below this line

        var hatValue = testObj.hat;      // Change this line
        var shirtValue = testObj.shirt;    // Change this line
___
82. Accessing Object Properties with Bracket Notation  

    The second way to access the properties of an object is bracket notation (<mark> **[ ]** </mark>). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

    However, you can still use bracket notation on object properties without spaces.

    *Here is a sample of using bracket notation to read an object's property:*

        var myObj = {
            "Space Name": "Kirk",
            "More Space": "Spock",
            "NoSpace": "USS Enterprise"
        };
        myObj["Space Name"]; // Kirk
        myObj['More Space']; // Spock
        myObj["NoSpace"];    // USS Enterprise

    **Note:** that property names with spaces in them must be in quotes (single or double).

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Read the values of the properties **`"an entree"`** and **`"the drink"`** of **`testObj`** using bracket notation and assign them to **`entreeValue`** and **`drinkValue`** respectively. 

        // Setup
        var testObj = {
            "an entree": "hamburger",
            "my side": "veggies",
            "the drink": "water"
        };

        // Only change code below this line

        var entreeValue = testObj["an entree"];   // Change this line
        var drinkValue = testObj["the drink"];    // Change this line
___
83. Accessing Object Properties with Variables  

    Another use of bracket notation on objects is to access a property which is stored as the value of a variable. This can be very useful for iterating through an object's properties or when accessing a lookup table.

    *Here is an example of using a variable to access a property:*

        var dogs = {
            Fido: "Mutt",  Hunter: "Doberman",  Snoopie: "Beagle"
        };
        var myDog = "Hunter";
        var myBreed = dogs[myDog];
        console.log(myBreed); // "Doberman"
        
    Another way you can use this concept is when the property's name is collected dynamically during the program execution, as follows:

        var someObj = {
            propName: "John"
        };
        function propPrefix(str) {
            var s = "prop";
            return s + str;
        }
        var someProp = propPrefix("Name"); // someProp now holds the value 'propName'
        console.log(someObj[someProp]); // "John"
    
    **Note** that we do not use quotes around the variable name when using it to access the property because we are using the value of the variable, not the name.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Set the **`playerNumber`** variable to **`16`**. Then, use the variable to look up the player's name and assign it to **`player`**.

        // Setup
        var testObj = {
            12: "Namath",
            16: "Montana",
            19: "Unitas"
        };

        // Only change code below this line

        var playerNumber = 16;       // Change this line
        var player = testObj[playerNumber];   // Change this line
___
84. Updating Object Properties  

    After you've created a JavaScript object, you can update its properties at any time just like you would update any other variable. You can use either dot or bracket notation to update.

    >For example, let's look at **`ourDog`**:

        var ourDog = {
            "name": "Camper",
            "legs": 4,
            "tails": 1,
            "friends": ["everything!"]
        };
    Since he's a particularly happy dog, let's change his name to "Happy Camper". Here's how we update his object's name property: <mark> ourDog.name = "Happy Camper"; </mark> or <mark> ourDog["name"] = "Happy Camper"; </mark> Now when we evaluate <mark> ourDog.name </mark>, instead of getting "Camper", we'll get his new name, "Happy Camper".

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Update the <mark> myDog </mark> object's name property. Let's change her name from "Coder" to "Happy Coder". You can use either dot or bracket notation.

        // Setup
        var myDog = {
            "name": "Coder",
            "legs": 4,
            "tails": 1,
            "friends": ["freeCodeCamp Campers"]
        };

        // Only change code below this line
        myDog.name = "Happy Coder";
___
85. Add New Properties to a JavaScript Object  

    You can add new properties to existing JavaScript objects the same way you would modify them.

    *Here's how we would add a **`"bark"`** property to **`ourDog`**:*

    ><mark>ourDog.bark = "bow-wow";</mark>

    or

    ><mark>ourDog["bark"] = "bow-wow";<mark>

    Now when we evaluate <mark>ourDog.bark</mark> , we'll get his bark, "bow-wow".

    **Example:**

        var ourDog = {
            "name": "Camper",
            "legs": 4,
            "tails": 1,
            "friends": ["everything!"]
        };

        ourDog.bark = "bow-wow";

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add a <mark>"bark"</mark> property to <mark>myDog</mark> and set it to a dog sound, such as "woof". You may use either dot or bracket notation.

        // Setup
        var myDog = {
            "name": "Happy Coder",
            "legs": 4,
            "tails": 1,
            "friends": ["freeCodeCamp Campers"]
        };

        // Only change code below this line
        myDog.bark = "woof";
___
86. Delete Properties from a JavaScript Object   

    We can also delete properties from objects like this:

    <mark>delete ourDog.bark;</mark>

    **Example:**

        var ourDog = {
            "name": "Camper",
            "legs": 4,
            "tails": 1,
            "friends": ["everything!"],
            "bark": "bow-wow"
        };

        delete ourDog.bark;
    After the last line shown above, <mark>ourDog</mark> looks like:

        {
            "name": "Camper",
            "legs": 4,
            "tails": 1,
            "friends": ["everything!"]
        }
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Delete the <mark>"tails"</mark> property from <mark>myDog</mark>. You may use either dot or bracket notation.

        // Setup
        var myDog = {
            "name": "Happy Coder",
            "legs": 4,
            "tails": 1,
            "friends": ["freeCodeCamp Campers"],
            "bark": "woof"
        };
        delete myDog.tails;
        // Only change code below this line
___
87. Using Objects for Lookups  

    Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to "lookup" values rather than a <mark> switch </mark> statement or an <mark> if/else </mark> chain. This is most useful when you know that your input data is limited to a certain range.

    *Here is an example of a simple reverse alphabet lookup:*

        var alpha = {
            1:"Z",
            2:"Y",
            3:"X",
            4:"W",
            ...
            24:"C",
            25:"B",
            26:"A"
        };
        alpha[2]; // "Y"
        alpha[24]; // "C"

        var value = 2;
        alpha[value]; // "Y"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Convert the switch statement into an object called <mark>lookup</mark>. Use it to look up <mark>val</mark> and assign the associated string to the <mark> result</mark>  variable.

        // Setup
        function phoneticLookup(val) {
            // Only change code below this line
            var lookup = {
                "alpha": "Adams",
                "bravo": "Boston",
                "charlie": "Chicago",
                "delta": "Denver",
                "echo": "Easy",
                "foxtrot": "Frank"
        };

        // Only change code above this line
        return lookup[val];
        }

        phoneticLookup("charlie")
___
88. Testing Objects for Properties  

    Sometimes it is useful to check if the property of a given object exists or not. We can use the <mark>.hasOwnProperty(propname)</mark> method of objects to determine if that object has the given property name. <mark>.hasOwnProperty()</mark> returns <mark>true</mark> or <mark>false</mark> if the property is found or not.

    **Example**

        var myObj = {
            top: "hat",
            bottom: "pants"
        };
        myObj.hasOwnProperty("top");    // true
        myObj.hasOwnProperty("middle"); // false

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify the function <mark>checkObj</mark> to test if an object passed to the function (<mark>obj</mark>) contains a specific property (<mark>checkProp</mark>). If the property is found, return that property's value. If not, return <mark>"Not Found"</mark>.

        function checkObj(obj, checkProp) {
            // Only change code below this line
            return obj.hasOwnProperty(checkProp)? obj[checkProp] : "Not Found";
            // Only change code above this line
        }

        <--test-->
        var myObj = {
            top: "hat",
            bottom: "pants"
        };
        checkObj(myObj, "top")  //"hat"
        checkObj(myObj, "right")  //"Not Found"
___
89. Manipulating Complex Objects  

    Sometimes you may want to store data in a flexible *Data Structure*. A JavaScript object is one way to handle flexible data. They allow for arbitrary combinations of *strings, numbers, booleans, arrays, functions,* and *objects.*

    **Here's an example of a complex data structure:**

        var ourMusic = [
            {
                "artist": "Daft Punk",
                "title": "Homework",
                "release_year": 1997,
                "formats": [ 
                    "CD", 
                    "Cassette", 
                    "LP"
                ],
                "gold": true
            }
        ];
    This is an array which contains one object inside. The object has various pieces of metadata about an album. It also has a nested <mark>"formats"</mark> array. If you want to add more album records, you can do this by adding records to the top level array. Objects hold data in a property, which has a key-value format. In the example above, <mark>"artist": "Daft Punk"</mark> is a property that has a key of <mark>"artist"</mark> and a value of <mark>"Daft Punk"</mark>. <u>JavaScript Object Notation</u> or <mark>JSON</mark> is a related data interchange format used to store data.

        {
            "artist": "Daft Punk",
            "title": "Homework",
            "release_year": 1997,
            "formats": [ 
                "CD",
                "Cassette",
                "LP"
            ],
            "gold": true
        }

    **Note**
    You will need to place a comma after every object in the array, unless it is the last object in the array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add a new album to the <mark>myMusic</mark> array. Add <mark>artist</mark> and <mark>title</mark> strings, <mark>release_year</mark> number, and a <mark>formats</mark> array of strings.

        var myMusic = [
            {
                "artist": "Billy Joel",
                "title": "Piano Man",
                "release_year": 1973,
                "formats": [
                    "CD",
                    "8T",
                    "LP"
                ],
                "gold": true
            },
        // Add a record here
            {
                "artist": "Pair",
                "title": "Drama Love",
                "release_year": 1992,
                "formats": [
                    "Live",
                    "Tunnel",
                    "Jook"
                ]
            }
        ];
___
90. Accessing Nested Objects  

    The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

    **Here is a nested object:**

        var ourStorage = {
        "desk": {
            "drawer": "stapler"
        },
        "cabinet": {
            "top drawer": { 
            "folder1": "a file",
            "folder2": "secrets"
            },
            "bottom drawer": "soda"
        }
        };

        ourStorage.cabinet["top drawer"].folder2;  // "secrets"
        ourStorage.desk.drawer; // "stapler"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Access the <mark>myStorage</mark> object and assign the contents of the <mark>glove box</mark> property to the <mark>gloveBoxContents</mark> variable. Use dot notation for all properties where possible, otherwise use bracket notation.

        // Setup
        var myStorage = {
        "car": {
            "inside": {
                "glove box": "maps",
                "passenger seat": "crumbs"
            },
            "outside": {
                "trunk": "jack"
            }
        }
        };

        var gloveBoxContents = myStorage.car.inside["glove box"]; // Change this line
___
91. Accessing Nested Arrays  

    As we have seen in earlier examples, objects can contain both nested objects and nested arrays. Similar to accessing nested objects, Array bracket notation can be chained to access nested arrays.

    **Here is an example of how to access a nested array:**

        var ourPets = [
            {
                animalType: "cat",
                names: [
                    "Meowzer",
                    "Fluffy",
                    "Kit-Cat"
                ]
            },
            {
                animalType: "dog",
                names: [
                    "Spot",
                    "Bowser",
                    "Frankie"
                ]
            }
        ];

        ourPets[0].names[1]; // "Fluffy"
        ourPets[1].names[0]; // "Spot"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Retrieve the second tree from the variable <mark>myPlants</mark> using object dot and array bracket notation.

        // Setup
        var myPlants = [
            {
                type: "flowers",
                list: [
                    "rose",
                    "tulip",
                    "dandelion"
                ]
            },
            {
                type: "trees",
                list: [
                    "fir",
                    "pine",
                    "birch"
                ]
            }
        ];

        // Only change code below this line

        var secondTree = myPlants[1].list[1]; // Change this line

___
92. Record Collection  

    You are given a JSON object representing a part of your musical album collection. Each album has several properties and a unique id number as its key. Not all albums have complete information.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)You start with an <mark>updateRecords</mark> function that takes an object like <mark>collection</mark>, an <mark>id</mark>, a <mark>prop</mark> (like <mark>artist</mark> or <mark>tracks</mark>), and a <mark>value</mark>. Complete the function using the rules below to modify the object passed to the function.

    * Your function must always return the entire object.  
    * If <mark>prop</mark> isn't <mark>tracks</mark> and <mark>value</mark> isn't an empty string, update or set that album's <mark>prop</mark> to <mark>value</mark>.  
    * If <mark>prop</mark> is <mark>tracks</mark> but the album doesn't have a <mark>tracks</mark> property, create an empty array and add <mark>value</mark> to it.  
    * If <mark>prop</mark> is <mark>tracks</mark> and <mark>value</mark> isn't an empty string, add value to the end of the album's existing <mark>tracks</mark> array.  
    * If <mark>value</mark> is an empty string, delete the given <mark>prop</mark> property from the album.  

            // Setup
            var collection = {
            2548: {
                albumTitle: 'Slippery When Wet',
                artist: 'Bon Jovi',
                tracks: ['Let It Rock', 'You Give Love a Bad Name']
            },
            2468: {
                albumTitle: '1999',
                artist: 'Prince',
                tracks: ['1999', 'Little Red Corvette']
            },
            1245: {
                artist: 'Robert Palmer',
                tracks: []
            },
            5439: {
                albumTitle: 'ABBA Gold'
            }
            };

            // Only change code below this line
            function updateRecords(object, id, prop, value) {
            if (value === "") {
                delete collection[id][prop];
            } 
            
            if (prop === "tracks") {
                collection[id][prop] = collection[id][prop] || [];
                collection[id][prop].push(value);
            } else {
                collection[id][prop] = value;
            }
            
            return object;
            }

            updateRecords(collection, 5439, 'artist', 'ABBA');
___
93. Iterate with JavaScript While Loops  

    You can run the same code multiple times by using a loop.

    The first type of loop we will learn is called a while loop because it runs <mark>"while"</mark> a specified condition is true and stops once that condition is no longer true.

        var ourArray = [];
            var i = 0;
            while(i < 5) {
            ourArray.push(i);
            i++;
        }
    In the code example above, the <mark>while</mark> loop will execute 5 times and append the numbers 0 through 4 to <mark>ourArray</mark>.

    Let's try getting a while loop to work by pushing values to an array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Add the numbers 5 through 0 (inclusive) in descending order to <mark>myArray</mark> using a <mark>while</mark> loop.

        // Setup
        var myArray = [];

        // Only change code below this line
        var i = 5;
        while(i > -1) {
            myArray.push(i);
            i--;
        }
___
94. Iterate with JavaScript For Loops  

    You can run the same code multiple times by using a loop.

    The most common type of JavaScript loop is called a <mark>for</mark> loop because it runs "for" a specific number of times.

    For loops are declared with three optional expressions separated by semicolons:

    <mark>for ([initialization]; [condition]; [final-expression])</mark>

    The <mark>initialization</mark> statement is executed one time only before the loop starts. It is typically used to define and setup your loop variable.

    The <mark>condition</mark> statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to <mark>true</mark>. When <mark>condition</mark> is <mark>false</mark> at the start of the iteration, the loop will stop executing. This means if <mark>condition</mark> starts as <mark>false</mark>, your loop will never execute.

    The <mark>final-expression</mark> is executed at the end of each loop iteration, prior to the next <mark>condition</mark> check and is usually used to increment or decrement your loop counter.

    In the following example we initialize with <mark>i = 0</mark> and iterate while our condition <mark>i < 5</mark> is true. We'll increment <mark>i</mark> by <mark>1</mark> in each loop iteration with <mark>i++</mark> as our final-expression.

        var ourArray = [];
        for (var i = 0; i < 5; i++) {
        ourArray.push(i);
        }

    <mark>ourArray</mark> will now contain <mark>[0,1,2,3,4].</mark>

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use a <mark>for</mark> loop to work to push the values 1 through 5 onto <mark>myArray.</mark>

        // Setup
        var myArray = [];

        // Only change code below this line
        for (var i = 1; i < 6; i++) {
            myArray.push(i);
        }
___
95. Iterate Odd Numbers With a For Loop

    For loops don't have to iterate one at a time. By changing our <mark>final-expression</mark>, we can count by even numbers.

    We'll start at <mark>i = 0</mark> and loop while <mark>i < 10</mark>. We'll increment i by 2 each loop with <mark>i += 2</mark>.

        var ourArray = [];
        for (var i = 0; i < 10; i += 2) {
            ourArray.push(i);
        }

    <mark>ourArray</mark> will now contain <mark>[0,2,4,6,8]</mark>. Let's change our <mark>initialization</mark> so we can count by odd numbers.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Push the odd numbers from 1 through 9 to <mark>myArray</mark> using a <mark>for</mark> loop.

        // Setup
        var myArray = [];

        // Only change code below this line
        for (var i = 1; i < 10; i += 2) {
            myArray.push(i);
        }
___
96. Count Backwards With a For Loop  

    A for loop can also count backwards, so long as we can define the right conditions.

    In order to count backwards by twos, we'll need to change our <mark>initialization</mark>, <mark>condition</mark>, and <mark>final-expression</mark>.

    We'll start at <mark>i = 10</mark> and loop while <mark>i > 0</mark>. We'll decrement <mark> i </mark> by 2 each loop with <mark>i -= 2</mark>.

        var ourArray = [];
            for (var i = 10; i > 0; i -= 2) {
            ourArray.push(i);
        }
    <mark>ourArray</mark> will now contain <mark>[10,8,6,4,2]</mark>. Let's change our <mark>initialization</mark> and <mark>final-expression</mark> so we can count backward by twos by odd numbers.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Push the odd numbers from 9 through 1 to <mark>myArray</mark> using a for <mark>loop</mark>.

        // Setup
        var myArray = [];

        // Only change code below this line
        for (var i = 9; i > 0; i -= 2) {
            myArray.push(i);
        }
___
97. Iterate Through an Array with a For Loop  

    A common task in JavaScript is to iterate through the contents of an array. One way to do that is with a <mark>for</mark> loop. This code will output each element of the array <mark>arr</mark> to the console:

        var arr = [10, 9, 8, 7, 6];
            for (var i = 0; i < arr.length; i++) {
            console.log(arr[i]);
        }
    Remember that arrays have zero-based indexing, which means the last index of the array is <mark>length - 1</mark>. Our condition for this loop is <mark>i < arr.length</mark>, which stops the loop when <mark> i </mark> is equal to <mark>length</mark>. In this case the last iteration is <mark>i === 4</mark> i.e. when <mark> i </mark> becomes equal to <mark>arr.length</mark> and outputs <mark>6</mark> to the console.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Declare and initialize a variable <mark>total</mark> to <mark>0</mark>. Use a <mark>for</mark> loop to add the value of each element of the <mark>myArr</mark> array to <mark>total</mark>.

        // Setup
        var myArr = [ 2, 3, 4, 5, 6];

        // Only change code below this line
        var total = 0;
        for (var i = 0; i < myArr.length; i++) {
            total += myArr[i];
        }
___
98. Nesting For Loops  

    If you have a multi-dimensional array, you can use the same logic as the prior waypoint to loop through both the array and any sub-arrays. Here is an example:

        var arr = [
            [1,2], [3,4], [5,6]
        ];
        for (var i=0; i < arr.length; i++) {
            for (var j=0; j < arr[i].length; j++) {
                console.log(arr[i][j]);
            }
        }
    This outputs each sub-element in <mark>arr</mark> one at a time. Note that for the inner loop, we are checking the <mark>.length</mark> of <mark>arr[i]</mark>, <mark>since arr[i]</mark> is itself an array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Modify function <mark>multiplyAll</mark> so that it returns the product of all the numbers in the sub-arrays of <mark>arr</mark>.

        function multiplyAll(arr) {
        var product = 1;
        // Only change code below this line
        for (var i = 0; i < arr.length; i++) {
            for (var j = 0; j < arr[i].length; j++){
            product = product * arr[i][j];
            }
        }
        // Only change code above this line
        return product;
        }

        multiplyAll([[1,2],[3,4],[5,6,7]]);
___
99. Iterate with JavaScript Do...While Loops 

    The next type of loop you will learn is called a <mark>do...while</mark> loop. It is called a <mark>do...while</mark> loop because it will first <mark>do</mark> one pass of the code inside the loop no matter what, and then continue to run the loop <mark>while</mark> the specified condition evaluates to <mark>true.</mark>

        var ourArray = [];
        var i = 0;
        do {
            ourArray.push(i);
        i++;
        } while (i < 5);

    The example above behaves similar to other types of loops, and the resulting array will look like <mark>[0, 1, 2, 3, 4]</mark>. However, what makes the <mark>do...while</mark> different from other loops is how it behaves when the condition fails on the first check. Let's see this in action: Here is a regular <mark>while</mark> loop that will run the code in the loop as long as <mark>i < 5</mark>:

        var ourArray = []; 
        var i = 5;
        while (i < 5) {
            ourArray.push(i);
            i++;
        }
    In this example, we initialize the value of <mark>ourArray</mark> to an empty array and the value of <mark> i </mark> to 5. When we execute the <mark>while</mark> loop, the condition evaluates to <mark>false</mark> because <mark> i </mark> is not less than 5, so we do not execute the code inside the loop. The result is that <mark>ourArray</mark> will end up with no values added to it, and it will still look like <mark>[ ]</mark> when all of the code in the example above has completed running. Now, take a look at a <mark>do...while</mark> loop:

        var ourArray = []; 
        var i = 5;
        do {
            ourArray.push(i);
            i++;
        } while (i < 5);

    In this case, we initialize the value of <mark> i </mark> to 5, just like we did with the <mark>while</mark> loop. When we get to the next line, there is no condition to evaluate, so we go to the code inside the curly braces and execute it. We will add a single element to the array and then increment <mark> i </mark> before we get to the condition check. When we finally evaluate the condition <mark> i < 5 </mark> on the last line, we see that <mark> i </mark> is now 6, which fails the conditional check, so we exit the loop and are done. At the end of the above example, the value of <mark>ourArray</mark> is <mark>[5]</mark>. Essentially, a <mark>do...while</mark> loop ensures that the code inside the loop will run at least once. Let's try getting a <mark>do...while</mark> loop to work by pushing values to an array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change the <mark>while</mark> loop in the code to a <mark>do...while</mark> loop so the loop will push only the number <mark>10</mark> to <mark>myArray</mark>, and <mark> i  </mark> will be equal to <mark>11</mark> when your code has finished running.

        // Setup
        var myArray = [];
        var i = 10;

        // Only change code below this line
        do {
            myArray.push(i);
            i++;
        }
        while (i < 11);
___
100. Replace Loops using Recursion
    
      Recursion is the concept that a function can be expressed in terms of itself. To help understand this, start by thinking about the following task: multiply the first n elements of an array to create the product of those elements. Using a <mark>for</mark> loop, you could do this:  

            function multiply(arr, n) {
                var product = 1;
                for (var i = 0; i < n; i++) {
                    product *= arr[i];
                }
                return product;
            }

      However, notice that <mark>multiply(arr, n) == multiply(arr, n - 1) * arr[n - 1]</mark>. That means you can rewrite <mark>multiply</mark> in terms of itself and never need to use a loop.

            function multiply(arr, n) {
                if (n <= 0) {
                return 1;
                } else {
                return multiply(arr, n - 1) * arr[n - 1];
                }
            }
     The recursive version of <mark>multiply</mark> breaks down like this. In the base case, where <mark>n <= 0</mark>, it returns 1. For larger values of <mark> n </mark>, it calls itself, but with <mark>n - 1</mark>. That function call is evaluated in the same way, calling <mark>multiply</mark> again until <mark>n <= 0</mark>. At this point, all the functions can return and the original <mark>multiply returns the answer.

     **Note:** Recursive functions must have a base case when they return without calling the function again (in this example, when <mark>n <= 0</mark>), otherwise they can never finish executing.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Write a recursive function, <mark>sum(arr, n)</mark>, that returns the sum of the first <mark> n </mark> elements of an <mark>array</mark> arr.

            function sum(arr, n) {
            // Only change code below this line
            if (n <= 0) {
                return 0;
            } else {
                return sum(arr, n - 1) + arr[n - 1];
            }
            // Only change code above this line
            }
___
101. Profile Lookup    

      We have an array of objects representing different people in our contacts lists.

      A <mark>lookUpProfile</mark> function that takes <mark>name</mark> and a property (<mark>prop</mark>) as arguments has been pre-written for you.

      The function should check if <mark>name</mark> is an actual contact's <mark>firstName</mark> and the given property (<mark>prop</mark>) is a property of that contact.

      If both are true, then return the "value" of that property.

      If <mark>name</mark> does not correspond to any contacts then return <mark>"No such contact"</mark>.

      If <mark>prop</mark> does not correspond to any valid properties of a contact found to match <mark>name</mark> then return <mark>"No such property"</mark>.

            // Setup
            var contacts = [
                {
                    "firstName": "Akira",
                    "lastName": "Laine",
                    "number": "0543236543",
                    "likes": ["Pizza", "Coding", "Brownie Points"]
                },
                {
                    "firstName": "Harry",
                    "lastName": "Potter",
                    "number": "0994372684",
                    "likes": ["Hogwarts", "Magic", "Hagrid"]
                },
                {
                    "firstName": "Sherlock",
                    "lastName": "Holmes",
                    "number": "0487345643",
                    "likes": ["Intriguing Cases", "Violin"]
                },
                {
                    "firstName": "Kristian",
                    "lastName": "Vos",
                    "number": "unknown",
                    "likes": ["JavaScript", "Gaming", "Foxes"]
                }
            ];

            function lookUpProfile(name, prop){
            // Only change code below this line
                for (var i = 0; i < contacts.length; i++) {
                    if (contacts[i].firstName === name) {
                        if (contacts[i].hasOwnProperty(prop)) {
                        return contacts[i][prop];
                    } else {
                        return "No such property";
                    }
                    }
            }
                    return "No such contact";
                
            // Only change code above this line
            }

            lookUpProfile("Akira", "likes");
___
102. Generate Random Fractions with JavaScript  

      Random numbers are useful for creating random behavior.

      JavaScript has a <mark>Math.random()</mark> function that generates a random decimal number between <mark> 0 </mark> (inclusive) and not quite up to <mark> 1 </mark> (exclusive). Thus <mark>Math.random()</mark> can return a <mark> 0 </mark> but never quite return a <mark> 1 </mark>

      **Note**  
      Like <u>Storing Values with the Equal Operator</u>, all function calls will be resolved before the <mark>return</mark> executes, so we can <mark>return</mark> the value of the <mark>Math.random()</mark> function.

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Change <mark>randomFraction</mark> to return a random number instead of returning <mark> 0 </mark>.

            function randomFraction() {
            // Only change code below this line

            return Math.random();

            // Only change code above this line
            }
___
103. Generate Random Whole Numbers with JavaScript  

      It's great that we can generate random decimal numbers, but it's even more useful if we use it to generate random whole numbers.

      1. Use <mark>Math.random()</mark> to generate a random decimal.

      2. Multiply that random decimal by <mark> 20 </mark>.

      3. Use another function, <mark>Math.floor()</mark> to round the number down to its nearest whole number.

      Remember that <mark>Math.random()</mark> can never quite return a <mark> 1 </mark> and, because we're rounding down, it's impossible to actually get <mark> 20 </mark>. This technique will give us a whole number between <mark> 0 </mark> and <mark. 19 </mark> .

      Putting everything together, this is what our code looks like:

      >Math.floor(Math.random() * 20);

      We are calling <mark>Math.random()</mark>, multiplying the result by 20, then passing the value to <mark>Math.floor()</mark> function to round the value down to the nearest whole number.

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use this technique to generate and return a random whole number between <mark> 0 </mark> and <mark> 9 </mark>.

            function randomWholeNum() {

            // Only change code below this line

            return Math.floor(Math.random() * 10);
            }
___
104. Generate Random Whole Numbers within a Range

      Instead of generating a random whole number between zero and a given number like we did before, we can generate a random whole number that falls within a range of two specific numbers.

      To do this, we'll define a minimum number <mark>min</mark> and a maximum number <mark>max</mark>.

      Here's the formula we'll use. Take a moment to read it and try to understand what this code is doing:

      >Math.floor(Math.random() * (max - min + 1)) + min

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Create a function called <mark>randomRange</mark> that takes a range <mark>myMin</mark> and <mark>myMax</mark> and returns a random whole number that's greater than or equal to <mark>myMin</mark>, and is less than or equal to <mark>myMax</mark>, inclusive.

            function randomRange(myMin, myMax) {
                // Only change code below this line
                return Math.floor(Math.random() * (myMax - myMin + 1)) + myMin;
                // Only change code above this line
            }
___
105. Use the parseInt Function  

     The <mark>parseInt()</mark> function parses a string and returns an integer. Here's an example:

     >var a = parseInt("007");

     The above function converts the string "007" to an integer 7. If the first character in the string can't be converted into a number, then it returns <mark>NaN</mark>.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use parseInt() in the convertToInteger function so it converts the input string str into an integer, and returns it.

            function convertToInteger(str) {
                return parseInt(str);
            }

            convertToInteger("56");
___
106. Use the parseInt Function with a Radix  

     The <mark>parseInt()</mark> function parses a string and returns an integer. It takes a second argument for the radix, which specifies the base of the number in the string. The radix can be an integer between 2 and 36.

     **The function call looks like:**

     >parseInt(string, radix);

     **And here's an example:**

     >var a = parseInt("11", 2);

     The radix variable says that "11" is in the binary system, or base 2. This example converts the string "11" to an integer 3.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use <mark>parseInt()</mark> in the <mark>convertToInteger</mark> function so it converts a binary number to an integer and returns it.  

            function convertToInteger(str) {
                return parseInt(str, 2);
            }

            convertToInteger("10011");
___
107. Use the Conditional (Ternary) Operator  

     The *conditional operator*, also called the *ternary operator*, can be used as a one line if-else expression.

     The syntax is:

     <mark>condition ? statement-if-true : statement-if-false;</mark>

     The following function uses an if-else statement to check a condition:

            function findGreater(a, b) {
                if(a > b) {
                    return "a is greater";
                }
                else {
                    return "b is greater";
                }
            }
     This can be re-written using the <mark>conditional operator:</mark>

            function findGreater(a, b) {
                return a > b ? "a is greater" : "b is greater";
            }
     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the <mark>conditional operator</mark> in the <mark>checkEqual</mark> function to check if two numbers are equal or not. The function should return either "Equal" or "Not Equal".

            function checkEqual(a, b) {
                return a == b ? "Equal" : "Not Equal";
            }
            checkEqual(1, 2);
___
108. Use Multiple Conditional (Ternary) Operators  

     In the previous challenge, you used a single conditional operator. You can also chain them together to check for multiple conditions.

     The following function uses if, else if, and else statements to check multiple conditions:

            function findGreaterOrEqual(a, b) {
            if (a === b) {
                return "a and b are equal";
            }
            else if (a > b) {
                return "a is greater";
            }
            else {
                return "b is greater";
            }
            }
     The above function can be re-written using multiple conditional operators:

            function findGreaterOrEqual(a, b) {
            return (a === b) ? "a and b are equal" 
                : (a > b) ? "a is greater" 
                : "b is greater";
            }
     It is considered best practice to format multiple conditional operators such that each condition is on a separate line, as shown above. Using multiple conditional operators without proper indentation may make your code hard to read. For example:

            function findGreaterOrEqual(a, b) {
                return (a === b) ? "a and b are equal" : (a > b) ? "a is greater" : "b is greater";
            }

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)In the <mark>checkSign</mark> function, use multiple conditional operators - following the recommended format used in <mark>findGreaterOrEqual</mark> - to check if a number is positive, negative or zero. The function should return <mark>"positive"</mark>, <mark>"negative"</mark> or <mark>"zero"</mark>.

            function checkSign(num) {
                return (num < 0) ? "negative"
                    : (num > 0) ? "positive"
                    : "zero";
                }

            checkSign(10);
___
109. Use Recursion to Create a Countdown  

     In a <u>previous challenge</u>, you learned how to use recursion to replace a for loop. Now, let's look at a more complex function that returns an array of consecutive integers starting with <mark> 1 </mark> through the number passed to the function.

     As mentioned in the previous challenge, there will be a base case. The base case tells the recursive function when it no longer needs to call itself. It is a simple case where the return value is already known. There will also be a recursive call which executes the original function with different arguments. If the function is written correctly, eventually the base case will be reached.

     For example, say you want to write a recursive function that returns an array containing the numbers <mark> 1 </mark> through <mark> n </mark>. This function will need to accept an argument, <mark> n </mark>, representing the final number. Then it will need to call itself with progressively smaller values of <mark> n </mark> until it reaches <mark> 1 </mark>. You could write the function as follows:

            function countup(n) {
            if (n < 1) {
                return [];
            } else {
                const countArray = countup(n - 1);
                countArray.push(n);
                return countArray;
            }
            }
            console.log(countup(5)); // [ 1, 2, 3, 4, 5 ]
     At first, this seems counterintuitive since the value of <mark> n </mark> decreases, but the values in the final array are increasing. This happens because the push happens last, after the recursive call has returned. At the point where <mark> n </mark> is pushed into the array, <mark> countup(n - 1)</mark> has already been evaluated and returned <mark>[1, 2, ..., n - 1]</mark>.

      ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a function called <mark>countdown</mark> with one parameter (<mark> n </mark>). The function should use recursion to return an array containing the integers <mark> n </mark> through <mark> 1 </mark> based on the <mark> n </mark> parameter. If the function is called with a number less than 1, the function should return an empty array. For example, calling this function with <mark>n = 5</mark> should return the array <mark>[5, 4, 3, 2, 1]</mark>. Your function must use recursion by calling itself and must not use loops of any kind.

            // Only change code below this line
            function countdown(n){
                if (n < 1) {
                    return [];
                } else {
                    const countArray = countdown(n - 1);
                    countArray.unshift(n);
                    return countArray;
                }
            }
            // Only change code above this line 
___
110. Use Recursion to Create a Range of Numbers   

     Continuing from the previous challenge, we provide you another opportunity to create a recursive function to solve a problem.

     We have defined a function named <mark>rangeOfNumbers</mark> with two parameters. The function should return an array of integers which begins with a number represented by the <mark>startNum</mark> parameter and ends with a number represented by the <mark>endNum</mark> parameter. The starting number will always be less than or equal to the ending number. Your function must use recursion by calling itself and not use loops of any kind. It should also work for cases where both <mark>startNum</mark> and <mark>endNum</mark> are the same.

            function rangeOfNumbers(startNum, endNum) {
                if (endNum - startNum === 0) {
                    return [startNum];
                } else {
                    var numbers = rangeOfNumbers(startNum, endNum - 1); 
                    numbers.push(endNum);
                    return numbers;
                }
            }
___
## ES6
> **Introduction to the ES6 Challenges**    

ECMAScript is a standardized version of JavaScript with the goal of unifying the language's specifications and features. As all major browsers and JavaScript-runtimes follow this specification, the term ECMAScript is interchangeable with the term JavaScript.

Most of the challenges on freeCodeCamp use the ECMAScript 5 (ES5) specification of the language, finalized in 2009. But JavaScript is an evolving programming language. As features are added and revisions are made, new versions of the language are released for use by developers.

The most recent standardized version is called ECMAScript 6 (ES6), released in 2015. This new version of the language adds some powerful features that will be covered in this section of challenges, including:

* Arrow functions
* Classes
* Modules
* Promises
* Generators
* let and const

**Note:** Not all browsers support ES6 features. If you use ES6 in your own projects, you may need to use a program (transpiler) to convert your ES6 code into ES5 until browsers support ES6.  
___
1.   

![Imgur](https://i.imgur.com/nMWBSol.jpg)
![Imgur](https://i.imgur.com/pI4q5Ng.jpg)

    let catName;
    let quote;
    function catTalk() {
    "use strict";

    catName = "Oliver";
    quote = catName + " says Meow!";

    }
    catTalk();
___
2.
![Imgur](https://i.imgur.com/lNMgACY.jpg)
![Imgur](https://i.imgur.com/4YbgU1K.jpg)
![Imgur](https://i.imgur.com/ncf7YMF.jpg) 

        function checkScope() {
            'use strict';
            let i = 'function scope';
            if (true) {
                let i = 'block scope';
                console.log('Block scope i is: ', i);
            }
            console.log('Function scope i is: ', i);
            return i;
        }
___
3. 
![Imgur](https://i.imgur.com/vBmKW42.jpg)

    function printManyTimes(str) {
    "use strict";

    // Only change code below this line

    const sentence = str + " is cool!";
    for (let i = 0; i < str.length; i+=2) {
        console.log(sentence);
    }

    // Only change code above this line

    }
    printManyTimes("freeCodeCamp");
___
4. 
![Imgur](https://i.imgur.com/AaR3Oql.jpg)

    const s = [5, 7, 2];
    function editInPlace() {
    'use strict';
    // Only change code below this line
    
    // Using s = [2, 5, 7] would be invalid

    s[0] = 2;
    s[1] = 5;
    s[2] = 7;

    // Only change code above this line
    }
    editInPlace();
___
5. 
![Imgur](https://i.imgur.com/2mvpkzg.jpg)

    function freezeObj() {
        'use strict';
        const MATH_CONSTANTS = {
            PI: 3.14
        };
        // Only change code below this line
        Object.freeze(MATH_CONSTANTS)

        // Only change code above this line
        try {
            MATH_CONSTANTS.PI = 99;
        } catch(ex) {
            console.log(ex);
        }
        return MATH_CONSTANTS.PI;
    }
    const PI = freezeObj(); 
___
6.
![Imgur](https://i.imgur.com/h5hXxYm.jpg)


![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Rewrite the function assigned to the variable magic which returns a new Date() to use arrow function syntax. Also, make sure nothing is defined using the keyword var.

    let magic = () => {
        "use strict";
        return new Date();
    };
___
7. 
![Imgur](https://i.imgur.com/ULOBUZQ.jpg)

    const myConcat = (arr1, arr2) => {
        "use strict";
        return arr1.concat(arr2);
    };

    console.log(myConcat([1, 2], [3, 4, 5]));
___
8. 
![Imgur](https://i.imgur.com/tiMDgi2.jpg)

    // Only change code below this line
    const increment = (number, value=1) => number + value;
    // Only change code above this line
___
9. 
![Imgur](https://i.imgur.com/hhCYH9p.jpg)

    const sum = (...args) => {
        return args.reduce((a, b) => a + b, 0);
    }
___
10. 
![Imgur](https://i.imgur.com/S5H1eZk.jpg)

    const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
    let arr2;

    arr2 = [...arr1];  // Change this line

    console.log(arr2);
___
11. 
![Imgur](https://i.imgur.com/vPwuGUa.jpg)

    const HIGH_TEMPERATURES = {
        yesterday: 75,
        today: 77,
        tomorrow: 80
    };

    // Only change code below this line

    const { today, tomorrow } = HIGH_TEMPERATURES;

    // Only change code above this 
___
12. 
![Imgur](https://i.imgur.com/BMt7UHU.jpg)

    const HIGH_TEMPERATURES = {
        yesterday: 75,
        today: 77,
        tomorrow: 80
    };

    // Only change code below this line

    const {today: highToday, tomorrow: highTomorrow} = HIGH_TEMPERATURES;
    // Only change code above this line
___
13. 
![Imgur](https://i.imgur.com/OntvikE.jpg)

    const LOCAL_FORECAST = {
        yesterday: { low: 61, high: 75 },
        today: { low: 64, high: 77 },
        tomorrow: { low: 68, high: 80 }
    };

    // Only change code below this line
    
    const {today: {low: lowToday, high: highToday}} = LOCAL_FORECAST;

    // Only change code above this line
___
14. 
![Imgur](https://i.imgur.com/QE9aJwm.jpg)

    let a = 8, b = 6;
    // Only change code below this line
    [a, b] = [b, a]
___
15. 
 ![Imgur](https://i.imgur.com/gyMeR2b.jpg)

    const source = [1,2,3,4,5,6,7,8,9,10];
    function removeFirstTwo(list) {
        "use strict";
        // Only change code below this line
        const [a, b, ...arr] = list; // Change this line
        // Only change code above this line
        return arr;
    }
    const arr = removeFirstTwo(source);
___
16. 
![Imgur](https://i.imgur.com/sygnNGd.jpg)

    const stats = {
        max: 56.78,
        standard_deviation: 4.34,
        median: 34.54,
        mode: 23.87,
        min: -0.75,
        average: 35.85
    };

    // Only change code below this line
    const half = ({max, min}) => (max + min) / 2.0; 
    // Only change code above this line
___
17. 
![Imgur](https://i.imgur.com/yqH8cEw.jpg)
![Imgur](https://i.imgur.com/HcKYGPq.jpg)

    const result = {
    success: ["max-length", "no-amd", "prefer-arrow-functions"],
    failure: ["no-var", "var-on-top", "linebreak"],
    skipped: ["id-blacklist", "no-dup-keys"]
    };
    function makeList(arr) {
    "use strict";

    // Only change code below this line
    const resultDisplayArray = [];
    for (let i = 0; i < arr.length; i++) {
        arr[i] = `<li class="text-warning">${arr[i]}</li>`;
        resultDisplayArray.push(arr[i]);
    }
    // Only change code above this line

    return resultDisplayArray;
    }

    const resultDisplayArray = makeList(result.failure);
___
18. 
![Imgur](https://i.imgur.com/H4C1Wnk.jpg)

    const createPerson = (name, age, gender) => {
        "use strict";
        // Only change code below this line
            return {
                name,
                age,
                gender
            };
        // Only change code above this line
    };
___
19. 
![Imgur](https://i.imgur.com/Jd24dlG.jpg)

    // Only change code below this line
    const bicycle = {
        gear: 2,
        setGear(newGear) {
            this.gear = newGear;
        }
    };
    // Only change code above this line
    bicycle.setGear(3);
    console.log(bicycle.gear);
___
20. 
![Imgur](https://i.imgur.com/3KXaOOy.jpg)
![Imgur](https://i.imgur.com/F4pkw8u.jpg)

    // Only change code below this line
    class Vegetable{
        constructor(name) {
            this.name = name;
        }
    }
    // Only change code above this line

    const carrot = new Vegetable('carrot');
    console.log(carrot.name); // Should display 'carrot'
___
21. 
![Imgur](https://i.imgur.com/CtUCVb2.jpg)
![Imgur](https://i.imgur.com/uLLoDCe.jpg)

    // Only change code below this line
    class Thermostat {
        constructor(fahrenheit) {
            this._fahrenheit = fahrenheit;
        }
        // getter
        get temperature() {
            return (5 / 9) * (this._fahrenheit - 32);
        }
        // setter
        set temperature(celsius) {
            this._fahrenheit = (celsius * 9.0) / 5 + 32;
        }
    }
    // Only change code above this line

    const thermos = new Thermostat(76); // Setting in Fahrenheit scale
    let temp = thermos.temperature; // 24.44 in Celsius
    thermos.temperature = 26;
    temp = thermos.temperature; // 26 in Celsius
___
22. 
![Imgur](https://i.imgur.com/OG1f2fP.jpg)

    <html>
        <!-- Only change code below this line -->
            <header>
            <script type="module" src="index.js"></script>
            </header>

        <!-- Only change code above this line -->
            <body>
        </body>
    </html>
___
23. 
![Imgur](https://i.imgur.com/gF4OXR2.jpg)

    const uppercaseString = (string) => {
         return string.toUpperCase();
    }

    const lowercaseString = (string) => {
         return string.toLowerCase()
    }

    export { uppercaseString, lowercaseString };
___
24. 
![Imgur](https://i.imgur.com/148mgQp.jpg)

    import {uppercaseString, lowercaseString} from './string_functions.js';

    // Only change code above this line

    uppercaseString("hello");
    lowercaseString("WORLD!");
___
25. 
![Imgur](https://i.imgur.com/Yo0eDuW.jpg)

    import * as stringFunctions from "./string_functions.js";

    // Only change code above this line

    stringFunctions.uppercaseString("hello");
    stringFunctions.lowercaseString("WORLD!");
___
26. 
![Imgur](https://i.imgur.com/q5BT9R1.jpg)

    export default function subtract(x, y) {
        return x - y;
    }
___
27. 
![Imgur](https://i.imgur.com/8u5bpVn.jpg)

    import subtract from "./math_functions.js";  
    // Only change code above this line

    subtract(7,4);
___
28. 
![Imgur](https://i.imgur.com/D4xXIn7.jpg)

    const  makeServerRequest = new Promise((resolve, reject) => {

    });
___
29. 
![Imgur](https://i.imgur.com/v05SkYQ.jpg)

    const makeServerRequest = new Promise((resolve, reject) => {
    // responseFromServer represents a response from a server
    let responseFromServer;
        
    if(responseFromServer) {
        resolve("We got the data"); // Change this line
    } else {  
        reject("Data not received"); // Change this line
    }
    });
___
30. 
![Imgur](https://i.imgur.com/uQjB9se.jpg)

    const makeServerRequest = new Promise((resolve, reject) => {
    // responseFromServer is set to true to represent a successful response from a server
    let responseFromServer = true;
        
    if(responseFromServer) {
        resolve("We got the data");
    } else {  
        reject("Data not received");
    }
    });

    makeServerRequest.then(result => {
    console.log(result);
    })
___
31.
![Imgur](https://i.imgur.com/7U1jzNq.jpg)

    const makeServerRequest = new Promise((resolve, reject) => {
    // responseFromServer is set to false to represent an unsuccessful response from a server
    let responseFromServer = false;
        
    if(responseFromServer) {
        resolve("We got the data");
    } else {  
        reject("Data not received");
    }
    });

    makeServerRequest.then(result => {
    console.log(result);
    });

    makeServerRequest.catch(error => {
    console.log(error);
    })
___
## Debugging
> **Introduction to the Debugging Challenges**    

Debugging is a valuable and (unfortunately) necessary tool for programmers. It follows the testing phase of checking if your code works as intended, and discovering it does not. Debugging is the process of finding exactly what isn't working and fixing it. After spending time creating a brilliant block of code, it is tough realizing it may have errors. These issues generally come in three forms:

1. syntax errors that prevent a program from running
2. runtime errors when code fails to execute or has unexpected behavior
3. semantic (or logical) errors when code doesn't do what it's meant to.  
Modern code editors (and experience) can help identify syntax errors. Semantic and runtime errors are harder to find. They may cause your program to crash, make it run forever, or give incorrect output. Think of debugging as trying to understand why your code is behaving the way it is. Example of a syntax error - often detected by the code editor:

        funtcion willNotWork( 
            console.log("Yuck");
        }
        // "function" keyword is misspelled and there's a missing parenthesis  

    Here's an example of a runtime error - often detected while the program executes:

        function loopy() {
            while(true) {
                console.log("Hello, world!");
            }
        }
        // Calling loopy starts an infinite loop, which may crash your browser

    Example of a semantic error - often detected after testing code output:

        function calcAreaOfRect(w, h) {
            return w + h; // This should be w * h
        }
        let myRectArea = calcAreaOfRect(2, 3);
        // Correct syntax and the program executes, but this gives the wrong answer

    Debugging is frustrating, but it helps to develop (and follow) a step-by-step approach to review your code. This means checking the intermediate values and types of variables to see if they are what they should be. You can start with a simple process of elimination.

    For example, if function A works and returns what it's supposed to, then function B may have the issue. Or start checking values in a block of code from the middle to try to cut the search space in half. A problem in one spot indicates a bug in the first half of the code. If not, it's likely in the second.

    This section will cover a couple helpful tools to find bugs, and some of the common forms they take. Fortunately, debugging is a learnable skill that just requires a little patience and practice to master.
___
1. Use the JavaScript Console to Check the Value of a Variable  

    Both Chrome and Firefox have excellent JavaScript consoles, also known as DevTools, for debugging your JavaScript.

    You can find Developer tools in your Chrome's menu or Web Console in Firefox's menu. If you're using a different browser, or a mobile phone, we strongly recommend switching to desktop Firefox or Chrome.

    The <mark>console.log()</mark> method, which "prints" the output of what's within its parentheses to the console, will likely be the most helpful debugging tool. Placing it at strategic points in your code can show you the intermediate values of variables. It's good practice to have an idea of what the output should be before looking at what it is. Having check points to see the status of your calculations throughout your code will help narrow down where the problem is.

    Here's an example to print 'Hello world!' to the console:

    <mark>console.log('Hello world!');</mark>

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)Use the console.log() method to print the value of the variable a where noted in the code.

        let a = 5;
        let b = 1;
        a++;
        // Only change code below this line
        console.log(a);

        let sumAB = a + b;
        console.log(sumAB);
___
2. Understanding the Differences between the freeCodeCamp and Browser Console  

    You may have noticed that some freeCodeCamp JavaScript challenges include their own console. This console behaves a little differently than the browser console you used in the last challenge.

    The following challenge is meant to highlight the main difference between the freeCodeCamp console and your browser console.

    When you run ordinary JavaScript, the browser's console will display your <mark>console.log()</mark> statements the exact number of times it is called.

    The freeCodeCamp console will print your <mark>console.log()</mark> statements a short time after the editor detects a change in the script, as well as during testing.

    The freeCodeCamp console is cleared before the tests are run and, to avoid spam, only prints the logs during the first test (see the note below for exceptions).

    If you would like to see every log for every test, run the tests, and open the browser console. If you prefer to use the browser console, and want it to mimic the freeCodeCamp console, place <mark>console.clear()</mark> before any other <mark>console</mark> calls, to clear the browser console.

    **Note:** <mark>console.logs</mark> inside functions are printed to the freeCodeCamp console whenever those functions are called, this can help debugging functions that are called during testing.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) First, use <mark>console.log</mark> to log the <mark>output</mark> variable. Then, use <mark>console.clear</mark> to clear the browser console.

        // Open your browser console.
        let output = "Get this to log once in the freeCodeCamp console and twice in the browser console";
        // Use console.log() to print the output variable.
        console.log(output);
        // Run the tests to see the difference between the two consoles.
        console.clear();
        // Now, add console.clear() before your console.log() to clear the browser console, and pass the tests.
        console.log(output);
___
3. Use typeof to Check the Type of a Variable  

    You can use <mark>typeof</mark> to check the data structure, or type, of a variable. This is useful in debugging when working with multiple data types. If you think you're adding two numbers, but one is actually a string, the results can be unexpected. Type errors can lurk in calculations or function calls. Be careful especially when you're accessing and working with external data in the form of a JavaScript Object Notation (JSON) object.

    Here are some examples using <mark>typeof</mark>:

        console.log(typeof ""); // outputs "string"
        console.log(typeof 0); // outputs "number"
        console.log(typeof []); // outputs "object"
        console.log(typeof {}); // outputs "object"

    JavaScript recognizes six primitive (immutable) data types: <mark>Boolean</mark>, <mark>Null</mark>, <mark>Undefined</mark>, <mark>Number</mark>, <mark>String</mark>, and <mark>Symbol</mark> (new with ES6) and one type for mutable items: Object. Note that in JavaScript, arrays are technically a type of <mark>object</mark>.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)  Add two <mark>console.log()</mark> statements to check the <mark>typeof</mark> each of the two variables <mark>seven</mark> and <mark>three</mark> in the code.

        let seven = 7;
        let three = "3";
        console.log(seven + three);
        // Only change code below this line
        console.log("typeof seven variable: "+typeof(seven));
        console.log("typeof three variable: "+typeof(three));
___
4. Catch Misspelled Variable and Function Names  

    The <mark>console.log()</mark> and <mark>typeof</mark> methods are the two primary ways to check intermediate values and types of program output. Now it's time to get into the common forms that bugs take. One syntax-level issue that fast typers can commiserate with is the humble spelling error.

    Transposed, missing, or mis-capitalized characters in a variable or function name will have the browser looking for an object that doesn't exist - and complain in the form of a reference error. JavaScript variable and function names are case-sensitive.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the two spelling errors in the code so the <mark>netWorkingCapital</mark> calculation works.

        let receivables = 10;
        let payables = 8;
        let netWorkingCapital = recievables - payable;
        console.log(`Net working capital is: ${netWorkingCapital}`);
        //this code above show--> ReferenceError: recievables is not defined

        // ---->Debugging<------  //
        let receivables = 10;  
        let payables = 8;  
        let netWorkingCapital = receivables - payables;  
        console.log(`Net working capital is: ${netWorkingCapital}`);  
        //this code above show--> Net working capital is: 2
___
5. Catch Unclosed Parentheses, Brackets, Braces and Quotes  

    Another syntax error to be aware of is that all opening parentheses, brackets, curly braces, and quotes have a closing pair. Forgetting a piece tends to happen when you're editing existing code and inserting items with one of the pair types. Also, take care when nesting code blocks into others, such as adding a callback function as an argument to a method.

    One way to avoid this mistake is as soon as the opening character is typed, immediately include the closing match, then move the cursor back between them and continue coding. Fortunately, most modern code editors generate the second half of the pair automatically.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the two pair errors in the code.

        let myArray = [1, 2, 3];
        let arraySum = myArray.reduce((previous, current) =>  previous + current);
        console.log(`Sum of array values is: ${arraySum}`);
        // this code show --> Sum of array values is: 6
___
6. Catch Mixed Usage of Single and Double Quotes  

    JavaScript allows the use of both single (<mark> ' </mark>) and double (<mark> " </mark>) quotes to declare a string. Deciding which one to use generally comes down to personal preference, with some exceptions.

    Having two choices is great when a string has contractions or another piece of text that's in quotes. Just be careful that you don't close the string too early, which causes a syntax error.

    **Here are some examples of mixing quotes:**

        // These are correct:
        const grouchoContraction = "I've had a perfectly wonderful evening, but this wasn't it.";
        const quoteInString = "Groucho Marx once said 'Quote me as saying I was mis-quoted.'";
        // This is incorrect:
        const uhOhGroucho = 'I've had a perfectly wonderful evening, but this wasn't it.';

    Of course, it is okay to use only one style of quotes. You can escape the quotes inside the string by using the backslash (<mark> \ </mark>) escape character:

        // Correct use of same quotes:
        const allSameQuotes = 'I\'ve had a perfectly wonderful evening, but this wasn\'t it.';

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the string so it either uses different quotes for the <mark>href</mark> value, or escape the existing ones. Keep the double quote marks around the entire string.

        let innerHtml = "<p>Click here to <a href=\"#Home\">return home</a></p>";
        console.log(innerHtml);
___
7. Catch Use of Assignment Operator Instead of Equality Operator  

    Branching programs, i.e. ones that do different things if certain conditions are met, rely on <mark>if</mark>, <mark>else if</mark>, and <mark>else</mark> statements in JavaScript. The condition sometimes takes the form of testing whether a result is equal to a value.

    This logic is spoken (in English, at least) as "if x equals y, then ..." which can literally translate into code using the =, or assignment operator. This leads to unexpected control flow in your program.

    As covered in previous challenges, the assignment operator (<mark>=</mark>) in JavaScript assigns a value to a variable name. And the <mark>==</mark> and <mark>===</mark> operators check for equality (the triple <mark>===</mark> tests for strict equality, meaning both value and type are the same).

    The code below assigns <mark>x</mark> to be 2, which evaluates as <mark>true</mark>. Almost every value on its own in JavaScript evaluates to <mark>true</mark>, except what are known as the "falsy" values: <mark>false</mark>, <mark>0</mark>, <mark>""</mark> (an empty string), <mark>NaN</mark>, <mark>undefined</mark>, and <mark>null</mark>.

        let x = 1;
        let y = 2;
            if (x = y) {
            // this code block will run for any value of y (unless y were originally set as a falsy)
            } else {
            // this code block is what should run (but won't) in this example
            }
     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the condition so the program runs the right branch, and the appropriate value is assigned to <mark>result</mark>.

        let x = 7;
        let y = 9;
        let result = "to come";

        if(x === y) {
        result = "Equal!";
        } else {
        result = "Not equal!";
        }

        console.log(result);
___
8. Catch Missing Open and Closing Parenthesis After a Function Call  

    When a function or method doesn't take any arguments, you may forget to include the (empty) opening and closing parentheses when calling it. Often times the result of a function call is saved in a variable for other use in your code. This error can be detected by logging variable values (or their types) to the console and seeing that one is set to a function reference, instead of the expected value the function returns.

    *The variables in the following example are different:*

        function myFunction() {
            return "You rock!";
        }
        let varOne = myFunction; // set to equal a function
        let varTwo = myFunction(); // set to equal the string "You rock!"

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the code so the variable <mark>result</mark> is set to the value returned from calling the function <mark>getNine</mark>.

        function getNine() {
            let x = 6;
            let y = 3;
            return x + y;
        }

        let result = getNine();
        console.log(result);  //9
___
9. Catch Arguments Passed in the Wrong Order When Calling a Function  

    Continuing the discussion on calling functions, the next bug to watch out for is when a function's arguments are supplied in the incorrect order. If the arguments are different types, such as a function expecting an array and an integer, this will likely throw a runtime error. If the arguments are the same type (all integers, for example), then the logic of the code won't make sense. Make sure to supply all required arguments, in the proper order to avoid these issues.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) The function <mark>raiseToPower</mark> raises a base to an exponent. Unfortunately, it's not called properly - fix the code so the value of <mark>power</mark> is the expected 8.

        function raiseToPower(b, e) {
            return Math.pow(b, e);
        }

        let base = 2;
        let exp = 3;
        let power = raiseToPower(base, exp);
        console.log(power);  //8
___
10. Catch Off By One Errors When Using Indexing  

    Off by one errors (sometimes called OBOE) crop up when you're trying to target a specific index of a string or array (to slice or access a segment), or when looping over the indices of them. JavaScript indexing starts at zero, not one, which means the last index is always one less than the length of the item. If you try to access an index equal to the length, the program may throw an "index out of range" reference error or print <mark>undefined</mark>.

    When you use string or array methods that take index ranges as arguments, it helps to read the documentation and understand if they are inclusive (the item at the given index is part of what's returned) or not. Here are some examples of off by one errors:

        let alphabet = "abcdefghijklmnopqrstuvwxyz";
        let len = alphabet.length;
            for (let i = 0; i <= len; i++) {
            // loops one too many times at the end
            console.log(alphabet[i]);
            }
            for (let j = 1; j < len; j++) {
            // loops one too few times and misses the first character at index 0
            console.log(alphabet[j]);
            }
            for (let k = 0; k < len; k++) {
            // Goldilocks approves - this is just right
            console.log(alphabet[k]);
            }
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) Fix the two indexing errors in the following function so all the numbers 1 through 5 are printed to the console.

        function countToFive() {
        let firstFive = "12345";
        let len = firstFive.length;
        // Only change code below this line
        for (let i = 0; i < len; i++) {
        // Only change code above this line
            console.log(firstFive[i]);
        }
        }

        countToFive();
___
11. Use Caution When Reinitializing Variables Inside a Loop  

    Sometimes it's necessary to save information, increment counters, or re-set variables within a loop. A potential issue is when variables either should be reinitialized, and aren't, or vice versa. This is particularly dangerous if you accidentally reset the variable being used for the terminal condition, causing an infinite loop.

    Printing variable values with each cycle of your loop by using <mark>console.log()</mark> can uncover buggy behavior related to resetting, or failing to reset a variable.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) The following function is supposed to create a two-dimensional array with <mark>m</mark> rows and <mark>n</mark> columns of zeroes. Unfortunately, it's not producing the expected output because the <mark>row</mark> variable isn't being reinitialized (set back to an empty array) in the outer loop. Fix the code so it returns a correct 3x2 array of zeroes, which looks like <mark>[[0, 0], [0, 0], [0, 0]]</mark>.

        function zeroArray(m, n) {
        // Creates a 2-D array with m rows and n columns of zeroes
        let newArray = [];
        let row = [];
        for (let i = 0; i < m; i++) {
            // Adds the m-th row into newArray

            for (let j = 0; j < n; j++) {
            // Pushes n zeroes into the current row to create the columns
            row[j] = 0
            }
            // Pushes the current row, which now has n zeroes in it, to the array
        
            newArray.push(row);
            
        }
        return newArray;
        }

        let matrix = zeroArray(3, 2);
        console.log(matrix);


___
12. Prevent Infinite Loops with a Valid Terminal Condition  

    The final topic is the dreaded infinite loop. Loops are great tools when you need your program to run a code block a certain number of times or until a condition is met, but they need a terminal condition that ends the looping. Infinite loops are likely to freeze or crash the browser, and cause general program execution mayhem, which no one wants.

    There was an example of an infinite loop in the introduction to this section - it had no terminal condition to break out of the <mark>while</mark> loop inside <mark>loopy()</mark>. Do NOT call this function!

        function loopy() {
            while(true) {
                console.log("Hello, world!");
            }
        }

    It's the programmer's job to ensure that the terminal condition, which tells the program when to break out of the loop code, is eventually reached. One error is incrementing or decrementing a counter variable in the wrong direction from the terminal condition. Another one is accidentally resetting a counter or index variable within the loop code, instead of incrementing or decrementing it.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) The <mark>myFunc()</mark> function contains an infinite loop because the terminal condition <mark>i != 4</mark> will never evaluate to <mark>false</mark> (and break the looping) - <mark> i </mark> will increment by 2 each pass, and jump right over 4 since <mark> i </mark> is odd to start. Fix the comparison operator in the terminal condition so the loop only runs for <mark> i </mark> less than or equal to 4.

        function myFunc() {
            for (let i = 1; i <= 4; i += 2) {
                console.log("Still going!");
            }
        }

        myFunc(); 

___
## Basic Data Structure
> **Introduction to the Basic Data Structure Challenges**    

Introduction to the Basic Data Structure Challenges
    Data can be stored and accessed in many different ways, both in JavaScript and other languages. This section will teach you how to manipulate arrays, as well as access and copy the information within them. It will also teach you how to manipulate and access the data within JavaScript objects, using both dot and bracket notation. When you're done with this section, you should understand the basic properties and differences between arrays and objects, as well as how to choose which to use for a given purpose.
___

1. Use an Array to Store a Collection of Data  

    The below is an example of the simplest implementation of an array data structure. This is known as a one-dimensional array, meaning it only has one level, or that it does not have any other arrays nested within it. Notice it contains booleans, strings, and numbers, among other valid JavaScript data types:

        let simpleArray = ['one', 2, 'three', true, false, undefined, null];
        console.log(simpleArray.length);
        // logs 7

    All arrays have a length property, which as shown above, can be very easily accessed with the syntax <mark>Array.length</mark>. A more complex implementation of an array can be seen below. This is known as a multi-dimensional array, or an array that contains other arrays. Notice that this array also contains JavaScript objects, which we will examine very closely in our next section, but for now, all you need to know is that arrays are also capable of storing complex objects.

        let complexArray = [
        [
            {
            one: 1,
            two: 2
            },
            {
            three: 3,
            four: 4
            }
        ],
        [
            {
            a: "a",
            b: "b"
            },
            {
            c: "c",
            d: "d"
            }
        ]
        ];
    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a variable called <mark>yourArray</mark>. Complete the statement by assigning an array of at least 5 elements in length to the <mark>yourArray</mark> variable. Your array should contain at least one string, one number, and one boolean.

        let yourArray = ['cat', 4, 'apple', true, 9, undefined, 0, ""]; // Change this line
        console.log(yourArray.length);
        // logs 7
___
2. Access an Array's Contents Using Bracket Notation  

    The fundamental feature of any data structure is, of course, the ability to not only store data, but to be able to retrieve that data on command. So, now that we've learned how to create an array, let's begin to think about how we can access that array's information.

    When we define a simple array as seen below, there are 3 items in it:

        let ourArray = ["a", "b", "c"];

    In an array, each array item has an index. This index doubles as the position of that item in the array, and how you reference it. However, it is important to note, that JavaScript arrays are zero-indexed, meaning that the first element of an array is actually at the zeroth position, not the first. In order to retrieve an element from an array we can enclose an index in brackets and append it to the end of an array, or more commonly, to a variable which references an array object. This is known as bracket notation. For example, if we want to retrieve the <mark>"a"</mark> from <mark>ourArray</mark> and assign it to a variable, we can do so with the following code:

        let ourVariable = ourArray[0];
        // ourVariable equals "a"
        
    In addition to accessing the value associated with an index, you can also set an index to a value using the same notation:

        ourArray[1] = "not b anymore";
        // ourArray now equals ["a", "not b anymore", "c"];

    Using bracket notation, we have now reset the item at index 1 from <mark>"b"</mark>, to <mark>"not b anymore"</mark>.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) In order to complete this challenge, set the 2nd position (index <mark>1</mark>) of <mark>myArray</mark> to anything you want, besides <mark>"b"</mark>.

        let myArray = ["a", "b", "c", "d"];
        // Only change code below this line
        myArray[1] = "b changed"
        // Only change code above this line
        console.log(myArray);
___
3. Add Items to an Array with push() and unshift()   

    An array's length, like the data types it can contain, is not fixed. Arrays can be defined with a length of any number of elements, and elements can be added or removed over time; in other words, arrays are mutable. In this challenge, we will look at two methods with which we can programmatically modify an array: <mark>Array.push()</mark> and <mark>Array.unshift()</mark>.

    Both methods take one or more elements as parameters and add those elements to the array the method is being called on; the <mark>push()</mark> method adds elements to the end of an array, and <mark>unshift()</mark> adds elements to the beginning. Consider the following:

        let twentyThree = 'XXIII';
        let romanNumerals = ['XXI', 'XXII'];

        romanNumerals.unshift('XIX', 'XX');
        // now equals ['XIX', 'XX', 'XXI', 'XXII']

        romanNumerals.push(twentyThree);
        // now equals ['XIX', 'XX', 'XXI', 'XXII', 'XXIII']Notice that we can also pass variables, which allows us even greater flexibility in dynamically modifying our array's data.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)We have defined a function, <mark>mixedNumbers</mark>, which we are passing an array as an argument. Modify the function by using <mark>push()</mark> and <mark>unshift()</mark> to add <mark>'I', 2, 'three'</mark> to the beginning of the array and <mark>7, 'VIII', 9</mark> to the end so that the returned array contains representations of the numbers 1-9 in order. 

        function mixedNumbers(arr) {
        // Only change code below this line
        arr.unshift('I', 2, 'three')
        arr.push(7, 'VIII', 9)
        // Only change code above this line
        return arr;
        }

        console.log(mixedNumbers(['IV', 5, 'six']));
___
4. Remove Items from an Array with pop() and shift()  

    Both <mark>push()</mark> and </mark>unshift() have corresponding methods that are nearly functional opposites: <mark>pop()</mark> and <mark>shift()</mark>. As you may have guessed by now, instead of adding, <mark>pop()</mark> removes an element from the end of an array, while <mark>shift()</mark> removes an element from the beginning. The key difference between <mark>pop()</mark> and <mark>shift()</mark> and their cousins <mark>push()</mark> and <mark>unshift()</mark>, is that neither method takes parameters, and each only allows an array to be modified by a single element at a time.

    *Let's take a look:*

        let greetings = ['whats up?', 'hello', 'see ya!'];

        greetings.pop();
        // now equals ['whats up?', 'hello']

        greetings.shift();
        // now equals ['hello']
    We can also return the value of the removed element with either method like this:

        let popped = greetings.pop();
        // returns 'hello'
        // greetings now equals []

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a function, <mark>popShift</mark>, which takes an array as an argument and returns a new array. Modify the function, using <mark>pop()</mark> and <mark>shift()</mark>, to remove the first and last elements of the argument array, and assign the removed elements to their corresponding variables, so that the returned array contains their values.

        function popShift(arr) {
            let popped = arr.pop(); // Change this line
            let shifted = arr.shift(); // Change this line
            return [shifted, popped];
        }

        console.log(popShift(['challenge', 'is', 'not', 'complete']));
___
5. Remove Items Using splice()  

    Ok, so we've learned how to remove elements from the beginning and end of arrays using <mark>shift()</mark> and <mark>pop()</mark>, but what if we want to remove an element from somewhere in the middle? Or remove more than one element at once? Well, that's where <mark>splice()</mark> comes in. <mark>splice()</mark> allows us to do just that: **remove any number of consecutive elements from anywhere in an array**.

    <mark>splice()</mark> can take up to 3 parameters, but for now, we'll focus on just the first 2. The first two parameters of <mark>splice()</mark> are integers which represent indexes, or positions, of the array that <mark>splice()</mark> is being called upon. And remember, arrays are zero-indexed, so to indicate the first element of an array, we would use <mark> 0 </mark>. <mark>splice()</mark>'s first parameter represents the index on the array from which to begin removing elements, while the second parameter indicates the number of elements to delete. For example:

        let array = ['today', 'was', 'not', 'so', 'great'];

        array.splice(2, 2);
        // remove 2 elements beginning with the 3rd element
        // array now equals ['today', 'was', 'great']

    <mark>splice()</mark> not only modifies the array it's being called on, but it also returns a new array containing the value of the removed elements:

        let array = ['I', 'am', 'feeling', 'really', 'happy'];

        let newArray = array.splice(3, 2);
        // newArray equals ['really', 'happy']
     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We've initialized an array <mark>arr</mark>0. Use <mark>splice()</mark> to remove elements from <mark>arr</mark>, so that it only contains elements that sum to the value of <mark> 10 </mark>.

        const arr = [2, 4, 5, 1, 7, 5, 2, 1];
        // Only change code below this line
        arr.shift();
        arr.splice(3);
        // Only change code above this line
        console.log(arr);   // [ 4, 5, 1 ] 
___
6. Add Items Using splice()

    Remember in the last challenge we mentioned that <mark>splice()</mark> can take up to three parameters? Well, you can use the third parameter, comprised of one or more element(s), to add to the array. This can be incredibly useful for quickly switching out an element, or a set of elements, for another.

        const numbers = [10, 11, 12, 12, 15];
        const startIndex = 3;
        const amountToDelete = 1;

        numbers.splice(startIndex, amountToDelete, 13, 14);
        // the second entry of 12 is removed, and we add 13 and 14 at the same index
        console.log(numbers);
        // returns [ 10, 11, 12, 13, 14, 15 ]

    Here we begin with an array of numbers. We then pass the following to <mark>splice()</mark>. The index at which to begin deleting elements (3), the number of elements to be deleted (1), and the elements (13, 14) to be inserted at that same index. Note that there can be any number of elements (separated by commas) following <mark>amountToDelete</mark>, each of which gets inserted.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a function, <mark>htmlColorNames</mark>, which takes an array of HTML colors as an argument. Modify the function using <mark>splice()</mark> to remove the first two elements of the array and add <mark>'DarkSalmon'</mark> and <mark>'BlanchedAlmond'</mark> in their respective places.

        function htmlColorNames(arr) {
        // Only change code below this line
        arr.splice(0, 2, 'DarkSalmon', 'BlanchedAlmond');
        // Only change code above this line
        return arr;
        }

        console.log(htmlColorNames(['DarkGoldenRod', 'WhiteSmoke', 'LavenderBlush', 'PaleTurquoise', 'FireBrick']));
___
7. Copy Array Items Using slice()  

    The next method we will cover is <mark>slice()</mark>. Rather than modifying an array, <mark>slice()</mark> copies or extracts a given number of elements to a new array, leaving the array it is called upon untouched. <mark>slice()</mark> takes only 2 parameters — the first is the index at which to begin extraction, and the second is the index at which to stop extraction (extraction will occur up to, but not including the element at this index). Consider this:

        let weatherConditions = ['rain', 'snow', 'sleet', 'hail', 'clear'];

        let todaysWeather = weatherConditions.slice(1, 3);
        // todaysWeather equals ['snow', 'sleet'];
        // weatherConditions still equals ['rain', 'snow', 'sleet', 'hail', 'clear']
    In effect, we have created a new array by extracting elements from an existing array.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a function, <mark>forecast</mark>, that takes an array as an argument. Modify the function using <mark>slice()</mark> to extract information from the argument array and return a new array that contains the elements <mark>'warm'</mark> and <mark>'sunny'</mark>.

        function forecast(arr) {
        // Only change code below this line
        let newArr = arr.slice(2, 4)
        return newArr;
        }

        // Only change code above this line
        console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));

___
8. Copy an Array with the Spread Operator  

    While <mark>slice()</mark> allows us to be selective about what elements of an array to copy, among several other useful tasks, ES6's new spread operator allows us to easily copy all of an array's elements, in order, with a simple and highly readable syntax. The spread syntax simply looks like this: <mark> ... </mark>

    *In practice, we can use the spread operator to copy an array like so:*

        let thisArray = [true, true, undefined, false, null];
        let thatArray = [...thisArray];
        // thatArray equals [true, true, undefined, false, null]
        // thisArray remains unchanged, and is identical to thatArray
    We have defined a function, <mark>copyMachine</mark> which takes <mark>arr</mark> (an array) and <mark>num</mark> (a number) as arguments. The function is supposed to return a new array made up of num copies of arr. We have done most of the work for you, but it doesn't work quite right yet. Modify the function using spread syntax so that it works correctly (hint: another method we have already covered might come in handy here!).

        function copyMachine(arr, num) {
        let newArr = [];
        while (num >= 1) {
            // Only change code below this line
            newArr.push([...arr]);
            // Only change code above this line
            num--;
        }
        return newArr;
        }

        console.log(copyMachine([true, false, true], 2));
___
9. Combine Arrays with the Spread Operator  

    Another huge advantage of the spread operator, is the ability to combine arrays, or to insert all the elements of one array into another, at any index. With more traditional syntaxes, we can concatenate arrays, but this only allows us to combine arrays at the end of one, and at the start of another. Spread syntax makes the following operation extremely simple:

        let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];

        let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
        // thatArray now equals ['basil', 'cilantro', 'sage', 'rosemary', 'parsley', 'thyme', 'coriander']
    Using spread syntax, we have just achieved an operation that would have been more complex and more verbose had we used traditional methods.

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a function <mark>spreadOut</mark> that returns the variable <mark>sentence</mark>. Modify the function using the spread operator so that it returns the array <mark>['learning', 'to', 'code', 'is', 'fun']</mark>.

        function spreadOut() {
        let fragment = ['to', 'code'];
        let sentence = ['learning', ...fragment, 'is', 'fun']; // Change this line
        return sentence;
        }

        console.log(spreadOut());
___
10. Check For The Presence of an Element With indexOf()  

    Since arrays can be changed, or mutated, at any time, there's no guarantee about where a particular piece of data will be on a given array, or if that element even still exists. Luckily, JavaScript provides us with another built-in method, <mark>indexOf()</mark>, that allows us to quickly and easily check for the presence of an element on an array. <mark>indexOf()</mark> takes an element as a parameter, and when called, it returns the position, or index, of that element, or <mark> -1 </mark> if the element does not exist on the array.

    **For example:**

        let fruits = ['apples', 'pears', 'oranges', 'peaches', 'pears'];

        fruits.indexOf('dates'); // returns -1
        fruits.indexOf('oranges'); // returns 2
        fruits.indexOf('pears'); // returns 1, the first index at which the element exists
    <mark>indexOf()</mark> can be incredibly useful for quickly checking for the presence of an element on an array. We have defined a function, <mark>quickCheck</mark>, that takes an array and an element as arguments. Modify the function using <mark>indexOf()</mark> so that it returns <mark>true</mark> if the passed element exists on the array, and <mark>false</mark> if it does not.

        function quickCheck(arr, elem) {
        // Only change code below this line
            return arr.indexOf(elem) >= 0
        // Only change code above this line
        }

        console.log(quickCheck(['squash', 'onions', 'shallots'], 'mushrooms')); //false
___
11. Iterate Through All an Array's Items Using For Loops  

    Sometimes when working with arrays, it is very handy to be able to iterate through each item to find one or more elements that we might need, or to manipulate an array based on which data items meet a certain set of criteria. JavaScript offers several built in methods that each iterate over arrays in slightly different ways to achieve different results (such as <mark>every()</mark>, <mark>forEach()</mark>, <mark>map()</mark>, etc.), however the technique which is most flexible and offers us the greatest amount of control is a simple <mark>for</mark> loop.

    *Consider the following:*

        function greaterThanTen(arr) {
        let newArr = [];
        for (let i = 0; i < arr.length; i++) {
            if (arr[i] > 10) {
            newArr.push(arr[i]);
            }
        }
        return newArr;
        }

        greaterThanTen([2, 12, 8, 14, 80, 0, 1]);
        // returns [12, 14, 80]

    Using a <mark>for</mark> loop, this function iterates through and accesses each element of the array, and subjects it to a simple test that we have created. In this way, we have easily and programmatically determined which data items are greater than <mark> 10 </mark>, and returned a new array containing those items.

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png)  We have defined a function, <mark>filteredArray</mark>, which takes <mark>arr</mark>, a nested array, and <mark>elem</mark> as arguments, and returns a new array. <mark>elem</mark> represents an element that may or may not be present on one or more of the arrays nested within <mark>arr</mark>. Modify the function, using a <mark>for</mark> loop, to return a filtered version of the passed array such that any array nested within <mark>arr</mark> containing <mark>elem</mark> has been removed.

        function filteredArray(arr, elem) {
        let newArr = [];
        // Only change code below this line
        const isNotEqual = (currentValue) => currentValue !== elem;
        for (let i = 0; i < arr.length; i++) {
        
            if(arr[i].every(isNotEqual)){
            newArr.push(arr[i])
            }
        }
        // Only change code above this line
        return newArr;
        }

        console.log(filteredArray([[3, 2, 3], [1, 6, 3], [3, 13, 26], [19, 3, 9]], 3)); // return []
        console.log(filteredArray([[10, 8, 3], [14, 6, 23], [3, 18, 6]], 18)) // return [ [10, 8, 3], [14, 6, 23] ]
        console.log(filteredArray([ ["amy", "beth", "sam"], ["dave", "sean", "peter"] ], "peter")) // return [ ["amy", "beth", "sam"] ]
___
12. Create complex multi-dimensional arrays  

    Awesome! You have just learned a ton about arrays! This has been a fairly high level overview, and there is plenty more to learn about working with arrays, much of which you will see in later sections. But before moving on to looking at Objects, lets take one more look, and see how arrays can become a bit more complex than what we have seen in previous challenges.

    One of the most powerful features when thinking of arrays as data structures, is that arrays can contain, or even be completely made up of other arrays. We have seen arrays that contain arrays in previous challenges, but fairly simple ones. However, arrays can contain an infinite depth of arrays that can contain other arrays, each with their own arbitrary levels of depth, and so on. In this way, an array can very quickly become very complex data structure, known as a multi-dimensional, or nested array. Consider the following example:

        let nestedArray = [ // top, or first level - the outer most array
        ['deep'], // an array within an array, 2 levels of depth
        [
            ['deeper'], ['deeper'] // 2 arrays nested 3 levels deep
        ],
        [
            [
            ['deepest'], ['deepest'] // 2 arrays nested 4 levels deep
            ],
            [
            [
                ['deepest-est?'] // an array nested 5 levels deep
            ]
            ]
        ]
        ];
    While this example may seem convoluted, this level of complexity is not unheard of, or even unusual, when dealing with large amounts of data. However, we can still very easily access the deepest levels of an array this complex with bracket notation:

        console.log(nestedArray[2][1][0][0][0]);
        // logs: deepest-est?
        And now that we know where that piece of data is, we can reset it if we need to:

        nestedArray[2][1][0][0][0] = 'deeper still';

        console.log(nestedArray[2][1][0][0][0]);
        // now logs: deeper still

    ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) We have defined a variable, <mark>myNestedArray</mark>, set equal to an array. Modify <mark>myNestedArray</mark>, using any combination of strings, numbers, and booleans for data elements, so that it has exactly five levels of depth (remember, the outer-most array is level 1). Somewhere on the third level, include the string <mark>'deep'</mark>, on the fourth level, include the string <mark>'deeper'</mark>, and on the fifth level, include the string <mark>'deepest'</mark>.

        let myNestedArray = [
        // Only change code below this line
        ['unshift', false, 1, 2, 3, 'complex', 'nested'],
        ['loop', 'shift', 6, 7, 1000, 'method'],
        ['concat', false, true, 'spread', 'array'],
        ['mutate', 1327.98, 'splice', 'slice', 'push'],
        ['iterate', 1.3849, 7, '8.4876', 'arbitrary', 'depth'],

        [
            ['deep', true, 5, 8.62] // arrays nested 3 levels deep
        ],
        [
            [
                ['deeper', 0, 'tatayoung', false] //arrays nested 4 levels deep
            ]
        ],
        [
            [
                [
                    ['deepest', 'folowup', 52.3, true] // array nested 5 levels deep
                ]
            ]
        ]
        // Only change code above this line
        ];

        myNestedArray[5][0][0];  //'deep'
        myNestedArray[6][0][0][0];  //'deeper'
        myNestedArray[7][0][0][0][0]; //'deepest'
___
13. Add Key-Value Pairs to JavaScript Objects  

    At their most basic, objects are just collections of key-value pairs. In other words, they are pieces of data (values) mapped to unique identifiers called properties (keys). Take a look at an example:

        const tekkenCharacter = {
            player: 'Hwoarang',
            fightingStyle: 'Tae Kwon Doe',
            human: true
        };
    The above code defines a Tekken video game character object called <mark>tekkenCharacter</mark>. It has three properties, each of which map to a specific value. If you want to add an additional property, such as <mark>"origin"</mark>, it can be done by assigning origin to the object:

        tekkenCharacter.origin = 'South Korea';

    This uses dot notation. If you were to observe the <mark>tekkenCharacter</mark> object, it will now include the <mark>origin</mark> property. Hwoarang also had distinct orange hair. You can add this property with bracket notation by doing:

        tekkenCharacter['hair color'] = 'dyed orange';

    Bracket notation is required if your property has a space in it or if you want to use a variable to name the property. In the above case, the property is enclosed in quotes to denote it as a string and will be added exactly as shown. Without quotes, it will be evaluated as a variable and the name of the property will be whatever value the variable is. Here's an example with a variable:

        const eyes = 'eye color';

        tekkenCharacter[eyes] = 'brown';
    After adding all the examples, the object will look like this:

        {
        player: 'Hwoarang',
        fightingStyle: 'Tae Kwon Doe',
        human: true,
        origin: 'South Korea',
        'hair color': 'dyed orange',
        'eye color': 'brown'
        };

     ![Logo](https://cdn1.iconfinder.com/data/icons/customicondesign-mini-deepcolour-png/16/File_edit.png) A <mark>foods</mark> object has been created with three entries. Using the syntax of your choice, add three more entries to it: <mark>bananas</mark> with a value of <mark> 13 </mark>, <mark>grapes</mark> with a value of <mark> 35 </mark>, and <mark>strawberries</mark> with a value of <mark>27</mark>.

        let foods = {
            apples: 25,
            oranges: 32,
            plums: 28
        };

        // Only change code below this line
        foods.bananas = 13;
        foods.strawberries  = 27;
        // Only change code above this line

        console.log(foods);
___
14. Modify an Object Nested Within an Object  

    Now let's take a look at a slightly more complex object. Object properties can be nested to an arbitrary depth, and their values can be any type of data supported by JavaScript, including arrays and even other objects. Consider the following:

        let nestedObject = {
        id: 28802695164,
        date: 'December 31, 2016',
        data: {
            totalUsers: 99,
            online: 80,
            onlineStatus: {
            active: 67,
            away: 13,
            busy: 8
            }
        }
        };

    <mark>nestedObject</mark> has three properties: <mark>id</mark> (value is a number), <mark>date</mark> (value is a string), and <mark>data</mark> (value is an object with its nested structure). While structures can quickly become complex, we can still use the same notations to access the information we need. To assign the value <mark>10</mark> to the <mark>busy</mark> property of the nested <mark>onlineStatus</mark> object, we use dot notation to reference the property:

        nestedObject.data.onlineStatus.busy = 10;

    Here we've defined an object <mark>userActivity</mark>, which includes another object nested within it. Set the value of the <mark>online</mark> key to <mark>45</mark>.

        let userActivity = {
            id: 23894201352,
            date: 'January 1, 2017',
            data: {
                totalUsers: 51,
                online: 42
            }
        };

        // Only change code below this line
        userActivity.data.online = 45;
        // Only change code above this line

        console.log(userActivity);
___
15. Access Property Names with Bracket Notation  

    In the first object challenge we mentioned the use of bracket notation as a way to access property values using the evaluation of a variable. For instance, imagine that our <mark>foods</mark> object is being used in a program for a supermarket cash register. We have some function that sets the <mark>selectedFood</mark> and we want to check our foods object for the presence of that <mark>food</mark>. This might look like:

        let selectedFood = getCurrentFood(scannedItem);
        let inventory = foods[selectedFood];

    This code will evaluate the value stored in the <mark>selectedFood</mark> variable and return the value of that key in the <mark>foods</mark> object, or <mark>undefined</mark> if it is not present. Bracket notation is very useful because sometimes object properties are not known before runtime or we need to access them in a more dynamic way.

    We've defined a function, <mark>checkInventory</mark>, which receives a scanned item as an argument. Return the current value of the <mark>scannedItem</mark> key in the <mark>foods</mark> object. You can assume that only valid keys will be provided as an argument to <mark>checkInventory</mark>.

        let foods = {
            apples: 25,
            oranges: 32,
            plums: 28,
            bananas: 13,
            grapes: 35,
            strawberries: 27
        };

        function checkInventory(scannedItem) {
        // Only change code below this line
        return foods[scannedItem];
        // Only change code above this line
        }

        console.log(checkInventory("apples"));
___
16. Use the delete Keyword to Remove Object Properties  

    Now you know what objects are and their basic features and advantages. In short, they are key-value stores which provide a flexible, intuitive way to structure data, and, they provide very fast lookup time. Throughout the rest of these challenges, we will describe several common operations you can perform on objects so you can become comfortable applying these useful data structures in your programs.

    In earlier challenges, we have both added to and modified an object's key-value pairs. Here we will see how we can remove a key-value pair from an object.

    Let's revisit our <mark>foods</mark> object example one last time. If we wanted to remove the <mark>apples</mark> key, we can remove it by using the <mark>delete</mark> keyword like this:

        delete foods.apples;
    Use the delete keyword to remove the <mark>oranges</mark>, <mark>plums</mark>, and <mark>strawberries</mark> keys from the <mark>foods</mark> object.

        let foods = {
            apples: 25,
            oranges: 32,
            plums: 28,
            bananas: 13,
            grapes: 35,
            strawberries: 27
        };

        // Only change code below this line
        delete foods.oranges;
        delete foods.plums;
        delete foods.strawberries; 
        // Only change code above this line

        console.log(foods);
___
17. Check if an Object has a Property  

    Now we can add, modify, and remove keys from objects. But what if we just wanted to know if an object has a specific property? JavaScript provides us with two different ways to do this. One uses the <mark>hasOwnProperty()</mark> method and the other uses the <mark>in</mark> keyword. If we have an object <mark>users</mark> with a property of <mark>Alan</mark>, we could check for its presence in either of the following ways:

        users.hasOwnProperty('Alan');
        'Alan' in users;
        // both return true

    We've created an object, <mark>users</mark>, with some users in it and a function <mark>isEveryoneHere</mark>, which we pass the <mark>users</mark> object to as an argument. Finish writing this function so that it returns <mark>true</mark> only if the <mark>users</mark> object contains all four names, <mark>Alan</mark>, <mark>Jeff</mark>, <mark>Sarah</mark>, and <mark>Ryan</mark>, as keys, and <mark>false</mark> otherwise.

        let users = {
        Alan: {
            age: 27,
            online: true
        },
        Jeff: {
            age: 32,
            online: true
        },
        Sarah: {
            age: 48,
            online: true
        },
        Ryan: {
            age: 19,
            online: true
        }
        };

        function isEveryoneHere(obj, prop) {
        // Only change code below this line
        return obj.hasOwnProperty(prop);
        // Only change code above this line
        }

        console.log(isEveryoneHere(users, 'Alan'));  //true
        console.log(isEveryoneHere(users, 'Sarah'));  //true
        console.log(isEveryoneHere(users, 'Baron'));  //false
___
18. Iterate Through the Keys of an Object with a for...in Statement  

    Sometimes you may need to iterate through all the keys within an object. This requires a specific syntax in JavaScript called a for...in statement. For our <mark>users</mark> object, this could look like:

        for (let user in users) {
        console.log(user);
        }

        // logs:
        Alan
        Jeff
        Sarah
        Ryan
    In this statement, we defined a variable <mark>user</mark>, and as you can see, this variable was reset during each iteration to each of the object's keys as the statement looped through the object, resulting in each user's name being printed to the console. **NOTE:** Objects do not maintain an ordering to stored keys like arrays do; thus a key's position on an object, or the relative order in which it appears, is irrelevant when referencing or accessing that key.

    We've defined a function <mark>countOnline</mark> which accepts one argument (a users object). Use a for...in statement within this function to loop through the users object passed into the function and return the number of users whose <mark>online</mark> property is set to <mark>true</mark>. An example of a users object which could be passed to <mark>countOnline</mark> is shown below. Each user will have an <mark>online</mark> property with either a <mark>true</mark> or <mark>false</mark> value.

       
        function countOnline(usersObj) {
            // Only change code below this line
            let sum = 0;
            for (let user in usersObj) {
                let count = +usersObj[user].online;
                sum+=count;
            }
            return sum;
            // Only change code above this line
        }

        let usersObj = {
            Alan: {
                online: false
            },
            Jeff: {
                online: true
            },
            Sarah: {
                online: false
            }
        };

        console.log(countOnline(usersObj)); //1
___
19. Generate an Array of All Object Keys with Object.keys()  

    We can also generate an array which contains all the keys stored in an object using the <mark>Object.keys()</mark> method and passing in an object as the argument. This will return an array with strings representing each property in the object. Again, there will be no specific order to the entries in the array.

    Finish writing the <mark>getArrayOfUsers</mark> function so that it returns an array containing all the properties in the object it receives as an argument.

        let users = {
            Alan: {
                age: 27,
                online: false
            },
            Jeff: {
                age: 32,
                online: true
            },
            Sarah: {
                age: 48,
                online: false
            },
            Ryan: {
                age: 19,
                online: true
            }
        };

        function getArrayOfUsers(obj) {
            // Only change code below this line
            return Object.keys(obj);
            // Only change code above this line
        }

        console.log(getArrayOfUsers(users));
___
20. Modify an Array Stored in an Object  

    Now you've seen all the basic operations for JavaScript objects. You can add, modify, and remove key-value pairs, check if keys exist, and iterate over all the keys in an object. As you continue learning JavaScript you will see even more versatile applications of objects. Additionally, the Data Structures lessons located in the Coding Interview Prep section of the curriculum also cover the ES6 Map and Set objects, both of which are similar to ordinary objects but provide some additional features. Now that you've learned the basics of arrays and objects, you're fully prepared to begin tackling more complex problems using JavaScript!

    Take a look at the object we've provided in the code editor. The <mark>user</mark> object contains three keys. The <mark>data</mark> key contains five keys, one of which contains an array of <mark>friends</mark>. From this, you can see how flexible objects are as data structures. We've started writing a function <mark>addFriend</mark>. Finish writing it so that it takes a <mark>user</mark> object and adds the name of the <mark>friend</mark> argument to the array stored in <mark>user.data.friends</mark> and returns that array.

        let user = {
            name: 'Kenneth',
            age: 28,
            data: {
                username: 'kennethCodesAllDay',
                joinDate: 'March 26, 2016',
                organization: 'freeCodeCamp',
                friends: [
                    'Sam',
                    'Kira',
                    'Tomo'
                ],
                location: {
                city: 'San Francisco',
                state: 'CA',
                country: 'USA'
                }
            }
        };

        function addFriend(userObj, friend) {
            // Only change code below this line
            userObj.data.friends.push(friend);
            return userObj.data.friends;
            // Only change code above this line
        }

        console.log(addFriend(user, 'Pete'));
___
## Basic Algorithm Scripting
> **Introduction to Basic Algorithm Scripting**     

A computer algorithm is a sequence of steps that is followed to achieve a particular outcome. To write an algorithm, you must first understand a problem, and then solve it with coding.

To make solving problems easier, it can be helpful to break them down into many chunks. Then, each chunk can be solved one by one. For example, if you are building a calculator, don't try to solve the problem as a whole. First, consider how to get inputs. Then, determine each arithmetic operation one by one. Finally, display the results.

In this section we will learn to solve basic algorithm problems using JavaScript. This will help you improve your problem solving skills and prepare you to later solve more complex problems.

**Hint:** If you get stuck, try using console.log() to log variable values to the console. This will help to debug problems.
___
1. Convert Celsius to Fahrenheit  

    The algorithm to convert from Celsius to Fahrenheit is the temperature in Celsius times <mark>9/5</mark>, plus <mark>32</mark>.

    You are given a variable <mark>celsius</mark> representing a temperature in Celsius. Use the variable <mark>fahrenheit</mark> already defined and assign it the Fahrenheit temperature equivalent to the given Celsius temperature. Use the algorithm mentioned above to help convert the Celsius temperature to Fahrenheit.

        function convertToF(celsius) {
        let fahrenheit = celsius*(9/5)+32;
        return fahrenheit;
        }

        console.log(convertToF(-10));
___
2. Reverse a String  

    Reverse the provided string.

    You may need to turn the string into an array before you can reverse it.

    Your result must be a string.

        function reverseString(str) {
             let arr = str.split("").reverse();
        
             return arr.join("");
        }

        console.log(reverseString("hello"));
___
3. Factorialize a Number  

    Return the factorial of the provided integer.

    If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.

    Factorials are often represented with the shorthand notation <mark> n! </mark>

    For example: <mark>5! = 1 * 2 * 3 * 4 * 5 = 120</mark>

    Only integers greater than or equal to zero will be supplied to the function.

        function factorialize(num) {
            let mul=1;
            for(let i=1; i <= num; i++){
                mul*=i;
            }
            return mul;
        }

        console.log(factorialize(5)); //120
___
4. Find the Longest Word in a String  

    Return the length of the longest word in the provided sentence.

    Your response should be a number.

        function findLongestWordLength(str) {
            let arr = str.split(" ");
            let lengthData = [];
            for (const element of arr) {
                lengthData.push(element.length);
            }
            return Math.max(...lengthData);
        }

        console.log(findLongestWordLength("The quick brown fox jumped over the lazy dog")); //6
___
5. Return Largest Numbers in Arrays  

    Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

    Remember, you can iterate through an array with a simple for loop, and access each member with array syntax <mark>arr[i]</mark>.

        function largestOfFour(arr) {
            let newArr = [];
            for (const element of arr) {
                let findMax = Math.max(...element);
                newArr.push(findMax);
            }
            return newArr;
        }

        let a = largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);

        console.log(a)  //[ 5, 27, 39, 1001 ]
___
6. Confirm the Ending  

    Check if a string (first argument, <mark>str</mark>) ends with the given target string (second argument, <mark>target</mark>).

    This challenge can be solved with the <mark>.endsWith()</mark> method, which was introduced in ES2015. But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.

        function confirmEnding(str, target) {
            return str.endsWith(target);
        }

        console.log(confirmEnding("Bastian", "n"));
___
7. Repeat a String Repeat a String

    Repeat a given string str (first argument) for num times (second argument). Return an empty string if num is not a positive number.

        function repeatStringNumTimes(str, num) {
            let newStr="";
            for(let i=0; i<num; i++){
            newStr+=str;
            }
            return newStr;
        }

        console.log(repeatStringNumTimes("abc", 3)); //'abcabcabc'
___
8. Truncate a String  

    Truncate a string (first argument) if it is longer than the given maximum string length (second argument). Return the truncated string with a <mark> ... </mark> ending.

        function truncateString(str, num) {
            let newText = str.substring(0,num);
            return newText+'...';
        }

        console.log(truncateString("A-tisket a-tasket A green and yellow basket", 8));
___
9. Finders Keepers  

    Create a function that looks through an array <mark>arr</mark> and returns the first element in it that passes a 'truth test'. This means that given an element <mark> x </mark>, the 'truth test' is passed if <mark>func(x)</mark> is <mark>true</mark>. If no element passes the test, return <mark>undefined</mark>.

        function findElement(arr, func) {

        let result = arr.filter(func);
        if(result.length == 0){
            return undefined;
        }
            return result.join(",");
        }


        console.log(findElement([1, 2, 3, 4], num => num % 2 === 0));  //2,4
___
10. Boo who  

    Check if a value is classified as a boolean primitive. Return true or false.

    Boolean primitives are true and false.

        function booWho(bool) {
            switch(bool){
                case true: 
                bool = true;
                break;
                case false: 
                bool = true;
                break;
            }
            if(Array.isArray(bool) || typeof(bool) === 'object' || typeof(bool) === 'function'){
                bool=false;
            }
            if(typeof(bool) === 'number' || typeof(bool) === 'string'){
                bool=false;
            }
        return bool;
        }

        console.log(booWho([].slice));  //false
___
11. Title Case a Sentence  

    Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

    For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

        function titleCase(str) {
            let arr = str.split(" ");
            let newArr = [];

            for (let element of arr) {
                newArr.push(element.toUpperCase());
            }
            return newArr.join(" ");
        }

        console.log(titleCase("I'm a little tea pot"));
___
12. Slice and Splice  

    You are given two arrays and an index.

    Copy each element of the first array into the second array, in order.

    Begin inserting elements at index <mark> n </mark> of the second array.

    Return the resulting array. The input arrays should remain the same after the function runs.

        function frankenSplice(arr1, arr2, n) {
        let newArr2 = [...arr2];
            newArr2.splice(n, 0, ...arr1);
        return newArr2;
        }

        console.log(frankenSplice([1, 2, 3], [4, 5, 6], 1));


___
13. Falsy Bouncer  

    Remove all falsy values from an array.

    Falsy values in JavaScript are <mark>false</mark>, <mark>null</mark>, <mark> 0 </mark>, <mark>""</mark>, <mark>undefined</mark>, and <mark>NaN</mark>.

    **Hint:** Try converting each value to a Boolean.

        function bouncer(arr) {
            let newArr = [];
            for (const element of arr) {
                switch(!element){
                case false:
                case "":
                case null:
                case 0:
                case NaN:
                case undefined:
                    newArr.push(element);
                    break;
                }
            }

            return newArr;
        }

        console.log(bouncer([7, "ate", "", false, 9]));   //[ 7, 'ate', 9 ]

        console.log(bouncer([null, NaN, 1, 2, undefined]));  //[ 1, 2 ]
___
14. Where do I Belong  

    Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

    For example, <mark>getIndexToIns([1,2,3,4], 1.5)</mark> should return <mark> 1 </mark> because it is greater than <mark> 1 </mark> (index 0), but less than <mark> 2 </mark> (index 1).

    Likewise, <mark>getIndexToIns([20,3,5], 19)</mark> should return <mark> 2 </mark> because once the array has been sorted it will look like <mark>[3,5,20]</mark> and <mark>19</mark> is less than <mark>20</mark> (index 2) and greater than <mark>5</mark> (index 1).

        function getIndexToIns(arr, num) {
            arr.sort(function(a, b){return a-b});
            let findInd = 0;
                for (const element of arr) {

                    if(element === num){
                        findInd = arr.indexOf(element);
                        break;
                    }
                    
                    if(element > num){
                        findInd = arr.indexOf(element);
                        break;
                    }

                }
            return findInd;
        }

        console.log(getIndexToIns([40, 60], 50)); //1
        console.log(getIndexToIns([5, 3, 20, 3], 5));  //2
        console.log(getIndexToIns([], 1)); //0
___
15. Mutations  

    Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

    For example, <mark>["hello", "Hello"]</mark>, should return true because all of the letters in the second string are present in the first, ignoring case.

    The arguments <mark>["hello", "hey"]</mark> should return false because the string "hello" does not contain a "y".

    Lastly, <mark>["Alien", "line"]</mark>, should return true because all of the letters in "line" are present in "Alien".

        function mutation(arr) {
        let index0 = arr[0].toLowerCase();
        let index1 = arr[1].toLowerCase();
        let bool = true;
            if(index0.length >= index1.length){
            for (const element of index1) {
                if(!index0.includes(element)){
                    bool = false;
                    break;
                } 
            }

            }
            if(index0.length < index1.length){
            for (const element of index0) {
                if(!index1.includes(element)){
                    bool = false;
                    break;
                } 
            }

            }
        
        return bool;
        }

        console.log(mutation(["hello", "hey"]));  //false
        console.log(mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"]));  //true
        console.log(mutation(["Mary", "Army"]))  //true
___
16. Chunky Monkey  

    Write a function that splits an array (first argument) into groups the length of <mark>size</mark> (second argument) and returns them as a two-dimensional array.

        function chunkArrayInGroups(arr, size) {
            let round = arr.length/size;
            let newArr = [];
                if((arr.length % size) === 0 ){
                    for(let i=0; i<round; i++){
                        let insert = arr.splice(0, size);
                        newArr.push(insert);
                    }
                }else{

                    for(let i=0; i < Math.ceil(round); i++){
                        let insert = arr.splice(0, size);
                        newArr.push(insert);
                    }
                }


            return newArr;
        }

        console.log(chunkArrayInGroups(["a", "b", "c", "d"], 2));
        console.log(chunkArrayInGroups([0, 1, 2, 3, 4, 5], 4));
        console.log(chunkArrayInGroups([0, 1, 2, 3, 4, 5, 6, 7, 8], 2));
___
## Object Oriented Programming 
> **Introduction to the Object Oriented Programming Challenges**    
    
   At its core, software development solves a problem or achieves a result with computation. The software development process first defines a problem, then presents a solution. Object oriented programming is one of several major approaches to the software development process.

As its name implies, object oriented programming organizes code into object definitions. These are sometimes called classes, and they group together data with related behavior. The data is an object's attributes, and the behavior (or functions) are methods.

The object structure makes it flexible within a program. Objects can transfer information by calling and passing data to another object's methods. Also, new classes can receive, or inherit, all the features from a base or parent class. This helps to reduce repeated code.

Your choice of programming approach depends on a few factors. These include the type of problem, as well as how you want to structure your data and algorithms. This section covers object oriented programming principles in JavaScript.
___
1. Create a Basic JavaScript Object  

    Think about things people see every day, like cars, shops, and birds. These are all objects: tangible things people can observe and interact with.

    What are some qualities of these objects? A car has wheels. Shops sell items. Birds have wings.

    These qualities, or properties, define what makes up an object. Note that similar objects share the same properties, but may have different values for those properties. For example, all cars have wheels, but not all cars have the same number of wheels.

    Objects in JavaScript are used to model real-world objects, giving them properties and behavior just like their real-world counterparts. Here's an example using these concepts to create a <mark>duck</mark> object:

        let duck = {
        name: "Aflac",
        numLegs: 2
        };

    This <mark>duck</mark> object has two property/value pairs: a <mark>name</mark> of "Aflac" and a <mark>numLegs</mark> of 2.

    Create a <mark>dog</mark> object with <mark>name</mark> and <mark>numLegs</mark> properties, and set them to a string and a number, respectively.

        let dog = {
        name: "Chobby",
        numLegs: 4
        };
___
2. Use Dot Notation to Access the Properties of an Object  

    The last challenge created an object with various properties. Now you'll see how to access the values of those properties. Here's an example:

        let duck = {
        name: "Aflac",
        numLegs: 2
        };
        console.log(duck.name);
        // This prints "Aflac" to the console

    Dot notation is used on the object name, <mark>duck</mark>, followed by the <mark>name</mark> of the property, name, to access the value of "Aflac".

    Print both properties of the <mark>dog</mark> object to your console.

        let dog = {
            name: "Spot",
            numLegs: 4
        };
        console.log(dog.name);
        console.log(dog.numLegs);
        // Only change code below this line
___
3. Create a Method on an Object  

    Objects can have a special type of property, called a method.

    Methods are properties that are functions. This adds different behavior to an object. Here is the <mark>duck</mark> example with a method:

        let duck = {
        name: "Aflac",
        numLegs: 2,
        sayName: function() {return "The name of this duck is " + duck.name + ".";}
        };
        duck.sayName();
        // Returns "The name of this duck is Aflac."

    The example adds the <mark>sayName</mark> method, which is a function that returns a sentence giving the name of the <mark>duck</mark>. Notice that the method accessed the name property in the return statement using <mark>duck.name</mark>. The next challenge will cover another way to do this.

    Using the <mark>dog</mark> object, give it a method called <mark>sayLegs</mark>. The method should return the sentence "This dog has 4 legs."

        let dog = {
            name: "Spot",
            numLegs: 4,
            sayLegs: function() {return "The dog has " + dog.numLegs + " legs.";}
        };

        console.log(dog.sayLegs()); //The dog has 4 legs.
___
4. Make Code More Reusable with the this Keyword  

    The last challenge introduced a method to the <mark>duck</mark> object. It used <mark>duck.name</mark> dot notation to access the value for the <mark>name</mark> property within the return statement:

    >sayName: function() {return "The name of this duck is " + duck.name + ".";}

    While this is a valid way to access the object's property, there is a pitfall here. If the variable name changes, any code referencing the original name would need to be updated as well. In a short object definition, it isn't a problem, but if an object has many references to its properties there is a greater chance for error.

    A way to avoid these issues is with the <mark>this</mark> keyword:

        let duck = {
        name: "Aflac",
        numLegs: 2,
        sayName: function() {return "The name of this duck is " + this.name + ".";}
        };

    <mark>this</mark> is a deep topic, and the above example is only one way to use it. In the current context, <mark>this</mark> refers to the object that the method is associated with: <mark>duck</mark>. If the object's name is changed to <mark>mallard</mark>, it is not necessary to find all the references to <mark>duck</mark> in the code. It makes the code reusable and easier to read.

    Modify the <mark>dog.sayLegs</mark> method to remove any references to <mark>dog</mark>. Use the <mark>duck</mark> example for guidance.

        let dog = {
            name: "Spot",
            numLegs: 4,
            sayLegs: function() {return "This dog has " + this.numLegs + " legs.";}
        };

        console.log(dog.sayLegs());
___
5. Define a Constructor Function

    Constructors are functions that create new objects. They define properties and behaviors that will belong to the new object. Think of them as a blueprint for the creation of new objects.

    Here is an example of a constructor:

        function Bird() {
            this.name = "Albert";
            this.color = "blue";
            this.numLegs = 2;
        }

    This constructor defines a <mark>Bird</mark> object with properties <mark>name</mark>, <mark>color</mark>, and <mark>numLegs</mark> set to Albert, blue, and 2, respectively. Constructors follow a few conventions:

    * <mark>Constructors</mark> are defined with a capitalized name to distinguish them from other functions that are not constructors.
    * Constructors use the keyword <mark>this</mark> to set properties of the object they will create. Inside the constructor, <mark>this</mark> refers to the new object it will create.
    * Constructors define properties and behaviors instead of returning a value as other functions might.

    *Create a constructor, <mark>Dog</mark>, with properties <mark>name</mark>, <mark>color</mark>, and <mark>numLegs</mark> that are set to a string, a string, and a number, respectively.*

        function Dog() {
            this.name = "Chobby";
            this.color = "white";
            this.numLegs = 4;
        }
___
6. Use a Constructor to Create Objects  

    Here's the <mark>Bird</mark> constructor from the previous challenge:

        function Bird() {
        this.name = "Albert";
        this.color  = "blue";
        this.numLegs = 2;
        // "this" inside the constructor always refers to the object being created
        }

        let blueBird = new Bird();

    Notice that the <mark>new</mark> operator is used when calling a constructor. This tells JavaScript to create a new instance of <mark>Bird</mark> called <mark>blueBird</mark>. Without the <mark>new</mark> operator, <mark>this</mark> inside the constructor would not point to the newly created object, giving unexpected results. Now <mark>blueBird</mark> has all the properties defined inside the <mark>Bird</mark> constructor:

        blueBird.name; // => Albert
        blueBird.color; // => blue
        blueBird.numLegs; // => 2

    Just like any other object, its properties can be accessed and modified:

        blueBird.name = 'Elvira';
        blueBird.name; // => Elvira
    Use the <mark>Dog</mark> constructor from the last lesson to create a new instance of <mark>Dog</mark>, assigning it to a variable <mark>hound</mark>.

        function Dog() {
            this.name = "Chobby";
            this.color = "white";
            this.numLegs = 4;
        }
        // Only change code below this line
        let hound = new Dog();

        console.log(hound)  //{ name: 'Chobby', color: 'white', numLegs: 4 }
___
7. Extend Constructors to Receive Arguments  

    The <mark>Bird</mark> and <mark>Dog</mark> constructors from last challenge worked well. However, notice that all <mark>Birds</mark> that are created with the <mark>Bird</mark> constructor are automatically named Albert, are blue in color, and have two legs. What if you want birds with different values for name and color? It's possible to change the properties of each bird manually but that would be a lot of work:

        let swan = new Bird();
        swan.name = "Carlos";
        swan.color = "white";
    Suppose you were writing a program to keep track of hundreds or even thousands of different birds in an aviary. It would take a lot of time to create all the birds, then change the properties to different values for every one. To more easily create different <mark>Bird</mark> objects, you can design your Bird constructor to accept parameters:

        function Bird(name, color) {
        this.name = name;
        this.color = color;
        this.numLegs = 2;
        }
    Then pass in the values as arguments to define each unique <mark>bird</mark> into the Bird constructor: <mark>let cardinal = new Bird("Bruce", "red");</mark> This gives a new instance of <mark>Bird</mark> with name and color properties set to Bruce and red, respectively. The <mark>numLegs</mark> property is still set to 2. The <mark>cardinal</mark> has these properties:

        cardinal.name // => Bruce
        cardinal.color // => red
        cardinal.numLegs // => 2
    The constructor is more flexible. It's now possible to define the properties for each <mark>Bird</mark> at the time it is created, which is one way that JavaScript constructors are so useful. They group objects together based on shared characteristics and behavior and define a blueprint that automates their creation.

    Create another <mark>Dog</mark> constructor. This time, set it up to take the parameters <mark>name</mark> and <mark>color</mark>, and have the property <mark>numLegs</mark> fixed at 4. Then create a new Dog saved in a variable terrier. Pass it two strings as arguments for the <mark>name</mark> and <mark>color</mark> properties.

        function Dog(name, color) {
            this.name = name;
            this.color = color;
            this.numLegs = 4;
        }

        let terrier = new Dog("barky","black");

        console.log(terrier.name);
        console.log(terrier.color);
        console.log(terrier.numLegs);
___
8. Verify an Object's Constructor with instanceof  

    Anytime a constructor function creates a new object, that object is said to be an instance of its constructor. JavaScript gives a convenient way to verify this with the <mark>instanceof</mark> operator. <mark>instanceof</mark> allows you to compare an object to a constructor, returning <mark>true</mark> or <mark>false</mark> based on whether or not that object was created with the constructor. Here's an example:

        let Bird = function(name, color) {
            this.name = name;
            this.color = color;
            this.numLegs = 2;
        }

        let crow = new Bird("Alexis", "black");

        crow instanceof Bird; // => true
    If an object is created without using a constructor, <mark>instanceof</mark> will verify that it is not an instance of that constructor:

        let canary = {
            name: "Mildred",
            color: "Yellow",
            numLegs: 2
        };

        canary instanceof Bird; // => false
    Create a new instance of the <mark>House</mark> constructor, calling it <mark>myHouse</mark> and passing a number of bedrooms. Then, use <mark>instanceof</mark> to verify that it is an instance of <mark>House</mark>.

        function House(numBedrooms) {
            this.numBedrooms = numBedrooms;
        }

        // Only change code below this line
        let myHouse = new House(3);

        console.log(myHouse instanceof House); // => true
___
9. 
![Imgur](https://i.imgur.com/e2hMgTD.jpg)
Add the <mark>own</mark> properties of <mark>canary</mark> to the array <mark>ownProps</mark>.

    function Bird(name) {
        this.name = name;
        this.numLegs = 2;
    }

    let canary = new Bird("Tweety");
    let ownProps = [];

    // Only change code below this line
    for (let property in canary) {
        if(canary.hasOwnProperty(property)) {
            ownProps.push(property);
        }
    }

    console.log(ownProps); // prints [ "name", "numLegs" ]
___
10. 
![Imgur](https://i.imgur.com/NGRXJJa.jpg)

    function Dog(name) {
        this.name = name;
    }

    Dog.prototype.numLegs = 4;

    // Only change code above this line

    let beagle = new Dog("Snoopy");
    console.log(beagle.numLegs);  //prints 4
___
11. 
![Imgur](https://i.imgur.com/FQHINuN.jpg)
![Imgur](https://i.imgur.com/cKF3BwG.jpg)

    function Dog(name) {
         this.name = name;
    }

    Dog.prototype.numLegs = 4;

    let beagle = new Dog("Snoopy");

    let ownProps = [];
    let prototypeProps = [];

    // Only change code below this line
    for (let property in beagle) {
        if(beagle.hasOwnProperty(property)) {
            ownProps.push(property);
        } else {
            prototypeProps.push(property);
        }
    }

    console.log(ownProps); // prints ["name"];
    console.log(prototypeProps); // prints ["numLegs"];
___
12. 
![Imgur](https://i.imgur.com/tLtAgxS.jpg)
![Imgur](https://i.imgur.com/cw0FJJy.jpg)

    function Dog(name) {
        this.name = name;
    }

    // Only change code below this line
    function joinDogFraternity(candidate) {
        if (candidate.constructor === Dog) {
            return true;
        } else {
            return false;
        }
    }

    let beagle = new Dog();
    console.log(beagle.constructor === Dog);  //prints true

___
13. 
![Imgur](https://i.imgur.com/j2VBWNd.jpg)
![Imgur](https://i.imgur.com/2lhfAMp.jpg)

    function Dog(name) {
        this.name = name;
    }

    Dog.prototype = {
        // Only change code below this line
        numLegs: 4, 
        eat: function() {
            console.log("eat chicken!!");
        },
        describe: function() {
            console.log("My name is " + this.name);
        }
    };
___
14. 
![Imgur](https://i.imgur.com/IBwrkgE.jpg)

    function Dog(name) {
        this.name = name;
    }

    // Only change code below this line
    Dog.prototype = {
        constructor: Dog, // define the constructor property
        numLegs: 4,
        eat: function() {
            console.log("eat chicken!!");
        },
        describe: function() {
            console.log("My name is " + this.name);
        }
    };
___
15. 
![Imgur](https://i.imgur.com/7hOtjQs.png)

    function Dog(name) {
        this.name = name;
    }

    let beagle = new Dog("Snoopy");

    // Only change code below this line
    console.log(Dog.prototype.isPrototypeOf(beagle));  // returns true
___
16. 
![Imgur](https://i.imgur.com/gBXczB7.png)

    function Dog(name) {
        this.name = name;
    }

    let beagle = new Dog("Snoopy");

    Dog.prototype.isPrototypeOf(beagle);  // yields true

    // Fix the code below so that it evaluates to true
    console.log(Object.prototype.isPrototypeOf(Dog.prototype)); //true

    console.log(beagle.hasOwnProperty("name")); // yields true
___
17. 
![Imgur](https://i.imgur.com/5BiZ1Ym.png)
![Imgur](https://i.imgur.com/1rmsBlA.png)

    function Cat(name) {
        this.name = name;
    }

    Cat.prototype = {
        constructor: Cat
    };

    function Bear(name) {
        this.name = name;
    }

    Bear.prototype = {
        constructor: Bear
    };

    function Animal() { }

        Animal.prototype = {
        constructor: Animal,
        eat: function() {
            console.log("nom nom nom");
        }
    };
___
18. 
![Imgur](https://i.imgur.com/x4pTqN8.png)
![Imgur](https://i.imgur.com/TzWSpvP.png)

    function Animal() { }

    Animal.prototype = {
        constructor: Animal,
        eat: function() {
            console.log("nom nom nom");
        }
    };

    // Only change code below this line

    let duck = Object.create(Animal.prototype); // Change this line
    let beagle = Object.create(Animal.prototype); // Change this line

    duck.eat(); // prints "nom nom nom"
    console.log(duck instanceof Animal); // prints true
___
19. 
![Imgur](https://i.imgur.com/xFsPTi0.png)

        function Animal() { }

        Animal.prototype = {
            constructor: Animal,
            eat: function() {
                console.log("nom nom nom");
            }
        };

        function Dog() { }

        // Only change code below this line

        Dog.prototype = Object.create(Animal.prototype);

        let beagle = new Dog();
        beagle.eat(); // prints "nom nom nom"
___
20. 
![Imgur](https://i.imgur.com/3baKeKg.png)

    function Animal() { }
    function Bird() { }
    function Dog() { }

    Bird.prototype = Object.create(Animal.prototype);
    Dog.prototype = Object.create(Animal.prototype);

    // Only change code below this line

    let duck = new Bird();
    let beagle = new Dog();

    Bird.prototype.constructor = Bird;
    duck.constructor // function Bird(){...}


    Dog.prototype.constructor = Dog;
    beagle.constructor // function Dog(){...}
___
21. 
![Imgur](https://i.imgur.com/6oA76jX.png)
![Imgur](https://i.imgur.com/iRqgIfa.png)

    function Animal() { }
    Animal.prototype.eat = function() { console.log("nom nom nom"); };

    function Dog() { }

    // Only change code below this line

    Dog.prototype = Object.create(Animal.prototype);
    Dog.prototype.constructor = Dog;

    Dog.prototype.bark = function() {
    console.log("Woof!");
    };

    let beagle = new Dog();
    beagle.eat(); // prints "nom nom nom"
    beagle.bark(); // prints "Woof!"

    // Only change code above this line
___
22. 
![Imgur](https://i.imgur.com/uuEZTMy.png)
![Imgur](https://i.imgur.com/S4JZrmm.png)

    function Bird() { }

    Bird.prototype.fly = function() { return "I am flying!"; };

    function Penguin() { }
    Penguin.prototype = Object.create(Bird.prototype);
    Penguin.prototype.constructor = Penguin;

    // Only change code below this line
    Penguin.prototype.fly = function() {
    return "Alas, this is a flightless bird.";
    };

    // Only change code above this line

    let penguin = new Penguin();
    console.log(penguin.fly());
___
23. 
![Imgur](https://i.imgur.com/hnaUdfd.png)
![Imgur](https://i.imgur.com/HSPtbQv.png)

    let bird = {
    name: "Donald",
    numLegs: 2
    };

    let boat = {
    name: "Warrior",
    type: "race-boat"
    };

    // Only change code below this line
    let glideMixin = function(obj) {
        obj.glide = function() {
        console.log("Gliding, wooosh!");
    }
    };

    glideMixin(bird);
    glideMixin(boat);

    bird.glide(); // prints "Gliding, wooosh!"
    boat.glide(); // prints "Gliding, wooosh!"
___
24. 
![Imgur](https://i.imgur.com/CUC7d3r.png)
![Imgur](https://i.imgur.com/R9K9TMU.png)

    function Bird() {
        let weight = 15;

        this.getWeight = function() { 
            return weight;
        };
    }

    let ducky = new Bird();
    console.log(ducky.getWeight()); // returns 15
___
25. 
![Imgur](https://i.imgur.com/ZPumZZT.png)

    (function makeNest() {
    console.log("A cozy nest is ready");
    })(); 

    // this is an anonymous function expression that executes right away
    // Outputs "A cozy nest is ready" immediately
___
26. 
![Imgur](https://i.imgur.com/eScRelk.png)
![Imgur](https://i.imgur.com/p3eGyiV.png)

    let isCuteMixin = function(obj) {
    obj.isCute = function() {
        return true;
    };
    };
    let singMixin = function(obj) {
    obj.sing = function() {
        console.log("Singing to an awesome tune");
    };
    };

    let funModule = (function () {
    return {
        isCuteMixin: function(obj) {
        obj.isCute = function() {
            return true;
        };
        },
        singMixin: function(obj) {
        obj.sing = function() {
        console.log("Singing to an awesome tune");
        };
        }
        
    }
    })(); 

    let duck = {};

    funModule.isCuteMixin(duck);
    funModule.singMixin(duck);
    console.log(duck.isCute());  //true
    duck.sing();  //prints "Singing to an awesome tune"