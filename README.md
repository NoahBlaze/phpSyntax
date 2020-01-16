# phpSyntax
a php syntax guide to use when confused about certain elements.
## SECTION 1 COMMENTS
comments are useful to keep track of your functions and explain aspects of your code if another programmer were to look through it, it is reccomended that coders put lots of comments documenting their code for there benefit and others aswell.
The following are examples of comments that can be made in php
### Single line comment:
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
  echo and print both output information to the file and are very similar to eachother small differences include; print has a return value of 1, echo has no return value.  
