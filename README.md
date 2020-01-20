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
  
### Super globals 
Superglobals are predefined variables that will always be global in scope, they are as follows
  - $GLOBALS used to declare variables you want to be global
  - $_SERVER gets information about the server
  - $_REQUEST performs same tasks as get and post
  - $_POST gets information form an html form in a hidden manner
  - $_GET gets information from an html form and then stores it in the url
  - $_FILES used when uploading files. will get information such as name and size
  - $_ENV means environnment an it gets information from the webserver about specific things
  - $_COOKIE gets information about a cookie
  - $_SESSION declare session_start() and all variables declared within the session will be accesible with this one
 
Syntax 
    
    $_POST['value_of_form_element_you_are_targeting'] this goes for post and get which relate directly to forms, however all superglobals use [] and quotes.
    
    $_FILES['name'] would get the name of the file that has been uploaded

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
  a boolean is a data type that has two states, a "true" state and a "false" state normally denominated by 1(true) and 0(false) respectively.
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
Operators are mathematical symbols (though not neccesarily the same structure as general math) that tell the code to execute in a certain manner depending on what is specified.

### The classics
- + addition
- - subtraction
- / division
- * multiplication
- % modulus (calculates remainder)


### Assigning value
- = equals
- += add to original value and display value $x = $x + $y
- -= subtract from original value and display new value $x = $x - $y
- *= multiply and assign value $x = $x * $y
- /= divide and assign value $x = $x / $y
- %= modulus and assign value 	$x = $x % $y

### Comparitive values
- == equals one another
- === equal one another and are the same data type also known as "identical"
- != not equal
- <> same as above^
- !== not identical to one another
- < less than 
- > greater than
- <= less than or equal
- >= greater than or equal 

### Incrementing values
- ++= add one to value and then display value
- =++ display value and then add one
- --= subtract one to value and then display value
- =-- display value and then add one

### Logical operators
Logical operators allow a method of adding more restrictions/parameters to a function or equation
- **and** returns true when $x **and** $y are both true
-	**Or**	$x or $y	True if either $x **or** $y is true
- **Xor**	$x xor $y	True if either $x or $y is true, but not both
- **&&** same as **and**
- **||** same as **or**
- **!** not, returns true if statement was untrue 

### Array operators
Array operators behave the way one would expect, it essentially means any comparison made between arrays will also occur for every indice in the array.
- +	Union	$x + $y	Union of $x and $y
- ==	Equality	$x == $y	True if $x and $y have the same key/value pairs
- ===	Identity	$x === $y	True if $x and $y have the same key/value pairs in the same order and of the same types
- !=	Inequality	$x != $y	True if $x is not equal to $y
- <>	Inequality	$x <> $y	True if $x is not equal to $y
- !==	Non-identity	$x !== $y	True if $x is not identical to $y

### Spaceship operator
The spaceship operator is a new operator that essentially does the same arithmetic but outputs the result as either -1, 0, or +1.
it does this by making it a table of sorts +1 meaning that the left side is greater, 0 is the middle meaning oth sides are equal, and -1 is the right side saying that the right side is greater.

> (2 <=> 1), output will be +1
>
> (1 <=> 2), output will be -1
>
> (2 <=> 2), output will be 0

## CONDITIONAL STATEMENTS
Often times code only should be executed when a previous requirement is met, this is where **if, else, and elsif** statements come in.
they allow one to put there code into blocks where requirements are met and passed on accordingly.

### Example for if and else
   
   
  
    $passcode = "1f4532abe2";
    $input = //random user input;
   
    $if($input == $passcode){
      echo "succesful log in!;
      } else {
      echo "wrong passcode";
      };
      

### Example of elseif
    if ($a > $b) {
      echo "a is greater than b";
    } elseif ($a < $b) {
    echo "a is less than b";
    } else {
    echo "a and b are equal";
    };
  
   
## Functions

Functions are blocks of code that make for easy access and also to share into other areas. Functions can have parameters that affect there outcome and they can be linked together. almost all code will be wrapped in a function of some sort. Functions make code manageable, they allow one to reduce repetition as that task can always be called upon by invoking the function. They allow errors to be caught and managed as all the checks and catches will be in one block of code before it would pass on through the function.

Functions are declared by writing function 


    function yourfunctionname(){ 
    
    your code between the brackets
    
    } //between the parentheses is where you would put your parameter(s)

### Basic function examples 

     function multiplyByTwo($param){
      $result = $param * 2;
      echo $result;
      }
      
      multiplyByTwo(5);
**or multiple parameters**

      function findTheRemainder($num1, $divisor){
        $result = $num1 % $divisor;
        echo $result;
      }
      
      findTheRemainder(10, 3);
       
 
### Built in functions
often times there are native functions in php that can do specific actions, if you find yourself thinking "This has to have been done before." while coding, take a moment to check out the list of methods https://www.php.net/manual/en/indexes.functions.php 

### Variable Scope
  When making functions one uses variables, variables will be accesible depending on where they are initialized in the code. This is known as scope. When declared within a function the variable is accesible by everything within the function even if it's another function, however, It will not be accesible outside of the function. If you had to declare a variable within a function but then access it outside of it you can declare it as a "global".
          
       e.g 
          $var = "this is a globally scoped variable";
          function myFunction(){
           echo $var // output: "this is a globally scoped variable"
           
          }
          
       e.g 2
          function myFunction(){
           $var = "this is function scoped";
          }
         
          echo $var //output: undefined variable
         
       e.g 3
         function myFunction(){
           $var = "this is function scoped";
           global $var;
          }
         
          echo $var; //output: "this is function scoped"
          
      
## Loops
Loops will perform a task until a condition has been met, There are a few different types that are more suited to certain processes.

Loops are bet for tasks that involve repetition and/or automation as they can run for aslong as dictated perofrming a calculation or function

### While 
a while loop excutes aslong as something is true, easily understood as **while** it is true.
    
    $i = 0;
    while($i <= 20){
    $i++;
    echo $i . "<br>";
    } //while i is less than 20 increment until it reaches the value of 20 and show each increment
    

### do while
 A do while loop performs the action first and then checks to see if the condition is met, this means that there will always be a final action before completion.
    
    $i = 0
    do{  
        $i++; 
        echo $i . "<br>";
    } while( $i <= 20 )
    // there will be an extra output because it will increment and then check if it is equal to 20
    
 
    
### For
for loops will excute for a certain "scenario", they tend to have much of their variables declared withing their parentheses

    e.g 
    for( $i = 0; $i <= 20; $i++){
    echo $i . "<br>";
    } // they are compact loops and tend to be used more than while loops
    
    
  
  
  
### Foreach
Foreach loops are used in reference to arrays, it is saying "execute this action for every instance(indice) in this array". an extension of the for loop but with a more specialized use. The syntax goes ($nameofarray as $key => $value) $key and $value are words known by php and can be left as is when in reference to an array

    $elements = array( "iron" => "26", aluminium => "13", "lead" => "82");
    
    foreach($elements as $key => $value){
     echo "the atomic number of" . $key . "is" . $value;
    }
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
