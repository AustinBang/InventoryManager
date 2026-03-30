Continuous Integration is a way to automatically check that new code works with the rest of the project whenever someone updates the repository. This helps prevent errors and makes sure all code stays in sync.

Continuous Deployment/Delivery means that software can be coded, built, tested, shipped, and updated continuously. It allows new tested systems and features to be released more efficiently.

It is important to have Continuous Integration and Continuous Deployment/Delivery because some systems, like government systems and banks, cannot afford delays or failures in updates. These systems need to stay running and up to date for society.

Pipeline Stages

Code pushed to GitHub
Developer creates a pull request to merge code into the main branch or another branch. An admin or reviewer approves it.

Pipeline starts
Once the code is pushed or the pull request is opened, the CI pipeline starts automatically.

Build
The software is built using the project tools to make sure the code compiles and runs correctly.

Tests
The system runs tests to make sure the product is working properly.

Quality checks
Code quality and bug checks are performed
