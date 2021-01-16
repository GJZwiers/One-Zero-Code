# Try To Finally Except Me - Handling Errors

At times there are errors that we don't want to cause a complete program stop. Instead, we want to handle them in some way and keep the program running. In Python we can do this using `try/except` blocks. With these you add the code to be executed in a `try` block, and add how to handle any errors in the `except` block:
```python
print("Starting program.")

try:
    file = open('weather.txt')
    file.write("Todays weather will be sunny.")
except:
    print("Something went wrong trying to open the file.")

print("Program done.")
```
The code will try to open the file `weather.txt` and write a line of text to it. But it that fails the `except` block will execute and print an error message. However, the program will keep running. You would see the following output on the console:
```cmd
Starting program.
Something went wrong trying to open the file.
Program done.
```

We can also add more than one `except` block to handle different error types. For example, the error could be due to the file not existing or because the system is not allowed to open or write text to the file because it does not have the required permissions:
```python
try:
    file = open('weather.txt')
    file.write("Todays weather will be sunny.")
except FileNotFoundError:
    print("Could not find the file to open.")
except PermissionError:
    print("Missing Permissions to perform the requested operations.")
except:
    print("Something went wrong trying to open the file.")
```

Finally, we can add a `finally` block to this construct which will execute a piece of code whether or not the code in the `try` block raises any errors:

```python
try:
    file = open('weather.txt')
    file.write("Todays weather will be sunny.")
except FileNotFoundError:
    print("Could not find the file to open.")
except PermissionError:
    print("Missing Permissions to perform the requested operations.")
except:
    print("Something went wrong trying to open the file.")
finally:
    print("Program done.")
```

Up next, it is time to look at lists.

<div style="text-align: right">
<a href="list.html">Next</a> | 
<a href="error.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>