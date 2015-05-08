Oatmeal lets you quickly see what's running on each of your workspaces (also known as "virtual desktops") and switch to the workspace you want. For example, upon invoking Oatmeal, you might see this:

.. image:: http://img36.imageshack.us/img36/3502/oatmealexample.png
  :target: http://img36.imageshack.us/img36/3502/oatmealexample.png
  :alt: Screenshot of the switcher
  :width: 300px
  :align: center

You could then hit the "c" key to jump to the workspace with Thunderbird in it or "e" to jump to the one with Firefox.

Oatmeal uses ``wmctrl`` to get a list of open windows, an image-viewing program such as ``xli`` to display a representation of your workspaces, and ``X11::Protocol`` to get keyboard input, so it should work on a variety of platforms.

Installation
============================================================

* Ensure you have each of the Perl modules listed at the top of the program. You can install modules with ``sudo cpan install X11::Protocol`` or ``sudo cpanm X11::Protocol`` (using cpanminus_) or your package manager.
* Edit Oatmeal's parameters as necessary. Notice that the default definition of ``view_output`` uses ``xli`` to display the bitmap, so you should either install ``xli`` or find an alternative.
* Say ``perl oatmeal test`` to try out the display. Press any key not included in ``@workspace_keys`` to dismiss the switcher without changing workspaces.
* Ensure Oatmeal is automatically launched each time you log in, and assign a key combination to the command ``pkill -USR1 oatmeal`` (which causes Oatmeal to display the switcher and wait for a keypress). How to do these things depends on your desktop. In KDE 4, take a look at the "Startup and Shutdown" and "Shortcuts and Gestures" panels in System Settings.

Motivation
============================================================

One thing I missed when I switched from GNOME 2 to KDE 4 in late 2011 was an indicator of which programs are running in which workspace. Whenever the user switches workspaces, GNOME 2 briefly displays on screen the layout of one's workspaces, the outlines of each window in each workspace, and an icon in each window representing the program it belongs to. KDE, on the other hand, displays only a layout, with no indication of what's running where.

This is a grotesque hack!
============================================================

Patches welcome.

Why is it called Oatmeal?
============================================================

I dunno. Backronyms welcome.

License
============================================================

Oatmeal is copyright 2012–2015 Kodi Arfer.

Oatmeal is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

Oatmeal is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the `GNU General Public License`_ for more details.

.. _cpanminus: https://github.com/miyagawa/cpanminus
.. _ImageMagick: http://www.imagemagick.org/
.. _`GNU General Public License`: http://www.gnu.org/licenses/
