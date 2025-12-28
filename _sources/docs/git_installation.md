# Git and GitHub: Getting Started

Before we set up your coding environment, let's clarify what Git and GitHub are:

- **Git** is a free version control system. It helps track changes in your files, manage different versions, and merge updates from collaborators.  
- **GitHub** is a company and platform (github.com) that hosts Git repositories online. Think of it as a central hub where you and your collaborators sync your code.  

You'll use Git to **download course materials** and **work on your homework assignments** throughout the term.  

GitHub is a web-based application and does not require set-up. Since you will be cloning the [course GitHub repository](https://github.com/UBC-CS/cpsc330-2025W1) in order to run the lecture notebooks locally, you need git installed locally. Follow the instructions below for this.

## Option 1: GitHub Desktop (easiest)

If you're new to the command line, you may prefer [GitHub Desktop](https://desktop.github.com/). It provides a simple interface for working with Git and GitHub.  

That said, we recommend at least some familiarity with the **command line version**, since it's widely used in data science and software development.  


## Option 2: Command-line Git (recommended)

### Step 1: Install Git

Follow the instructions for your operating system:

#### macOS
Open Terminal (Applications –> Utilities folder or search with Spotlight). From the terminal, run the command:

```bash
xcode-select --install
```

This will install git and many other very useful applications as well (including `make`).

#### Ubuntu Users

Open the terminal and install git using your system package manager. For example

```bash
sudo apt-get install git
```

should do the trick on Ubuntu.

#### Windows Users

- Go to http://git-scm.com.
- Click on the download link
- Run it and accept all defaults in the installation process. 

This will install Git and also give you a Git Bach terminal, which provides a Linux-like environment on Windows. 

If the above does not work for you, follow the [installation instructions here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### Step 2: Testing your Git installation

Open your Terminal (or Git for Windows) and run 

```bash
git --version
```

If you are returned the version of git, it means your install was successful!


### Step 3: Authenticating with GitHub (important!)
For cloning public repositories (like the course repo), no authentication is needed. However, for pushing changes to your **private homework repository**, GitHub requires authentication.  

You have two options:  

1. **Personal Access Token (PAT)**  
   - Easiest for beginners.  
   - You'll log in with your GitHub username and a token (instead of your password).  
   - Follow GitHub's guide: [Creating a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).  

2. **SSH Keys**  
   - Recommended if you'll use Git a lot.  
   - You only set it up once, then you can push/pull without entering credentials.  
   - Follow GitHub's guide: [Generating a new SSH key and adding it to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).  

Our recommendation: use **[choose one: PAT or SSH depending on what you prefer for this class]**. If you get stuck, bring your laptop to tutorials or office hours, and w'll help you set it up.  

That's it! With Git installed, you're ready to clone [the course GitHub repository](https://github.com/UBC-CS/cpsc330-2025W1) and start working on your homework assignments. 

## Learning git

There are many free online resources for learning git. One possibility is the [Software Carpentry git tutorial](https://swcarpentry.github.io/git-novice/). 

