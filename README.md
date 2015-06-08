T3rminator
==========

A GTK 3+/VTE 0.3x/Python 3 fork of Terminator
---------------------------------------------

T3rminator is a GTK3+/VTE 0.3x/Python 3 fork of [Terminator](https://launchpad.net/terminator), based on the [terminator-gtk3](https://code.launchpad.net/~gnome-terminator/terminator/gtk3) trunk with additional fixes for Python 3 and **lots of removed features**. The removed features is the main point of this fork, since upstream probably wouldn't support the removal of these features that I don't use anyway, but they really slow down the development of the port. For example, ``dbus`` support is completely absent from [PyGI](https://wiki.gnome.org/action/show/Projects/PyGObject), so this mean no ``remotinator`` support. And there is lots of deprecated widgets (including transparency, sadly D:) that upstream still tries to support in their port to GTK3+, and I removed then for good. Going ahead I removed some unused code, trying to clean-up the code so we can later try to re-added features.

The code in this repository is **highly experimental**, so it may crash, eat your cat, launch a nuclear missile, etc. Since I don't have lots of time to play with this code anymore (it isn't even synched with lastest upstream changes), I am opening it so it may be useful for someone. I do want to remove even more code and, in the end, create a small program with features that is important to me (like window stacking) without including bloat (plugin support, for example), but this depends more of will to work/free time then anything else.

How to install
--------------

You will need Python 3, ``python-gobject`` and ``python-configobj`` installed in your system. ``python-configobj`` may be installed using ``pip``, but ``python-gobject`` no, you need to manually [compile it](https://python-gtk-3-tutorial.readthedocs.org/en/latest/install.html). You will probably want to install this package from your distro repository. [In this page](https://wiki.gnome.org/action/show/Projects/PyGObject) you can find how this package is called in some common distributions. In Arch Linux you can use the following command to install the dependencies:

    # pacman -Sy python-gobject python-configobj

After that, just clone this repository and run ``terminator`` with Python 3:

    $ python3 terminator

If everything is alright the main screen from ``terminator`` should run.
