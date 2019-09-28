# CherryTree GitHub Sync

**What is it?**
- A script that syncs CherryTree files to Git.

**Why do I want this?**
- It lets you use a single CherryTree file across several machines/operating systems.
- Your CherryTree files are stored in your own private Git repo.
- You can roll back to a previous version in case of a catastrophic corruped file.

**How does it work?**
- Simply stated, your CherryTree file is stored in a private Git repo (your repo, not mine, obviously). When you launch CherryTree, the launcher shell script will check out the latest files from Git, open them, and commit them back into the Git repo once CherryTree closes.

**OK, I'm sold. What do I have to do?**
1) Create/initialize your private git repo where you'll store your CherryTree files.
2) Copy "[launcher.sh](https://raw.githubusercontent.com/MrChrisWeinert/CherryTreeGitSync/master/launcher.sh)" to your newly-created git repo.

>**Linux**:
>Make it executable: `chmod 755 launcher.sh`
2) Create your shortcut:
>**Linux**:
>Create an alias like this, using the location of your local git repo:
>`alias cherry="cd ~/git/CherryTreePrivate && ./launcher.sh"`

>**Windows**:
>Create a shortcut file, using the location of your local git shell executable, and your local git repo:
>`"C:\Program Files\Git\bin\sh.exe" -c "cd /c/Code/MrChrisWeinert/CherryTreePrivate && ./launcher.sh"`

>Set the "Run" dropdown value to `Minimized`.
>
>Give your shortcut a nice icon by hitting the `Change Icon...` button. Browse to the CherryTree.exe executable and use its icon.*
>
>Finally, you'll need to add the CherryTree.exe executable's path to your environment's PATH variable.

3) Run the program:
>**Linux**:
> type `cherry`

> **Windows**:
> double-click the shortcut
