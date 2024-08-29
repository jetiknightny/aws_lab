Hands-on Lab Exercise
Lab Activity: AWS CI/CD Pipeline Design and Implementation
Objective: The objective of this lab activity is to familiarize participants with
planning, designing, and implementing effective CI/CD pipelines on AWS.
Participants will learn about considerations for pipeline design, mapping out
stages and tasks, selecting appropriate tools for different pipeline stages, and
ensuring compatibility and efficiency.
Requirements:
● Participants should have basic knowledge of AWS services, Git, and
CI/CD concepts.
Lab Activity:
1. Setting Up Source Stage:
● Assignment 4: Create a Git repository for your sample web application
and push the code to it.
● Explanation: Explain how to integrate AWS CodePipeline with the Git
repository to trigger pipeline execution on code changes.
2. Configuring Build Stage:
● Assignment 5: Set up a build environment using AWS CodeBuild to
compile and package your web application.
● Explanation: Discuss the build specifications, environment variables,
and artifacts generated during the build process.
3. Implementing Test Stage:
● Assignment 6: Integrate testing frameworks/tools (e.g., Selenium, JUnit)
with AWS CodeBuild to automate testing.
● Explanation: Explain the importance of automated testing in CI/CD
pipelines and how it ensures the quality of deployments.
4. Deploying Application Stage:
● Assignment 7: Configure AWS CodeDeploy to deploy your web
application to an EC2 instance.
● Explanation: Discuss deployment strategies, such as rolling
deployments, blue/green deployments, and how AWS CodeDeploy
facilitates automated deployments.
5. Adding Post-Deploy Actions:
● Assignment 8: Implement post-deployment actions using AWS
Lambda to perform tasks like database migrations or cache
invalidation.
● Explanation: Highlight the significance of post-deployment actions in
maintaining application consistency and performance.
6. Ensuring Compatibility and Efficiency:
● Assignment 9: Optimize your CI/CD pipeline for efficiency by
implementing parallelism and caching mechanisms where applicable.
● Explanation: Discuss techniques to minimize build and deployment
times, such as parallel testing, artifact caching, and resource
optimization.
7. Monitoring and Feedback:
● Assignment 10: Set up Amazon CloudWatch alarms to monitor pipeline
health and trigger notifications for failures.
● Explanation: Emphasize the importance of continuous monitoring and
feedback loops in identifying and addressing issues in the pipeline.
Sep by step Instructions
Assignment 1: Setting Up Source Stage
Step-by-Step Hands-On Instructions:
1. Open your web browser and navigate to your Git hosting platform (e.g.,
GitHub, Bitbucket).
2. Create a new repository for your sample web application.
3. Clone the repository to your local machine using Git.
4. Write some code or copy an existing project into the repository.
5. Commit and push the code changes to the remote repository.
6. Open the AWS Management Console and navigate to AWS
CodePipeline.
7. Click on "Create pipeline" and follow the wizard to configure the source
stage to connect to your Git repository.
8. Trigger the pipeline and verify that it successfully fetches the code from
the Git repository.
Assignment 2: Configuring Build Stage
Step-by-Step Hands-On Instructions:
1. Open the AWS Management Console and navigate to AWS CodeBuild.
2. Click on "Create build project" and configure the build settings:
● Select your source repository and branch.
● Choose the runtime environment and operating system.
● Define build commands or use a buildspec file to specify the build
process.
● Configure environment variables and artifacts output.
3. Save the build project configuration and trigger a manual build to
ensure it compiles and packages your web application successfully.
4. Once the build is complete, review the build logs and artifacts to verify
the correctness of the build process.
Assignment 3: Implementing Test Stage
Step-by-Step Hands-On Instructions:
1. Identify the testing frameworks and tools you want to use for your web
application (e.g., Selenium for UI testing, JUnit for unit testing).
2. Open the AWS Management Console and navigate to your CodeBuild
project.
3. Modify the buildspec file or build commands to include commands for
running automated tests.
4. Configure CodeBuild to fail the build if any tests fail during execution.
5. Trigger a pipeline execution and monitor the test stage to ensure that
automated tests are executed and passed successfully.
Assignment 4: Deploying Application Stage
Step-by-Step Hands-On Instructions:
1. Open the AWS Management Console and navigate to AWS CodeDeploy.
2. Click on "Create deployment" and choose the deployment type (e.g.,
EC2, Lambda, ECS).
3. Select the deployment group and specify the revision (artifact) to
deploy.
4. Configure deployment settings such as deployment configuration,
rollback options, and alarms.
5. Start the deployment and monitor its progress in the CodeDeploy
console.
6. Once the deployment is complete, verify that your web application is
successfully deployed and accessible.
Assignment 5: Adding Post-Deploy Actions
Step-by-Step Hands-On Instructions:
1. Identify the post-deployment actions you want to perform (e.g.,
database migrations, cache invalidation).
2. Open the AWS Management Console and navigate to AWS Lambda.
3. Create a new Lambda function for each post-deployment action.
4. Write the code to perform the desired action within each Lambda
function.
5. Configure CodeDeploy to trigger the Lambda functions as
post-deployment hooks after a successful deployment.
6. Trigger a deployment and verify that the post-deployment actions are
executed as expected.
Assignment 6: Ensuring Compatibility and Efficiency
Step-by-Step Hands-On Instructions:
1. Open your CodeBuild project configuration in the AWS Management
Console.
2. Enable parallelism by adjusting the concurrent build limit and batch
build settings.
3. Configure caching for dependencies to speed up build times.
4. Optimize resource allocation by adjusting compute type and instance
sizes based on your application's requirements.
5. Trigger a build and monitor the build duration and resource utilization
to ensure efficiency improvements.
Assignment 7: Monitoring and Feedback
Step-by-Step Hands-On Instructions:
1. Open the AWS Management Console and navigate to Amazon
CloudWatch.
2. Create CloudWatch alarms for key metrics such as build failures,
deployment duration, and error rates.
3. Configure SNS (Simple Notification Service) topics to send email or SMS
notifications for alarm triggers.
4. Trigger intentional pipeline failures and verify that the alarms are
triggered and notifications are sent.
5. Adjust alarm thresholds and notification settings as needed for
effective monitoring and feedback loops