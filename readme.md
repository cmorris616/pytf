# PyTF
## **This readme is based on the current plan for PyTF, not the current state of the project**
PyTF (Python Testing Framework) is a framework for assisting with the automated testing process.
PyTF is not meant to replace pytest, behave, or other testing frameworks.  Instead, it is meant to
augment the process to provider further automation.  It can be configured based on the needs of
the project and the availablility of other technologies.

PyTF features include:
- Exporting feature files from JIRA for progression and regression testing
- Loading test data to be used during the testing process
- Cleaning up the test data after the testing has completed
- Uploading test results to JIRA
- Moving user stories based on the outcome of the tests

## Test Plugins
PyTF is built to use multiple testing frameworks via plugins.  Currently, PyTF only supports the
behave framework for business-driven development.

## Project Management Plugins
Like the testing plugins, PyTF can also use multiple project management software suites (such as
JIRA) via plugins.

### Authentication
In most cases, authentication needs to happen in order to interact with project management software
suites.  This interaction can use certificates, API keys, or simple username/password combinations.
The difficult part is how to secure the credentials.  For starters, a keyring authenticator is
implemented that just uses the keyring functionality for the underlying OS.