## Take user input and print it with other string.
There are two common method to take **input** in R.  
- `readline()` method
- `scan()` method

1. **`readline()` method**
```R
# Sntax
var = readline(“Your prompt message : “)
```

In R language `readline()` method takes input in string format.  
To convert the inputted value to the desired data type, there are some functions in R:
- `s.integer(n)`—> convert to integer
- `as.numeric(n)`—> convert to numeric type (float, double etc)
- `as.complex(n)`—> convert to complex number (i.e 3+2i)
- `as.Date(n)  —> convert to date …, etc


**Taking multiple inputs in R**
```R
# Syntax
var1 = readline(“Enter 1st number : “); 
var2 = readline(“Enter 2nd number : “); 
var3 = readline(“Enter 3rd number : “); 
var4 = readline(“Enter 4th number : “);
or,
{ 
var1 = readline(“Enter 1st number : “); 
var2 = readline(“Enter 2nd number : “); 
var3 = readline(“Enter 3rd number : “); 
var4 = readline(“Enter 4th number : “); 
}
```
2. **To learn about `scan()` method go to this [link](https://www.geeksforgeeks.org/taking-input-from-user-in-r-programming/)**

### Print user input with string
1. We can use `paste` with `print`
```R
print(paste0("User's input is: ", var)
```
**NB:** Here, we used `paste0` instead of `paste`, that's why there will be no automatic **spacing** between string and variable. If we want any space, we have to add it inside string.  

2. Or, we can use `cat` function
```R
cat("User's input is:", var)
```
**NB:** `cat` be default adds a **space** between string and variable.


