Student Setup
-------------
Normally, repositories house code that all developers use as a base to build their changes off of.
When other developers make changes, all developers pull them in and continue their work on top.
In our case, however, each student will have a separate fork of this repository in order to complete
their assignments. Furthermore, each student must keep their fork private so as to prevent any
possible plagiarism. Unfortunately, GitHub does not allow private forks of public repositories.

For this reason, we won't be using the standard GitHub workflow here. Instead, we have to jump
through some hoops in order to support our specific use case, while also using GitHub's repository
hosting platform.

Part 1: Bootstrap Your Repository
---------------------------------
Use the following instructions to properly set up your environment and your repository.

- Ensure you have a GitHub account, have verified your email address, and are signed in
- [Create a new repository](https://github.com/new) on GitHub
  - Name your repository `cs404.1`
  - Ensure the repository is marked private
  - Create the repository
- Add `fsareshwala` as a collaborator
  - Visit the `Settings` tab
  - Select the `Collaborators` section on the left
  - Add the `fsareshwala` user as a collaborator to your repository
- Configure `git` properly
  - Tell `git` who you are (replace my information with yours)
    ```
    git config --global user.name 'Faraaz Sareshwala'
    git config --global user.email 'fsareshwala@berkeley.edu'
    ```
  - Tell `git` to fix whitespace problems for you:
    ```
    git config --global core.whitespace fix,-indent-with-non-tab,trailing-space,cr-at-eol
    ```
  - Tell `git` to update line endings automatically once you commit your changes:
    - Mac/Linux
      ```
      git config --global core.autocrlf input
      ```
    - Windows
      ```
      git config --global core.autocrlf true
      ```
- Bootstrap your repository
  - Execute the following command in a new terminal
  - **Note**: make sure to replace `username` in the command with your GitHub username
  ```
  curl https://raw.githubusercontent.com/fsareshwala/cs404.1/master/tools/bootstrap.sh | bash -s username

  ```
  - You will now have a directory named `cs404.1` where you executed the command above. This is your
    assignment directory where you will do your work.

Part 2: Installing an IDE
-------------------------
An integrated development environment (IDE) is a tool that developers use to work on code. The IDE
includes all of the elements necessary to compile, run, and debug our programs. The IDE we will use
for this class is Visual Studio Code (VSCode).

**Note**: you are not required to use VSCode or even an IDE. You may use whatever tools you prefer
using. However, VSCode is the supported IDE for this class. If you venture off on your own, you will
be responsible for ensuring your environment works and runs programs properly. It is up to you to
determine whichever development environment works best for your personal tastes. As such, detailed
instructions on how to perform various environment related operations won't be provided. I assume
that by this stage of your software engineering career, you are familiar with your tools of choice.

Follow the instructions below to install and properly set up your IDE.

- [Download](https://code.visualstudio.com/Download) and install VSCode
- Open VSCode and open the extension installation page
- Search for and install the `vscode-bazel` extension
- Restart VSCode
- Load your assignment repository in your IDE and ensure you can compile and run programs and tests

Part 3: Making Your First Commit
--------------------------------
Now that you have properly configured your system, let's start making some changes.

- Identify yourself within your repository
  - Open the `name.md` file in the top level root of the repository
  - Replace the contents with your name
  - Commit the addition and push the change to GitHub
  - This is how I know who the repository belongs to
- Identify your language of choice
  - Open the `language.md` file in the top level root of the repository
  - Add your language of choice, in fully lowercase characters (e.g. java, python)
  - Commit the addition and push the change to GitHub
  - This is how I know which language you will be using