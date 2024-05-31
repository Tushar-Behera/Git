## License
[MIT License](LICENSE)

1\. To set User Details :

git config \--global user.name \"xxxxxxxx xxxxxxxx xxxxxxx\" -\> to set
user name git config \--global user.email \"xxxxxxxxx@xxxxxx.com\" -\>
to set user email

2\. Initialize Git On a Folder :

git init ( .git folder will generate which store all records)

\*\*NOte\*\* Some times files are protected or attaching these files to
git may create Problem in that case -

git config \--global \--add safe.directory \'address/path of your
File/repo\'

3\. Check Item inside a Folder :

ls -\> see all unhide File ls -a -\> see all all file including hidden
files

4\. Jump into a Folder :

cd Folder_Name -\> Jump into a particular Folder cd - -\> jump out to
previous Folder

5\. To see what all inside a Folder :

ls Folder_Name -\> to check what inside the Folder

6\. To create/remove a New File :

touch filename.extension -\> create a particular type of File rm
filename.extension -\> remove/delete a particular File

7\. To create/remove Folder :

mkdir Folder_Name -\> create new Folder rm -r Folder_Name -\>
remove/delete a folder

8\. To Check the changes :

git status -\> show all details about the files inside our repo
(untracked/modiffied/staged)

9\. To add files to staging area :

git add filename.extension -\> push particular untracked file in to
staging area git add . \|or\| git add -A -\> move all untracked file
into staging area

10\. Restore from staging area to untracked mode :

git restore \--stage filename.extension -\> move a particular file to
untracked mode git restore \--stage . -\> move all files from staging
area to untracked mode

11\. Finalize files for commit or to save updates on a file :

git commit -m \"Type what are the changes u made\" -\> finalize ur
staging file with date and comment for future use git commit -am \"your
comment \" -\> Directly commit untracked file to commit area

12\. Commit/stage area to untracked area :

git rm \--cached filename.extension -\> directly send the file from
commit/stage area to untracked area git rm -f filename.extension -\> to
force remove that file

13\. To see content inside a file :

cat filename.extension -\> see all the content inside a file

14\. To restore a File content :

restore filename.extension -\> restore the file content before commit

\*\*\*NOTE\*\*\*

\# if \" warning: in the working copy of \'filename.extension\', LF will
be replaced by CRLF the next time Git touches it \" this type of warning
appear while adding files to \"staging area\" to avoid these warning use
\--

==\> git config \--global core.autocrlf false

\*\*\*\*\*\*\*\*\*\*\*\*\*\*

15\. To display all the files committed in the specified commit_id :

git show paste_commit_id_here \--name-only -\> Display commited files
under that commit id

16\. To show all commits :

git log -\> Help to check all commit

17\. To ignore unwanted files during push to github repo

touch .gitignore -\> in this you can paste the name of files and
directory to be ignore

\*\*\*NOTE\*\*\*

in .gitignore if you want to ignore a directory type -\> foldername/ if
you want to ignore particular extension file type -\> \*.extension

18\. To rename or move a file from one directory to another :

git mv -f existing_filename.extension newfilename.extension -\> force
rename a file git mv -f existing_filename.extension foldername/ -\> move
the file to a particular folder

19\. Manupulate with commits :

git commit \--amend -\> add this commit with the previous one using Vim
editor

20\. To create/remove branch :

git branch name_of_new_branch -\> create new branch git branch -d
branch_name -\> delete a particular branch

21\. changing branch :

git checkout branch_name -\> help to change directory

22\. merging one branch to another :

git merge branch_name_to_be_merge -\> first go to particular branch and
put the branch name which to be merged

23\. Link git remote Repository To Working Directory :

git remote add origin your_repository_URL -\> copy the url from tab bar
or repo HTTPS Link

24\. To add ssh Key for read-write from your personal pc with out login
every time :

ssh-keygen -t ed25519 -C \"your_email@example.com\" -\> Help to generate
your ssh key / only press enter on passphrase and agin press enter to
confirm eval \"\$(ssh-agent -s)\" -\> Run your ssh key on background and
give your agent pid ssh-add \~/.ssh/id_ed25519 -\> Add your SSH private
key to the ssh-agent clip \< \~/.ssh/id_ed25519.pub -\> copy your ssh
key to clipboard

\# Now Go to setting \> SSH and GPG keys \> add new key paste the key
and in title put your pc name to verify on which u link the SSH key.

25\. Switch normal HTTPS URL to SSH URL for easy push without repeated
login :

git remote set-url origin SSH_url_of_your_repository -\> link your pc
with remote repo with SSH url git remote -v -\> To check the url for
fetch and push

26\. if error: failed to push some refs to \'your repo url\' :

git pull \--rebase origin master git pull origin master
\--allow-unrelated-histories

if showing : error: cannot pull with rebase: You have unstaged changes.
error: please commit or stash them.

git pull \--rebase \--autostash

27\. How to push on a git repo :

git push origin master -\>push file from local repo to remote repo git
push -u origin master -\> local branch linked with remote branch
Automatically

28\. git clone of remote repo on a local repo :

git clone \"repo link from code section\" -\> on local folder open git
bash and run the command generate that remote repo with exist name on
local git push -\> after cloning, editing , commiting you can directly
push with this command

29\. chek which branch is merge and which one is not :

git branch \--merge -\>show which branch is merge with current branch
git branch \--no-merge -\>show which branch is not merged merged on
current branch
