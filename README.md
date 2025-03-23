# fyer_deck
The STLs and build/install instrcutions for the Fyerdeck cyberdeck project!

I do plan to make insructional videos for assembly and software installation to include here, but I'll do that when the design is finalized!

# Purpose
I like computers. Alot. I've always wanted to build my own mobile computing system, kind of like a laptop but more unique. I then discovered Cyberdecks and thought they were the coolest thing ever. Especially with their tie into Cyberpunk media, I was instantly hooked. While existing Cyberdeck designs typically utilize SBCs like rasbperry pis, I wanted mine to be a powerhouse that I could use as my "personal laptop" but  with it being in a more interesting form factor. Then Framework entered the picture with its user upgradable and servicable laptop. I immediatly saw the potential to use Framework parts to build a kick ass cyber deck. Framework also released designs for not only their parts, but a 3d printable case for their components that would turn the framework13 mainboard into a desktop. This was so close to what I wanted!

Finally I decided this was they year I would do it (especially with their ryzen ai 9 mainboard shipping this april). So I immediatly pre-ordered that board, and started looking at existing designs, and finalized my requirements for what I wanted my Cyberdeck to do. I came up with the following list of requirements the deisgn would need to accomodate.

## need to haves:
1. The framework battery would need to be included, this allows me to utilize the framework mainboard USB-C charging capability.
2. The framework powerbutton would need to be incorporated, this would allow me to utilize fingerprint authentication within the system.
3. the framework trackpad needs to be included. While I will primarily use it with a regular desktop mouse, the ability to use it without a desk is a must.
4. I want to use my desktop keyboard with it. I have a particular layout that I love to use (alice).
5. It needs to have a small (8 inches or less diagonally) screen on it for diagnostics and boot sequence monitoring.
6. the primary screen setup will be AR glasses or VR goggles with camera passthrough.

## Nice to haves:
1. the framework speakers so I don't *need* to use headphones if I don't want to.
2. the framework audio port so I can use 3.5mm audio gear with it.

# Design
Luckily the design for the bottom parts of the case that accomodate all of my need to haves and all of my nice to haves was already done by @ShadowChaser on printables! (https://www.printables.com/model/1051364-framework-13-mainboard-case-with-battery).

With that part done all I needed to do was figure out a top cover design that would integrate the trackpad and powerbutton, as well as have plenty of ventilation for the CPU cooler, since the bottom intake would be obstructed by the battery. I did find a good top mount design that had plenty of ventilation, but did not encorporate the trackpad and powerbutton, so it would need to be tweaked. I can't find the original designer for the one I used anymore (sorry if that's you, please open an issue with this repo with how you'd like to be attributed as well as a link to your design so I can give you credit!).

I took this deign and put in in tinker cad. I then 3d modeled the trackpad and powerbutton. After trying a few ideas I setteled on having the trackpad be flush with the top cover, and supported from the back. Ideally you'd probably want to glue, tape, or magnetically mount it in place to make sure it doesn't fall out the top, but I'm still experimenting with that.

I just designed some holding struts for the trackpad, then turned the trackpad into a hole and combined the shapes.

The track pad is mounted at 90 degrees relative to how you'd expect it to be mounted based on laptop design... we'll get to that.

From the get go I wanted this cyberdeck to be versitile. I wanted to use it on a desktop and place it where ever I wanted on that desktop, as well as on the go just in my lap. To facilitate this I dediced that a mounting frame that can hold both the keybaord and cyberdeck would be the best solution then trying to integrate them in to a permanently affixed single piece. This would allow me to make a few modification to the case design as possilbe, while still giving me extreme flexibility. Since the trackpad and powerbutton are top mounted on the case design stacking the keyboard ontop of it vertically was out of the question. So the design locks onto the side of the keyboard with magnets (this will require alittle drilling into the keyboard case, but very minor drilling). and secures around the cyberdeck case itself, so it will kind of resemble a T when fully assembled in the mobile configuration. This puts the trackpad in the natrual position for right handed peopl, and if you are left handed, just drill the magnets into the other side of the keyboard and mount it there! This is why the track pad is rotated 90 degrees, to allow for the "vertical" mounting position. An enhancement would be if the trackpad mount were a separate part that magnetically attaches so you could rotate it at will, but I haven't really looked into that at all.

I'm still in the prototyping phase (I'm close to a final design, so the current ones shouldn't change much) so expect changes and for it to not quite fit perfectly yet. Again I'm working on it. 

I also have not figured out the screen solution yet, so bear with me, I'm still working on it!

# Assembly
1. print out all the parts, starting with the battery tray.
2. assemble the battery tray halves together (it may require a hammer to get the halves flush, since they are friction fit it will be a VERY tight fit, this is expected.
3. put the framework speaker modules in the slots for them. At the moment they are just friction fit, so I might design some kind of locking mechanism for them, but haven't had to yet. 
4. make sure the connector is run about where it will pop through the motherboard tray.
5. put the battery in the battery tray, making sure the connector is about where it needs to be to pop through the motherboard tray.
6. assemble the motherboard tray halves together (the same way you did the battery tray) If some of the support blocks are getting in the way just break them off with pliers. (I'll try to clean up the stls to avoid these once the design is finalized).
7. place the mainboard in the mainboard tray and line it up with the battery tray (do not snap them together yet).
8. connect the power lead from the battery to the port on the mainboard.
9. connect the speakers to the mainboard (this is a PITA and you will need tweezers for it)
10. insert your framework usbc connector modules, this locks the motherboard to the tray.
11. snap the battery tray to the mainboard tray (this may take some finagling, its a tight fit.
12. place the audo port into the mainboard tray and connect the ribbon cable to the mainboard. (you may need to glue it down, still working on a solution to that)
13. insert the assembly pins into the holes for them on the mainboard tray
14. install wifi antenna solution, there are two possible solutions for this:
	1. glue in two rpsma to mini pcie wifi card adapter pigtails into the holes on the top of the motherboard tray and run the cables to where the wifi card gets installed.
	2. stick the framework wifi antenna (screwed into the bottom of the display pannel on the framework 13 laptop) to the case somewhere, and run the wires through the small hole by where the wifi card will be inserted.
15. connect the wifi antenna wires (either from the adapters or from the framework wifi antenna) to the wifi card and insert the card into the mini pcie slot.
16. place the connector guard over the wires and screw the protector, and wifi card into the mainboard case with the screw provided by framework. (note this is a metal screw going into plactic... screw carefull and don't over tighten. Just tight enough to hold it.)
17. take the powerbutton and powerbutton bracket and line them up.
18. secure them together (either with screws and nuts or with glue)
19. figure out where you want the power button monted on the center piece of the top cover
20. run the power button lead through a ventilation hole near where you want it mounted, and glue the power button bracket to the top cover.
21. glue the powerbutton cover over top of the power button (this is optional, but should make it harder to aciddentally hit when its in a bag.
22. connect the ribbon cables for the trackpad and power button to the trackpad itslef.
23. insert the trackpad into the center piece of the top cover, being carful to run the ribbon cables through to they can used.
24. connect the power button ribbon cable to the power button lead on the back side of the center piece of the top cover.
25. connect the center piece of the top cover to the motherboard tray, being carful to make sure the ribbon cables aren't touching the cooling fan.
26. connect the trackpad ribbon cable to the slot for it on the mainboard.
27. connect the other two top cover pannels to the mainboard tray, being carful to not put too much stress on the ribbon cables when you press them down.
28. you're DONE enjoy your cyber deck 


# Software
I'm a linux guy, so this will primarlily focus on setting Linux up for this.

1. install your linux distro of choice normally (you will likely need to connect to a monitor for this, or the xreal glasses can act as a normal monitor as well.)
2. once you have that installed and configured how you would like it, decide if you'll be using AR glasses (like the xreals), a VR headset (like the quest 3), or both as your primary monitor solution.
3. If you choose the Xreals, congrats you're done!

## VR goggles/fully 3d envrionment
If you want to use a fully 3d envrionment for your cyberdeck (like I do) there's a bit more setup. You can just install immeresed on both the headset, and the cyber deck and use virtual "monitors" if you'd like, that setup is pretty easy, you just need a way to generate virtual monitors. This can be done with either Xrandr on x11 based desktop sessions, or if you use Plasma sessions you can create 1920x1080@60hz monitors using the screen sharing desktop portal. There's a python DBUS script that you can use to spin those up before you launch immersed. I have that covered in my AR/VR hacking environment repository that you can check out if you'd like.

the primary software I use for this is StardustXR (https://stardustxr.org)

Otherwise, the whole purpose of VR/AR compute environments is to not be constraied by archaeic limitations like "monitors", right? For that we need a bit more setup, but its sick!

1. install an XR run time like wivrn, monado, or steamVR. Personally I think wivrn is the best for this project since it supports camera passthrough by default.
2. pair your VR headset with your XR runtime (varies but all projects have pretty decent documentation to set this up).
3. Now we need to setup stardust to do what we want. In order for passthrough to work as expected we need the dev branches of stardust. 
4. stardust is written in rust, and we'll need to compile it so install the following packages:
	1. rustup
	2. cmake
	3. fontconfig
	4. dlopen
	5. openxr-loader
	6. EGL+GLES (I didn't need to explicetly install this, but since its listed in stardust's repo I wanted to inclue it)
	7. GLX+Xlib (I didn't need to explicetly install this, but since its listed in stardust's repo I wanted to inclue it)
5. create a folder to keep your stardust files in `mkdir stardust && cd stardust`
6. clone the dev branches of the needed stardust repositories
	1. `git clone -b dev https://github.com/StardustXR/server.git`
	2. `git clone -b dev https://github.com/StardustXR/flatland.git`
	3. `git clone -b dev https://github.com/StardustXR/protostar.git`
	4. `git clone -b dev https://github.com/StardustXR/non-spatial-input.git`
7. compile the binaries we need
	1. `cd server; cargo build --release || cargo build --release` (for this one the first time building sometimes fails for me, but usually just re-running the build command works)
	2. `cd ../flatland; cargo build --release`
	3. `cd ../protostar; cargo build --release`
	4. `cd ../non-spatial-input/manifold; cargo build --release`
	5. `cd ../simular; cargo build --release`
8. (optional) copy the resulting binaries to somewhere on your $PATH, to make running them easier.
9. make a stardust startup script.
	1. `mkdir ~/.config/stardust`
	2. `nano ~/.config/startudst/startup`
	3. paste the following script into the editor, and edit the paths to accurately reflect where you either compiled the binaries, or saved them to your path:

```
#!/bin/bash

xwayland-satellite :69 &
DISPLAY=:69 path/to/your/hexagon_launcher & /path/to/your/flatland &

```
10. save and close the editor
11. make that script executable! `chmod +x ~/.config/stardust/startup`
12. you're done! (kinda) 

With all of that done you can now start up stardust in your XR runtime. You can do this by starting your runtime (like wivrn) and connecting your headset to it. Once you're connected you can either launch stardustxr with wivrn using the custom executable option, or just run the stardust binary you compiled.
This will launch stardust and autmatically run that startup script we created. You should be able to see a hexagon shaped button (you may need to lean back a bit to see it) you can use either controller grip buttons or hand tracking to grab it and move it around you.

Once you have the hexagon button placed where you want it, simply tape it with hand tracking or with your controller trigger to open the launcher menu. This will lay out all of your installed applications in a hexagon grid. To launch a program simply grab the hexagon icon for the program and drop it where you want tne new window to spawn.
Mouse inputs can be handled by controller or hand tracking, but keyboard isn't working!  Let's fix that.

Remember that non-spatial-input repo you downloaded and compiled manifold and simular from? Here's where that comes into play! To capture your mouse and keyboard simply run manifold and pipe it into simular! `/path/to/your/manifold | /path/to/your/simular` 
Now a black window should open on your normal desktop environment! click inside of it to capture your inputs. Keyboard and mouse inputs are sent to which ever application you're currently looking at, though mouse inputs are currently broken. This is being worked on. 

