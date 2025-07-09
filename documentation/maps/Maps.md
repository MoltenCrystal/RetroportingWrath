# Retroporting maps

## Notes
This example is made for Zereth Mortis, things could vary in difficulty in extracting, fixing M2s, textures and so on. If something does not end up working like you wanted it to on the map you are wanting to port, you will have to tinker on your own. I am no expert at this, as all of this has been done with a lot of passion, love, frustration, trial and error.

## Map

### Requirements
* Notepad++
* Noggit Red
* Noggit 3
* WowExporter
* MapTools

### Tools prepp
Before you start, make sure to run Get-LatestListfile.ps1 first!
This is to make sure we have everything up to date before converting anything.

### Extraction
1. Open wow.export and select what map you want
2. Click on the map, and press CTRL + A to select all tiles
3. Make sure that every box is ticked before exporting
This is what it should look like before you export everything:
![alt text](https://github.com/MoltenCrystal/RetroportingWrath/blob/main/documentation/maps/mapsImgs/wowExport.png)
4. Wait for it to complete
5. Done!

### Noggit prepp
1. Create a folder in %userprofile%\Documents\NoggitProjects\YOUR_PROJECT_NAME, and <ins>make sure that the folder does not have any spaces in the name</ins>
2. Open Noggit and create a new Wrath of the Lich King project in Noggit
3. Set the project folder to the one we created in the first step

It should look something like this:</br>
![alt text](https://github.com/MoltenCrystal/RetroportingWrath/blob/main/documentation/maps/mapsImgs/noggitProject.png)

4. Press Ok
5. Open your created project
4. Press "Add new map"
5. Make sure the name of the map is the ID/name of the map you extracted
6. Set expansion as Wrath of the Lich King

If you have done everything right, these parameters should then look something like this:
![alt text](https://github.com/MoltenCrystal/RetroportingWrath/blob/main/documentation/maps/mapsImgs/noggitSettings.png)

6. Save and close Noggit

### Conversion: ADT, WDT, WDL
1. Run MapTools.bat
2. Enter the exact name you created for your Noggit project
3. Wait for it to complete
4. Done!

### Get max UID

**IMPORTANT**, depending on map the loading time could be very long depending on how big the map is and how good your hardware is for running Noggit.

1. Open Noggit
2. Select your map, and double click any ADT
3. When asked about UID, select "Get max UID"
4. Select an ADT and double-click to load in
5. Let it load and check to see if any texture has rendered or not
6. Close Noggit
7. Done!

## M2 and WMO

### Conversion: M2
1. Open C:\WowTools\MapToos\M2\FixTXID
2. Open FixTXID.exe and drag-and-drop all M2 files in the program
3. Press fix and wait for it to finish
4. Now go back and open C:\MapTools\Multiconverter
5. Open Multiconverter.exe all M2 files in the program
6. Press fix
7. Done!

### Conversion: WMO

**IMPORTANT**, the current multiconverter doesn't really support any WMO's above 9.2.7 to convert properly. If they work, they do, if they don't you are on your own here.

1. Open C:\WowTools\MapToos\WMO
2. Edit ran.bat to the correct path potinting to where your project is located
3. Run ran.bat as administrator and wait for it to close
4. Now go back and open C:\WowTools\MapTools\Multiconverter
5. Open Multiconverter.exe all WMO files in the program
6. Press fix
7. Done!

### Adding it to the game

**IMPORTANT**, there would be times where the map cannot load, or something crashes or whatnot. This could be due to something called "fuckporting" meaning something hasn't been ported properly. Please redo the whole process if this occurs, unless you know what went wrong.

1. Create a folder inside your Wrath of the Lich King client called patch-M.MPQ (yes a folder, you read that right).
2. Drag and drop all files from your Noggit project folder into patch-M.MPQ.
3. Inside the DBFilesClient, copy Maps.dbc and replace that in where your server dbc files are.
4. Start the server and the client, enter the coordinates from Noggit using .go zoneyx.
5. Done!
