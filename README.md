test-main
=========
Our master project:

    git clone git@github.com:mathias-tervo/test-main.git

Project we want as a git subtree:

    git clone git@github.com:mathias-tervo/test-subtree.git



Add the project we want to be a subtree as a remote with the ``-f`` flag

    git remote add -f test-subtree git@github.com:mathias-tervo/test-subtree.git


Add the project as a git subtree:

    git subtree add --prefix src/subtree test-subtree master

Explanation syntax:

    git subtree add --prefix path/to/destination remote-name branch

Getting changes to the subtree:

   git fetch test-subtree master

   git subtree pull --prefix src/subtree/ test-subtree master

If the above pull results in an error, try:

   git pull -X subtree=src/subtree test-subtree master




