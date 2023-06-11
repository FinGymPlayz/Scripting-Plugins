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
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img1.png"width="350px">

All of the `import`'s are what notepadplus run of, and are needed. With out these imports notepadplus will not work properly. The main one is the `import handler.main as npp`

The `npp.main()` is what actually runs the program, so any code you put before it, will run before the window opens, and any code put after it will run when the window is closed<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img2.png" width="350px">

## Leaning the notepadplus module

Anything you want to modify or add to notepadplus, is done by typing `npp.` This gives you a bunch of options you can choose from to edit!<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img3.png"width="350px">
<br>
A simple option in the `npp.alert()` function. You can make it alert the user with a message by adding a string of text, here is an example<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img4.png"width="350px"><br>
When you run this, with the extension `code runner` in <a href="https://code.visualstudio.com/">VsCode</a>.<br> You will see a message which looks like this:<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img5.png"width="350px"><br>

# Making a GUI in the plugin tab

To make a GUI in the plugin tab, we need to import another package called `tkinter`, to do this type `from tkinter import *`.<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img6.png" width="350px">
<br>
Next we need to make a function with our GUI held in here, we can make our function with<br>
`def run_gui()` - Call it what ever you like!<br>
Next we need to make the window with <br>
`root = Tk()`<br>
`root.mainloop()
`
<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img7.png" width="350px"><br>
The last thing we need to do, is tell notepadplus that we want to execute this function when ever we click on one of the options in the Plugins Tab. To do this we can type<br>
`npp.set_custom_gui("NAME HERE",FUNCTION_NAME)`<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img8.png" width="350px">

# Use the logging module

The logging module is pretty easy to learn, there are only a few functions that can be ran, this includes the following:<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img9.png" width="350px">

# Creating a simple config

To create a simple config, we need to define what the config is actually going to be, so to do this we will make a varible, in our case i called it `js`. and then we are going to write in a string, all of the `JSON` data.<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img10.png" width="350px">
<br>
Next we want to create our config, To do this make sure that the plugin name is lowercase and has no spaces in. This is just what defines the plugin to notepadplus, so this won't be the final name of the plugin<br>
`config.create("plugin_name_lowercase",js)`<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img11.png" width="350px">
<br>
We can get all of these values from the config, by simply typing <br>
`config.get_config("NAME_OF_VALUE")`<br>
<b>NOTE</b>: These are cap sensitive, so make sure you get them correct!<br>
<img src="https://raw.githubusercontent.com/FinGymPlayz/Scripting-Plugins/main/imgs/img12.png" width="350px">
