# Jenkins-Demo
#### This Repo is used in Jenkins and it must be build automatic there.

## Build Triggers
### Difference between using Poll SCM and GitHub hook trigger for GITScm polling:

## **1- Poll SCM "Source Control Management":**
   #### It periodically checks the repositories for changes.
   #### Jenkins periodically checks the version control system by comparing the current state with the previous state. If changes are detected, a build will trigger.
   #### It is used for projects with infrequent code changes.
 
   ### Configuration Of Jenkins Poll SCM:
   * Step 1: Access Jenkins Dashboard
     
     <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201170744/J1-dashboard-(1).jpg">
     
   * Step 2: Create or Select a Jenkins Job
     
     <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201170921/J2-create-job.jpg">
     
   * Step 3: Configure Source Code Management
        ###### find the “Source Code Management” section. Select the appropriate version control system (e.g., Git) to add your repository and branch to build.

        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201171106/J3git.jpg">

        ###### Configuring the jenkins build triggers with choosing branch specifier.

        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201171216/J4branch.jpg">
     
   * Step 4: Enable Poll SCM under Build Triggers
        ###### Look for the option labeled “Poll SCM”. Specify the frequency in cron format (e.g., H/30 * * * * for every 30 minutes).
     
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201171639/build30.jpg">

        ###### then, Save the changes to apply the Poll SCM configuration to your Jenkins job.

   * Step 5: Triggering Builds
        ###### Jenkins will now automatically check for changes in the specified interval and trigger a build if changes are detected.
 
 
## **2- GitHub hook trigger for GITScm polling:**
   #### It receives direct notifications from the VCS.
   #### Real-time triggers based on VCS events.
   #### It depends on VCS support for webhooks.
   #### It efficiently uses resources only trigger when changes occur.
   #### It is use for real-time integration, and to get quick feedback on code changes.
 
   ### Configuration Of Jenkins GitHub hook trigger:
   * Step 1: Access Jenkins Dashboard
     
     <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201170744/J1-dashboard-(1).jpg">
     
   * Step 2: Create or Select a Jenkins Job
     
     <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201170921/J2-create-job.jpg">
     
   * Step 3: Configure Source Code Management
        ###### find the “Source Code Management” section. Select the appropriate version control system (e.g., Git) to add your repository and branch to build.

        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201171106/J3git.jpg">

        ###### Configuring the jenkins build triggers with choosing branch specifier.

        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20240201171216/J4branch.jpg">
     
   * Step 4: Enable GitHub hook trigger for GITScm polling under Build Triggers.
     
        <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*-Enehhst2AHeq4ZRye08qw.png">

        ###### Under the Pipeline option, select Pipeline script from SCM, and in the SCM option, select Git and specify the Git repository URL.
        <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*wRxkizru1z20lup2aWpkjQ.png">

        ###### Simply scroll down. In Jenkins, we must also specify the branch name.
        <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*LWWjsyXdLwMsXyt7mb_W0w.png">

        ###### Once you have configured the Jenkins job, save the changes.


   * Step 5: Creating a webhook in GitHub and Configuration
        ###### Jenkins URL should have the following format: http://<jenkins_server>/github-webhook/
        ###### Click on settings in GitHub branch which you want to add webhook in Jenkins Pipeline
        ###### On the left side of the page click on Webhooks

        <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*NFwi9QrLaIWWQoeFlW4XeA.png">
       
        <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*MkrneYnqKP--UzXjNqfCPA.png">
        
        ###### Now save the changes.

   * Step 6: Test the webhook.

      ###### To test the webhook, make changes to the GitHub repository and push them to it. This will activate the webhook, and Jenkins should automatically begin the job. To ensure that the job was executed, 
      ###### navigate to the Jenkins job and review the build history. The GitHub webhook should have triggered a new build. If the build completed successfully,
      ###### the changes you pushed to the repository should have been built and tested.



   

