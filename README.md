# Deadlock_Multiplayer
This code allows Deadlock: Planetary Conquest to be played online over TCP Sockets.

Known issues:
1) If there are more than 2 human players, and the host player disconnects, the other 2 players will no longer be able to play. No current way to switch masters.
2) If a player disconnects before everyone has selected a race, Deadlock will show a message box saying "The player controlling the ChCh't has disconnected".
3) Unsure how stable a 3+ player game will be.

Because of the way Deadlock was originally made, the developers recommended not playing multiplayer games with AI players because they will lag the host.
If you are hosting a game, you can press Ctrl + F1 to bring up the command dialog box in a multiplayer game. If you input the code 

    "Kill AI"

then if a human player disconnects from the game, their colony will be destroyed. Inputting the code again will turn this feature off. This code currently will NOT kill
any AI that were in the game before the code was input. You will need to input this code every time a multiplayer game is started or loaded for it to be in effect.
