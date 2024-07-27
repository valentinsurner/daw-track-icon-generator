# daw track icon generator

customized track icons in your daw? here's a solution: a script batch generates icons according to your tracks.<p>
this script is made for Logic Pro X but should work just as well with Cubase, Studio One, Reaper and any DAW that allows you to use custom track icons.

## dependencies
- **Python 3.1** or above
- **Pillow Library** *(https://pillow.readthedocs.io/en/stable/index.html)*

## resources
- **icon-maker.py** :: Python code, see comments inside for settings
- **tracks.json** :: list of icons to generate
- **emboss64.png** :: a 64x64 png to create an emboss effect
- **emboss128.png** :: a 128x128 png to create an emboss effect

## how to use
- **copy all resources** into a new folder that you are going to use
- **edit *tracks.json*** as you want*
- **run *icon-maker.py*** and have fun 🌝

## tracks.json editing guidelines*

each line should have the following structure :: `{"main":"TPT","sub":["solo 1","solo 2","solo 3","solo 4","solo 5","a3","a6","bass","lead"],"style":0,"color":"#00CBC9","invert":1},`
- **main** :: contains the main text of the icon, best to stay between 2 and 4 characters
- **sub** :: contains a list of variations in brackets; each variation will generate an icon with the main text on top and a smaller text below; can be set to [""] if you don't want the small text; it's best to stay below 8 characters
- **style** :: it can take 3 values
  - 0 creates a regular icon
  - "group" creates an icon with an outline, I use this for ensemble libraries
  - "folder" creates a half-height folder icon with an outline and without any subtext
- **color** :: icon background color encoded as HEX
- **invert** :: if set to 1, the text will be black, otherwise it is white by default
