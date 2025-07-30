# 🐍 Python Testing/Debugging – Learning Notes

## 🧪 Unit Tests

Summary: 
Unit tests are just an automated program that tests a small "unit" of code. Usually just a function or two. The editor will have tabs: the "main.py" file containing your code, and the "main_test.py" file containing the unit tests.

Test your code's _functionality_ rather than its output. Tests will call functions in your code with different arguments, and expect certain return values. If your code returns the correct values, you pass. If it doesn't, you fail.

There are two reasons for this change:

1. It's more realistic. In the real world, you'll be writing unit tests and running them against your code to make sure it works as expected.
2. You can run and debug your code with `print` statements, and leave those print statements in when you submit. Unlike the output-based lessons, you won't have to remove your `print` statements to pass.

## 🐜 Debugging

Summary: 
You write some code, run it, and if it doesn't work, you fix the bugs. You repeat this process until you're confident that your code works as expected.

The goal is to write _small amounts of code_, and then _test_ each bit of code to make sure it's doing what we expect before moving on. **Trying to write entire programs at once is a recipe for pain and suffering.** The goal is to write a few lines, test them, and then write a few more lines, and repeat until you're done.

#### 〰️ Stack Trace

Summary:
A stack trace (or "traceback") is a scary-looking error message that the Python interpreter prints to the console when it encounters certain problems. Stack traces are most common (at least for you right now) when you're trying to run invalid Python code.

Example:

PythonError: Traceback (most recent call last):
  File "<exec>", line 17, in <module>
  File "<string>", line 1, in <module>
  File "/home/pyodide/main.py", line 3
    msg = f"You have {strength} strength, {wisdom} wisdom, and {dexterity} dexterity for a total of {total} stats.
                                                            ^
IndentationError: unindent does not match any outer indentation level