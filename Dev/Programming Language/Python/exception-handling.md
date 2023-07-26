# Python - Exception handling

Execution errors are commonly called exceptions and that is why from now on we will use that name. During the execution of a program, if an exception arises within a function and the function does not handle it, the exception propagates to the function that invoked it, if this other one does not handle it either, the exception continues to propagate until it reaches the initial function of the program and if this one does not handle it either, the execution of the program is interrupted. Let's see then how to handle exceptions.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4fc53d3e-6e14-48d0-8bf8-b4ee6c7b929c">
</p>

For exception handling, languages provide certain reserved words, which allow us to handle exceptions that may arise and take recovery actions to avoid interrupting the program or, at least, to perform some additional actions before interrupting the program.

In the case of Python, exception handling is done through the blocks that use the try, except and finally statements.

The try block contains all the code that can raise an exception, the term raise is used to refer to the action of generating an exception.

Next is the except block, which is responsible for catching the exception and gives us the opportunity to process it.

```python
>>> try:
...     quotient = dividend / divisor
... except:
...     print "Error Here!"
...
```

Since exceptions of different types can occur within the same try block, it is possible to use several except blocks, each one catching a different type of exception.

This is done by specifying after the except statement the name of the exception to be caught. The same except block can catch several types of exceptions, which is done by specifying the exception names separated by commas after the except word. It is important to note that although there may be several except blocks after a try block, at most one of them will be executed.

```python
try:

except IOError:
except ZeroDivisionError:
except:
```

Now if we want to know which exception is occurring, the ideal would be to use the following routine:

```python
try:
except Exception as err:
    print(f"Unexpected {err=}, {type(err)=}")
    raise
```

## References: 

- https://docs.python.org/es/3/tutorial/errors.html
- https://uniwebsidad.com/libros/algoritmos-python/capitulo-12/excepciones