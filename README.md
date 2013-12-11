PEP8 Git Commit Hook
====================

This is a pre-commit hook for Git that checks the code to be committed
for Python PEP8 style compliance.  The hook will prevent the commit in
case style violations are detected.

Installation:

1. Install the pep8 program: ```$ pip install pep8``` or ```easy_install pep8```
2. Run ```$ pep8``` command to check that it insall correctly
3. Clone project ```$ git clone git@github.com:helveticafire/pep8-git-hook.git```
4. Add ```pre-commit``` to your python project folder
  * Make a symbolic link from the pep8-git-hook location to the git project location with
    ```cd pep8-git-hook_project_location && ln -s pre-commit  your_project/.git/hooks/pre-commit``` 
5. Mark pre-commit executable: ```$ chmod +x your_project/.git/hooks/pre-commit```

The hook can be overridden: ```$ git commit --no-verify```

Currently, ignoring the following PEP8 code:
  * E501 line too long (82 > 79 characters)

In case you want to modify the list of codes to ignore, edit the
```ignore_codes``` list in the pre-commit file.   
If you want to select only specific codes to scan for, use the
```select_codes``` list.

This code was forked from [https://gist.github.com/810399](https://gist.github.com/810399).
