# vils-ng

**vils-ng** is a mass renaming script that allows you to rename files with all
the comfort of your favorite editor. It is a small bash rewrite of the original
**_vils_** tool. I also added a few features I was missing in the original script.


## History

The original **_vils_** was written by Oliver Fromme in 2002. It uses zsh and is an
enormous timesaver. You can find the original code of the vils script
[here][1].


## Usage

```
  vils-ng [options] [file1] [file2] [file3] [...]

    -h help
    -r recursive
    -v verbose
    -x use $VISUAL instead of $EDITOR

  Example usage:

    rename files in actual dir:
    > vils-ng

    rename files in actual dir and all subdirs:
    > vils-ng -r

    rename specific files:
    > vils-ng testfile1.txt testfile2.mkv testdir/testfile3.log

```


## Authors

**Simon Schiele** (mailto:[<simon.codingmonkey@gmail.com>](mailto:simon.codingmonkey@gmail.com "mailto:simon.codingmonkey@gmail.com"))

  [1]: http://www.secnetix.de/~olli/scripts/Generic-utilities/vils
