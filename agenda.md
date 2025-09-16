# It's my agenda as a way to learn linux.
> <mark>'So we will start from start...'</mark> 

#### I've learnt the basic topics as `ls, mkdir, mkcd, awk, vim, rm, cp, mv, less...` etc.
---
This file not about what I have to learn, it's about the *agenda of my learning* path and also progress *tracking tool*.
So here's the agenda as is:
1. Everyday within 1 hour, try to remember what I have learnt previous time, use commands, maybe make some additional notes.
2. Then I need to be concentrated, so the next step is planning what I have to learn this day(just write here), ***minimum 2 topics***.
3. This step I will start to learn concentrated to topic's subject.
4. Then go to the [OverTheWire](https://overthewire.org/wargames/bandit/), and just complete at least 5 levels, and feel free).
5. After the game, I need to summarize all the information learnt, so I will write down it to this file.
---
## Example of written agenda:

## Agenda

### Commands
1. [x] `grep`.
2. [ ] `find`. 

### Concepts
1. [ ] [What is kernel: basics](https://youtu.be/pJ607nDnyE0?si=RgQBad1dsE2nl3TW).
2. [ ] [10 powerfull tips](https://youtu.be/AvGv2PmBwqA?si=tHG8s6275AAFK7vi).

*Write `x` inside of [] brackets to show the task is completed.*

## Summary
1. `grep` is really powerfull text finder that searches the patterns within file's content.
2. `find` ...
3. `tee` ...
4. `where` ...

...

---

> So just note yourself...

---

***09.09.2025 : 2:05PM***

*The awk needs file to be __NOT EMPTY__ .*

### Commands

1. [x] `grep`- content seacrhing tool.
2. [x] `find`- file searching and action tool. 

### Concepts

1. [x] [What is kernel: basics](https://youtu.be/pJ607nDnyE0?si=RgQBad1dsE2nl3TW).
2. [x] [10 powerfull tips](https://youtu.be/AvGv2PmBwqA?si=tHG8s6275AAFK7vi).

*Write `x` inside of [] brackets to show the task is completed.*

1. Linux - it isn't an operating system, by itself, Linux is a Kernel, and the Kernel is not an operating system, the Kernel by itself doesn't provide any utilities, libraries, compilers, that's all the work of **Distributions**.
2. Why linux called GNU/Linux? Because GNU was created without a Kernel, and Linux was like a puzzle in the whole system calles GNU(GNU's not Unix), because without a GNU, Linux is just a Kernel, and the GNU is like a layer that provides the instruments to work with Kernel.

*Also: GNU is like basic set of software that needed to work with files, and system at all*

*On the other hand: Distro is a set of **Additional software** that layered upon the GNU, that layered upon Kernel.*

3. I've got a plenty of advices, such as a "How to start learn linux really smoothly, without burning out, and just having much fun", I must enjoy some community: (LearnLinuxTV)[https://community.learnlinux.tv/], note everythingI know, embrace the process, test other distributions. 

---

***10.09.2025 : 7:35PM***

## Commands

1. [x] `tee`- that's simple command to distribute the input of other commands into **stdin, stdout, and file specified**.
2. [x] `whereis` - is a handy tool to search the mans, binaries, or source files of command.

## Concepts

1. [x] (/dev/null)[https://youtu.be/TA5CsDv64c4?si=NNCDC2ZoyE3DymGW].
2. [x] (Block and Symbolic Devices)[https://youtu.be/aOgOoqEmWjg?si=_hx183zxgl6GSl5C]

### /dev/null
1. /dev is a dir with all virtual and physical devies listed.
2. virtual devices - devices that are not really exist physically, but can act in system like them.
3. All the info written in /dev/null is will be vanished.
4. It's also called *bitbucket or black hole*.
5. /dev/null can be used to turn on the *Silent Mode* in every command.

### Block and Sybolic Devices
1. Block devices are usually referencing to the slower devices as **SSD, HDD, some virtual devices also**, but the Symbolic(Character) devices are referencing to a faster devices as **Keyboard, RAM, NVME drives**.

***11.09.2025 : 11:22AM***

## Commands 

1. [x] `which`- locates binaries(or aliases) related paths. 
2. [x] `command -v`- slightly seems like `which`, but can output even line of `~/.zshrc or ~/.bashrc`.
3. [x] `type`- name information, similar to which, command -v, etc.
4. [x] `locate`-tool that helps to locate file faster than `find`, but found can be outdated.

## Concepts

1. [x] (Streams as *>, >>, stdout, stdin, stderr*)[https://youtu.be/zMKacHGuIHI?si=-Sr8NIlsKMx5yENc].

## Summary 

1. Example of `stderr` can be when you type `sudo apt install codeas`(that's stdin BTW), this command will output 'E: Unable to locate package codeas', and that's **stderr**.
2. `echo $?` gives us a return code of previous command.
3. Designation numbers of them:
    - `stdin`=0.
    - `stout`=1.
    - `stderr`=2.

    So, if you want to send the input or output or errors to some file silently, you can just make such thing:
    ```Bash
        ls ldeslefk 2> /dev/null
    ```
    - that will redirect the **stderr** messages in black hole(/dev/null).

    And the same thing with **stdin, stdout**.
4. By the way, if you're using default redirection mark `>`, it's takes all **stdout** into a file after him everytime, even if **stderr** printed in terminal.
5. > stands for writing to the file, and also overwriting the existing text.
6. >> stands for 'append' to the file.

***15.09.2025 : 10:40AM***

## Commands 

1. [x] `sort`- is a tool that sorts `stdout` by different props.
2. [x] `uniq`- is a tool that reports or deletes the duplication lines from `stdout`. 
3. [x] `wc`- really useful for know the file words, lines, bytes, characters count in handy format.
4. [x] `sed`- this command is great for searching and substituting the text in the file, accepts substitute expression like in vim.

## Concepts

1. [x] (std)[https://youtu.be/YYz8Y_UBrvw?si=aMK-jap4nJo9mpvQ].
2. [x] (Named pipes)[https://youtu.be/hthUAYVqors?si=cE98z0ADXHjLoIDX].
3. [x] (Confused engineering conceps)[https://youtu.be/z5lpHsl8qQ4?si=lEYRJYmBMIr7GsFs].

## Summary 

1. < is used for input redirection, means only the way of opening the file, whether it shell(<) or the command (e.g. cat file.txt).

2. Named pipes are useful when u need to create half-duplex mode of communicaion, u can create pipe with `mkfifo` command, and make the basic communication with it, like `cat mypipe` - for reading, `echo hello > mypipe` - for writing.

3. Encoding is a process of substituting the characters, for the purpose of data transmition. In that way URL can replace spaces with '%20'. In that way word "Like" can be encoded in three different forms - Binary, Base64, Hexadecimal. - **ENCODING IS REVERSIBLE**

4. Hashing is a process that converts data to irreversible form, using hashing algorithms. - **HASHING IS IRREVERSIBLE** 

5. Encryption is a process that converts(hides) data, until u apply a key, e.g. chipher. - **ENCRYPION IS REVERSABLE**

***16.09.25 : 04:39PM***

## Commands

1. [x]  `cut`- command that allows to output the specified bytes, characters, or fields from file.
2. [x]  `diff`- shows differences in files, very handy for code.
3. [x]  `comm`- allows to compare sorted files.

## TODO

1. [x] to make the network indoors.
2. [x] to install GIMP.
3. [ ] to find out how to make copymanager or wayland.

## Summary 

I haven't cope with third TODO task, but it still good result

***17.09.25 : ______***

## Commands

1. [ ]  `join`-

## Concepts


