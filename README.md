# Deadlock_Multiplayer
This code allows Deadlock: Planetary Conquest to be played online over TCP Sockets. Currently DLLs are only being released for version 1.31. (See ReadMe2.md for information about single player features.)

You will need to download the 2 SFML library dlls, and a set of the "WING32" and "DLTCP" dlls (from same version) and put them into your Deadlock folder. If you are playing the GOG version of Deadlock, you will need to perform the GOG multiplayer patch found on the Gallius IV forums (http://forum.galliusiv.com/viewtopic.php?f=4&t=351&sid=9ac01f392614f1f161dd75da350f7344), which will add the multiplayer game button back to the main menu dialog.

Known issues:
1) If there are more than 2 human players, and the host player disconnects, the other 2 client players will no longer be able to play (no current way to switch hosts). I will try to implement a fix for this in 1.0.0.5 or 1.0.0.6.
2) Unsure how a 3+ player game will play.

Because of the way Deadlock was originally made, the developers recommended not playing multiplayer games with AI players because they will lag the host.
If you are hosting a game, you can press Ctrl + F1 to bring up the command dialog box in a multiplayer game. If you input the code 

    "Kill AI"

then if a human player disconnects from the game, their colony will be destroyed. Inputting the code again will turn this feature off. This code currently will NOT kill
any AI that were in the game before the code was input. You will need to input this code every time a multiplayer game is started or loaded for it to be in effect.

Change Log:
11/3/2020 - 1.0.0.4
1) Fixed an issue where the host player's game would freeze if a client disconnected before getting to the Select Race Dialog.
2) Did not fully fix net message problem in 1.0.0.3, but it has been corrected now.
3) Clients should now receive a message that displays the username of other clients that disconnect in a 3-7 player game. Have not had a chance to fully test this yet with 2 clients, so it may need some work.

10/27/2020 - 1.0.0.3
1) Fixed an issue where messages from clients were not getting sent to other clients in 3+ player games.

10/26/2020 - 1.0.0.2
1) Fixed a bug with the net message queue not processing for all players when a new turn was started causing the games to be out of sync.

10/26/2020 - 1.0.0.1 (no longer available for download due to end turn bug.)
1) Added DLL Version Checks to prevent players with different versions from playing together and causing problems.
2) Added the ability for users to choose a username that will be used at various points. Currently it is only used to notify other players when someone has disconnected. (Currently may only show the name to the host player or to the clients if the host disconnects. Need to do some extra work to notify other clients when a client disconnects.)
3) If someone disconnects from the game, Deadlock will automatically save a copy of the game to the Deadlock folder in the form of "NetGameSaveX.Sav", where X is a number. X will start at 0 and increment until it finds a save game name that is available. 
Note: If the host has enabled the "Kill AI" command, Deadlock will still save a copy of the game before it destroys the disconnected player's colony.

10/20/2020 - 1.0.0.0 (no longer available for download due to lack of DLL version checking)
1) Initial Release
