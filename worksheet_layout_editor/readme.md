Notes:

LOADING A DEFAULT WORKSHEET TEMPLATE:

Start Page Layout Editor  (AKA Worksheet Layout Editor)
open pagelayout_default.kicad_wks
save as: yourname.kicad_wks in the root of your project

GOTCHA!!!
  Save As DOES NOT reopen the document with the new name in the root of the project.
SO:
open yourname.kicad_wks in the root of your project

Leave the page layout editor window open and use your text editor to open the file "yourname.kicad_wks in the root of your project directory.

This plain text file is composed of single line records that described the worksheet layout and add parameters that are automatically filled in from information contained in your project.

Open Eeschema. 
Click on the "File" menu and choose "Page Settings...".
Loof at the bottom of the dialog for the line "Page layout description file".
Click "Browse".
Navigate to your project directory and select "yourname.kicad_wks"
Click "OK".

You should immediately see that the sheet has changed from a blank page to one that has borders and a worksheet information block in the lower right corner.

MODIFYING A DEFAULT WORKSHEET TEMPLATE:

Information contained in the File|Page Settings... menu are interpolated into the worksheet automatically according to a set of place holders that are called "format symbols" (!?) these are in fact template variables and are interpolated automatically by KiCAD when you complete these details in the Page Settings dialog of eeschema. 

The publically documented variables are:

