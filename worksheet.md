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

```shell
  pwd
```

Print working directory 'pwd' will output the current directory you are working in. This would be:

```shell
  /home/pi
```

This is telling us that in the base system there is a folder called 'home' and in that folder is a folder called 'pi'. Since that is where we are working, if we were to make a file 'pete.txt' the file would be at this location '/home/pi/pete.txt'

### Make a friend 

As we are starting our little journy using command line we are going to need a friend to help us along the way.

```shell
  touch pete.txt
```

Touch is a command that will simply create an empty file. 

### Are we alone

Type: 

```shell
  ls
```
'ls' will list the directories and files of your current working directory. So now we can see that 'pete.txt' is there.

### Man Up

A question you might be asking yourself is: Ok 'ls' looks nice! Can I see how big the files are?

Type the following:

```shell
  man ls
```
'man' meaning manual will open the instuctions for the command written after 'man'. 'man ls' would give me the manual for command 'ls'

We want to look at the option that looks like this:

```shell
  -s , --size
      print the allocated size of each file, in blocks
```

Our command now to see the file size of 'pete.txt' 

```shell
  ls -s 
```
'pete.txt' has a 0 next him meaning there is nothing in the file.

### Give Pete a personality 

Pete does not have much going on so we are going to edit him and give him some text.

```shell
  nano pete.txt
```

Nano is a text editing program that works in command line.

Type at the top of the screen 

```shell
  Hello I am pete!
```

At the bottom of the screen there are some short cut tips on how to use nano. 

Press 'CTRL' + X to start to exit the file 

The bottom of the screen will change and ask if we want to save. Press Y for yes.

Then press 'Enter' to confirm we are writing the file.

Now we are out of Nano back into the command prompt.

### Don't forget what we have learned.

Now we have data inside 'pete.txt' can we see if the file size has changed.

```shell
  ls -s
```
There is now a 4 next to 'pete.txt' but what does that mean. Its not very clear. The manual for 'ls' said that '-s' would display the size in blocks. Can we make this human readable change it to something we know like kilobytes or megabytes file sizes?

Checking the manual again you can find the option:

```shell
  -h, --human-readable
      with -l, print sizes in human readable format (e.g., 1K 234M 2G)
```
Lets add that to our 'ls' command

```shell
  ls -sh
```
Now pete.txt says 4.0K (K meaning kilobytes)

Why not check out the other options like '-l'. Also take a look at the manual for 'nano'

