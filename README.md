# Update 01/16/18:

Update multiple player map supporting the upcoming multiplayer update of pysc2. 

\_multi map can use for both single player or multiplayer combat ML use. These maps run continuously until exit command (in pysc2 or exit in SC2) is issued. Score of current episode will reset to zero at the start of next episode and 2 game seconds time period is given at the end of current episode and before the start of next episode to record this score. 

New mini-map: Defeat_marine_and_tank. Focus on midgame TvT combat, marine with lv1 attack and lv1 defend with stimpack and shield. 20 marines and 4 tanks are in game for each side. 120s is the time limit. I believe ML should be able to learn by combating with itself in this minigame.

mini_games.py: Names of these minigames are now included into library of minigame so one can use it in system command directly. Just copy this file and replace the old file in the directory of pysc2/maps/minigames.py

Call to multiplayer pysc2: Multiplayer pysc2 is available in dev branch. "--agent" and "--agent_race" is for player1, give "--agent_race terran" if you want player 1 to use terran in minigame. "--agent2" and "--agent2_race is for player2. Default race of player 1 is terran but you can change it use this command. For multiplayer pysc2, \_multi map is require or an error will pop out.

# Update 01/12/18:

Update the race selection of minimap. Now, player can select which side they want to play, versus build-in AI or another human player. Also, these maps are now multiplayer map which mean you can play with your friend or practice versus AI. Default race for player 1 is terran.

I'm not sure if one can control his race use pysc2 command (give command to game before map initiated).

# multiplayer-minimap
Change the original minimap so player can control both side of army

In this map friendly is still marines and hostile lings. F2 (select all army) only select friendly marine unit. One have to manully choose zerglings and banelings to control their move. Basically this still a single player game with control of both side.

I'll see if I can turn this into multiplayer game with seperate control.
