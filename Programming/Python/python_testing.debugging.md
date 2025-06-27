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