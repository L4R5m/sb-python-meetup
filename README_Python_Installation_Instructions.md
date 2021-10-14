# Python Dev Environment Setup Guide

The Python installation process is platform-specific (ie: Windows vs MacOS vs Linux),
but installing 3rd-party packages via the PIP package management system is common for
all platforms.

A word on virtual-environments… while virtualenv’s are a ‘best practice’, we’ll
keep things simple and just work with one Python environment. (FYI, virtualenvs
allow you to install 3rd-party packages in a lightweight ‘virtual environment’,
so you can use different versions of 3rd-party package for your various projects).

Before proceeding with installation instructions, check and see if you already have a recent version of Python3 installed…
In a terminal type:
```
$ python3 —version
```
If it returns an error then you need to install Python3.
If it shows a version older than Python 3.7 it is recommended to install the latest Python3.


## Python3 Installation

### MacOS
MacOS comes with Python pre-installed. <br>
Great, please don’t ever use it for development!<br>
Why not? Because MacOS uses this ‘System Python’ instance and needs it for several
OS operations & tools. If you were to corrupt this installation, you can cause
system-level problems. <br>
And it’s old (Python 2)…

Instead, install a recent version, eg: the Python 3.10 installer: <br>
https://www.python.org/ftp/python/3.10.0/python-3.10.0-macos11.pkg

Detailed installation instructions: <br>
https://docs.python.org/3/using/mac.html

Once finished running the installer your Mac will have:
- a Python folder with some development tools in your Applications directory
- a Python executable & packages:
	- /Library/Frameworks/Python.framework
		- this path is added to your CLI shell path
		- a symlink is added to /usr/local/bin

### Windows
Detailed installation instructions:
https://docs.python.org/3/using/windows.html

Using the ‘Microsoft Store’ is probably the best option.


### Linux
As with MacOS, Linux comes with Python pre-installed.
And like with MacOS, you probably don’t want to use that version, primarily because
it’s likely an old verion.

Assuming you’re using a Debian variant (Ubuntu, Mint, etc) you can use the
‘deadsnakes’ ppa to get more recent Python3 versions. See instructions here: <br>
https://computingforgeeks.com/how-to-install-python-on-ubuntu-linux-system/

### Check that the Python3 installation was successful
```bash
# Display installed Python version (eg: 3.10)
$ python3 --version
```

## Documentation
### Python Language Reference Documentation
To learn more about the Python language, syntax, semantics: <br>
https://docs.python.org/3/reference/index.html#reference-index

### Python Standard Library Documentation
Python’s built-in Standard Library offers an extensive range of functionalities: <br>
https://docs.python.org/3/library/index.html

## PIP Install 3rd Party Packages
To add additional 3rd-party packages (eg: Numpy, Pandas, Matplotlib, Jupyter Notebook, etc)
use PIP, Python’s default package manager.

### Example usage
```bash
# Print pip basic usage
$ pip help

# Print pip help for ‘command’ (eg: install)
$ pip help <command>

# List all installed packages
$ pip list

# Install pandas package
$ pip install pandas

# Install packages in requirements.txt file
$ pip install -r requirements.txt
```
### Packages to install
Some suggested data-science / scientific computing packages
```bash
$ pip install pandas numpy jupyter nb-extensions
```

