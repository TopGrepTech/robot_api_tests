# Robot Framework API Testing with robotframework-requests
This project utilizes Robot Framework along with the `robotframework-requests` library for testing API requests. It is intended to be integrated with Jenkins for continuous testing.

## Installation
To install the necessary dependencies, run the following command:
```bash
  pip install robotframework-requests
```

## Running Tests
1. Navigate to the project directory in your terminal.
2. Run the desired test suite using the robot command followed by the path to the test file.
```bash
  robot tests/api_tests.robot
```
This will execute the specified test suite and display the results in the terminal.

## Test Suites
`api_tests.robot`: This file contains test cases for API requests. It verifies the functionality and responses of various API endpoints.

## Writing Test Cases
- Test cases are written in Robot Framework's plain text format, making them easy to read and understand.
- Utilize the keywords provided by the robotframework-requests library to interact with API endpoints.
- Maintain clear and descriptive test case names and documentation for better understanding.

## Test Data
Test data such as endpoint URLs, request payloads, and expected responses should be stored in variables for easier maintenance and reuse.

## Continuous Integration with Jenkins
Integrate the test suite into your Jenkins pipeline for continuous testing:

1. Configure a Jenkins job for your project.
2. Add a build step to execute the test suite using the robot command.
3. Schedule the job to run at regular intervals or trigger it automatically on code changes.

## Jenkinsfile
A Jenkinsfile is a text file that defines the entire pipeline configuration as code in Jenkins Pipeline. It allows you to specify the stages, steps, triggers, and other actions to be executed during the build process. Jenkinsfiles are typically stored alongside your application code in a version control repository, enabling you to manage your pipeline configuration just like any other piece of code.

### Usage
Jenkinsfiles are used to automate and define continuous integration and continuous delivery (CI/CD) pipelines in Jenkins. They provide a structured and repeatable way to define build workflows, integrate with external tools and services, and ensure consistent and reliable build processes.

The 'Jenkinsfile' consists of the following:

The line 'agent any' specifies that the pipeline can execute on any available agent in the Jenkins environment.

In this Jenkins pipeline script we have four stages:
1. Build: Echoes a message indicating the application is being built.
2. Unit Test: Echoes a message indicating unit tests are being run.
3. Deploy: Echoes a message indicating the application is being deployed.
4. Test: Echoes a message indicating tests are being run.

Each stage simulates a step in the CI/CD process in the deployment process.
You can customize the pipeline by adding or modifying stages and steps according to your project requirements.

## Additional Resources
- [Robot Framework Documentation](https://robotframework.org/)
- [robotframework-requests Documentation](https://github.com/bulkan/robotframework-requests)

Happy testing!