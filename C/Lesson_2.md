# What Happens After We Run the Program?

If you're running your program by clicking the ▶️ button, stop for a moment and understand what is actually happening.

> **Tip:** The more you understand how things work, the better programmer you'll become. Avoid mindlessly pressing buttons—learn what they do!

## What is the ▶️ Button Doing?

The ▶️ button is using a **GCC wrapper**. Remember when you installed the GNU compiler? That button is just a wrapper for it.

## What is a Wrapper?

A **wrapper** is a script or program that acts as an intermediary between the user and the actual **GCC (GNU Compiler Collection)** compiler. Instead of interacting with the compiler manually, you just click a button, and it handles everything for you.

But since we are here to **learn**, let's do it the manual way!

## Manually Compiling a C Program

Open your terminal and type:

```bash
gcc -o <output_file_name> <your_c_file>.c
```

### Breaking It Down:

- `gcc` – Calls the GCC compiler.
- `-o <output_file_name>` – Specifies the name of the compiled output file.
- `<your_c_file>.c` – The source file you want to compile.

For example, if your file is `hello.c`, run:

```bash
gcc -o hello hello.c
```

Now, you'll see a new file named `hello` (without `.c`). This is your **machine code**.

## Running the Compiled Program

To execute it, type:

```bash
./hello
```

You should see:

```bash
Hello, World!
```

---

Now you understand what happens behind the scenes when you run a C program. And now we'll learn basics of the programming.

> **Tip:** If you're a beginner then I am sure you're also worried about people around you saying that *"don't learn this language, learn Python, learn Java, don't listen to others learn JavaScript"*. Then let me assure you it won't matter what you learn because the definition of function, and other stuff like variable, arguments, etc., all remain the same in every language. Learning C is recommended first because it'll tell you what's happening under the hood!