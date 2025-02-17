# Variables  
A variable is a labelled container that stores information.  
A **value** is the actual piece of data stoerd in a variable.  

### Declaring variables
Declaring a variable means creating it without assigning a value. This tells JavaScript that a variable exists, but it does not have any value yet.  
The following are ways of declaring a variable:  
- var: old, not recommended for modern code.  
e.g. var name = "Daniel Spectre";  
- let: preferred for variables that change.  
e.g. let age = 45;  
- const: used for values that should not change.  
e.g. const pi = 3.142;  
Initializing a variable means assigning it an initial value at the time of declaration. When you try to read the value of a variable that has been declared but has not been initialized, you will get undefined as the output.  
```
let weight; // Declared but not initialized
console.log(weight); // Output: undefined
```
```
let weight = 67;
let grade = "A"; // Declared AND initialized with a value
console.log(weight); // Output: 67
console.log(grade); // Output: A
```
The variable constant `const` must be initialized immediately.  
### Rules for naming a variable  
1. Can only start with a letter, _ or $.  
2. Cannot be JavaScript reserved keywords e.g. let, var, console.  
3. Variabe names can only contain letters, numbers, underscore and dollar sign. Special characters and spaces should not be used.   
4. Variable names are case sensitive.  
5. Use meaningful and descriptive names.    


If a variable name is made up of multiple words, use the following:  
**snake case convention - python**  
let minutes_tuill_new_year = 55;  
**camel case convention - javascript**   
let minutesTillNewYear = 55;  
**pascal case convention - pascal, js: classes**  
let MinutesTillNewYear = 55;  