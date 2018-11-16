**TITLE:** Workflow Documentation for KiCAD Page Layout Editor with Template Set

**VERSION:** _This documentation was created using KiCAD 5.0.0 (stable)

**CITATIONS:**

1. [KiCAD 5.0.0-stable Documentation for Page Layout Editor](http://docs.kicad-pcb.org/5.0.0/) (Choose your language to go to documentation)
2. [Source Code (Build Generated) for Page Layout Editor Lexer] (https://kicad-info.s3.dualstack.us-west-2.amazonaws.com/original/2X/4/44dbc845022890b690366f35acbd3e98a4ece286.h) (Thanks to @bobc for link!)
3. [Comments in KiCAD 5.0 page_layout_default_description.cpp] (https://github.com/KiCad/kicad-source-mirror/blob/5.0/common/page_layout/page_layout_default_description.cpp)

**DATE:** _07-OCT-2018_

**AUTHOR:** Brig Young, github.com/sonophoto

# OPENING AND EDITING THE DEFAULT TEMPLATE:

1. Start Page Layout Editor in the main KiCAD window (AKA Worksheet Layout Editor)
2. Choose menu item `File | Open...`
3. In the dialog box navigate to the location of your KiCAD installation's shared data, on Linux/unix systems this will likely be `/usr/local/share/kicad/template` or `/usr/share/kicad/template`; on windows systems the path will likely be `C:\[TODO]`
4. Select the file named: `pagelayout_default.kicad_wks`
5. Click the `Open` button
6. Choose menu item `File | Save As...`
7. Examine the selected directory in the file browser and verify that it is the root of your project's directory. If not you will need to use the file browser to navigate to the root of your project. (The root of your project is the location of your project's .pro file)
8. In the text field at the top of the pop-up window enter a new name such as `your_project_name.kicad_wks`
9. Click the `Save` button at the bottom of the dialog box.

* **HEAD UP!** `Save As...` DOES NOT reopen the document so that you can edit it (like you might expect), you must open it manually after saving it:

10. Choose menu item `File | Open...`
11. In the pop-up window navigate to the root of your project and open the `.kicad_wks` file you saved in step 9.

Now you have a default worksheet template opened and ready to edit.

**Aside Note:** If you want to dive right into the text file go to the main KiCAD window and right click on the file's name in the project tree and select `Edit in a Text Editor`. You can setup KiCAD to use your preferred editor such as vim, emacs, code, notetab etc. by selecting the menu item `Preferences | Set Text Editor...` in the main KiCAD window. This plain text file is composed of single line records that described the worksheet layout and names variables that are automatically filled in from information contained in each schematic. The Projects main `.pro` file contains the reference that specifies which worksheet template to use, and each schematic can have metadata records that will populate the worksheet template for each individual schematic. [Working with the text file directly](https://github.com/Sonophoto/KiCAD_docs/blob/master/worksheet_template_editor/TextFormat.md)

# POPULATE A SCHEMATIC WITH METADATA
1. Start **Eeschema** from the main KiCAD window.
2. Select `File | Page Settings...`
3. Using the dialog box, enter any information and/or comments you want displayed in the title box of the schematic

The metadata should appear in the worksheet of Eeschema immediately when you click the `Ok` button.

# MODIFYING A DEFAULT WORKSHEET TEMPLATE:

Information contained in the `File | Page Settings...` menu are interpolated into the worksheet automatically according to a set of place holders that are called "format symbols" (!?) these are in fact template variables and are interpolated automatically by KiCAD after you populate them in the `File | Page Settings...` of Eeschema. The checkbox item `Export to other sheets` can be used to propogate a variable to all sheets in a project. This could be useful for the Company name or the Revision variables for example.

## The documented variables are:

### Metadata for the design

`%T` Title

`%Y` Company name

`%D` Date

`%R` Revision

### Metadata for the document.:

`%P` File system's path to this sheet.

`%F` Filename

`%K` KiCad version

`%S` Sheet number

`%N` Number of sheets in project

`%Z` Paper format name (A4, USLetter …)

### Additional Information:

`%%` Escapes the `'%'`, prints a `'%'` in your worksheet.

`%Cx` Comment (x = 0 to 9 to identify the comment)
    
There are no special variables for Approvals, Authors, Copyright Notices, Patent Numbers, etc. This information must be added to each document as static text or you can use the comment variables to add them to the project.




