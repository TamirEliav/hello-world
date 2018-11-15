# hello-world
Learn how to use GutHub :)

This is my first project I'm using Git.
I used to work with Mercurial so far, let's see how it goes... :)

I have cloned the repo in my using MATLAB
Let's try to commit this change!

I managed to commit and push my previous comment to GitHub repo!!
Let's find out if commit was to the LOCAL repo (Git) and the push did the update in GitHub!

To avoid re entering the username / password each time, I'm using the git wrapper for MATLAB.
The git wrapper is using the git installed in my PC to communicate with GitHub, and it has my credinals....
There is another option to solve this (and use the build-in MATLAB interface), which is to use SSH, but that seems to much effort...

I managed to configure the external diff tool bc3 (see here: https://stackoverflow.com/questions/2069490/git-diff-with-beyond-compare)
Let's see if  I can get a diff of the entire project at once!!
I found this link: https://www.scootersoftware.com/vbulletin/showthread.php?7578-git-difftool-load-all-files-into-a-folder-compare-view
It tells how to run full folder comparison (didn't tried yet!)

I now able to run diff on the entire project directory (using dir-diff), this is in my .gitconfig file
[diff]
	tool = bc3
[difftool "bc3"]
	cmd = \"c:/program files (x86)/beyond compare 3/bcompare.exe\" -rro "$REMOTE" "$LOCAL"
	trustExitCode = true
[alias]
	dif= difftool --dir-diff