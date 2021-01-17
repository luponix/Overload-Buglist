# Overload-Buglist
```
# Olmod-Bugs
  - Picking up a super leads to a message that tells you "you picked up this ... super". That meesage appears in the language
    of the server and not of the client for some reason. reproducable on DF.net
  
  - Invisible Ships: Frequently in big Anarchies you will encounter invisible but hitbox posessing ships
  
  - occasional old missile symbol when the count is empty
    

# Joystick mod bugs
  1. the joystick sensitivity doesnt work linearly but in steps where if you go from 15 to 16 it makes a bigger difference than going from 10 to 15
  2. there is something wrong with the saving and loading of the sensitivity
     - when creating a new pilot and choosing "copy from current" it copies the sensitivity from a different* but not the current pilot file.
       it also doesnt apply the sensitivity and deadzone, as in if it copied the deadzone 1 which should be minimal, the game instead uses
       its default settings for a new pilot with a much higher deadzone. this can be worked around by manually moving the deadzone around a bit for it to update
     - loading the game with the joystick mod once and then removing it and restarting the game will reset the sensitivities of all pilots to normal
     - sometimes on loading the game, a pilot will not load from his saved sensitivities but instead from the earlier mentioned different* pilot file 


 # Update and Improve
  Auto Select
   1. AutoSelect should be disabled by default when no config is found
   2. The config should be profile dependant. how does olmod handle that in general ? should it be its own file ?
   3. The Menu should be moved to Options. look into how arne handles that with his added level select screen
   4. Remove Overloads autoselect for primary component. transpiler ? (since there are a couple prefixes that hook into the relevant method)
   5. Make autoselect work in singleplayer/challenge mode. / make a test map for sp to make all of this slightly less of a pain

  Remote Player Interpolation
   1. Record exact packets and timings for each player to figure out what the client receives when
   2. Extrapolate ship position by difference in time since the last update + ping
   3. Store the expected ship positions and timings
   4. On receiving a new packet: Extrapolate a new ground point. if the new point is more than 0.15m away from the current position.
      teleport the ship 60% of the way between current position and ground point to smooth out the error
   5. compare the accuracy of the expected ship positions and the actual positions
   6. let the algorith optimise the prediction parameters by letting two ships run into each other at high ping
    


 # Projects to look into:
  - 3. Cloning trackerdata
    + perfect sql project
    
  - 4. Visualise tracker data
      1. Idea: how did general map/weapon preferences change over time
      2. Idea: how did player weapon preferences change
      3. Idea: Use the matches to calculate a player ranking and experiment with elo
       
   - 8. Change the damage/creeper color to their respective team colors
   
   - 9. Replace team color in 2 team scenarios with enemy color and friendly color
   
   - 10.Check out how the Light code changed in the pre/after console release versions
   
   - 11. Add a Damage Overlay during Death to show the PlayerDamageRecords
       > clients do not have that data yet <
   
   - 12. Adjust Projectile Positions according to ping
   
   - 13. further testing and smoothing the extrapolation of enemy ships instead of the currently used interpolation
   
   - 14. Experiment with adding bots to mp. start with just trying to display ships

```
