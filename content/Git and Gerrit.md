Don't use ``git pull`` -- use ``git fetch`` and ``git merge`` then instead

``git fetch`` retrieves (or "fetches", as the name suggests) commits and changes made to a remote branch to your local repo, but has zero effect on the working tree of your local repo. It is safe and is a way to keep track of the commit history

``git pull`` essentially performs a ``git fetch`` followed by an automatic ``git merge``. In other words, it not only updates your local repo with updates to the remote branch but also merges to your current branch, which may be unsafe (you will lose data)


Local branches saved in .git/refs/heads
Remote-tracking branches saved in .git/refs/remotes