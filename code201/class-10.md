# Class 10 Notes

## Debugging

Debugging is the process of finding errors. It involves a process of deduction.

To find the source of an error, it helps to know how scripts are processed. the order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run.

If you understand execution contexets (which have two stages) and stacks, you are more likely to find the error in your code.

The console helps narrow down the area in which the error is located, so you can try to find the exact error.

JavaScript has 7 different types of error:

- Error: Generic error: The other errors are all based upon this error.

- SyntaxError: Syntax has not been followed.

- ReferenceError: Tried to reference a variable that is not declared within scope

- TypeError: An unexpected data type that cannot be coerced.

- RangeError: Numbers not in acceptable range.

- URIError: `endcodeURI()`, `decodeURI()`, and similar methods used incorrectly.

- EvalError: `eval()` function used incorrectly.

### Dealing with Errors

**Debug the script to fix errors**; if you come across an error while writing script, you will need to debug the code, track down the source error and fix it.

You will find that the developer tools available in every major modern browser will help you with this task. 

**Handle errors gracefully**; you can handle errors using try, catch, throw and finally statements.

Sometimes, an error may occur in the script for a reason beyond your control. For example, you might request data from a third party and their server may not respond. In such cases, it is particularly important to write error-handling code.

### Debugging Tips

- Another Browser: Some problems are browser-specific. Try the code in another browser to see which onea are causing a problem.

- Add Numbers: Write numbers into the console so you can see which items get logged. It shows how far your code runs before errrs stop.

- Strip it Back: Remove parts of code and strip it down to the minimum you need. You can do this either by removing the code altogether or by commenting it out.

- Explain the Code: Programmers often report finding a solution to a problem while explaining the code to someone else.

- Search: Stack Overflow is a resourse for programmers. Or traditional search engines.

- Validation Tools: There are a number of online validation tools that can help you try and find errors in your code:
  - JavaScript; jslint.com
  - JSON; jsonlint.com
  - JQUERY; There is a jQuery debugger plugin available for Chrome which can be found in the Chrome web store.



