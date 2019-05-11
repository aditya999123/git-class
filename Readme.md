parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "

# Add these lines in ~/.bashrc file

git config --global push.default current

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com

# https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

# common commands
git init
git add
git commit -a -m
git log --oneline
git pull
git status
git diff
git apply
git merge --squash
git checkout -b
git branch -D

# https://en.wikipedia.org/wiki/Linus_Torvalds
# https://git-scm.com/