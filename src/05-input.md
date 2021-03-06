# Input

We are making programs for the user and unless we are interested in writing scripts for absolute and utter automation,
we will have to take some sort of input from the user. And for this, we have one core function for taking user input.

## The `scan` Function

Nritya has an `io` function `scan()` which allows the programmer to take user input. It can optionally take in a prompt string
and returns the input entered by the user as a string. The programmer has complete control to do whatever they want with this input string.

For example,
```py
# taking simple input in a variable
let var1 = io.scan();
# taking input after a prompt
let var2 = io.scan('Enter some data: ');
```
In the second case, the user will first be greeted by `Enter some data: ` and they can provide input after that.
Similar to the output from `print` function, this prompt will not append a newline character at the end automatically.
If we want a newline character at the end, we will have to manually add that like so:
```py
let var = io.scan('Enter some data in next line:\n');
```

Let's understand this better using a very simple program extending our `Hello world` program.

This time, we want to ask the user their name, and we will print `Hello, <their name>`. Basically, we will be doing three things:
1. Giving prompt and taking input
2. Storing the input in a variable
3. Displaying our message

Ideally, you should try to making such a program by yourself first, but for this guide, here is the solution:
```py
let name = io.scan('Enter your name: ');
io.println('Hello, ', name);
```
That's it! Easy right?!

There is one more input function `scaneof`. The only difference between `scan` and `scaneof` is that `scaneof` reads till it finds the `EOF` character in the input. Therefore, `scaneof` can span multiple lines, unlike the `scan` function which reads only a single line at a time.

Well, there isn't anything else to learn about input for now. The `scan` function will most likely be extended later on to perhaps provide
more fine grain control over taking input.

This guide has used the term `function` a lot of times. Next up, it is time to understand what exactly they are and how to work with them
in Nritya.