Installation Instructions:
Pre-Requisites: You must have Python 3.5.1+ installed to run this script.
Checkout this Repo and a Repo with contains the SC2Hotkeys in the same folder. i.e. https://github.com/Hancho2009/TheCore
If the folder is i.e. C:\ws than it should look like this:
C:\ws\TheCoreConverter\TheCoreRemapper.py
C:\ws\TheCore\seeds\*.SC2Hotkeys

Run the script
Now you go into the TheCoreConverter folder open a command line window and run script with:
python TheCoreRemapper.py ../TheCore

(old)
The workflow is:
   a. Copy and paste the *LM.SC2Hotkeys file into your Starcraft 2 Hotkey folder.
   b. Load up SC2 and edit the layouts in game.
   c. Copy and paste the edited files back into TheCoreConverter directory, overwriting the existing ones.
   d. Run python InGameGUIImport.
   e. Check the log if any hotkeys or commands are missing in the TheCoreSeed.ini and add the ones to the NewDefaults.ini with the default value from sc2 go to d.
   f. Verify that the changes made to TheCoreSeed.ini are accurate.


Brief Overview of Important Files:

- MapDefinitions.ini - This file stores the mappings that are used to convert the USQwerty left-handed medium layouts to the right handed, large and small USQwerty layouts. 

- KeyboardLayouts.ini - This file stores mappings for other keyboard layouts.
   
- TheCoreRemapper.py - This is the script that makes the magic happen. You can run python TheCoreRemapper.py, and it will generate all SC2Hotkeys files, and check them for errors.

- <target folder>/config.ini
Contains Settings for the script

- <target folder>/seeds/
Contains the original seed SC2Hotkeys layouts for USQwerty left-handed medium size. 
It is best the edit this files with the in-game editor if possible (if you do i.e. campaign stuff you proably cannot youse the in-game editor).

- <target folder>/generated/<keyboard layout name>/*.SC2Hotkeys
Here the script generates the different layouts.

- Defaults.ini
This file comes from https://github.com/BeedeBdoo/Sc2HotkeyData

The important thing to note about editing SC2Hotkeys files with the in-game editor is that any overlaps between the edited files and the SC2 Standard hotkey layout will be stripped from the file.
This is why we need to store the default Standard layout hotkeys from the USQwerty keyboard layout in this file, so that it can fill these back in when you run the script.

If in the seed layouts commands/hotkeys are found which are not in the Defaults.ini file than they are added to the Defaults.ini with but with no key.

- reports/Defaults.log
List problems that are detected through the script wich are related to the default hotkeys.

- DifferentDefault.ini
This file comes from https://github.com/BeedeBdoo/Sc2HotkeyData
I cannot remeber - ask BeedeBdoo.

- ConflictChecks.py
This file comes from https://github.com/BeedeBdoo/Sc2HotkeyData
I cannot remeber - ask BeedeBdoo.

- <target folder>/reports/ConflictCheck.log

- SameChecks.py und <target folder>/reports/SameCheck.log
I cannot remeber - ask BeedeBdoo.

- <target folder>/Inheritance.ini und <target_folder>/reports/WrongInheritance.log
- <target folder>/reports/SuggestInheritance.log
