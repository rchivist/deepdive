# Comments

These are pretty basic so i'll just finish them in short.
```c
int x; // After double slash whatever we write will be ignored by compiler these are called comments.
/*
These are Multi-Line comment if we want to write long comments.
Although you might think to not write them but trust me writing these is extremely important,
you might feel that you can't write long code or a big project but i'll prove you wrong. you can and you will write a big program and when that happens these comments will save you.
*/
```

---

# Conditional Statements

These are simple construct statements which decide what to do/ execute depending upon the condition.
like ```if, if-else, if-elseif, switch``` just by reading these you can take a guess about what'll these do.
let's dive into them more deeply with a basic code.

```c
#include <stdio.h>

int main(void){
    int number = 12; // Variable declaration and initialization

    if( number = 12 ){
        printf("This code executed because the number is 12\n"); // block of code if condition was true
    }else{
        printf("This code would have executed if the number wasn't 12\n") // block of code if condition was false
    }
}
```
As you can see if-else conditional is pretty easy once you get the hang of it.
Try to create a program to check if a number is even or odd. Also i'll explain you scanf() for user inputs so that you can write a interactive program that'll take an user input and outputs if entered number is even or odd.

## scanf() || user input


