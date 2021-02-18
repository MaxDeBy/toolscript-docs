As of the version Beta 1.2, there is a code editor for the AACS Scripts.

This section serves as a quickstart guide for the script editor.

>**Overview:**
>
This is the main scripting window.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom.png)
>In the top left section of the screen, there are two entries: File and View
>>The "File" menu opens the option for common commands in a text editor. The "Save as Template" option will be discussed later.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_2.png)
>
>>The "View" menu gives you three options to adjust certain visual aspects of the editor.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_3.png)


>**Syntax Highlighting:**
>
The script has syntax highlighting as well, highlighting instructions, punctuation, strings, booleans, and numbers for ease of reading.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_4.png)
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_5.png)

>**File Browser:**
>
The editor also features a small file browser which is viewable on the right side. Only scripts can be managed here when a project is linked to the editor.
>
The only viewable elements in the file editor are folders and .aacs files. This enables you to manage multiple script files for a single project while in the code editor. A file can be opened by doubleclicking it.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_6.png)
>>Right-clicking anywhere in the file broswer will reveal additional options.
"New Folder" creates a new folder for organizing script files, "New Script" creates a new script file for instructions, "Delete" deletes a script file or folder, "Open folder" opens the folder where the scripts are stored for the project, and "Refresh" refreshes the file browser to reflect any changes made externally to the script folder.
>>
Script files can be linked and unlinked. Unlinking means that the script file will not be read during compiling. This means that they do not appear in a compiled game. Linking readds the file.
>>
Unlinked files are not deleted. They appear in a grey font to symbolise that they are not linked.
"Link all" links all unlinked files.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_7.png)

>**Templates:**
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_8.png)
Templates are for groups of instructions that you intend to use multiple times. These templates are normal .aacs files.
You can create them via the editor and then click on "Save as Template" in the "File" menu. The script will be saved in a "Templates" folder in the same place as the code editor.
>
Templates can be selected from the dropdown menu on the bottom right by clicking "Use Template". You can also add a placeholder called "%VALUE%" to the script.
>
This placeholder is case-sensitive so it only works if it's written all in capital. Use these for dynamic values that might change per use of the script. Any value can be entered in the input field labeled "Value", and after hitting the "Use Template" button every placeholder is replaced by the specified value.

>**Tool Bar:**
The toolbar next to the "View" menu entry contains two options.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_9.png)
The first option is for commenting out a highlighted section of the script. This currently only works one way, so you can comment out a highlighted part, but not reverse it. Sections that are commented out are ignored when compiling and quick testing.
>
The second option, labeled "Quick Test", executes a highlighted section of instructions in the script. If you don't highlight anything and simply press "Quick Test", then the whole script will be ran.
>
Using quick test requires having a linked project first so that editor is able to find the assets. To link a project, you either have to open a project (.aact) with the editor or open the editor from the Asset Maker. To do that, you have the option in the menu at the top.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_10.png)
This will open the code editor and link a project to it. The actual use of the editor won't change, it will just enable the Quick Test function.
If a project is linked, the name of it will be present in the title of the window in the form of a message saying "(Linked to PROJECT)".
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_11.png)

>**Compiling the Game**
>
The "Compile Game" next to the toolbar will compile a releaseable version of your game. The Data.aact and all linked scripts will be compiled into a Windows Executable (.exe) file in the Exports folder of the AACT directory. If the button "Compile Game" appears green, that means there have been no changes since the last time the game was compiled. Clicking it while it is green will open the folder of the game. If it appears red, that means changes have been made and the game be recompiled. This option is not available if no project is linked.

>**Code Completion**
>
Code Completion allows you to type the name of an instruction into a shortcut window and have the engine automatically complete the instruction in the script for you. This feature can be accessed by typing Shift+Space or CTRL+T.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_12.png)
After pressing either of these keybinds, a list of instructions will appear. Beginning to type the desired instruction will narrow the list of instructions down based on your input. Certain instructions may appear twice if they have a shortened version, such as LoadScene.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_13.png)
Once the correct instruction is highlighted, hit enter to complete the instruction in the script.

>**Pinpointer:**
>
Certain instructions, such as SelectSpot, require X and Y coordinates on the game screen to function as intended. The pinpointer is a tool to allow you to easily find and record these coordinates.
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_14.png)
Moving your cursor over the black area in the pinpointer will display the X and Y coordinates of it as if it were on the game screen. Left clicking the screen will place a SelectSpot instruction in the script with the cursor's coordinates already inputted as parameters. Right clicking will allow you to change the background of the pinpointer.

>**Script Inclusion & Compiler Instructions**
>
Compiler instructions are a special type of instruction that do not affect gameplay, but are integral to creating games with AACT.
>
Currently, only one compiler option has been added: The @Include instruction. It is not necessary to know the technical details of what the compiler does with this instruction, but it is necessary to know what it is used for.
>
This script contains the @Include compiler instruction:
![](https://www.debygames.com/aacs/drex_3__aacs_code_editor_custom_15.png)
Compiler instructions, unlike all other types of instructions, always start with an @ and **do not** end with a semicolon. When an @Include instruction is encountered, the designated script file is loaded and executed at that position. In this case, "Trial1.aacs" would be loaded and executed. This instruction can be placed anywhere in the script, and also works while debugging.
>
The benefit of this is that the 2GB limit of a single script file can be circumvented by loading other scripts, but as a consequence there must be a Prelude.aacs file. This is the first script that will be executed by the compiler, and it is automatically added when a new project file is created. It **must not** be deleted. If it is not present, the game will not compile.