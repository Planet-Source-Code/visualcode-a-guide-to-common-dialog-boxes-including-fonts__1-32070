<div align="center">

## A Guide To Common Dialog Boxes Including Fonts


</div>

### Description

This is for anyone who is having trouble with common dialog boxes.

Common Dialogs

I have seen many examples on pscode.com , that have messed up

Common Dialogs , mainly when it comes to the font dialog. This tutorial should teach you all you need to know for common dialogs.

Definitions:

Flags - These are simply options or choices you can use.

Using the flags:

'Setting it for use

CommonDialog.Flags = &H1

'Setting it for use of more than one

CommonDialog.Flags = &H1 Or &H4

Activating Dialogs:

This is simply the code to start up each dialog box.

CommonDialog.ShowColor 'Lets the user pick a color

CommonDialog.ShowFont 'Lets the user pick font

CommonDialog.ShowOpen 'Lets the user pick a file to open

CommonDialog.ShowPrinter 'Shows Printer Setup

CommonDialog.ShowSave 'Lets the user pick a file to save to

ShowColor:

The following are some flags for using the Color dialog boxes.

&H1 - This is one i personally like. This makes the common dialog start showing 	its current color.

&H2 - This starts with the custom color tab open.

&H4 - This makes it so they can not create custom colors.

&H8 - This adds a help button to the dialog.

&H10 - This will reset the common dialog to default.

ShowFont:

The following are some flags for using the Font dialog boxes.

&H1 - Allows the dialog only to list fonts supported by the system.

&H2 - Allows the dialog only to list fonts supported by the printer.

&H3 - Lists the fonts from the two above.

&H4 - Adds a help button.

&H100 - Allows the choices of underline strike thru and color selection.

&H2000 - Shows only font sizes between the min and max.

&H20000 - Allows only fonts that can be scaled.

&H40000 - Allows only true type fonts

Applying to a textbox - For each property you must set it here is an example

that sets it assuming you have &H100 and have a textbox named Text1

Text1.FontName = CommonDialog.FontName

Text1.FontItalic = CommonDialog.FontItalic

Text1.FontBold = CommonDialog.FontBold

Text1.FontStrikethru = CommonDialog.FontStrikethru

Text1.FontUnderline = CommonDialog.FontUnderline

Text1.FontSize = CommonDialog.FontSize

Text1.ForeColor = CommonDialog.Color

ShowOpen And ShowSave:

The following are some flags for using the Open dialog boxes.

&H2 - Forces a warning before overwriting a file

&H8 - Stops default directory from changing

&H10 - Shows help button.

&H200 - This makes it so more than one file can be selected.

&H1000 - This makes it so the file must exist.

&H2000 - This warns the user before creating a new file.

Opening a file:

CommonDialog.ShowOpen

Open CommonDialog.FileName for Input as #1 'Opens The File

Do until Eof(1) "Loops till complete file added to Textbox

Line Input #1, Tmp

Text1.Text = Text1.Text & Tmp

Loop

Close #1 'Closes the file

Saving a file:

CommonDialog.ShowSave

Open CommonDialog.FileName for Output as #1 'Opens The File

Print #1, Text1.Text 'Creates The File

Close #1 'Closes the file

ShowPrinter:

The following are some flags for using the Printer dialog boxes.

&H4 - Makes it so they cant choose to print only selected text.

&H8 - Does not allow you to choose to print certain pages like 4-7.

&H800 - This shows the help button.

&H40 - This shows the print setup dialog box rather than the printer dialog box.

&H100000 - This gets rid of the print to file option box.

Printing Landscape - Printer.Orientation = 2

Printing Portrait - Printer.Orientation = 1

Please vote and leave comments.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |2002-02-23 14:08:44
**By**             |[Visualcode](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/visualcode.md)
**Level**          |Intermediate
**User Rating**    |4.0 (64 globes from 16 users)
**Compatibility**  |VB 6\.0
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__1-43.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[A\_Guide\_To571302232002\.zip](https://github.com/Planet-Source-Code/visualcode-a-guide-to-common-dialog-boxes-including-fonts__1-32070/archive/master.zip)








