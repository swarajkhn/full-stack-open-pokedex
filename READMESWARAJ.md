Readme file for 'Getting familiar with github actions'

Step 1: Forking of the repository

- Create your own github repository if not already there 
- Take a fork of the repository present at this link

Step 2: Cloning the project onto your local machine

- Clone the repo from github to your local using gitbash

Step 3: Open the code on local machine using VS code

- Install node v16 from chrome
- Then run npm -v and node -v to confirm node and npm is installed

Step 4: Run the code in your local 

>Run all the commands such as 
- 'npm install' inside the project folder
- 'npm start' to run the webpack dev server 
- 'npm test' to run tests 
- 'npm run eslint' to run eslint 
- 'npm run build' to make a production build 
- 'npm run start-prod'

- Linting of the code is used to find the errors in code without actually running it
- After running the above code,there will be linting errors and broken tests
- In localhost:8080 you will get a dev build and in localhost:5000 you will get the prod build

Step 5: Getting familiar with workflows in Github actions

- Create a simple workflow with the name 'hello.yml' which can be used to print 'helloworld' by defining jobs
- Also run pipeline to display date and directory content

Step 6: To automate the process of lint, test and build

- Create a workflow by the name 'pipeline.yml' to lint, test and build the source code present in the repository
- First set a trigger which will trigger the pipeline if any push to a commit is done on 'main' branch of the repository
- Next create a job with the name 'simple-deployment-pipeline' 
- Next declare an ubuntu resource on which the production build will be running
- Next create a step which will create a checkout action to checkout the source code from the git 
- Next create an action which will setup Node.js of the prefered version, the version is passed as a parameter using 'with'
- Next be installing dependencies just like in local by running ' npm install'
- Next run 'npm run eslint' to lint the code to check for any styling errors
- Name of step also can be given or else a default name will be assigned
- Name of step also can be given or else a default name will be assigned
- Commit the changes made to pipeline.yml

Step 7:	Rectify the linting errors

- Go to the action section, a pipeline will be triggered from the previous commit 
- In the console output of Deployment pipeline, the linting step will show errors in the code 
- Rectify those errors and commit till a green output is obtained

Step 8: Add test and build steps to 'pipeline.yml' file

- Add steps 'npm run build' and 'npm test' to 'pipeline.yml' files
- The pipeline will run and
- It will have failed two of the three tests
- Rectify the code so as to pass those tests 
- Workflow will then run and it will be green again
