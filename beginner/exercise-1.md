# Exercise 1: Age in Seconds

Make a console program that asks the user for a number of years. The program should calculate what that number is when converted to seconds and show it to the user on the console window. For this exercise assume there are no leap years.

---


<details>
    <summary>Solution</summary>

<pre>
<code>
age_years = input("What is your age in years?")
age_seconds = age_years * 365 * 24 * 60 * 60
print("Your age in seconds is:" + age_seconds)
</code>
</pre>

</details><br>

<div style="text-align: right">
<a href="string.html">Next</a> | 
<a href="input.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>