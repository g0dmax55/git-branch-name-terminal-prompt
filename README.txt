#git-branch-name-terminal-prompt
function parse_git_branch() {                                                                                                                                        
    git branch 2> /dev/null | sed -n -e 's/^\* \(.*\)/-[\1]-/p'
}

PROMPT=$'${debian_chroot:+($debian_chroot)}${VIRTUAL_ENV:+($(basename $VIRTUAL_ENV))}%B%F{red}%n@%m%b%F{reset}:%B%F{blue}%~%b%F{reset}%(#.#.$(parse_git_branch))$ '

#Default-kali-prompt
PROMPT=$'${debian_chroot:+($debian_chroot)}${VIRTUAL_ENV:+($(basename $VIRTUAL_ENV))}%B%F{red}%n@%m%b%F{reset}:%B%F{blue}%~%b%F{reset}%(#.#.$) '
