# What do i get for making a plugin in notepadplus?

When you make your first plugin and upload it, you will get a developer page on both <a href="http://npnp.lifeserverf.org/social/">NotepadPlus Social</a> and the Plugin Webstore on the program. This will show your username and all the plugins you have made!<br>
People can also search for your name, and plugins!

# REQUIREMENTS
To code in notepadplus, you need a basic knoledge of how python works!

# 1. How to set up your development environment for notepadplus
We have a full dedicated post to how to set it up with images here:
https://github.com/FinGymPlayz/NotepadPlus-PluginTutorial/blob/main/README.md

# 2. Start coding!

## Simple code
After running the `plugindefaults` command in the console, then running `plugin` to launch it in <a href="https://code.visualstudio.com/">VsCode</a><br>
You will get the basic code that is needed to run noteadplus as a plugin<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img1.png">

All of the `import`'s are what notepadplus run of, and are needed. With out these imports notepadplus will not work properly. The main one is the `import handler.main as npp`

The `npp.main()` is what actually runs the program, so any code you put before it, will run before the window opens, and any code put after it will run when the window is closed<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img2.png">

## Leaning the notepadplus module

Anything you want to modify or add to notepadplus, is done by typing `npp.` This gives you a bunch of options you can choose from to edit!<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img3.png">
<br>
A simple option in the `npp.alert()` function. You can make it alert the user with a message by adding a string of text, here is an example<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img4.png"><br>
When you run this, with the extension `code runner` in <a href="https://code.visualstudio.com/">VsCode</a>.<br> You will see a message which looks like this:<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img5.png"><br>

# Making a GUI in the plugin tab

To make a GUI in the plugin tab, we need to import another package called `tkinter`, to do this type `from tkinter import *`.<br>
