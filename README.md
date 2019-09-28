# CherryTree GitHub Sync

**What is it?**  
A script that syncs CherryTree files to Git.

**Why do I want this?**  
You can use a single CherryTree file across several machines/operating systems.  
CherryTree files are stored in your own private Git repo.  
You can roll back to a previous version in case of a catastrophic corrupted file.  

**How does it work?**  
Simply stated, your CherryTree file is stored in a private Git repo (your repo, not mine, obviously).  
When launching CherryTree, the shell script will pull latest files from Git, open them, and commit/push them once CherryTree is closed.

**Pics or it didn't happen.**  
[https://youtu.be/WkR1DFFOHhc](https://youtu.be/WkR1DFFOHhc)

**OK, I'm sold. What do I have to do?**
1) Create/initialize your private git repo where you'll store your CherryTree files.
2) Copy "[launcher.sh](https://raw.githubusercontent.com/MrChrisWeinert/CherryTreeGitSync/master/launcher.sh)" to your newly-created git repo.

>**On Linux**:
>Make the launcher executable: `chmod +x launcher.sh`
>Create an alias like this, using the location of your local git repo:  
>`alias cherry="cd ~/git/CherryTreePrivate && ./launcher.sh"`
>Type `cherry`

>**On Windows**:
>Create a shortcut file, using the location of your local git shell executable, and your local git repo:  
>`"C:\Program Files\Git\bin\sh.exe" -c "cd /c/Code/MrChrisWeinert/CherryTreePrivate && ./launcher.sh"`
>Add the CherryTree.exe executable's path to your environment's PATH variable.
>Double-click the shortcut
>
>Optional:  
>Set the "Run" dropdown value to `Minimized`.  
>Use the original "Cherries" icon from the CherryTree executable. 
