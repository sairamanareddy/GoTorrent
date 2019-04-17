## Guidelines for contribution :
1. **Working on seperate branch**
	- Clone the repository : ```git clone https://github.com/IITH-SBJoshi/concurrency-8.git```
	- Create a issue specific branch in cloned repository : ```git checkout -b issue#<issue number>```
	- Run the code by following the steps above
	- You can now start working on your current branch
2. **Testing the changes**
	- Run the test cases if any: ```go test <test file>.go```
	- Check the linting (Install [golint](https://github.com/golang/lint), if not already installed): ```golint <file_name>```
	- Run `./build.sh` to check if the build passes
3. **Commiting the changes**
	- Update ```.gitignore``` if there is any need .
	- To add changes in your working directory : ```git add .```
	- Commit your changes : ```git commit -m "<message>"```
	- Follow a simple commit message guideline eg . ``` Fix <issue_id> : <small description> Author@<your name>```
4. **Pushing the changes**
	- Get current master: `git fetch origin master`
	- Merge master with your branch: `git merge master`
	- Push your changes : ```git push origin <your branch name>:<your branch name>```
	- Make sure that ```CI build``` passes.
5. **Generating Pull requests :**
	- [Generate a pull request](https://help.github.com/articles/about-pull-requests/) from your ```branch``` branch to ```master``` branch.
	- Give the PR and apt title, and mention `Fixes #<issue_number>` in the comment to link it with the issue.
6. **Commenting your Code**
	- Include your comments directly preceding an object for GoDoc to document it.
	- Indent pre-formatted comments.
	- Refer to the [Guidelines](https://blog.golang.org/godoc-documenting-go-code) for more info on commenting.
