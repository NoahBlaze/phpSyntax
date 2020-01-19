# phpSyntax
a php syntax guide to use when confused about certain elements.
## SECTION 1 COMMENTS
comments are useful to keep track of your functions and explain aspects of your code if another programmer were to look through it, it is reccomended that coders put lots of comments documenting their code for there benefit and others aswell.
The following are examples of comments that can be made in php
### Comments:
  - // this is a single line comment
  - #this is also a single line comment
  - /* this is a multi line comment, you would use these if you had a large block of text explaining something central to your php */
## SECTION 2 VARIABLES
There are a few rules to variables in php they tend to be similar to javascript syntax
  - Variables start with $ symbol
  - The first character after the $ symbol must be a letter or an _
  - No spaces within the name of the variable
  - PHP is case sensitive meaning $var and $Var are different variables 
---
Constants follow the same rules but are declared as a function 
  > define("name_of_var", "value of var")
  >
  > eg
  >
  > define("constVar", 50)
  >
  > echo constVar // output 50
## SECTION 3 ECHO AND PRINT
  echo and print both output information to the file and are very similar to eachother small differences include; print has a return value of 1, echo has no return value. This means print can be used in expressions.
### Rules
  - Strings and vairables are added or "concantenated" with '.' 
    > eg $var . "a string" . $anotherVariable;
## SECTION 4 STRINGS
  strings are collections of characters enclosed between single quotes or double quotes, the function of single quotes and double quotes is different. single quotes will take everything within the string and represent it as it is written. double quotes will translate variables into their respective values. each string character is equivalent to a byte*
  >e.g
  >$example_string = 'hello world'
  >
  >output1_string = '$example_string is a cliche' //output: $example_string is a cliche
  >
  >output2_string = "$example_string is a cliche" //output: hello world is a cliche  >
  
  The backslash is how to tell the string to do certain structural things aswell as represent certain characters. the following are different special character statements that can be represented in a string.
  
  - \n new line
  - \r return the cursor to the beginning of the line
  - \t insert a Tab in the string
  - \$ show a literal dollar sign "$" 
  - \\" show a literal quation mark '"'
  - \\\ show a literal slash "/"
  
  ## DATA TYPES
  Coding involves the transfer and use of information, and information can be expressed in a few different forms that are easy for the computer to understand.
  ### Strings
  As was discussed previously strings are a way to store characters and each character is equivalent to one byte
  
  ### Integers
  One could view this as "easy" numbers rational whole numbers with out decimals they can be stored in a few different ways, including;
  decimal, hexadecimal, and octal. The following examples are all equivalent.
  > $deci = 332;
  >
  > $deci = -332;
  >
  > $hexa = 14C // I dont get it either
  >
  > $octal = 514
  
  ### Floating points
  This is the data type for decimal values.
  > $deci = 3.32;

  ### Booleans 
  a boolean is a data type that has two states a "true" state and a "false" state normally denominated by 1(true) and 0(false) respectively.
  > eg
  >
  > $boolean = "true";
  >
  > echo $boolean;
  ### Arrays
  Arrays store multiple variables in a sequence that can be manipulated, the sequence is called the index and each index has a value.
  there are three types of arrays 
  > INDEXED ARRAYS: probably the most common, they use numeric indexes for each value
  >
  > $indexArr = array("value1", "value2", "value3");
  >
  > $indexArr[0] = "value1";
  >
  > $indexArr[1] = "value2";
  >
  > $indexArr[2] = "value3";
  >
  > ASSOCIATIVE ARRAYS: these are arrays with named keys that have a value associated with the name. 
  >
  > $elements = array( "iron" => "26", aluminium => "13", "lead" => "82");
  >
  >  echo "the atomic number of iron is" . $element("iron");
  >
  > MULTIDIMENSIONAL ARRAYS: An array that contains other arrays within it, as the name implies it has many layers and each array could be index or associative depending on the requirements of the function.
  >
  > $multiDim = array( array("iron", "26", "metal"), array("aluminium", "13", "metal"), array("lead", "82", "heavy-metal"))
  >
  
## Operators

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
