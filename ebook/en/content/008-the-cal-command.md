# 008 The-Cal-Command in Linux

If a user wants a quick view of the calendar in the Linux terminal, cal is the command for you. By default, the cal command shows the current month calendar as output. 

cal command is a calendar command in Linux which is used to see the calendar of a specific month or a whole year. 

Syntax: 
cal [ [ month ] year]

The rectangular bracket means it is optional, so if used without an option, it will display a calendar of the current month and year.  

cal : Shows current month calendar on the terminal with the current date highlighted. 

Example commands of cal:

cal -y : Shows the calendar of the complete current year with the current date highlighted.
cal 08 2000 : Shows calendar of selected month and year. 
cal 2018 : Shows the whole calendar of the year. 
cal 2018 | more : But year may not be visible in the same screen use more with cal use spacebar to scroll down. 
cal -3 : Shows calendar of previous, current and next month 

cal -j : Shows the calendar of the current month in the Julian calendar format not in the default Gregorian calendar format. In Julian calendar format, the date does not reset to 1 after every month’s end i.e. after 31st Jan,  Feb will start as 32nd Feb, not as 1st Feb. But in the Gregorian calendar format, the date is reset to 1 after every month’s end i.e after  31st Jan, Feb will start as of 1st Feb.


