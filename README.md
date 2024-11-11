## Builds
[Build Bot](https://buildbot.flathub.org/#/apps/com.github.louis77.tuner)

## Assets
_io.elementary.BaseApp_ latest version is [juno-23.08](https://github.com/flathub/io.elementary.BaseApp)

## Patches
_Windows.vala_ has a patch to remove the _adjust_theme_ calls which currently do not work in the flatpak.
If _Windows.vala_ is modified, regenerate the patch.

To create a patch, duplicate the subject code into two directories in a structure that mirrors that of the project. In this case _Window.vala_ goes into _a/src/Widgets_ and _b/src/Widgets_. Make the changes you want to apply in _Window.vala_ in _b_. 
From the directory root create a diff: _diff -ur a b > Windows.vala.patch_
To test, drop into _a_ and run _patch -p1 -i ../Windows.vala.patch_, then back up and rerun the diff - there should be no differences.