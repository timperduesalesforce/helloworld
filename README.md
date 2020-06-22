This is the Readme that goes with the helloworld repo.

1. Intro:
- Use case is app (Hello World) exists in source repository and current version lives in production/sandbox
- We need to make a change to the LWC
- Show app in production and source in Git

2. Project Setup:
- Create New Project using Command Palette using SFDX: Create Project with Manifest
- Note a few interesting features about VSCode
- Run git init to initialize the local repo

3. Connect to Orgs:
- Connect to a Dev Hub using the Command Palette using SFDX: Authorize a Dev Hub
- Run sfdx force:org:list and explain (D) which means connected to Dev Hub
- Connect to 2nd Org using the Command Palette using SFDX: Authorize an Org
- Run sfdx force:org:list and explain (U) which means as a Default Org (menu shows up)

4. Create Scratch Org:
- Link to Hello World Repo using git remote add origin https://github.com/tperduesalesforce/helloworld
- Check with git remote -v
- Pull master branch to sync up repo with git pull origin master
- Create new Scratch Org
- Open Scratch Org with icon
- Push Component to Scratch Org using sfdx force:source:deploy --sourcepath force-app
- Open Flexipage and Activate for default org

5. Edit App:
- Change HTML Component
- Let's test it
- sfdx force:source:deploy --sourcepath force-app
- Run git status
- Run git add force-app/main/default/lwc/helloWorld/helloWorld.html
- Run git commit -m "Made a change"
- Run git push -u origin master 
- Show Git Repo via browser and show change

6. Sandbox QA:
-Next we would push it up to the Sandbox for proper testing similar to above
