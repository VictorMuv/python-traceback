### Python Traceback in General

There are several sections to every Python traceback, that are important. The diagram below was an attempt to help you see those different parts.

![{% img 'python-traceback-diagram' centered=True %}]()

In python its best to read the traceback starting from the bottom moving upwards. 
The last line of the traceback is called the error message line, and it contains the raised exception name(outlined in green). 


After the exception name, there is the error message (outlined in yellow). 
This message, usually contans helpfull information for understanding the reasons of the raised exception. 


Moving up in the traceback (out-lined in yellow); are different functon calls moving from bottom to top or from most recent to least recent. 
These calls are repressented by two line entries for each call. 
The first line of each call contains information like: the file name, line number and module name; all specifying where the code can be found. 
The second line for these call contains the actual code that was executed (underline in red).

There are a few differences between tracebacks output when executing your code in the command-line and running code in the REPL, below are same codes from previous sections executed in an `REPL` and the resulting traceback output.

```python
>>> def greet( someone ):
>>>
...   print('Hello, ' +someon)
... 
>>> greet("Chad")

Traceback (most recent call last):
  File "", line 2, in 
  File "", line 1, in greet
NameError: name 'someon' is not defined
```
