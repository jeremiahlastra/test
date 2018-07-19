# Deployment

This will provide you steps in order to deploy the changes made in a specific branch towards the environment. (ex. develop, test, production)

## Steps

 1. Check current branch via `git status`
	 - branch that you want to deploy
	 - run `git pull` to get all the changes made
 2.  Check yaml files and config files.
	 - list of yaml files
		 - app.yaml.dev
		 - app.yaml.test
		 - app.yaml.pre
		 - app.yaml.train
		 - app.yaml.prod
	 - list of config files
		 - config.py.dev
		 - config.py.test
		 - config.py.pre
		 - config.py.train
		 - config.py.prod
	 - **Note:** |copy the files for the environment you want to deploy. For example, to deploy in **`dev`** environment, use copy command,  **`cp app.yaml.dev app.yaml`** and **`cp config.py.dev config.py`**|

3. Also check the **`version.txt`** file
	- Change the Version Number and add the current date. 
	- Ex. **`v0.3.3-2018-07-19 `**

5. You can now proceed with deploying the changes, using gcloud app deploy
	- run command **`gcloud app deploy --project meralco-orange-191502 --version test071918`**
	- **Note:** |always check --project value and change the --version value|
