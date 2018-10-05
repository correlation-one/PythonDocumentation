# PythonDocumentation
### To regenerate the docs using this folder easily

    - cd into sphinx folder
    - move the files you want to document into sphinx/gamelib
    - Delete gamelib.rst and modules.rst
    - Delete the contents of ./html
    - run sphinx-apidoc -o . ./gamelib
    - run sphinx-build . ./html

### To create a folder like this from scratch

    - Make sure sphinx is installed and updated
    - Run sphinx quickstart in the folder and fill out the options as follows
        - Provide project info when prompted
        - yes for auto generate from docstrings
        - yes for add links to source code
        - yes for add makefile
        - no for add Windows file (assuming you are not on windows)
    - In conf.py, uncomment 'import os' and 'import sys'.
    - In conf.py, add the following lines just below imports
        - sys.path.insert(0, os.path.abspath('.')) 
        - sys.path.append(os.path.abspath('./gamelib'))  
        - sys.path.append(os.path.abspath('..'))
    - If you want to use this exact structure, create an html directory to hold your built html
