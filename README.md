# C64maze
## A 3D maze game written in C

### Intro

This project (distributed with the GPLv.3 license) is a very simple 3D maze originally written for
the Commodore 64 computer, hence the name, and then ported to UNIX. The source code is written in C (with some inline
assembly for the C64 version) and it is meant to be compiled with the cc65 compiler or gcc with the SDL2 library.

The game started as an exercise in high resolution graphics on the C64 and was inspired to those old 3D maze games in BASIC that were popular at the time. However, the C language is much faster than BASIC and one can do some pretty nice things. Some routines are tweaked in assembly for better performances.

![m1](https://user-images.githubusercontent.com/104295046/223793251-fd31bf2d-c048-4f62-8caf-35294391ea2a.gif)
<img width="1440" alt="m2" src="https://user-images.githubusercontent.com/104295046/223793321-4bcf33b3-1f22-45d5-85b1-ce97471d9091.png">


The goal of the game is to find the exit of the maze in the shortest possible amount of time. The entrance of the maze is changed randomly each time the game is played. You can have a look at the maze map, but beware! Each time this is done, a penalty of 30s is applied:

<img width="1440" alt="m3" src="https://user-images.githubusercontent.com/104295046/223793744-59f28bd6-9165-4ee8-ac6f-ba60b1c371a4.png">

You should explore the maze to find the exit:

![m5](https://user-images.githubusercontent.com/104295046/223793888-edf6e629-f8b1-469f-a3b2-3d22717d617c.gif)

And once you find your way through it, you will know how much time you needed:

![m9](https://user-images.githubusercontent.com/104295046/223794168-a2b2ab4d-27d5-4bfe-b1bc-b0eff8c51447.gif)

![m10](https://user-images.githubusercontent.com/104295046/223794336-8777975c-783d-498a-a1e6-e9bdb1932d21.gif)

Here is a screenshot of the game running on a Unix machine:

![UNIX PORT 1st version](./screenshots/unix_first.jpg "you must see it")

### Music
The music is a 3-part reduction for the SID of J.S. Bach's "little" fugue in G minor, BWV578. Hommage to Wendy Carlos. The music driver is fully interrupt-driven and it is also written in C.

### How to build the game
To build the game for UNIX\GNU linux install SDL2 library and type:
~~~
make PLATFORM=UNIX
~~~

To build for the Commodore 64, make sure you have CC65 installed and type:
~~~
make PLATFORM=C64
~~~
