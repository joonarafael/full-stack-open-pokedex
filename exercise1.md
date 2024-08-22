While working on a Python project, the process could look something like this:

Linting with tools such as Flake8 or Pylint. These tools could be used to enforce coding standards. Flake8 also supports some rudimentary error detection and complexity checking, which could be useful information to have in a CI pipeline.

Testing would most likely include Pytest & Coverage. While the tests would be written with, and powered by, Pytest, the Coverage tool could check the coverage of the tests and inform developers how extensively their tests cover the application logic. Good to remember that a coverage percent does not by itself mean anything :).

However the build stage could look really different depending on the nature of the application. Is the Python app built simply into a package as a source distribution? Then tools like Setuptools or Wheel could be used. If the Python program is meant to be packed into, for example, a .dll or .exe executable, tools like PyInstaller or Py2exe, could be used.

Due to the ease of Python virtual environments, the choice between the CI provider does not really matter. Some options besides Jenkins and GitHub Actions include TravisCI and CircleCI.

As mentioned above, the Python virtual environments make the CI pipeline quite independent of the CI provider and other underlying infrastructure & environment. For a smaller Python application built by a 6-people team, easiest solution should be a cloud-based CI provider. Running local does come with its benefits, like total control over everything & no additional billing, but might unnecessarily increase the required work hours.
