![image](https://github.com/user-attachments/assets/558e6715-caaa-45a4-8b8b-10f0c20fd362)


# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   It is important because it can track changes in code overtime, it
    also allows collaborative works on projects and in addition of
    providing a robust set of features for branching and mering which
    helps teams to work more efficiently and avoid conflicts. It also
    lowers costs since developoers can use Git without paying or
    subscribing to anything.

2.  How does Git track changes in a project?

-   Every time a file changes, Git stores a new copy of that file in its
    database. A commit stores a reference to the most recent version of
    a file tracked by that commit. This means that when a commit is
    created, it uses the reference stored by its parent for unchanged
    files, and the reference to the newly added version for changed
    files.

3.  What is the difference between a local repository and a remote
    repository in Git?

-   A **local repository** is one that already exists or is already
    stored on your machine. It can be a repository that you already
    cloned before or was cloned outside of SourceTree (ex.
    using git commands on the command line). **You don\'t clone local
    repositories**, you just need to add their folders to the SourceTree
    interface, as indicated in the UI to \"*drag & drop repository
    folders*\" into SourceTree, so that they will appear in the UI.

-   A **remote repository** is one that exists somewhere else, in
    Github, Gitlab, Bitbucket, or in any other server that hosts Git
    repositories. This is the one you need to **clone** into your own
    machine, where it can now become a **local** copy of the **remote
    repository**.

4.  What are the basic Git commands?

-   Configuration

    -   git config \--global user.name \"Your Name\"

    -   git config \--global user.email \"your.email@example.com\"

-   Repository Management

    -   To create a new local repository, use:

        -   git init

    -   To clone an existing repository from a remote server:

        -   git clone \<repository_url\>

-   Staging and Commiting

    -   To add files to the staging area

        -   git add \<filename\>

    -   To add all modified and new files

        -   git add

    -   To commit changes to the local repository:

        -   git commit -m \"Commit message\"

    -   To commit all changes, including those not staged:

        -   git commit -a -m \"Commit message\"

-   **Pushing and Pulling**

    -   To push changes to the remote repository:

        -   git push origin master

    -   To fetch and merge changes from the remote repository:

        -   git pull

-   **Branching and Merging**

    -   To create and switch to a new branch:

        -   git checkout -b \<branchname\>

    -   To switch between branches:

        -   git checkout \<branchname\>

    -   To merge a branch into the current branch:

        -   git merge \<branchname\>

-   **Status and Logs**

    -   To check the status of your repository:

        -   Git status

    -   To view the commit history:

        -   git log

-   **Tags**

    -   To create a tag for a significant changeset:

        -   git tag \<tagname\>

    -   To push tags to the remote repository:

        -   git push \--tags

-   **Undoing Changes**

    -   To discard changes in a file:

        -   git checkout \-- \<filename\>

    -   To reset the repository to the last commit:

        -   git reset \--hard

-   **Searching**

    -   To search for a specific pattern in your working directory:

        -   git grep \"pattern\"

5.  How do you check the status of a Git repository?

    -   git status

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   A branch in Git is simply a lightweight movable pointer to one of
    these commits. The default branch name in Git is master. start in
    making commits, it gives a master branch that points to the last
    commit made.

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   **GitHub** and **GitLab** are both web-based platforms designed to
    host Git repositories, manage code changes, and enable collaboration
    among developers. They provide tools like pull requests, issue
    tracking, and CI/CD integration to streamline the software
    development process. GitHub is known for its large community and
    open-source culture, offering a wide array of public repositories
    and a social element where users can star, fork, and follow
    projects. GitLab, on the other hand, is more focused on providing a
    complete DevOps lifecycle, offering features that support the entire
    development pipeline from planning and coding to testing and
    deployment. GitLab also allows users to host repositories on their
    own servers, giving more flexibility for private or on-premises
    deployments.

-   In contrast, **Git** is a distributed version control system (VCS)
    that underpins both GitHub and GitLab. Git is a tool that tracks
    changes in source code and enables collaboration, but it does not
    provide the cloud-hosting, project management, and collaboration
    features that GitHub and GitLab offer. Git is used locally on a
    developer's machine to manage code, and repositories can be pushed
    to platforms like GitHub or GitLab for sharing and collaboration.
    Therefore, while GitHub and GitLab are platforms built around Git
    repositories, Git itself is the underlying system that tracks
    changes and manages versions of files in a decentralized manner.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

-   **Step 1:** Initialize Git

    -   **Get init**

-   Running this command initializes a hidden .git folder in your
    project directory, which is essential for tracking changes in your
    project. You can verify its presence using:

    -   ls --a

-   **Step 2: **Check Untracked Files

    -   git status

-   **Step 3: **Add Files

    -   git add \<file name\>

-   **Step 4:** Commit Changes

    -   git commit -m "commit message"

-   **Step 5:** Push to Remote Repository

![image](https://github.com/user-attachments/assets/bbba14c8-c2d0-43a3-bf2b-d201907f14d8)


-   To fix the above error : git remote add \<name\> \<GitLab Repository
    URL\>

-   **Step 6: **Set Upstream

    -   git push --- set-upstream \<name\> \<name of the branch\>

-   **Step 7:** Obtain Access Token in GitLab

![image](https://github.com/user-attachments/assets/22b226fa-0d22-427f-8acf-3baf6ad00974)

-   **Step 8: **Push Your Code using the Gitlab user name and secrete.

![Uploading image.png…]()


9.  What are the steps to collaborate with others using GitLab or
    GitHub?

-   To collaborate with others using GitLab or GitHub, follow these
    steps: create or fork a repository, clone it locally, create a new
    branch for your changes, make and commit your changes, push the
    branch to the remote repository, and open a pull request (GitHub) or
    merge request (GitLab) for review. Collaborate with reviewers to
    address any feedback, resolve merge conflicts if needed, and once
    approved, merge the request. Finally, pull the latest changes from
    the main branch and clean up by deleting the feature branch locally
    and remotely.

10. How do you resolve merge conflicts in Git?

-   **Identify the conflict**: Use git status to see conflicted files.

-   **Open conflicted files**: Look for conflict markers
    (\<\<\<\<\<\<\<, =======, \>\>\>\>\>\>\>).

-   **Resolve the conflict**: Edit the file to choose or combine
    changes, then remove conflict markers.

-   **Stage the resolved files**: Use git add \<file-name\> to stage the
    changes.

-   **Commit the merge**: Use git commit to complete the merge.

-   **Push the changes**: Push to the remote repository with git push
    origin branch-name.

11. What is a pull request, and why is it used in GitHub?

-   A pull request (PR) in GitHub is a way to propose changes from one
    branch to another. It is used for code review, collaboration, and
    quality control, allowing team members to review, discuss, and
    approve changes before merging them into the main codebase.

12. What are some best practices for writing commit messages?

-   **Use a concise, clear summary**: Limit to 50-72 characters,
    describing the change.

-   **Write in the imperative mood**: e.g., \"Add feature,\" \"Fix
    bug.\"

-   **Capitalize the first letter** of the commit message.

-   **Provide a detailed description** (if needed) in the body,
    explaining why the change was made.

-   **Separate subject and body** with a blank line.

-   **Reference issues or PRs**: e.g., \"Closes #123\" or \"Fixes
    #456.\"

-   **Avoid vague messages**: Be specific about the change (e.g., \"Fix
    navbar alignment on mobile\").

*References:*

*How do you resolve merge conflicts in Git? - Bing*. (n.d.). Bing.
https://www.bing.com/search?q=10.+How+do+you+resolve+merge+conflicts+in+Git%3F&cvid=775f79a0f7184a1ea599773b1991c69b&gs_lcrp=EgZjaHJvbWUyBggAEEUYOdIBCDE4ODdqMGo5qAIAsAIA&FORM=ANAB01&PC=U531

*basic git commands - Bing*. (n.d.). Bing.
https://www.bing.com/search?q=basic+git+commands&cvid=8f4623788e89458c91081515f9c79cb9&gs_lcrp=EgZjaHJvbWUqBggAEAAYQDIGCAAQABhAMgYIARAAGEAyBggCEAAYQDIGCAMQABhAMgYIBBAAGEAyBggFEAAYQDIGCAYQABhAMgYIBxAAGEAyBggIEAAYQNIBCDQwOTRqMGo5qAIIsAIB&FORM=ANAB01&PC=U531

GeeksforGeeks. (2024, July 23). *Difference between GitLab and GitHub*.
GeeksforGeeks.
https://www.geeksforgeeks.org/difference-between-gitlab-and-github/

*How does git track changes to files*. (n.d.). Stack Overflow.
https://stackoverflow.com/questions/31995829/how-does-git-track-changes-to-files

*What is Git & why should you use it? \| Noble Desktop blog*. (n.d.).
https://www.nobledesktop.com/blog/what-is-git-and-why-should-you-use-it

*What is the difference between remote repository and local repository
in git?* (n.d.). Stack Overflow.
https://stackoverflow.com/questions/60825928/what-is-the-difference-between-remote-repository-and-local-repository-in-git
