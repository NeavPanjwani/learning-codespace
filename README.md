Q1. Introduction of codespace :- 
GitHub Codespaces is a cloud-based development environment that allows you to code directly in VS Code without setting up anything locally. 
It provides a fully configured workspace with all dependencies , making it ideal for quick prototyping, team collaboration, and working from any device. 
Codespaces also offers pre-built templates for different programming languages and frameworks, including blank projects, JavaScript, React, Python, Node.js, and more.
To run HTML and JavaScript files, you need to install the "Live Server" extension in VS Code. Additionally, you can install other useful extensions

Q2. uses & importants 

Use Cases:
1. Quick prototyping – No installations needed, start coding right away.
2. Team collaboration – Work on the same project without compatibility issues.
3. Develop on any device – Works smoothly on low-powered laptops and tablets.
4. Safe testing – Run code in an isolated environment.

Why It’s Important for Teams:
1. Same setup for everyone – No "works on my machine" problems.
2. Easy onboarding – New team members can start coding immediately.
3. Real-time collaboration – Multiple developers can work together seamlessly.

Q3. Instructions for new users on how to set it up in VS Code.

a. Create a Codespace from GitHub
  1. Go to your GitHub repository.
  2. Click the "Code" button.
  3. Select "Codespaces" → "Create Codespace on main".
  4. Wait for the Codespace to launch in your browser.

b. Open Codespace in VS Code
  1. In the Codespaces tab, click “Open in VS Code” (requires the GitHub Codespaces extension).
  2. VS Code will connect to the Codespace automatically.

c. Start Writing Code
  1. Your Codespace is pre-configured and ready to use.
  2. Write and edit code as you normally would.

d. Set Up Automatic Git Push & Pull
  To automatically push changes after every commit and pull updates when starting a Codespace:

- Auto-Push Setup:
    1. Open the terminal and run:
              cd .git/hooks
              nano post-commit
    2. Add the following script:
            #!/bin/bash
            git push origin main
       
    3. Save and exit (Ctrl + X, then Y, then Enter).
 
    4. Make it executable:
           chmod +x post-commit

- Auto-Pull Setup:
    1. Run:
         nano auto-pull.sh
       
    2. Add the script:
          #!/bin/bash
          cd /path/to/your/repo
          git pull origin main

    3. Save and exit, then make it executable:
           chmod +x auto-pull.sh

Now, every commit will automatically push to GitHub, and you can run ./auto-pull.sh to sync changes from the repository.
Note: Before executing any Git operations, always verify which branch you are working on to avoid unintended modifications. 
Use git branch to check your current branch.
