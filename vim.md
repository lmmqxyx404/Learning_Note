# modes
There are three modes command mode, insert mode, last line mode
number+dd delete multiple lines.

# different keyword value means various effect
G cursor jump to the last line of the file.
number + G cursor jump to the specified line of the file.
gg cursor jump to the first line of the file.

escape(ESC)  alter the mode 
h j k l means different arrows
d$ delete the character from the cursor to the tail of the line.
d0 delete the character from the cursor to the head of the line.
d means delete the content and copy the content to clip
y$ y0 yy the same function like delete, But this command means duplicate
p paste the data on the next line
J connect the cursor with the next line(pay attention that J is capital)
u means discard the former command
ctr+R redo the former command

:q! force quit and discard the chang.
:wq store the change and quit the file
:w filename store the current file to a new file
:r filename read the content and write in the next line

:set nu display the line number
:set nonu hide the line number