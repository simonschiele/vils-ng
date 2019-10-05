# vils-ng

[**_vils-ng_**][1] is a mass renaming script that allows you to rename files with all
the comfort of your favorite editor. It is a small bash rewrite of the original
**_vils_** tool. The desciption for the original script is 'edit an ls' which I
find quite fitting.

I mostly did this rewrite since I'm not a zsh user. I also added a few features
I was missing in the original script, like:
* recursive (for listing and moving)
* dry-run
* control over hidden-files
* confirmation before moving
* ...


## History

The original **_vils_** was written by Oliver Fromme in 2002. It uses zsh and
is an enormous timesaver. You can find the original code of the vils script
~~[here][1]~~.

**Update:** Sadly Olivers original page is not up anymore. So instead I will
link to freshports, there you can find a copy and some information about the
original script: https://www.freshports.org/sysutils/vils/.


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
 -d    dry-run (only print what would be done, do not actually move files)
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

Moving to different directories is supported. If the target directory is not
existing, it will be created.

A combination of -r (recursive) and directly targeting directories as
command-line arguments is not supported at the moment.


## Authors

**Simon Schiele**
    ([<simon.codingmonkey@gmail.com>](mailto:simon.codingmonkey@gmail.com "mailto:simon.codingmonkey@gmail.com"))

[1]: https://github.com/simonschiele/vils-ng
[2]: http://www.secnetix.de/~olli/scripts/Generic-utilities/vils
