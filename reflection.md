1. Which issues were the easiest to fix, and which were the hardest? Why?

The easiest issues to fix were style-related warnings from Flake8, such as trailing whitespace, missing blank lines, and replacing the bare except: with a specific exception type. These only required minor formatting or syntax changes.
The hardest issues were those identified by Pylint and Bandit, such as the mutable default argument and the use of eval(). This requires more Python Practices incorrect fixes could change program logic or introduce new bugs.

2. Did the static analysis tools report any false positives? If so, describe one example.

Yes. Pylint flagged some naming convention issues (like addItem or removeItem not following snake_case). While technically valid under PEP 8, in this lab context they weren’t real bugs — the functions still worked correctly, and renaming them wasn’t necessary for functionality.

3. How would you integrate static analysis tools into your actual software development workflow?

Static analysis tools can be integrated into the workflow using Continuous Integration (CI) pipelines such as GitHub Actions or Jenkins. Each time code is pushed, Pylint, Bandit, and Flake8 can automatically run to detect issues before merging.

4. What tangible improvements did you observe in the code quality, readability, or potential robustness after applying the fixes?

After applying the fixes, the code became cleaner, safer, and more maintainable. Using with open() improved resource management, removing eval() eliminated a security risk, and adding clear exception handling made the program clear.