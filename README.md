# learning-git

learning git and it's feature, a dummy project

## I am a dummy, don't take me seriously.


## how to edit commit message after it has been push

To change a typo in a Git commit message after it has been pushed, you will need to use the "git rebase" command.

Here's how to do it:

Clone the repository locally if you haven't already done so.
Checkout the branch that contains the commit you want to modify.
Use the command "git rebase -i HEAD~n" where n is the number of commits you want to go back.
In the editor that opens, find the line with the commit you want to edit and change "pick" to "edit".
Save and close the editor.
Use the command "git commit --amend" to edit the commit message.
Use the command "git rebase --continue" to continue the rebase process.
Force push the updated branch to the remote repository using "git push -f".

Note: Be aware that rewriting Git history can cause problems if other people have already pulled the commits you're rewriting. So, use caution when using this method and make sure to coordinate with others on your team before proceeding.


Thanks 

## testing verified commit 