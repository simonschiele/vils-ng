# vils-ng

**_vils-ng_** is a mass renaming script that allows you to rename files with all
the comfort of your favorite editor. It is a small bash rewrite of the original
**_vils_** tool. I also added a few features I was missing in the original
script.


## History

The original **_vils_** was written by Oliver Fromme in 2002. It uses zsh and
is an enormous timesaver. You can find the original code of the vils script
[here][2].


## Usage

vils-ng will simply use the editor configured via the environment-variable
**$EDITOR** to let you edit a file-listing and will rename the files accordingly
after you close the editor.

Options and usage examples can be found in the help-message:


```bash
simon@cpad ~ > vils-ng -h
vils-ng [options] [file1] [file2] [file3] [...]

Mass-renaming with your favorite editor!

Options:
 -h    help
 -r    recursive
 -v    verbose
 -D    debug
 -x    use x11 editor

Examples:

 # rename files in current dir:
 > vils-ng

 # rename specific files:
 > vils-ng testfile1.txt testfile2.mkv testdir/testfile3.log

 # rename files in current dir and all subdirs:
 > vils-ng -r

simon@cpad ~ >
```

If started with the '-x' option, the GUI-editor from the **$VISUAL** environment-
variable will be used.

If not configured the normal editor will fallback to /usr/bin/vi, while VISUAL
will fallback to _/usr/bin/gvim_.


## Authors

**Simon Schiele**
    ([<simon.codingmonkey@gmail.com>](mailto:simon.codingmonkey@gmail.com "mailto:simon.codingmonkey@gmail.com"))

[2]: http://www.secnetix.de/~olli/scripts/Generic-utilities/vils
