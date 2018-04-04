# 03: Fibonacci numbers

This exercise will involve computation of the Fibonacci numbers.
See also <https://en.wikipedia.org/wiki/Fibonacci_number>.

Write a command line program that takes a variable number of
arguments that are intended to be whole numbers. These are
the `input`.

Write a `fibonacci` function that takes one `n` parameter, and
returns the appropriate Fibonacci number.

Hint: The `fibonacci` function may call itself recursively
as needed.

For each of the `input` numbers, the program should compute a
Fibonacci number, and print both the input number and the
computed result.

Expected outcome:

<pre>
03-fibonacci/$ node main.js 0 1 2 3 4 5 8 9 10
0  = 0
1  = 1
2  = 1
3  = 2
4  = 3
5  = 5
8  = 21
9  = 34
10 = 55
</pre>
