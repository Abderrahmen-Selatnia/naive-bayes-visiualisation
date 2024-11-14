# projet_algo3
on this repo we will work for the project
oki nice 
now this is how we gona work each has a file to work on 
the one with his name eac file is a window each window is responsible for somthing 
on this projec
one for control & debugging 
one for core visualization 
one for implimenting the naive bayer algorithem
i need both of you chose a role 
so we start
cause evry one is offline am making for each role a header file when you pick a role 
just copy the starter code to the header file wiht your name on 

Team Member 1: Handles the main logic, SDL initialization, event handling, and calling the rendering functions from the other modules. This person will ensure everything is coordinated and control the main event loop.
Team Member 2: Implements the Bayer algorithm visualization and renders it to a specific window.
Team Member 3: Implements the main display, such as showing the output of the algorithm, user interface elements, or debugging info.

***************************how to set up the repo****************** 

Setting Up SSH for Windows Users
Follow these steps to set up SSH for accessing this repository on Windows:

1. Install Git for Windows (if not installed)
Download and install Git for Windows.
During the installation, choose Git Bash as the default terminal for Git.
2. Generate an SSH Key
Open Git Bash.
Run the following command to create a new SSH key. Replace your_email@example.com with your email address:
bash
Copy code
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
When prompted, press Enter to save the key to the default location (C:\Users\YourUsername\.ssh\id_rsa).
Optionally, add a passphrase for additional security, or just press Enter to skip.
3. Start the SSH Agent and Add the SSH Key
Start the SSH agent by running the following command:
bash
Copy code
eval "$(ssh-agent -s)"
Add the SSH key to the agent:
bash
Copy code
ssh-add ~/.ssh/id_rsa
4. Add Your SSH Key to GitHub/GitLab
Copy the SSH public key to your clipboard:
bash
Copy code
cat ~/.ssh/id_rsa.pub
Go to your GitHub or GitLab account:
For GitHub: Go to Settings > SSH and GPG keys.
For GitLab: Go to Settings > SSH Keys.
Click on New SSH Key, paste the key you copied, and save it.
5. Test the SSH Connection
Run this command to test if SSH was set up correctly (replace github.com with gitlab.com if using GitLab):

bash
Copy code
ssh -T git@github.com
If successful, you should see a message like:

rust
Copy code
Hi username! You've successfully authenticated...
6. Clone the Repository Using SSH
When cloning the repository, use the SSH URL provided by GitHub/GitLab:

bash
Copy code
git clone git@github.com:username/repository.git
Note: If you've already cloned the repository using HTTPS and want to switch to SSH, use the following command:

bash
Copy code
git remote set-url origin git@github.com:username/repository.git
7. Push and Pull Without Entering Credentials
Once SSH is set up, you should be able to push and pull without entering your credentials every time.