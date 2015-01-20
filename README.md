Pundler
=======

Python bundler-alike alternative to virtualenv.

For now works only with PyPI packages.
Git, svn and so on support planned to support a bit later.

Now this is expirement.

Commands
--------

`pundler [install]` will install files from freezed.txt file.

`pundler upgrade` will recreate freezed.txt from requirements.txt (Now conservative. TODO make real upgrade)

`pundler fixate` installs site costumization for current python


How to play with it
-------------------

    git clone git@github.com:Deepwalker/pundler.git
    python pundler/pundler.py fixate

    cd testproject
    python -m pundler upgrade

Pundler will create directory `Pundledir` and file `freezed.txt`.


DONE
----
- install by freezed.txt
- on update rewrite freezed.txt
- on launch check if freezed.txt is in touch with requirements.txt
- Search through hierarchy upward
- tie packages to python version.
- package scripts
- upgrade must lookup PyPI for new version


TODO
----
- ! write cause to freezed.txt then we can check unneeded requirements without installed packages
- ! add vcs support
- ? tie packages only where we need this (C extensions, py2 without __pycache__ support)
- ? bundle distlib
- ? bundle pkg_resources