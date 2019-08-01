# git-add-empty-folder
add empty folder into git repository

## Why?

Git can not add a empty folder. and I don't want add any file in it.  
After google, I found this thread.  
https://stackoverflow.com/questions/115983/how-can-i-add-an-empty-directory-to-a-git-repository  
And I write this script. I use it to mantain my rootfs.  
In roorfs, some folder should be empty for mount point. (ex: /dev, /sys, /proc)

## usage

    cd <git-repository>
    git-add-empty-folder <folder1> <folder2> ...

## Warning!!!

`A empty folder that added to git by this method, can not be track.`  
All changes inside the folder will be ignored.  
`If you want add/commit changes, untrack it first.` command show below:

    git rm -r --cached <commited-empty-folder>

after untrack, you can add and commit it.
