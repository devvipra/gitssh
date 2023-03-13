Steps to assign SSH key to your GitHub account

Open Terminal
Locate and navigate to saved SSH key.
Enter  cat (name of your public key)
Copy SSH key in its entirety.
Navigate to your Github account settings and click on the SSH and GPG keys tab.
Then paste and add the key to the your account.
Before attempting to SSH to GitHub, you need to add your private key to the SSH agent on your computer.

Open your terminal and run the following command to start the SSH agent:  eval "$(ssh-agent -s)" 

Add your private key to the SSH agent by running the following command:  ssh-add ~/.ssh/demokey  replace "demokey" with the name of your PRIVATE key

Verify that the key has been added to the SSH agent by running:  ssh-add -l  This command will list all the keys currenlty added to the SSH agent.

Try and SSH to GitHub by entering:  ssh -T git@github.‌com 

You will be prompted to verify the authenticity of the host. Type yes and press enter.

Success! You will now be able to connect to GitHub using SSH.
