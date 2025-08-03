🔐 HOW TO SET UP SSH FOR GitHub ON WSL (Ubuntu) — A Step-by-Step Guide for Developers

Are you tired of typing your GitHub token every time you push code? You're not alone!

As developers, we crave smooth workflows — and secure SSH authentication is the best way to simplify GitHub operations, especially when using WSL (Windows Subsystem for Linux). This guide walks you through setting up SSH for GitHub the clean and modern way.


---

✅ Why Use SSH Over HTTPS?

🔒 Secure: SSH uses public/private key cryptography.

🔁 Effortless: No need to paste tokens every time you push or pull.

🤓 Professional: It’s the preferred method for devs working across multiple environments.



---

🚀 Step-by-Step: Configure GitHub SSH on WSL (Ubuntu)

🔧 1. Check for Existing SSH Keys

ls -al ~/.ssh

If you see files like id_rsa and id_rsa.pub, you already have SSH keys. Otherwise, move to step 2.


---

🗝 2. Generate a New SSH Key Pair

ssh-keygen -t ed25519 -C "your_email@example.com"

When prompted for a file location, just press Enter.

Set a passphrase or leave it blank for simplicity.


> 🔐 ed25519 is preferred for better security and performance.




---

👁 3. Start the SSH Agent

eval "$(ssh-agent -s)"


---

➕ 4. Add Your Private Key to the Agent

ssh-add ~/.ssh/id_ed25519


---

📋 5. Copy Your Public Key

cat ~/.ssh/id_ed25519.pub

Copy the output — this is what you'll paste into GitHub.


---

🌐 6. Add the SSH Key to Your GitHub Account

1. Go to GitHub > Settings > SSH and GPG Keys.


2. Click “New SSH Key”.


3. Paste the key.


4. Give it a name (e.g., WSL Ubuntu).




---

🧪 7. Test the Connection

ssh -T git@github.com

You should see:

Hi your-username! You've successfully authenticated...


---

🔄 8. Set Your Repo to Use SSH

Change the remote URL of your Git repo:

git remote set-url origin git@github.com:your-username/your-repo.git

Now you’re free to git push without typing your credentials again!


---

🧠 Summary Cheat Sheet

Task	Command

Generate SSH Key	ssh-keygen -t ed25519 -C "email"
Start SSH Agent	eval "$(ssh-agent -s)"
Add Key to Agent	ssh-add ~/.ssh/id_ed25519
Copy Public Key	cat ~/.ssh/id_ed25519.pub
Test Connection	ssh -T git@github.com
Update Remote URL	git remote set-url origin git@github.com:...



---

🧩 Bonus Tip: Where SSH Keys Are Stored

~/.ssh/id_ed25519        # private key
~/.ssh/id_ed25519.pub    # public key

Never share your private key. Keep it safe!


---

✍ About the Author

Nicholas Udoh
AI & NLP Engineer | Technical Writer for Data-Driven Brands
Helping developers, researchers, tech brands etc simplify complex concepts through engaging writing.

🔗 linkedin.com/in/nikkifiok | 📫 nikkifiok@gmail.com | 💼 GitHub: N-UDOH


---

> If you found this helpful, share it with a fellow developer!
Follow for more developer-friendly tutorials on Git, AI, NLP, and Python.
