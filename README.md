# explore-bash
Explore using Bash, a key foundation for HPC workflows

The Bash shell scripting language is one of the key tools for high performance computing (HPC) workflows. [Ryan Chadwick's tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) is a great starting point. Please focus on Sections 1-5 to support scripts used in an HPC workflow context. The sections below are meant to complement/extend the tutorial as a set of challenges specific to the needs of HPC workflows to practice using Bash.

## Redirection of standard output/input

Redirecting output from one command to become input for another command is extremely useful and creates a sort of "one-line mini-workflow" where multiple programs are linked together and builds on the [Unix Philosophy] (https://en.wikipedia.org/wiki/Unix_philosophy#Origin). Some examples of this are in [Ryan's Section 3 Input](https://ryanstutorials.net/bash-scripting-tutorial/bash-input.php) and a little more about controlling STDOUT and STDERR is available [in this Linuxize post](https://linuxize.com/post/bash-redirect-stderr-stdout/).

1. Practice redirecting standard output and standard error to sample log files by using `ls` to list a file that you know **does not exist.** In this case, `ls` will generate error messages.
2. In your experimentation with the Unix/Linux commands below, practice linking together Unix/Linux commands with `|` and redirecting output with `>` and `>>` (see example below).

## Interactive command line usage

The Unix/Linux convention of `comamnd [optional_selection <selection_for_option>] REQUIRED_SELECTION` is really important for reading documentation and understanding the building blocks of what can be done in Bash (and any other shell). For the list of Unix/Linux commands below,
1. run each command with the `--help` option (or `man COMMAND`) to access its documentation,
2. provide a snippet of code to run the command with at least one option/flag, and
3. write a sentence or two describing the purpose of the command.
For example, for the `tr` command:
```bash
# Here is an example using tr. This command will replace all characters in a
# stream of standard out that match the first selection with the second selection.
# Note that this example uses | to redirect the standard output of echo to be
# input to tr.
echo a b c | tr b X
```
Here is a list of Unix/Linux commands that often appear in HPC workflows:
+ ls
+ pwd
+ echo
+ touch
+ whoami
+ hostname
+ cat
+ more
+ date
+ env
+ rm (Careful with this one!)

Finally, the following Unix/Linux commands also appear frequently, but they
have so many options and so much extensability that whole books are written 
about them.
+ awk
+ grep
+ sed

## Shell startup

The `~/.bashrc` file is run every time you start a Bash shell. Add an `echo` 
command to your `~/.bashrc` to verify this startup process. Use the `vi` text 
editor, a summary of this editor's commands is available courtesy of the
[Theoretical and Computational Biophysics group at UIUC](https://www.ks.uiuc.edu/Training/Tutorials/Reference/virefcard.pdf).

