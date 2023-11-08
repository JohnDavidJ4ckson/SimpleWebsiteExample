# SimpleWebsiteExample
A simple website based on python with a pipeline for automatic deployment of python changes and vulnerability tests

Creating a Github repository with a simple "Hello World" version of a website is a simple task that can be completed using the web interface.

1. You create a new project and choos the configuration options needed, such as repository name. This triggers the initial commit for the master branch of the repository
2. Create the basic "hello world" version of a web application for Python using the Flask framework. The details of the code can be found in the begginer tutorial at: https://pythonbasics.org/flask-tutorial-hello-world/
3. Implementing automatic deployment can be done with github actions as shown in various tutorials. The pipeline that implements the commit to the masterbranch, sets up a Python versions, installs its dependencies, checks for errors with a basic quality tool, applies a dummy unit test, uploades tests results to a dummy log file, builds the package and publishes it can be found at: ".github/workflows/python-app.yml"
https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python
4. Adding an open-source tool to do vulnerability tests with the tools provided by Github was implemented as instructed in the CodeQL tutorial
https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning
Third party-tools can be implemented by adding their set up (dependencies installation, build, and test running) to the automatic deployment workflow from the previous step.
