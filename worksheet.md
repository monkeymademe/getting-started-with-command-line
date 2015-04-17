## Getting started with command line

Boot up your Raspberry Pi. Congratulations you have had your fist experiance with command line. Each line or sometimes grouping of lines represents a command the Raspberry Pi has been told to do while booting. Once this stops you have logged into the pi, you are left with the following command prompt.

```shell
  pi@raspberrypi $
```

At this point the system is waiting for your command. We would commenly call this the command prompt.

## Our first commands

### Where are we? (pwd)

Before we start our little journey though command line we need to understand where we are in the system and what folder stucture means.

Write the following command:

```shell
  pwd
```

Print working directory 'pwd' will output the current directory you are working in. This would be:

```shell
  /home/pi
```

This is telling us that in the base system there is a folder called 'home' and in that folder is a folder called 'pi'. Since that is where we are working, if we were to make a file 'pete' the file would be at this location '/home/pi/pete'

### Make a friend (touch)

As we are starting our little journy using command line we are going to need a friend to help us along the way.

```shell
  touch pete
```

Touch is a command that will simply create an empty file. 

### Are we alone (ls)

Type: 

```shell
  ls
```
'ls' will list the directories and files of your current working directory. So now we can see that 'pete' is there.

### Man Up (man)

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

Our command now to see the file size of 'pete' 

```shell
  ls -s 
```
'pete' has a 0 next him meaning there is nothing in the file.

### Give Pete a personality (nano)

Pete does not have much going on so we are going to edit him and give him some text.

```shell
  nano pete
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

Now we have data inside 'pete' can we see if the file size has changed.

```shell
  ls -s
```
There is now a 4 next to 'pete' but what does that mean. Its not very clear. The manual for 'ls' said that '-s' would display the size in blocks. Can we make this human readable change it to something we know like kilobytes or megabytes file sizes?

Checking the manual again you can find the option:

```shell
  -h, --human-readable
      with -l, print sizes in human readable format (e.g., 1K 234M 2G)
```
Lets add that to our 'ls' command

```shell
  ls -sh
```
Now 'pete' says 4.0K (K meaning kilobytes). Thats better!

Why not check out the other options like '-l'. Also take a look at the manual for 'nano'

### Checking whats inside Pete (cat)

A lots happend and we have learned to make pete, edit him and see how big he is. But what about just checking whats inside pete.

The first instinct is to use nano but opening nano just to look inside a file can feel a little bit of overkill. We don't want to edit we just want to look. 

Type: 

```shell
  cat pete
```

cat will concatenate files and print the contents. Since pete simply has text, the output would be 'Hello I am Pete!'

### Making Pete a home (mkdir)

In a computer system its important to keep things orginised. Files in folder properly marked means you can find things easily.

```shell
  mkdir peteshome
```
Hopfully you might guess that 'mkdir' would mean make directory. If you use the 'ls' command you can now see the directory in the list!

### Moving pete in (mv)

We have peteshome directory but petes not in there so lets move him in. 

```shell
  mv pete peteshome/
```
If we check using the 'ls' command we can see pete is infact gone.

The move 'mv' command is constucted like this: 

```shell
  mv [SOURCE] [DESTINATION]
```
For the destination we used the relative path. 

Before we used the command 'pwd' to find out where we are in the system. The path is '/home/pi'. Thats where we are working. Anything we have done so far has been relative to where we are working. We can use the absolute path in our 'mv' command.

```shell
  mv /home/pi/pete /home/pi/peteshome/
```
This does the same as we did before but takes longer to type. We could also mix relative and absolute paths.

```shell
  mv pete /home/pi/peteshome/
  mv /home/pi/pete peteshome/
```
These are all doing the same thing.


------ Drafts Next thins -----

cd into peteshome
Clone pete from the home to the wd
edit pete to sue and move her in
cp pete again to evilpete
rm evilpete
grep?

