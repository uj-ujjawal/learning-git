# learning-git

learning git and it's feature, a dummy project

> I am a dummy, don't take me seriously.

## how to edit commit message after it has been push

To change a typo in a Git commit message after it has been pushed, you will need to use the "git rebase" command.

### Here's how to do it

Clone the repository locally if you haven't already done so.
Checkout the branch that contains the commit you want to modify.
Use the command `git rebase -i HEAD~n` where n is the number of commits you want to go back.
In the editor that opens, find the line with the commit you want to edit and change "pick" to "edit".
Save and close the editor.
Use the command `git commit --amend` to edit the commit message.
Use the command "git rebase --continue" to continue the rebase process.
Force push the updated branch to the remote repository using "git push -f".

Note: Be aware that rewriting Git history can cause problems if other people have already pulled the commits you're rewriting. So, use caution when using this method and make sure to coordinate with others on your team before proceeding.

Thanks

## verified commit

- install  gpg tool
- after instaling add this to the path (linux/mac)
`export GPG_TTY=$(tty)` and/or add that to your ~/.bashrc or ˜/.bash_profile

Now,

run `gpg --full-generate-key`

choose the following option

- 1
- 4096
- Default (just press enter)

Fill the personal detail likes

- Name
- Email id
- comment (if you want otherwise just press enter)
- Then Secure your gpg key with passpharse

After that run

- `gpg --list-secret-keys --keyid-format=long`
- `[gpg --armor --export [3AA5C34371567BD2]` Your case it will be different

Then Copy your GPG key, beginning with -----BEGIN PGP PUBLIC KEY BLOCK----- and ending with -----END PGP PUBLIC KEY BLOCK-----

Resource: <https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key>

### For troubleshooting, two things to first try

    run gpg --version, and make sure you have GnuPG version 2+ (not version 1) installed
    run echo "test" | gpg --clearsign, to make sure gpg itself is working

## verified commit with ssh

`ls -al ~/.ssh` to check existing ssh keys if it says doesn't exist means you don't have any keyes

### lets start with new->

`ssh-keygen -t ed25519 -C "your_email@example.com"` replace email with your github email

`eval "$(ssh-agent -s)"` it will start ssh in background

## Testing Start

SSH Testing phase 1.
CHECKING SIGNING COMMIT
SSH Testing phase 2.
CHECKING SIGNING COMMIT
