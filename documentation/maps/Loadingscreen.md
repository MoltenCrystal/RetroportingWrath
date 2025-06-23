# Loadingscreen

## DBC
* LoadingScreen - Path to your loadingscreen
* Map - To set the ID of the loadingscreen you added

## Exporting

### Important notes!
If you extract a loadingscreen that is bigger than 2048x1024 or if it is DXT5 you need to convert!

### DXT1, less or equal size to 2048x1024
1. Open wow.export and select what loadingscreen you want
2. Press Export selected as BLP and wait until it's done extracting
3. Done!

### DXT5, bigger or equal size to 2048x1024
1. Open wow.export and select what loadingscreen you want
2. Press Export selected as PNG and wait until it's done extracting
3. Open the exported PNG in paint and edit/resize to your liking and save
4. Open BLPNG Converter.exe, drag the PNG to the BLP icon
5. Done!

## Adding the loadingscreen to a map
1. Place LoadingScreen.dbc and Maps.dbc in DBFilesClient
2. Open WDBX in LoadingscreenTools and open LoadingScreen.dbc and Maps.dbc
3. In the LoadingScreen.dbc, add a new row, and set the path to where your loadingscreen BLP will be in the patch MPQ
4. Save LoadingScreen.dbc, and then go to Maps.dbc
5. Go to the column LoadingscreenID and set the ID of the loadingscreen you created in LoadingScreen.dbc and then save
6. Drag and drop the dbc files from you patch MPQ into dbc of your server folder
7. Restart both worldserver.exe and wow.exe
8. Login and go load where ever you set the loading screen
9. Done!