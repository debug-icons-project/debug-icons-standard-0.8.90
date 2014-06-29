debug-icons-oxygen-4
====================

The goal of the debug-icons-project is to create icon themes which can be used to a) debug and modify existing icon themes, b) check the correct usage of icons in UIs/DEs and c) as a basis for new themes. In addition, the project provides a set of Python scripts which can be used to easily modify, extend and update the icon themes.

The variant "debug-icons-oxygen-4" is based on the Oxygen icon theme for KDE 4 and covers all its icons (except flags and animations). Since the official site currently offline (June 2014), the latest Oxygen version was downloaded from: http://download.kde.org/stable/4.13.2/src/oxygen-icons-4.13.2.tar.xz

Usage
-----

###Installation
Copy the folder 'debug-icons-standard-0.8.90' and all the containing files to the corresponding icon folder of you system. For KDE this might for example be '~/.kde/share/icons'. Another default location is '/usr/share/icons'. After copying the data, the new icon theme should show up in the system settings (in KDE: System Settings -> Common Appearance and Behavior -> Application Appearance -> Icons).

If you also want to update and extend the icon theme from time to time, you have two possibilities: either run the script(s) and copy the updated icon theme to one of the aforementioned places or b) make a symlink in one of those places which links to wherever you put the whole debug-icons project folder. This way you don't have to copy the updated themes every time, but it is very likely that you still have to switch the icons theme or flush the icon cache. Otherwise new or updated icons might not be recognized.

###Fall-back theme for another icon theme
If you are developing a new icon theme or want to extend an existing icon theme it might make sense to set debug-icons as a fallback icon of your icon theme. This way, all missing icons of your theme will be replaced with icons from the debug-icons theme. This makes finding the correct filenames of missing icons much easier.

In order to do so add the debug-icons theme to your theme file. At the top of the file there should be a line similar to:

    Inherits=gnome,hicolor

Change this line to

    Inherits=debug-icons,gnome,hicolor

Contact
---------
For bug reports please open an issue on the project page: https://github.com/debug-icons-project/debug-icons-standard-0.8.90

If you have questions, comments or requests you can also send me an email: jnmllr42 (at) gmail.com

License
-----------
The icon theme and all corresponding files are licensed under the Creative Common Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license (see http://creativecommons.org/licenses/by-sa/4.0/ ). 
