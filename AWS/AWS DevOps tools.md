(Getting Started with DevOps on AWS, amazone course)
***
## CI/CD pipeline using AWS diagram

![[Pasted image 20221215165342.png]]

***
- ### AWS CodePipeline
	 Is a continuos delivery service allow you to visualize, set up and implement steps required to release you software

	 #### Why use?:
	 - Capture and visualize your pipeline, view real-time status and retry failed actions.
	 - Automate your release processes, eliminate human error, sped up delivery and improve quality of the release.
	 - Incorporate your source, test, build and deploy tools.
	 - Log pipeline history details.
	 - Can be integrated with third-party CI/CD tools.

	 #### Monitoring
	 You can monitor your pipeline in a number of ways to assure its performance, reliability, and availability, and to find ways to improve it. You can monitor the pipeline directly from the AWS CodePipeline console, the command line interface (CLI), use [[Amazon EventBridge]], or [[AWS CloudTrail]].

	 #### Security
	 Secutity is always important. Using CodePipeline you can manage permisiions to any part of your pipeline. Someone might have only read-only access, while others might have access to a particular stage or action within a stage.

	 #### How to work with it
	 CodePipeline allow you to model query of stages and actions that provide your release.
	 
	 - Every pipeline require next stages:
		 - Source
		 - Build
		 - Test
		 - Deploy
		 - Approval (manual or notification)

	 - Example 3 stage pipeline:
		![[Pasted image 20221215172654.png]]

***
- ### AWS Codecommit
	 Fully managed source control service to host git-based repositories.

	 #### Why use?:
	 - You don't need to manage your own hardware and software to store your code code.
	 CodeCommit is fully managed, highly available, and has no limits in the type or size of files it can store.
	 - CodeCommit is Git-based, your team doesn't need to learn new commands and can handle large numbers of files, code branches, and lenghty revision histories.
	 - You can improve your existing workflow by integrating CodeCommit with other AWS services, IDEs, and third-party software (for example, Jira).

	 #### Monitoring
	 You can create notifications and trigger actions based on events such as creation of a branch, or when a commit is made.

	 #### Security
	 From the side of security CodeCommit provide managed policies and user accounts.
	 Also data transmission is realized using https and ssh.

	 #### How to work with it?
	 Using CodeCommit you create your own repository. Developers clone it to their environments, creating their own copies of your repo.

	 After they make changes using git commands they can push changes to the parent repo located in cloud.

	 If CloudCommit is part of a pipeline it can trigger next stage to start, in case of changes in one of branches.

	 #### CodeCommit console:
	 ![[Pasted image 20221215190053.png]]
	 There you can see "myAppRepo" repository and what file it contains.
	 Above, drop list menus and buttons used to create notifications, choose branch, pull and clone repo.

*** 
- ### AWS CodeBuild
	 Is a fully managed build service that automatically compiles source code, run tests and produces software packages.

	 #### Why use?:
	 - You don't need to set up, patch, update and manage your own build servers.
	 - Automatically compile source code, run tests, and produce build artifacts.
	 - Process multiple builds concurrently, for example, developers can continuously build and test their code, catch errors early, and correct them early.
	 - Leverage out of the box preconfigured build environments (such as .NET Core, Java, Ruby, Python, Go, NodeJS, Android and Docker). Build environments contain the operating system, programming language runtime, and build tools (such as Apache Maven, Gradle). You can also provide custom build environments suited to your needs by means of Docker images.
	 - Pull source code from CodeCommit, Amazon S3, GitHub, GitHub Enterprise, and Bitbucket.
	 - Integrate CodeBuild with Jenkins to simplify the build process.

	 #### Monitoring 
	 Using CodeBuild console you can monitor build process, also you can CloudWatch and a number of other ways.

	 #### Security
	 Build artifacts are encrypted and you control access to your build projects through resource-level permissions in AWS Identity and Access Management (IAM) policies.

	 #### How it works 
	 CodeBuild uses information provided by a build project to create build environment(probably docker container) where it then runs the build.

	 Steps that CodeBuild takes during the build:
	 1) Take information from build project, it includes source repository, runtime environment, build commands, and location of build output.
	 2) Create build environment.
	 3) Download the code, run buildspec file. It is a file that contain instructions about how to run build, query of commands to install tool packages, run tests, package code.
	 4) Any build output is uploaded to an Amazon S3 bucket and able to configure notifications.
	 5) Build output is streamed to the service console, and CloudWatch Logs.

	 #### Build phases diagram
	 ![[Pasted image 20221215194211.png]]

***
- ### AWS CodeDeploy
	 Is a fully managed service that automate software and code deployment process to a variety of compute services, including [[Amazone EC2]], [[AWS Fargate]], [[AWS Lambda]].

	 #### Why use?:
	 - Deploy to servers, serverless, or container applications.
	 - Deployment process is automated.
	 - Supports variety compute platforms.
	 - Can deploy on one or multiple instance at the same time.
	 - Minimize production downtime if you use updated instances to replace old ones.
	 - Automatically (or through user intervention) stop an unsuccessful deployment and roll back your deployment to a previous version.

	 #### Monitoring
	 AWS provides various tools that you can use to monitor CodeDeploy, including CloudWatch alarms, the CodeDeploy console and more.

	 #### Security
	 You can configure CodeDeploy to meet your security and compliance objectives. For more information on security.

	 #### How to use it?
	 To automate deployment process, CodeDeploy need to know which files ot copy, 
	 what scripts to run, and where deploy.

	 The concept of an _application_ is used by CodeDeploy to ensure it knows what to deploy (correct revision of code), where to deploy (deployment group), and how to deploy (deployment configuration).

	 - ##### Code
		  - Identify correct version(revision) of the code.
		  - Look for application specification file in the root directory, which is used to manage each deployment.
		  - AppSpec file specifies where to copy the code and how to get it running. For example, it tells CodeDeploy how to stop the application if it is already running, how to install the code, what command to run before and after the code is installed, and how to get the application running again.

	 - ##### Deployment group
		  - Specify target environment to deploy. The information it contains is specific to the target compute platform: AWS Lambda, Amazon ECS, Amazon EC2, or on-premises. For example, Amazon ECS lets you specify the Amazon ECS service, load balancer and more. For Amazon EC2, it is a logical group of deployment target instances or physical environments.
		 - Security needs to be assigned so the environment can communicate with CodeDeploy.
		 - The CodeDeploy agent is needed if you are deploying to Amazon EC2 or an on-premises compute platform. It is installed and configured on the target instances. It accepts and executes requests on behalf of CodeDeploy.

	 - ##### Deployment configuration
		  - A _deployment configuration_ is a set of deployment rules and deployment success and failure conditions used by AWS CodeDeploy during a deployment.

	 #### Example of a deployment to Amazone EC2 instance.
	 ![[Pasted image 20221215201043.png]]