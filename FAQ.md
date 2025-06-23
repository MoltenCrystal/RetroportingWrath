# Issues and solutions

## Maps
Issue: No textures are loading after I moved all extracted things from wow.export folder!
Solution: Make sure you replaced every _s.blp with .blp. The listfile is default to CRLF, and should be set to LF.

Issue: I cannot save my map in Noggit, due to models not being loaded!
Solution: Make sure you really converted ALL M2s and WMOs.s

Issue: Noggit only crashes and I've done all steps above!
Solution: Restart PC, Noggit tend to hogg RAM even after closing.

Issue: Help! My textures are green ingame?!
Solution: Try redo the process of copying all folder from your project folder to your patch MPQ.

Issue: FixTXID had errors when I ran the M2 files!
Solution: Check logs, test it ingame and see if it works or not. Sometimes it works even with errors.

## Loadingscreens
Issue: Texture is green upon loading!
Solution: Redo everything, either the size is wrong or file exported could be corrupted. And double check your pathing to the BLP file in LoadingScreen.dbc

## Gobjects
N/A

## Creatures
N/A

## Items
N/A
