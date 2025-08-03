FROM FORK TO PULL REQUEST: A Beginner’s Guide to Git & GitHub (with Terminal Commands!)

Overview

This guide walks you through the complete process of contributing to a GitHub project using Git commands in the terminal. You’ll learn how to fork a repo, clone it, make changes, push, and finally create a pull request (PR) back to the original repo.

✅ Perfect for beginners looking to contribute to open-source or showcase collaboration skills.

What You’ll Learn

✅What a fork is
✅ How to clone the fork to your computer
✅ How to create a new branch
✅How to edit a specific file
✅ How to commit and push your changes
✅How to create a pull request (PR)

Real-World Scenario

Let’s say you want to contribute to a popular repository:

• Original Repository: github.com/kingben/Python
• Your GitHub username: N-UDOH
• Your fork repo: github.com/N-UDOH/Python (“Python” is the repo you fork from the original repository)
• The file you want to edit: data cleaning/Data_cleaning_using_Python_with_Pandas_Library.ipynb which is present in the Python repo

N.B: You’ll be editing just this one file and submitting a pull request (PR) to the original owner.

NOW THE STEPS:

Step 1: Fork the Repository
Forking creates a personal copy of someone's repository under your GitHub account
i. Go to the repository you want to contribute to (e.g., KingBen’s Python repo, which is github.com/kingben/Python).
ii. Click the “Fork” button (top-right corner).
iii. This creates a copy of the repo in your GitHub account at https://github.com/N-UDOH/Python

Step 2: Clone the Fork to Your Local Machine
Open your terminal and type👇:
git clone https://github.com/N-UDOH/Python.git
cd Python
This downloads the repo into a folder named Python on your machine.

Step 3: Create a New Branch for Your Changes
It’s best practice to work in a separate branch 👇 (master, main, or any other customized):
git checkout -b master
N.B: master is your branch name. You can name it anything related to your task.

Step 4: Make Your Changes
Open the notebook file you want to change in Jupyter Notebook or any code editor:
In Jupyter Notebook, navigate to👇:

cd data\ cleaning/
Open the notebook👇:

jupyter notebook
Data_cleaning_using_Python_with_Pandas_Library.ipynb
Make your changes such as fixing typos, adding comments, or improving code readability, save and close. Don’t touch other files!🚫

Step 5: Stage and Commit Your Changes
Once you’re done editing, stage and commit 👇:
git add “data cleaning/Data_cleaning_using_Python_with_Pandas_Library.ipynb”
git commit -m “Fix typos and improve comments in data cleaning notebook”
📌Write meaningful commit messages that describe what you have changed

Step 6: Push to GitHub
Push your changes to the branch in your forked repository 👇:
git push origin master

Step 7: Create the Pull Request
i. Go to your fork on GitHub: https://github.com/N-UDOH/Python
ii. GitHub will prompt you: “Compare & pull request” → Then Click it.
iii. Fill in the PR form:
• Title: Fix data cleaning notebook typos
• Description: Improved comments and fixed typos in the Pandas data cleaning tutorial notebook.
iv. Click “Create pull request.”

You Did It! 🙌

The repository owner (King Ben in this example) will now review your pull request. If everything looks good, he’ll merge it into the main project. You’ve just contributed to an open-source project! Congrats!🙌

📌 Pro Tips

Always create a branch for each task/feature.
Keep your pull request focused on one thing (e.g., one file).
Write clear commit messages.
Follow the project’s contribution guidelines (check CONTRIBUTING.md if available).

🖊️W Nicholas Udoh
AI & NLP Engineer | Technical Writer

Follow me on GitHub (https://github.com/N-UDOH)
Email: nikkifiok@gmail.com
LinkedIn: linkedin.com/in/nikkifiok

Let’s Grow Together — One Pull Request at a Time.
