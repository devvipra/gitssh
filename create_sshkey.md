Open Terminal
Enter the command  ssh-keygen -t ed25519 
Choose where to save the key, press ENTER to save key in default location, or wirte out the path and choose a name for the key.
Choose a passphrase for the key or leave it blank.
The terminal will then generate the SSH key and display a message indicating that the key has been created.
Before attempting to use the SSH key, you need to add your private key to the SSH agent on your computer.
Open your terminal and run the following command to start the SSH agent:  eval "$(ssh-agent -s)" 
Add your private key to the SSH agent by running the following command:  ssh-add ~/.ssh/demokey  replace "demokey" with the name of your PRIVATE key
Verify that the key has been added to the SSH agent by running:  ssh-add -l  This command will list all the keys currenlty added to the SSH agent.
