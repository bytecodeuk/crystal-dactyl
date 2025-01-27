# Forked Version of Dactyl (Hactyl)

This is a fork of the [crystalhand fork](https://github.com/crystalhand/dactyl-keyboard) of the [Dactyl](https://github.com/adereth/dactyl-keyboard), a parameterized, split-hand, concave, columnar, ergonomic keyboard.

## Customization for Hactyl (Derek changes)
- Hotswap holder i designed (hotglue recommended)
- North switch orientation support
- Cutout for tiny little teeth in front and back of many switchs
- Renamed, commented, and cleaned up some of the code to make more readable
- Added pre-rendered STL files, and ZIP files for SCAD that generated the STL files.

## Preview of the keyboard in a 3d printer slicing software (IdeaMaker).
![3D Printing](/resources/3dprintingsupports.png)

## Updated Wiring Diagram
![Fancy Wire Diagram](/resources/fancy-wiring-diagram.png)

## Timelapse Video
[![Dactyl Timelapse Video](/resources/timelapse-screenshot.png)](https://youtu.be/jucJIm_TujM)

## Hactyl With Per-key RGB
![Hactyl Glamourshot](/resources/hactyl_glamourshot.jpeg)

# Generate OpenSCAD and STL models

## OLD
* Run `lein repl`
* In the repl run `(load-file "src/dactyl_keyboard/dactyl.clj")`
* This will regenerate the `things/*.scad` files
* Use OpenSCAD to open a `.scad` file.
* Make changes to design, repeat `load-file`, OpenSCAD will watch for changes and rerender.
* When done, use OpenSCAD to render, then export model STL files which can be printed by 3d printer slicing software.

## NEW (faster)
* Run `lein auto generate`
* This will regenerate the `things/*.scad` files whenever the .clr file is saved
* Use OpenSCAD to open a `.scad` file.
* Make changes to design in `src/dactyl_keyboard/dactyl.clj`, open scad files will auto regenerate, OpenSCAD will rerender.
* When done, use OpenSCAD to render, then export model STL files which can be printed by 3d printer slicing software.

## Batch (parallel) Processing
* Edit the path for OpenSCAD in `create-models.sh` if needed
* Change any other settings for which files you want to render
* Wait for STL files to appear (this may take a minute or two) 

# Customization for dactyl (Crystalhand)
This is my version of the Dactyl with a number of modifications and additions.  I changed a number of constants to variables to make it easier to modify.
- Ergodox like layout for a wider range of supported keys
- Curve/slope front back and left/right for alphas and thumb controlled separately
- Thumb cluster layout
- Thumb offset and orientation angle
- Number of rows (5-dactyl or 4-lightcycle)
- Profile selection (ie high low or custom)
- Optional detachable wrist rests with customizable height and slope



# Notes
All screws used are m3x12 for the dactyl.  
Brass knurled nuts m3x5x5 are used for to attatch the dactyl top and bottom case and the Manuform top and bottom cover.
m3x12 screws and nuts are used to attatch the wrist rests to the case

TRRS jack being used is SJ-43514.






