# What is an IDE?

An **IDE (Integrated Development Environment)** is a feature-rich text editor that includes **syntax highlighting, extensions, debugging tools, and more**—things that a basic editor like Notepad lacks.

You can use **any IDE** you like. For beginners, I recommend **Visual Studio Code (VS Code)**, but feel free to choose whatever works best for you.

> 🔗 **Download Visual Studio Code** from [here](https://code.visualstudio.com/download).

---

# What is GCC?

**GCC (GNU Compiler Collection)** is a widely used compiler for C and other programming languages. A compiler converts human-readable code into machine code (binary) that the CPU can understand.

Even though C looks like readable text to us, it's just gibberish to a computer. The CPU only understands **0s and 1s**, so we need a compiler like **GCC** to translate our code into something the computer can execute.

To write and run C programs, you'll need both an **IDE** and a **compiler**. The most common C compiler is **GCC**, so I recommend installing it.

> 📺 **Watch a tutorial on how to install GCC** [here](https://youtu.be/1PBD5qFWdq8?si=CEgrMdCU31fE7cJS).

---

# Creating a C File

First, create a C file. If you don't know how, watch [this tutorial](https://youtu.be/FrkoRrhTQ7s?si=YeFJfjVjx9E-X1rj). After that write this code in your IDE, don't copy paste no matter what i know you are 
well aware of memes on internet showing that a senior developer is copy pasting stuff but you're not a senior
developer so don't do it.

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

---

# Understanding the "Hello, World!" C Program

Let's break down this simple C program step by step.

## 1. The `#include <stdio.h>` Directive

The first line:

```c
#include <stdio.h>
```

This is a **preprocessor directive**, meaning it is executed before the program is compiled. It imports the `stdio.h` header file, which contains pre-written C code, including the `printf()` function.

### What is `stdio.h`?

- `stdio.h` stands for **Standard Input/Output**.
- It provides functions for handling input and output in C.
- The `printf()` function, which we use in this program, is defined in `stdio.h`.

### Why do we need it?

Without including `stdio.h`, we wouldn’t be able to use `printf()`. Writing such functionality from scratch would require **hundreds of lines of code**. By using pre-written functions, we make our program **more efficient and manageable**.

> **Tip:** Even though these functions are pre-written, it's beneficial to check out their implementations to understand how they work under the hood.

---

## 2. The `main()` Function

```c
int main(void) {}
```

- `main()` is the **entry point** of a C program.
- The keyword `int` indicates that the function returns an integer value.
- The `void` inside parentheses means that `main()` **does not take any arguments**.
- Everything inside `{}` (curly braces) belongs to the `main()` function.

---

## 3. Using `printf()`

```c
printf("Hello, World!\n");
```

- `printf()` is a function that prints text to the console.
- `"Hello, World!"` is the **argument** passed to `printf()`, specifying what to print.
- `\n` is an **escape sequence** that moves the cursor to the next line.

### What is an argument?

An **argument** is a value passed to a function when it is called. In this case, `"Hello, World!"` is passed to `printf()`, instructing it to print that text.

**Try removing `\n` and see how the output changes!**

---

## 4. The `return 0;` Statement

```c
return 0;
```

- This statement **ends** the `main()` function.
- Returning `0` typically indicates that the program executed **successfully**.

---

## 5. Closing the Function

The program ends when the closing `}` is reached. Any code written after this will be **outside** of the `main()` function.

---

This is how the **"Hello, World!"** program works in C! 🎉

> **Note:** If you are feeling overwhelmed by the terminologies, you're on the right track! Learning programming concepts can be challenging at first, but with patience, everything will start making sense for now try to understand what happened and move on to next lesson.

---