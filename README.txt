Pre-Requisites: You must have Python 3.5.1+ installed to run this script.

Brief Overview of Important Files:

- MapDefinitions.ini - This file stores the mappings that are used to convert the USQwerty left-handed medium layouts to the right handed, large and small USQwerty layouts. 

- KeyboardLayouts.ini - This file stores mappings for other keyboard layouts.
   
- TheCoreRemapper.py - This is the script that makes the magic happen. You can run python TheCoreRemapper.py, and it will generate all SC2Hotkeys files, and check them for errors.

-<target_folder>/config.ini

-<target folder>/seeds/*.SC2Hotkeys
-<target folder>/generated/<keyboard layout name>/*.SC2Hotkeys 

-Defaults.ini und <target folder>/reports/defaults.log
-DifferentDefault.ini

-ConflictChecks.py und <target folder>/reports/ConflictCheck.log
-SameChecks.py und <target folder>/reports/SameCheck.log

-<target_folder>/Inheritance.ini und <target_folder>/reports/WrongInheritance.log
-<target folder>/reports/SuggestInheritance.log

The important thing to note about editing files with the in-game editor is that any overlaps between the edited files and the SC2 Standard hotkey layout will be stripped from the file.
This is why Default.ini stores the default Standard layout hotkeys from the USQwerty keyboard layout, so that it can fill these back in when you run the TheCoreRemapper.py.

(The following is old)
The workflow is:
   a. Copy and paste the *LM.SC2Hotkeys file into your Starcraft 2 Hotkey folder.
   b. Load up SC2 and edit the layouts in game.
   c. Copy and paste the edited files back into TheCoreConverter directory, overwriting the existing ones.
   d. Run python InGameGUIImport.
   e. Check the log if any hotkeys or commands are missing in the TheCoreSeed.ini and add the ones to the NewDefaults.ini with the default value from sc2 go to d.
   f. Verify that the changes made to TheCoreSeed.ini are accurate.
