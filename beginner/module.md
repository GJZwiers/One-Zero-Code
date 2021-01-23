# Python Modules

Thus far, we have been coding using the Python standard library. This is code that is included by default in any Python program for us to use. It includes the functions such as `print` and `input`. But there is also lots of prewritten Python code that we can use when we need it. These are called **modules** and they can be imported into a program with the `import` keyword. In the following example, we import the `datetime` module and use it to fetch the current date and time.
```python
import datetime

current_date = datetime.datetime.now()
```

For a complete list of modules provided by the standard library, you can check [this page](https://docs.python.org/3/library/).