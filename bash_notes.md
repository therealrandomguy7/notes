### BASH
[question & answers](https://www.unix.com/unix-for-beginners-questions-and-answers/) for __beginners__

#### How is bash invoked?
- it is invoked differently for login & non-login shells
- the [mindmap](./minder/bash-invocation-notes.minder) is present

#### Setting up bashrc

- [ascii art](https://fossbytes.com/linux-distribution-logo-ascii-art-terminal/)
    - used in _rc_ files with comments
    - achieved by manual editing, and using `sed` (notes below)

- understand `$-` in the be 1st case statement
    - [search for symbols](http://symbolhound.com/)
    - useful info on variables in [bash hackers wiki](https://wiki.bash-hackers.org/start)

- set `shopt` parameters, [reference](https://www.gnu.org/software/bash/manual/html_node/The-Shopt-Builtin.html)
    - `autocd`
    - `cdspell` - correct minor spelling mistakes in directory names

- [parameter expansion](https://wiki.bash-hackers.org/syntax/pe#simple_usage) to understand the use of the chroot env variable

- Modifying `$PS1` value
    - [using tput](https://linux.101hacks.com/ps1-examples/prompt-color-using-tput/)
    - [escape chars](https://linux.101hacks.com/ps1-examples/cutomize-your-prompt/)
    - [tput codes, ascii values](https://wiki.bash-hackers.org/scripting/terminalcodes?s[]=tput)
    - [some other uses for setting colours](http://tldp.org/HOWTO/Bash-Prompt-HOWTO/x329.html)

- adding aliases for ease of use

#### Editing ASCII art using `sed`
- used figlet to get the required ASCII art
- used sed, to append with comments in the beginning
- adding to the respective _rc_ file using sed
- although, this can be done in multiple line, doing it one line is awesome!
- [unix stackexchange link](https://unix.stackexchange.com/questions/568407/how-to-insert-multi-line-text-which-is-the-o-p-from-a-command-to-the-beginning) of the post

#### Using sed to put ASCII patterns intro rc files
 - to be done

#### Mindmaps
- `bash invocation` [mindmap](./minder/bash-invocation-notes.minder)
- notes on `sed` [mindmap](./minder/sed-notes.minder)
- `bash basics` [mindmap](./minder/bash-basics-notes.minder)
- `bashrc notes` [mindmap](./minder/bashrc-notes.minder)
    - __PARAMETER EXPANSION__ [mindmap](./minder/bashrc-notes-parameter-expansion.minder)
    - __setting up prompt__ [mindmap](./minder/bashrc-notes-setting-up-prompt.minder)