# Guide to writing this proposal

This FET proposal will be written collaboratively. This document presents the
process for editing the files jointly.

## The files

The proposal is found in the `*.tex` files in this repository. The main LaTeX
file is `proposal.tex`. It uses the LaTeX class
[LaTeX-proposal](https://github.com/KWARC/LaTeX-proposal/) developed by Michael
Kohlhase.

The reference files for the project are the ones located in this online
repository. They are tracked with the [git](http://git-scm.com/) system.

The general content of the project is divided by sections, corresponding to the
FET-Open template: [excellence.tex](excellence.tex), [impact.tex](impact.tex)
and [implementation.tex](implementation.tex).
For these files, you can either edit them online (see more info below) or
coordinate with Christian via email.

Parts of the project are organized in individual files: CVs of participants
(`CVs/firstname.name.tex`), work packages (`WorkPackages/WP.name.tex`) and
partners (`Participants/participant.name.tex`).
There are appropriate templates. Please copy either the template (or someone
else's file) to create the files that "belong" to you. Either add them online or
send them directly to Pierre by email.

It is impossible to compile the files directly because the reliance on the local
version of `LaTeX-proposal`. Solutions to that problem:
- Use the provided makefile and run `make -B draft` and `make -B final`.
- For Windows users, there is a batch file `windows-script.bat` that you can run
  with `cmd.exe` directly in the proposal directory.
- In a terminal, set the environment variable `TEXINPUTS` (see file
  `debian-env.sh` and adapt it to your environment). It is then possible to
  compile using `pdflatex draft` and `pdflatex final`.
- Install the provided `LaTeX-proposal` files in your LaTeX path and run
  `texhash`.

*Summary:* take care of the files that are specific to you or your site and
 coordinate with Christian for the body of the project.


## Editing the proposal

The proposal is a regular LaTeX file. So any equation, etc, will work fine.

A few recommendations:
- Avoid lists as they take a lot of space.
- If you need a list anyway, use the `compactitem` environment instead of
  `itemize`. The LaTeX package [paralist](http://ctan.org/pkg/paralist) has
  other useful environments.
- Split your paragraphs into lines of about 100 characters maximum. This allows
  an easier collaborative editing as it is based on line by line content.


## Using git

If you feel somehow that editing a collaborative document by sending emails
around is not the best use of technology, feel free to read further. Else, you
may ignore this.
The idea to manage the proposal writing via GitHub comes from the
[OpenDreamKit](http://opendreamkit.org/) project that successfully submitted a
FET infrastructure proposal.

### Crash course on git

git is a software that keeps track of text files in a storage area called a
repository. A repository is, for instance,
https://github.com/pdebuyl-lab/fet-open-promane-2015

To register a change to the file `FILENAME` (think of the "save" button), you
use `git commit FILENAME` and enter a short message about your changes. This
operations updates the "recorded" state of the file. You can commit several
files at once.

The list of operations ("commit log") is recorded
https://github.com/pdebuyl-lab/fet-open-promane-2015/commits/master
Any past state of the repository can be retrieved.

### Ways to operate on the git repository

To edit the files, there are several options:
1. login on https://github.com/, navigate to a file in
   https://github.com/pdebuyl-lab/fet-open-promane-2015 and clic the pen
   icon. when done editing, go to the bottom of the page and clic "commit".
2. use GUI of github at https://desktop.github.com/ : open the program, enter
   your login details and select "clone" to have a local version of the files on
   your computer. use the github program to "commit" your changes and then
   "publish" them so that the changes are made available to others.
3. use git in a command line. First, login to the website and "fork" (clic on
   the fork button at https://github.com/pdebuyl-lab/fet-open-promane-2015) the
   main repository. open a terminal and type

       git clone git@github.com:YOURUSERNAME/fet-open-promane-2015
   
   You may start working
