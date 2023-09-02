Clone this repo to your local
git clone https://github.com/devopsbychandu01/project9-nodejs.git

remove the .git foler. then git data will be lost.
Intialize and move to local git using following commands.
git init git add . git commit -m "project6"

create new project on azure devops
click on repo, and copy the remote origin url and update the origin in your local
git remote add origin

push the code to azure devops using following command.
git push -u origin --all

check if you have any free agent available in your azure devops pipeline, if not create one agent for running the pipeline.
Create one service connection for connecting azure devops to cloud. For doing that use the follwoing process
Click on azure devops project settings --> Click on service connections --> New service connections --> Azure Resource Manager --> Next --> Service Principle (Automatic) --> next --> Select your subscription, resource Group, And service connection name --> select "Grant access permission to all pipelines" option --> save.

click on pipeline --> new pipeline --> Select "Azure Repos Git" --> Select your repo --> Select "Select an existing YAML file" option --> Under path Select "/azure-pipelines.yml" and click on continue --> save the pipeline
create one azure webapp in azure cloud with dotnet 6 runtime
run the pipeline, your code should automatically pick up by the app service.