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
# User Input

In Lesson 1, we learned how to print something—meaning how to give an output. But what about input?
How do we take user input? Remember the header files? `<stdio.h>` stands for **standard input/output**. So, if there's output, there must be input too!

Just like the `printf()` function, there's a `scanf()` function for taking input. Let's dive into it.

```c
#include <stdio.h> // Pre-processor directive

int main(){
    int input;

    printf("Enter a Number\n>>>"); // A nice message to notify user for input
    scanf("%d", &input);

    printf("You entered %d as your number", input);
}
```

### Breaking Down the Code
By now, you should recognize familiar components like `#include`, `int main()`, etc.

You'll notice that we called the `scanf()` function, passing two arguments:
1. **`%d`** - The format specifier for an integer.
2. **`&input`** - The **ampersand** (`&`) operator.

But why use `&`? Isn't this similar to the logical AND operator? **No, it's different.**

- `%d` is a format specifier, meaning we expect an **integer** input.
- `&` is called the **address-of operator** and is used to pass the memory address of a variable.

### Why Use `&` Instead of Just the Variable Name?
C programming **passes variables to functions by value**, meaning a copy of the variable is passed instead of the actual location in memory.

In our case, the `scanf()` function wants to store the user input **inside** the `input` variable. But if we pass just `input`, it only gets a copy and can't modify the original variable. 
Instead, we pass the **memory address** of `input` using `&`, allowing `scanf()` to store the input directly in the correct location.


---

# Conditional Statements

These are simple construct statements that decide what to execute depending on the condition.
Statements like `if`, `if-else`, `if-elseif`, and `switch` give a good hint about their behavior just from their names.
Let's dive deeper with some basic examples.

---

## `if-else`
```c
#include <stdio.h>

int main(void){
    int number = 12; // Variable declaration and initialization

    if( number == 12 ){
        printf("This code executed because the number is 12\n"); // Block of code if condition is true
        printf("This will execute too! As long as it's inside the curly braces of the if statement.\n");
    }else{
        printf("This code would have executed if the number wasn't 12\n"); // Block of code if condition is false
    }
}
```
As you can see, `if-else` conditionals are pretty easy once you get the hang of them.

**Try This:** Create a program to check if a number is even or odd. If you struggle, read through the explanation again and try again. Of course, you can use AI, but where's the fun in that? 😉

---

## `if-elseif`
```c
#include <stdio.h>

int main(void){
    int number = 10;
    float num = 3.14;

    if ( number <= 0 ){
        printf("This message will not print since number is not smaller than zero\n");
    }else if ( num >= 203 ){
        printf("This message will not print either since float num isn't greater than 203\n");
    }else{
        printf("This message will print since both conditions are false\n");
    }
}
```

As you can see, `if-elseif` allows multiple conditions, with `else` acting as a fallback when all conditions are false.

---

## `switch case`
```c
#include <stdio.h>

int main(void){
    int weekday = 3;

    switch(weekday){ // Switch case
        case 1: 
            printf("Sunday\n");
            break;
        case 2:
            printf("Monday\n");
            break;
        case 3:
            printf("Tuesday\n"); // This will be the output
            break;
        case 4:
            printf("Wednesday\n");
            break;
        case 5:
            printf("Thursday\n");
            break;
        case 6:
            printf("Friday\n");
            break;
        case 7:
            printf("Saturday\n");
            break;
        default:
            printf("There are 7 days in a week, what did you even write?\n");
            break;
    }
}
```

The `switch` statement evaluates an expression to an integer value and jumps to the corresponding `case` label. Execution resumes from that point until a `break` statement is encountered, which exits the switch block.

**Differences Between `switch` and `if-elseif`**
1. `switch` is faster in some cases.
2. `if-elseif` can evaluate relational conditions (e.g., `<`, `>`, `!=`) and work with various types like floating-point numbers, while `switch` cannot.

---

## What Happens if We Don't Use `break`?
If we don’t include `break`, execution continues into the next case. This is called **fall-through**.

```c
switch (x) {
    case 1:
        printf("1\n");
        // Fall through!
    case 2:
        printf("2\n");
        break;
    case 3:
        printf("3\n");
        break;
}
```

### Expected Output:
- If `x == 1`, the program prints `1` and then `2` (since it falls through to `case 2` before hitting `break`).
- If `x == 2`, the program prints `2` and breaks.
- If `x == 3`, the program prints `3` and breaks.

Not having a `break` is a common source of **bugs** in C programs. If you intend to allow fall-through, always **leave a comment** to make it clear to others.

**Pro Tip:** Keep `switch` statements limited to **integer types**. Floating-point numbers and strings don’t work, but **character types** (`char`) can be used because they are internally represented as integers in C.
