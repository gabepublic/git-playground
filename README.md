# git-playground
Experimenting with github process

## Git Flow

### Gemini suggested flow

- prompt
```
Please create a best practice step by step process for two developers collaborative development using github, starting from: create a repo, clone, start development, etc.
```
- RESPONSE
#### A Collaborative Development Process Using GitHub

##### 1. **Create a Repository**
* **Log in to GitHub:** Access your GitHub account.
* **Create a new repository:** Click on the "New repository" button.
* **Configure the repository:** Give your repository a descriptive name, add an optional description, and choose the appropriate visibility settings (public, private, or internal).
* **Initialize with a README:** Check the box to initialize the repository with a README file. This will provide a basic starting point for documentation.
* **Create the repository:** Click the "Create repository" button.

##### 2. **Clone the Repository**
* **Clone the repository:** On your local machine, use Git to clone the newly created repository:
  ```bash
  git clone https://github.com/<your-username>/<repository-name>.git
  ```
  Replace `<your-username>` and `<repository-name>` with your actual GitHub username and repository name.

##### 3. **Create a New Branch**
* **Create a new branch:** Before making changes, create a new branch to isolate your work:
  ```bash
  git checkout -b <branch-name>
  ```
  Replace `<branch-name>` with a descriptive name for your branch.

##### 4. **Start Development**
* **Make changes:** Make your desired changes to the codebase.
* **Commit changes:** When you're ready, commit your changes:
  ```bash
  git add .
  git commit -m "Your commit message"
  ```
  Replace "Your commit message" with a clear and concise description of your changes.

##### 5. **Push Changes to Your Branch**
* **Push changes:** Push your changes to your remote branch on GitHub:
  ```bash
  git push -u origin <branch-name>
  ```

##### 6. **Create a Pull Request**
* **Create a pull request:** On GitHub, navigate to your repository and click on the "Pull requests" tab.
* **Create a new pull request:** Click the "New pull request" button, select your branch as the head branch, and choose the main branch (e.g., "main") as the base branch.
* **Add a description:** Provide a clear and concise description of the changes you've made.
* **Assign reviewers:** If necessary, assign other developers to review your changes.
* **Submit the pull request:** Click the "Create pull request" button.

##### 7. **Review and Merge**
* **Review changes:** The assigned reviewers will examine your code and provide feedback.
* **Address feedback:** Make any necessary changes based on the feedback.
* **Merge the pull request:** Once the changes are approved, merge the pull request into the main branch.

##### 8. **Update Your Local Branch**
* **Update your local branch:** Pull the merged changes from the remote repository:
  ```bash
  git pull origin main
  ```

**Additional Best Practices:**
* **Use meaningful commit messages:** Write clear and concise commit messages that accurately describe the changes you've made.
* **Keep branches up-to-date:** Regularly rebase your branch on the main branch to avoid merge conflicts.
* **Utilize GitHub features:** Take advantage of features like issues, milestones, and labels to organize your work and track progress.
* **Communicate effectively:** Collaborate with your team members to ensure everyone is on the same page.

By following these steps and best practices, you and your collaborators can effectively work together on GitHub projects.

## EXPERIMENTS

## Branch "change_001"

- Perform on the Windows desktop with: Github desktop (GD).
- Create a branch, "change_001" from GD; after create, GD automatically
  make the branch current (or `git checkout`); any changes onward will
  be on the "change_001" branch
- The branch has not been published to remote; as indicated by the 
  GD
- making changes to `README.md`, this file, on the branch.
- GD detected the changes
- From GD, commit then push to origin
- Go to `github.com` to try the pull request.
- After commit & push origin, the `github.com` alerted the new branch.
- There are two branches now: main, change_001
- Switch to "change_001" and the changes in the `README.md` are shown.
- From GD, click the "Current branch" down arrow, then go to "Pull requests" tab. Click the "create a pull request" link.
- There is no integration. GD just popup open the browser pointing to `github.com` pull request. HOWEVER, the benefit is the page has been pre-configured to compare "main" and "change_001" branches. In addition, it pre-checks whether the branch can be merged.
```
 Able to merge. These branches can be automatically merged.
``` 
- The page also shows the file(s) difference.
- Click Assignees: to self; enter title & description, click the green "Create pull request" button. Note: in this case, I assign it to myself.
- After clicking the "Create pull request", now the page refresh to show a button for "Merge pull request"; when clicked, the "Confirm merger" button is shown.
- Enter comment and click the "Confirm merger".
```
Pull request successfully merged and closed
You’re all set—the change_001 branch can be safely deleted.
```
- GD, go to the "main" branch then click "Pull origin" to get the latest merged code. 
- In the meantime, I have made the changes also on the "change_001" branch. When switching to the "main branch" to do the "pull origin" (above), there were option to: keep the changes in the branch, or to bring the changes to "main". I chose the first option, keeping in branch.
- After "pull origin", go back to the "change_001" branch, and from "View stash"
the options are: Restore the changes, or Discard. Choose Restore.
- Now, when returning back to "main" branch, again the choice of: 
keep the changes in the branch, or to bring the changes to "main".
- Let's take it to the main and commit & push from main.
- As indicated above, the "change_001" brach can be purged, after pull request -> merge to main.
  If not ourged, from GD when go back to the "change_001" branch, there is an option
  to "Preview Pull Request"; in this case the pull request from "main" to merge into "change_001" branch; sort of the opposite of the above pull request. 