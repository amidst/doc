Basic steps for contributing
============================

Here we will explain the basic github commands for modifying the AMIDST
source code and for uploading such changes to the server. Alternatively,
you can watch this
`video-tutorial <https://www.youtube.com/watch?v=HegfZZyQ8u4>`__. The
general scheme to follow for contributing to the AMIDST source code is
shown below:

.. figure:: img/scheme_contributing.png
   :alt: Scheme for contributing to AMIDST toolbox.
   :width: 12cm

   Scheme for contributing to AMIDST toolbox.

[fig:scheme_contributing]

Now we will explain each of these steps and the involved commands.

Clone the repository
--------------------

First, you can download the source code from github using the following
command:

::

   $ git clone https://github.com/amidst/toolbox.git      

Once the download has finished, enter into the downloaded folder:

::

   $ cd toolbox     

Create a new branch from develop 
---------------------------------

All the new development will be done in the branch develop. **Do not
modify the master branch** because it should always contain the source
of the very last release. Thus we change into the develop branch with
the following command:

::

   $ git checkout develop    

The terminal replies with the following output:

::

   Checking out files: 100% (469/469), done.
   Branch develop set up to track remote branch develop from origin.
   Switched to a new branch 'develop'

To avoid overlapping, we advise you to perform all your developments or
changes in a new branch created from develop. The name of this new
branch will be newfeature and it can be created with the following
command

::

   $ git branch newfeature  

We move into the recently created branch:

::

   $ git checkout newfeature  

::

   Switched to branch 'newfeature'

At any moment, we can verify which is the current branch with the
command show below. Make sure that your current branch is always the one
you have created.

::

   $ git branch

Previous command shows a list with all the local branches, being the
current branch the one with the symbol \*, for example:

::

   develop
   master
   * newfeature

The new branch is not yet a remote branch. For uploading it to the
server, we will use the following command:

::

   $ git push --set-upstream origin newfeature

::

   Total 0 (delta 0), reused 0 (delta 0)
   To https://github.com/amidst/toolbox.git
   * [new branch]      newfeature -> newfeature
   Branch newfeature set up to track remote branch newfeature from origin.

Modify the code and upload your changes 
----------------------------------------

As an example, we will simply create a new text file and upload it to
the server. For creating such file run:

::

   $ echo "file to be deleted" > newfile.txt

Now, we have to set the new file as a tracked file, for that purpose:

::

   $ git add newfile.txt 

Which generates the output shown below indicating which of the tracked
files contain changes to be committed

::

   $ git status

that generates the following output:

::

   On branch newfeature
   Your branch is up-to-date with 'origin/newfeature'.
   Changes to be committed:
   (use "git reset HEAD <file>..." to unstage)

   new file:   newfile.txt

   Untracked files:
   (use "git add <file>..." to include in what will be committed)

   ...

| Now we will do a commit including the message “added newfile.txt” with
  the following command:

::

   $ git commit -m "added newfile.txt"

::

   [newfeature f256d1e] added newfile.txt
   1 file changed, 1 insertion(+)
   create mode 100644 newfile.txt

| Finally, we have upload all the changes to the server:

::

   $ git push

Merge the new branch with develop 
----------------------------------

| Until now, the changes done are only present in the branch newfeature.
  However, we should integrate these changes with the develop branch.
  Thus, we first change to the branch develop:

::

   $ git checkout develop

| Now, we will merge both branches:

::

   $ git merge newfeature

| If there is not conflicts, an output similar to the following one will
  be generated:

::

   Updating 20ff914..f256d1e
   Fast-forward
   newfile.txt | 1 +
   1 file changed, 1 insertion(+)
   create mode 100644 newfile.txt

| Finally, we will upload the result of merging both branches to the
  server:

::

   $ git push

Now, if we go to the AMIDST github website
(https://github.com/amidst/toolbox), we can verify that the branch
develop contains the changes in the code:

.. raw:: latex

   \centering

.. figure:: img/merge_result.png
   :alt: View of the result of the contribution in the github website.
   :width: 10cm

   View of the result of the contribution in the github website.

[fig:merge_result]
