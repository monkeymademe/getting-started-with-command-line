## Getting started with command line

Boot up your Raspberry Pi. Congratulations you have had your fist experiance with command line. Each line or sometimes grouping of lines represents a command the Raspberry Pi has been told to do while booting. Once this stops you have logged into the pi, you are left with the following command prompt.

```shell
  pi@raspberrypi $
```

At this point the system is waiting for your command. We would commenly call this the command prompt.

## Our first commands

### Where are we?

Before we start our little journey though command line we need to understand where we are in the system and what folder stucture means.

Write the following command:

'''shell
  pwd
'''

Print working directory (pwd) will output the current directory you are working in. This would be:

'''shell
  /home/pi
'''

This is telling us that in the base system there is a folder called 'home' and in that folder is a folder called 'pi'. Since that is where we are working, if we were to make a file 'pete.txt' the file would be at this location '/home/pi/pete.txt'

### Make a friend 

As we are starting our little journy using command line we are going to need a friend to help us along the way.

```shell
  pi@raspberrypi $ touch pete.txt
```

Touch is a command that will simply create an empty file. 

### Give Pete a personality 

Pete does not have much going on so we are going to edit him and give him some text to save.

