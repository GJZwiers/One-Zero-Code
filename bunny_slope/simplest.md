# Say Hi in Python

> In this guide you will learn how to write and run a line of Python code.

Now we are going to write some Python code and run it. To do this we will at the very least need only two things: Notepad and a program that can understand and execute code written in a certain language.

Let's get this program for the Python programming language. You can download the latest version [here](https://www.python.org/downloads/). Make sure to select the option to 'Add Python to PATH' when going through the installation menu. This allows you to run Python from anywhere on your computer.

Next, open a new text file in Notepad. That's right, just a plain `.txt` file. Write the following on the first line:
```python
print("Hi!")
```
`print` is a built-in Python _function_ that we can use to write text to a screen. The parentheses `()` are used to _call_ a function and inside them we can provide inputs to the function called _arguments_. The quotes around Hi! are to inform the computer it is text data.

Save the file as anything you like, I will use `hi.py` and will save the file in `C:/Users/Gordon/hi.py`. Replace Gordon with whatever your own username is on your computer.

Next, open a console window (if you are on Windows, press the Windows button on the keyboard, search for 'CMD' and press Enter when you see Command Prompt). Look at the path on the command line. If you are not yet in the location `C:/Users/Gordon` then you can change to it by typing the command `cd C:\Users\Gordon`. Type in the following on the command line:
```cmd
python hi.py
```

Now you should see the text 'Hi!' printed to the console window. Congratulations, you have just run your first line of code!

What happened behind the scenes is that Python does not look at a file extension and will execute anything that is valid Python code. If we had named the file `hi.txt` that would have worked too. The line `print("Hi!")` was translated to binary instructions, ones and zeroes, and executed by the computer.

To work with code for real Notepad will not do! Let's get ourselves an editor.

[next](editor.md)