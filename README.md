# **Week#02**

# **PROJECT 2: VERSION CONTROL WITH GIT**

**Author:** DevOps Intern

**Domain:** DevOps Engineering

**Batch:** 2026

**Status:** Completed & Verified

---

## **1. Executive Summary**

This project demonstrates the basic use of Git and GitHub for version control and project management. The main purpose of the project was to understand how project files can be tracked, updated, committed, and stored in a remote GitHub repository.

During the project, I worked with a responsive HTML and CSS website. I used Git to manage the project changes and GitHub to store the project remotely.

I also practiced working with a separate feature branch, creating a Pull Request, merging the changes into the main branch, and synchronizing the local repository with GitHub.

As part of the project, I also worked with an AWS EC2 Ubuntu server and Nginx to understand the basic process of deploying a website on a Linux web server.

---

# **2. Workflow Verification & Evidence**

## **Step 1: Project Repository Setup**

The project was first connected to a GitHub repository so that the website files could be managed using Git and stored remotely.

* **GitHub Repository:**

```text
https://github.com/Salman-Ahmad542/DecodeLabs-project-2
```

The project mainly contained:

```text
index.html
style.css
README.md
```

### **Explanation**

The Git repository provides version control for the project. Instead of manually keeping different copies of the project, Git keeps track of changes made to the files.

GitHub was used as the remote location where the project could be stored and managed online.

---

## **Step 2: Check Git Remote Repository**

The configured remote repository was verified using:

```bash
git remote -v
```

### **Explanation**

The `git remote -v` command displays the remote repositories connected to the local Git project.

It normally shows two URLs:

* **fetch** – used to download or retrieve changes.
* **push** – used to upload local changes to GitHub.

This step was important to confirm that the project was connected to the correct GitHub repository.

---

## **Step 3: Create a Feature Branch**

A separate branch was created for making changes to the website.

* **Branch:**

```text
feature/update-page
```

### **Explanation**

A branch allows developers to work on changes without directly modifying the main branch.

The `feature/update-page` branch was used for the website updates. This made the workflow safer because the changes could be completed and reviewed before being merged into `main`.

The basic idea was:

```text
main
  |
  └── feature/update-page
```

---

## **Step 4: Update the Website**

The website design and content were updated on the feature branch.

The updated website included:

* Navigation bar
* Hero section
* Project introduction
* Git and GitHub features
* Learning section
* About project section
* Git workflow
* Footer
* Responsive design

### **Explanation**

The purpose of this step was to make practical changes to the project while working inside the feature branch.

Git can then detect these changes and allow them to be saved as a commit.

---

## **Step 5: Check Project Changes**

Before committing the changes, the project status was checked using:

```bash
git status
```

### **Explanation**

The `git status` command shows the current state of the Git repository.

It helps identify:

* Modified files
* New files
* Deleted files
* Untracked files
* Current branch

This command is useful before committing because it allows us to verify which files have changed.

---

## **Step 6: Stage the Changes**

The modified project files were added to the Git staging area.

```bash
git add .
```

### **Explanation**

The `git add` command tells Git which changes should be included in the next commit.

The `.` means that changes in the current project directory are added.

The basic Git workflow at this stage is:

```text
Working Directory
       ↓
    git add
       ↓
Staging Area
```

---

## **Step 7: Create a Commit**

After staging the changes, a commit was created:

```bash
git commit -m "Update project homepage"
```

### **Explanation**

A commit saves a snapshot of the staged changes in the Git repository.

The message:

```text
Update project homepage
```

describes what was changed.

Commits are useful because they provide a history of changes and make it easier to understand how a project developed over time.

The workflow becomes:

```text
Working Directory
       ↓
    git add
       ↓
Staging Area
       ↓
  git commit
       ↓
 Git History
```

---

## **Step 8: Push Feature Branch to GitHub**

The feature branch was pushed to the GitHub repository.

```bash
git push origin feature/update-page
```

### **Explanation**

The `git push` command uploads local commits to a remote repository.

Here:

* `origin` represents the GitHub remote repository.
* `feature/update-page` is the branch being uploaded.

After this step, the feature branch and its changes were available on GitHub.

---

## **Step 9: Create Pull Request**

After pushing the feature branch, a Pull Request was created on GitHub.

The Pull Request was created from:

```text
feature/update-page
```

into:

```text
main
```

### **Explanation**

A Pull Request is a request to merge changes from one branch into another branch.

In this project, the Pull Request was used to request that the completed website changes from `feature/update-page` be added to the `main` branch.

This demonstrates a common GitHub collaboration workflow.

```text
feature/update-page
          ↓
    Pull Request
          ↓
        main
```

---

## **Step 10: Merge Pull Request**

The Pull Request was successfully merged into the `main` branch.

### **Explanation**

Merging combines the changes from the feature branch with the main branch.

After the merge, the updated website code became part of the main project.

This completed the feature development workflow.

---

## **Step 11: Update Local Main Branch**

After the Pull Request was merged, the local repository was switched back to the main branch.

```bash
git checkout main
```

The latest changes were then downloaded from GitHub:

```bash
git pull origin main
```

### **Explanation**

`git checkout main` switches the working repository to the `main` branch.

`git pull origin main` retrieves the latest changes from the remote GitHub repository and updates the local main branch.

This ensures that the local project contains the same changes that are available on GitHub.

---

## **Step 12: Verify Final Git Status**

The final repository status was checked using:

```bash
git status
```

The result confirmed:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### **Explanation**

This result means:

* The current branch is `main`.
* The local branch is synchronized with GitHub.
* There are no uncommitted changes.
* The working directory is clean.

Therefore, the Git/GitHub workflow was successfully completed.

---

# **3. Nginx Deployment**

As an additional part of the project, the website was prepared for deployment on an AWS EC2 Ubuntu server using Nginx.

## **Step 1: Nginx Document Root**

The website files were placed inside the Nginx document root:

```text
/usr/share/nginx/html/
```

The main website files were:

```text
index.html
style.css
```

### **Explanation**

The Nginx document root is the directory from which Nginx serves website files.

When a user opens the server's public IP address, Nginx looks inside this directory for the website files.

The `index.html` file acts as the main homepage.

---

## **Step 2: Verify Website Files**

The files inside the Nginx directory were checked using:

```bash
ls -la /usr/share/nginx/html/
```

### **Explanation**

The `ls -la` command displays the files inside the directory along with detailed information such as permissions, ownership, and file size.

This was used to confirm that `index.html` and `style.css` were present in the correct location.

---

## **Step 3: Configure File Permissions**

The following permissions were used:

```bash
sudo chmod 755 /usr/share/nginx/html
sudo chmod 644 /usr/share/nginx/html/index.html
sudo chmod 644 /usr/share/nginx/html/style.css
```

### **Explanation**

The `chmod` command is used to change file and directory permissions.

`755` on the directory allows the directory to be accessed and entered.

`644` on the website files allows the files to be read while keeping normal write permissions restricted.

Correct permissions are important because Nginx needs permission to access and read the website files.

---

## **Step 4: Test Nginx Deployment**

The website was opened using the public IP address of the EC2 server.

During testing, Nginx displayed:

```text
403 Forbidden
nginx/1.28.3 (Ubuntu)
```

### **Explanation**

A `403 Forbidden` response means that Nginx received the request but was not allowed to serve the requested content.

The website files were already present in the correct Nginx document root, so further investigation was required into the Nginx server configuration and access permissions.

The configuration can be checked using:

```bash
nginx -t
```

The default Nginx configuration can also be inspected using:

```bash
cat /etc/nginx/sites-enabled/default
```

This troubleshooting step helps identify configuration problems that may prevent Nginx from serving the website.

---

# **4. Technical Learnings & Takeaways**

* **Git Repository:** Learned how Git manages project files and keeps track of changes.

* **Git Remote:** Learned how a local repository is connected to a remote GitHub repository.

* **Git Branch:** Learned how to create a separate branch for working on new features.

* **`git status`:** Used to check the current state of the repository and identify modified or untracked files.

* **`git add`:** Used to move changes into the staging area before creating a commit.

* **`git commit`:** Used to save a snapshot of project changes in Git history.

* **`git push`:** Used to upload local commits and branches to GitHub.

* **Pull Request:** Learned how to request that changes from a feature branch be merged into the main branch.

* **Merge:** Used the GitHub workflow to combine the completed feature into the main branch.

* **`git pull`:** Used to synchronize the local repository with the latest version available on GitHub.

* **Nginx:** Learned the basic concept of serving a website through the Nginx web server.

* **Nginx Document Root:** Learned that `/usr/share/nginx/html/` is used to store website files for the configured Nginx server.

* **Linux Permissions:** Practiced checking and setting permissions for directories and website files.

* **Troubleshooting:** Encountered a `403 Forbidden` response and learned that Nginx configuration and file access permissions need to be checked when a web server cannot serve website content.

---

# **5. Conclusion**

This project gave me practical experience with Git and GitHub and helped me understand the basic version-control workflow used in a DevOps environment.

I learned how to manage a project repository, create a feature branch, make and commit changes, push code to GitHub, create a Pull Request, merge changes into the main branch, and synchronize the local repository with GitHub.

I also gained practical experience with AWS EC2, Linux file management, and Nginx website deployment. Although the Nginx test resulted in a `403 Forbidden` response, the website files were correctly placed in the Nginx document root and the issue was identified for further configuration troubleshooting.

Overall, this project improved my understanding of **Git, GitHub, Linux, branching, Pull Requests, and basic web-server deployment**, which are important skills for working in a DevOps environment.
