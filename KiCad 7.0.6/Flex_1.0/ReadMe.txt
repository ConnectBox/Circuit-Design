Re: Saving project with new name (ie file names change)

From: https://forum.kicad.info/t/how-to-clone-a-project/3878/12

--------------------
I did an experiment to see the minimum set of files I needed to rebuild a design. Here they are:

myproj.pro : The project file that ties everything together.
myproj.sch : The Schematic file (or files in the case of a hierarchical design).
myproj.kicad_pcb : The PCB layout. It also contains the footprint for every component used in the PCB layout.
myproj-cache.lib : This contains the schematic symbol for every component used in the schematic file. It gets generated whenever you save the schematic or project.

So all you need are those four files. If the shared libraries with the component footprints and/or schematic symbols are missing, then KiCad seems to get the information it needs from these files. These files may also be given priority even if the shared libraries are present; I don’t know.
-------------------



(NOTE: In KiCAD 5.99 the myproj-cache.lib file is missing... but it doesn't seem to be needed as saving the other files in a new folder and opening the project with KiCAD seems to work fine. There is a file "fp-info-cache" that I DIDN'T copy into the new project directory... but KiCAD seems to have created a new fp-info-cache when I opened the project.) 



From that same link we get the following on using the tool "git":


------------------
You probably don’t want to hear this (most people don’t), but git easily does this for you. (Note that I’m talking about git, not Github.)

In your kicad project directory, just do git init. This creates a repository that stores all your project versions.

Add the project files you want to keep track of. For kicad, there’s really only three you need: git add myproj.pro myproj.sch myproj.kicad_pcb.

Store the current state of your project: git commit -a -m "Some message about this version".

That’s all you need to do to setup versioning. Then whenever you have a version you want to save, run the command git commit -a -m "A message about this version". If you also want to give the snapshot an easy-to-remember name, you can use the command git tag my_version_tag. Then if you ever want to return to that version, use the command git checkout my_version_tag. And if you want to see the history of your project, use git log.
-----------------

