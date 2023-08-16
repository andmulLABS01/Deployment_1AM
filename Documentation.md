
## Deployment Instructions:
1. Log into the instructor's Jenkins server
   
	a. Login using provided credentials

2. Create and run a Jenkins build for the application (Review Jenkins setup lesson video)
   
	a.Select new item

	b.Name your item (Follow naming convention)

	c.Select pipeline and click ok

	Next page

	d.Put in description

	e.Pipeline dropdown select "pipeline script from SCM"

		*In SCM select Git
   		*Repository URL copy/paste your GitHub, repository, HTTPS url (Make sure to select the correct repository)
   
			click add and select Jenkins
   				Username of GitHub account
   				Password (use generated token)
   					Generate token in GitHub
   					Settings, Developer settings
   					click personal access token (classic)
   					click Generate new token
   						Name token
   						click on repo and admin:repo_hook
   						click Generate token
   					Copy your token and save it, as it is visible one time
   					ID: name_it
   					description: put what it is
   					click add
   
			Click the dropdown and select credentials
   
			Change branch to build to main
   
			click Apply
   
			click Save
   
	f.Click build now
		
3. Make sure you include your name on your build's name (first name_letter of last name)

4. Observe the pipeline stages via the console output and document what occurred
	Stage Log Used credentials, Deploy 1, to access remote Git Repository Cloned the repository and checked the access

	Build - Run shell script to check Python installed Checked requirements to see if PIP is installed and the correct version Found version 22.0.2 and uninstalled it. Downloaded and installed 23.2.1 py

	Test - Run Shell script to test Python using py.test and return the results, pass the test

5. If the pipeline is successful, download the application files from your repository and proceed to the next step:

Manually deploy AWS Elastic Beanstalk

Followed the steps in the scribe documentation 
	Note: Please check how you zip the files when you upload them to ESB
