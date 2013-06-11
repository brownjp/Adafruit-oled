Adafruit-oled
=============

Code to drive Adafruit's 128x32 and 128x64 i2c oleds on a Raspberry Pi.  This code is for C++ development.  It is available for personal use, but not released for any type of commercial use.  I have made efforts to credit folks that have their portions of code in this, such as Gertboard code, Adafruit 5x7 font, snipets of Gordon's code base as well.

The structure of this code base on my Pi is as follows:

[any dir]/common/*.c *.cpp *.h files

[any dir]/gertboard/gb_common.c gb_common.h

[any dir]/oled/*.c *.cpp *.h files

I have used codeblocks to compile this code, and to compile, include all *.c and *.cpp files into a project.  I have included an example main.cpp I use on the Raspberry Pi.  It displays the CPU temp and also an IP address if available.  To have the Raspberry Pi display this info on power up:
   sudo nano /etc/rc.local
   
add the following lines before exit 0 command:

   /home/pi/ipaddr
   
   /home/pi/cpusn
   
   /home/pi/[program file dir]/oled/Release/oled
   
Add these files to the ~/ directory:

   cpusn
   cputemp
   ipaddr
   
I may not have the most effecient way of reading these, but this was the quick and dirty way of finding the IP addr, temp, and SN, and then put in a text file.

I am sure I have left out a lot of important stuff, but as good programmers it does us good to do some code surfing to find the answers.

John
