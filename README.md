**vils-ng**
=====================

**vils-ng** is a mass renaming script that allows you to rename files with all the comfort of your favorite editor. It is a small bash rewrite of the original *vils* tool. I also added a few features I was missing in the original script.

----------

History
---------

The original *vils* was written by Oliver Fromme in 2002. It uses zsh and is an enormous timesaver. You can find the original code of the vils script [here][1].  
I rewrote the script in Bash 'cause I wanted to use it everywhere without installing zsh as a dependency. Also I was missing some features like recurisve usage. I shamelessly copied the idea and even used a few lines from the original script, so all the fame goes to Oliver Fromme who wrote the fantastic original.

----------

Usage
---------------

    vils-ng [options] [file1] [file2] [file3] [...]

    -h help  
    -r recursive  
    -v verbose  

Example usage:

    rename files in actual dir:
    > vils-ng

    rename files in actual dir and all subdirs:
    > vils-ng -r

    rename specific files:
    > vils-ng testfile1.txt testfile2.mkv testdir/testfile3.log

You can select your editor of choice via environment variables. \$RENAME_EDITOR, $EDITOR or a failover to /usr/bin/vi will be used (in this order).

----------

## Authors

**Simon Schiele**

 * [http://simon.psaux.de/][2]
 * [https://github.com/simonschiele/][3]
 * mailto:[<simon.codingmonkey@googlemail.com>](mailto:simon.codingmonkey@googlemail.com "mailto:simon.codingmonkey@googlemail.com").


  [1]: http://www.secnetix.de/~olli/scripts/Generic-utilities/vils
  [2]: http://simon.psaux.de/
  [3]: https://github.com/simonschiele/
