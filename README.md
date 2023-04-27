# JS-Fbonacci-Explanation
 
.This line of code gets the value entered by the user in the text box with the ID 'txtNumber' and stores it in the variable `numberEntered`.

```var counter = 1;```
This line of code initializes a counter variable to 1, which will be used to keep track of the number of Fibonacci numbers generated.

```var fib = [];```
This line of code initializes an empty array `fib`, which will be used to store the generated Fibonacci numbers.

if (numberEntered == 0) {
    fib = [0];
    document.getElementById('dialogboxbody').innerHTML = fib;
} else if(numberEntered == 1){
    fib = [1];
    document.getElementById('dialogboxbody').innerHTML = fib;
} else if(numberEntered == 2){
    fib = [1, 1];
    document.getElementById('dialogboxbody').innerHTML = fib;
} else if(numberEntered > 2){
    fib = [1, 1];
    while (counter < (numberEntered - 1)) {
        fib.push(fib[counter] + fib[counter - 1]);
        counter++;
    }
    document.getElementById('dialogboxbody').innerHTML = fib;
}
This block of code checks the value of `numberEntered` to determine what Fibonacci sequence to generate. If `numberEntered` is 0, it generates `[0]`, if it's 1, it generates `[1]`, and if it's 2, it generates `[1,1]`. If `numberEntered` is greater than 2, it generates the first `numberEntered` Fibonacci numbers using a while loop. The loop continues until the counter reaches `numberEntered - 1`, at which point all the Fibonacci numbers have been generated and stored in the `fib` array. Finally, the generated Fibonacci numbers are displayed in the dialog box with the ID 'dialogboxbody'.
