# explore-bash
Explore using Bash, a key foundation for HPC workflows

The Bash shell scripting language is one of the key tools for high performance computing (HPC) workflows. [Ryan Chadwick's tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) is a great starting point. The excercise below is meant to complement/extend the tutorial as a set of challenges specific to the needs of HPC workflows to practice using Bash.

## Interactive command line usage

The Unix/Linux convention of `comamnd [optional_selection <selection_for_option>] REQUIRED_SELECTION` is really important for reading documentation and understanding the building blocks of what can be done in Bash (and any other shell) and builds on the [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy#Origin). For the list of Unix/Linux commands below,
1. run each comamnd with the `--help` option to access its documentation,
2. provide a snippet of code to run the command with at least one option/flag, and
3. write a sentence or two describing the purpose of the command.
For example, for the `tr` command:
```bash
# Here is an example using tr. This command will replace all characters in a
# stream of standard out that match the first selection with the second selection.
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

Finally, the following Unix/Linux commands appear frequently, but they are
extremely powerful and have so many options and so much extensability that
whole books are written about them.
+ awk
+ grep
+ sed
