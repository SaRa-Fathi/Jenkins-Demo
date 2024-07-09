# Jenkins-Demo
#### This Repo is used in Jenkins and it must be build automatic there.

## Build Triggers
### Difference between using Poll SCM and GitHub hook trigger for GITScm polling:

##**Poll SCM "Source Control Management":**
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
 
 
## * **GitHub hook trigger for GITScm polling:**
 #### secondly start. :(

