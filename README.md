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

I took this deign and put in in tinker cad. I then 3d modeled the trackpad and powerbutton. After trying a few ideas I settled on having the trackpad be flush with the top cover, and supported from the back. I added small tracks for the bottom wings of the trackpad to slot into, and blank spaced for the top wings. You can still glue it in if you would like for more security, but I haven't found that to be necessary, its held in place pretty well just with the bottom wing tracks.

I just designed some holding struts for the trackpad, then turned the trackpad into a hole and combined the shapes.

The track pad is mounted at 90 degrees relative to how you'd expect it to be mounted based on laptop design... we'll get to that.

From the get go I wanted this cyberdeck to be versitile. I wanted to use it on a desktop and place it where ever I wanted on that desktop, as well as on the go just in my lap. To facilitate this I decided that a mounting frame that can hold both the keyboard and cyberdeck would be a better solution than trying to integrate them in to a permanently affixed single piece. This would allow me to make as few modifications to the case design as possible, while still giving me extreme flexibility. Since the trackpad and powerbutton are top mounted on the case design stacking the keyboard ontop of it vertically was out of the question. So the design locks onto the side of the keyboard with magnets I simply super glued some magnets onto the side and bottom of the keyboard. This does mean that you need to use the built in feet of the keyboard otherwise it slides around a bit, but that's not a bad trade off since most people use the keyboard feet anyways. I also decided to magnetically mount the cyberdeck. When in the mounting dock it will kind of resemble a T when fully assembled in the mobile configuration. This puts the trackpad in the natrual position for right handed peopl, and if you are left handed, just glue the magnets onto the other side of the keyboard and mount it there! This is why the track pad is rotated 90 degrees, to allow for the "vertical" mounting position. An enhancement would be if the trackpad mount were a separate part that magnetically attaches so you could rotate it at will, but I haven't really found the need or use case to do this. If you need a left handed trackpad setup, simply mirror the mounting dock.

I'm still figuring out the powerbutton solution. The current one just glues into the top cover itself, but since its not supported from the back pressing the button is kind of a PITA. Ideally I'd have some kinds of pocket for the button to slide into that you could slide it into, but I haven't really settled on a design for that I like yet. 

I knew from the get go that I wanted a small screen mounted to the cyberdeck that would be used to enter the LUKs password if the drive is encrypted (which it should be since this is a mobile computer). After doing way too much research into the eDP port on the framework mainboard and trying to adapt it to one of those cheap USB pc monitor screens you can get from ali express I finally just bit the bullet and settled for a small 5 inch HDMI and USB-C powered screen. I already had a small dongle that plugged into a USB-C port and provided a USB-A port and HDMI port. To ensure the screen only took one of my I/O ports on the framework mainboard. I also really wanted the screen to fold over the top cover to make sure it didn't get scratched up in a bag. So I needed a hinge solution. Luckily Framework also had me covered there. I just use one of the original screen hinges. I hollowed out a little slot in the top cover to glue one half of the hinge into. The screen I ended up buying on amazon had a little metal bracket and a mounting hole on the back of the screen, so I just needed to find a way to attach the bracket to the hinge. After trying a few direct attachment idea I settled on a small 3d printed box that you can fill with glue or epoxy. The bot fits around the part of the hinge that the screen should connect to, and the bracket that came with the screen, then you just fill the box with glue or epoxy and let it cure. the result is a fairly secure connection between the hinge and the screen bracket.

In the original case design the battery is just kinda exposed on the back. This is fine for stationary use cases, but I wanted to make sure the battery was at least somewhat protected while in a bag. I thought about doing some kind of snap in battery door, but I'm not good at 3d modeling so that proved to be a bit tricky for my skill set. Instead I just added some holes for magnets to the bottom of the case, and modeled a door that would have magnets in the same spot. Now we have a magnetically attacking battery door, that still allows the battery to breath for cooling. The downside to this approach is the magnetic fields produced by the door when its attached interfere with the magnetic fields used by the mounting dock. My solution is to just take the door off when I'm using the mounting dock, but it could probably be solved by either carefully choosing the polarity of the magnets, moving the magnets for the door, or doing the snap in door idea. This solution works good enough for me, but if you come up with a mod that works better please let me know!

# Assembly
1. print out all the STLs in the fyerdeck_files folder, you will need 10 connector pins(though printing extras is a good idea because they are easy lose). I personally used PETG for all the parts except the connector pins which I printed in PLA.
2. Slot the battery tray halves together, and the motherboard tray halves together.
3. insert the speakers and battery into the battery tray, making sure to run the cables about where they are going to go.
4. line the motherboard tray and the battery tray up, there might be one support pylon from the original motherboard tray design that you need to snap off, I can't remember if I removed that or not, so check for interference.
5. push the battery and speaker cables up through the motherboard tray holes where needed, then press the motherboard tray into the battery tray. Note it may take considerable force to mate them properly.
6. Test fit the magnets into the magnet holes. I tried to account for some tolerance, but some are still a bit tight. If needed use needle nose pliers, or a round file to expand the magnet holes.
7. glue the magnets into the magnet holes. I just used off the shelf super glue and that seems to work pretty well.
8. insert the connector pins into the motherboard tray
9. Mount the wifi card and ssd to the framework mainboard.
10. place the mainboard in the motherboard tray, connecting the battery and speaker cables as you do.
11. insert the exapnsion I/O cards into the motherboard tray, and connect them to the USB-C interfaces on the mainboard, this is how the mainboard is retained in the motherboard tray.
12. plug the Audio board into the mainboard, and screw it into the motherboard tray using the original screws from the framework laptop.
13. take the top cover where the screen needs to mount and insert the longer part of the framework hinge into the hollowed out slot. 
14. adjust where it sits to suit your preferance.
15. fill the slot with dual part epoxy and let it sit for 24 hours to ensure it's fully cured. (TIP: you can hotglue the hinge part in place to hold it where you want it before you fill it with epoxy to make sure it doesn't move)
16. slide the hinge connector box around the shorter side of the framework hinge. slide the bracket that came with the screen into the hinge connector box, and fill the box with glue. Dual part epoxy would probably be a good idea here, but I was lazy and just used hot glue, and that seems to have worked well enough.
17. glue the power button to the metal bracket it comes with at the connection point where the screws would have held them together.
18. glue the metal bracket on the power button to the inside of the center top pannel, lining up the power button with the hole.
19. inser the bottom wings of the trackpad into the slots in the center part of the top pannel, and push backwards letting the top wings come to rest inside the holes in the side cut out for them.
20. connect the power button to the trackpad via the normal cable.
21. plug the trackpad into the main board, making sure to line it up in such a way that it bends as little as possible.
22. press the center panel into the connector pins on the motherboard tray.
23. (optional) attach the antenna mounts for the wifi card to the holes provided in the top panel and plug the antennas into the wifi card
24. press the panel that covers the side of the main board with the wifi card into the connector pins
25. press the last top cover panel into the connector pins. and screw the screen onto the mounting bracket.
26. attach the USB-C -> USB-A + HDMI adapter to the back of the screen (I just used double sided tape).
27. connect the screen to the USB-A and HDMI ports of the dongle, using very short cables if possible.
28. connect the dongle to one of the USB-C ports on the mainboard, I used a right angle adapter to make sure it didn't interfere with the hinge.
29. match the cyber deck up with the keyboard dock, and make sure the magnets are facing the right way. 
30. test fig the magnets, again the holes may need some expanding.
31. double check the magnet direction multiple times! 
32. glue the magnets into the keyboard dock.
33. glue the magnets onto your keyboard, making sure to line them up and again checking multiple times for magnet direction.
34. let the glue dry and you're done!


# Software
I'm a linux guy, so this will primarlily focus on setting Linux up for this.

1. install your linux distro of choice normally, installing on the small diagnostic screen may be possible, but it'll also be a PITA, so maybe connect a normal monitor, or use the Xreal Glasses.
2. once you have that installed and configured how you would like it, decide if you'll be using AR glasses (like the xreals), a VR headset (like the quest 3), or both as your primary monitor solution.
3. If you choose the Xreals, congrats you're done!

## VR goggles/fully 3d envrionment
If you want to use a fully 3d envrionment for your cyberdeck (like I do) there's a bit more setup. You can just install immeresed on both the headset, and the cyber deck and use virtual "monitors" if you'd like, that setup is pretty easy, you just need a way to generate virtual monitors. This can be done with either Xrandr on x11 based desktop sessions, or if you use Plasma sessions you can create 1920x1080@60hz monitors using the screen sharing desktop portal. There's a python DBUS script that you can use to spin those up before you launch immersed. I have that covered in my AR/VR hacking environment repository that you can check out if you'd like.

the primary software I use for this is StardustXR (https://stardustxr.org)

The whole purpose of VR/AR compute environments is to not be constrained by archaic limitations like "monitors", right? For that we need a bit more setup, but its sick!

1. install an XR run time like wivrn, monado, or steamVR. Personally I think wivrn is the best for this project since it supports camera pass-through by default.
2. pair your VR headset with your XR runtime (varies but all projects have pretty decent documentation to set this up).
3. Now we need to setup stardust to do what we want. In order for pass-through to work as expected we need the dev branches of stardust. 
4. stardust is written in rust, and we'll need to compile it so install the following packages:
	1. rustup
	2. cmake
	3. fontconfig
	4. dlopen
	5. openxr-loader
	6. EGL+GLES (I didn't need to explicitly install this, but since its listed in stardust's repo I wanted to include it)
	7. GLX+Xlib (I didn't need to explicitly install this, but since its listed in stardust's repo I wanted to include it)
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

Once you have the hexagon button placed where you want it, simply tap it with hand tracking or with your controller trigger to open the launcher menu. This will lay out all of your installed applications in a hexagon grid. To launch a program simply grab the hexagon icon for the program and drop it where you want tne new window to spawn.
Mouse inputs can be handled by controller or hand tracking, but keyboard isn't working!  Let's fix that.

Remember that non-spatial-input repo you downloaded and compiled manifold and simular from? Here's where that comes into play! To capture your mouse and keyboard simply run manifold and pipe it into simular! `/path/to/your/manifold | /path/to/your/simular` 
Now a black window should open on your normal desktop environment! click inside of it to capture your inputs. Keyboard and mouse inputs are sent to which ever application you're currently looking at. Each application will draw its own cursor, and whichever application you're currently looking at will receive mouse and keyboard input. It switched application targets automatically as you look around. You can also tap on the application window like a touch screen for mouse input, but this isn't as accurate and can be a bit tricky.

