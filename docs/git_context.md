# Git _the need to know_

## **What are GitHub Actions?**

> GitHub Actions is an automation platform that helps you **build, test, and deploy** your code directly from GitHub. It lets you automate almost any task that happens in your code repository.

**How it Works (The Core Components):**

* **Workflow:** Your automation "recipe," written in a YAML file. It tells GitHub what to do and when to do it.  
* **Event:** Something that triggers your workflow (e.g., pushing code, opening a Pull Request, creating an issue, or a schedule).  
* **Job:** A set of steps that run together on a dedicated virtual machine. Workflows can have multiple jobs that run at the same time or one after another.  
* **Step:** An individual task within a job. This can be a simple command you write or a pre-built "Action."  
* **Action:** A reusable piece of code that performs a common, complex task (like checking out your code or setting up a programming environment). You can find them in GitHub Marketplace or write your own.  
* **Runner:** The virtual machine (Linux, Windows, or macOS) where your job actually runs. GitHub provides these, or you can host your own.

**In short: GitHub Actions lets you automate tasks in your repository by defining *workflows* that run *jobs* (sets of *steps*) on *runners* when specific *events* occur, often using pre-built *actions*.**

## GitHub Branches & Pull Requests

> Imagine your project's code is a main story (the main branch).

**Branches:** When you want to work on a new feature or fix something without messing up the main story, you create a "branch". This is like making a copy of the main story to work on separately. You can make changes and experiments on your branch without affecting anyone else's work.

**Pull Requests (PRs):** Once your changes on a branch are finished and ready, you create a "Pull Request." This is a way to:

> Tell others :clap:: "Hey, I've finished my work on this new part of the story."

**Show your changes:** Let others see exactly what you've done.

**Ask for feedback:** Get your teammates to review your changes and make sure they're good.

**Ask to merge:** Request that your changes be added back into the main story.

So, you branch off to work safely, and then create a pull request to share your work, get it reviewed, and eventually blend it back into the main project.
