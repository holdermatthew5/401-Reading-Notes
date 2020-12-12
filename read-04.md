## Read & Write Files in Python

- `open('filename.txt')` and `open('filename.txt', r)` are both ways to open a file for reading. `open('filename.txt', rb)` is not.
- File path still uses '/' so what's the point of using dot notation when importing modules? Is that only for the open() statements? Are there other commands that us '/' instead of dot notation?
- `open('filename.txt', rb)` is to open a file for reading as a buffered binary file.
- Absolute path starts with '/' and contains .whatever (`.txt`, `.gif`, etc).
- Relative path also includes .whatever^^.
- How am I supposed to use `with` to make sure a file is properly closed before moving on in my code file? Why would `.close()` not be the right answer?
  - When using `with` to open a file the file is automatically closed after leaving the with code block.

## Exceptions in Python

- Use `raise` to force an exception error (`raise Exception('error text')`). Useful for (but not limited to) telling a user to change their input.
  - What is `.format()`?
- `assert ('linux' in sys.platform), "This code runs on Linux only."` throws an assertion error with the text, 'This code runs on Linux only.'if the OS running the program is not linux.
- Tailor the computers response to an exception by using try: and except: in the same manner as a js try and catch. If not tailored the program will 'crash' (Are errors similar to this the only reason for programs crashing or is there something unrelated that can cause it to crash? Specifically, I'm thinking of games and desktops in general). Does `pass` just let the code continue running by skipping the failed code to after the pass?