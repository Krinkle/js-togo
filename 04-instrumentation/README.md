# 04: Instrumentation

Create a copy of your program from the `03-fibonacci/` directory
and save it in this directory.

This exercise will be about instrumentation. Instrumentation is
the term for adding additional code that will measure aspects of
your program. For today's example, we will measure how often
the `fibonacci` function is called.

To do this, create a variable in the main program scope and
increment by one it at the start of the `fibonacci` function.

Then, print it at the end of the program.

Expected outcome:

<pre>
04-instrumentation/$ node main.js 8 9 10
8  = 21
9  = 34
10 = 55

Total: 353 function calls!
</pre>
