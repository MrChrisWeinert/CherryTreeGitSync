# CherryTree GitHub Sync

**A simple process &amp; script that syncs CherryTree files to Git.**

- Do you want your CherryTree files backed up in a safe, private location?
- Do want to use CherryTree on several machines/operating systems?
- Do you want to be able to roll back to a previous version in case of a catastrophic *cat-dancing-on-keyboard-deleted-all-the-things* incident?

If you answered `yes` to any of these questions, then CherryTree GitHub Sync is for you!

1) Create/initialize your private git repo where you'll store your CherryTree files. I'm super-creative so I'll call mine "CherryTreePrivate".
2) Copy "[launcher.sh](https://raw.githubusercontent.com/MrChrisWeinert/CherryTreeGitSync/master/launcher.sh)" to your newly-created git repo.
>**Linux**
>Make it executable: `chmod 755`
2) Create your shortcut:
>**Linux**:
>Create an alias like this:
>`alias cherry="cd ~/git/CherryTreePrivate && ./launcher.sh"`
>You'll want to replace `~/git/CherryTreePrivate` with the location of *your* git repository

>**Windows**:
>Create a shortcut file with this as the command:
>`"C:\Program Files\Git\bin\sh.exe" -c "cd /c/Code/MrChrisWeinert/CherryTreePrivate && ./launcher.sh"`
>You'll want to replace  `/c/Code/MrChrisWeinert/CherryTreePrivate` with the location of *your* git repository. Similarly, you may need to replace the location of `sh.exe` if it's different than what I have listed.
>
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
