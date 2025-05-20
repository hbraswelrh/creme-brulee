### **What are GitHub Actions?**

> GitHub Actions is an automation platform that helps you **build, test, and deploy** your code directly from GitHub. It lets you automate almost any task that happens in your code repository.

**How it Works (The Core Components):**

* **Workflow:** Your automation "recipe," written in a YAML file. It tells GitHub what to do and when to do it.  
* **Event:** Something that triggers your workflow (e.g., pushing code, opening a Pull Request, creating an issue, or a schedule).  
* **Job:** A set of steps that run together on a dedicated virtual machine. Workflows can have multiple jobs that run at the same time or one after another.  
* **Step:** An individual task within a job. This can be a simple command you write or a pre-built "Action."  
* **Action:** A reusable piece of code that performs a common, complex task (like checking out your code or setting up a programming environment). You can find them in GitHub Marketplace or write your own.  
* **Runner:** The virtual machine (Linux, Windows, or macOS) where your job actually runs. GitHub provides these, or you can host your own.

**In short: GitHub Actions lets you automate tasks in your repository by defining *workflows* that run *jobs* (sets of *steps*) on *runners* when specific *events* occur, often using pre-built *actions*.**
