# Overload-Buglist

# Olmod
  - Occasional Empty Weapons when joining a game (in pregame ?) 
  
  - Missile names sometimes dont get updated correctly (missed sync ?) 
     video: https://clips.twitch.tv/EncouragingYummyGoblinPeteZarollTie
  
  - Broken assists, update to 16 player compatibility broke sth that prevents some assists to be given to any players despite
    valid over 30 damage in the last 5 seconds
  
  - Picking up a super leads to a message that tells you "you picked up this ... super". That meesage appears in the language
    of the server and not of the client for some reason. reproducable on DF.net
  
  - Impulse: all weapons have issues with lag but the impulse also has trouble with its correct position
    If player A fights player B with an Impulse and just fires in a ring around him there will sometimes be ghost shots that 
    hit player B. why does the server think its a hit ? does it have throuble with handling the player input and position ?
  
  - Creeper desync ...
  
  - Invisible Ships: Frequently in big Anarchies you will encounter invisible but hitbox posessing ships
    Looks like its a ship from a pilot that has completed its deathroll but not been respawned yet
    
  - Devastators: Devastators sometimes become reliably unreliable. then they explode as soon as they spawns without any
    user input or it swallows the userinput to detonate it on the server and keeps flying despite exploding on the client 
 
 # Projects to look into:
  - 1. shifting the majority of the changes that olmod makes into the Overload assemblies
    + reduces loading times
    + fixes gsync
    - time consuming
    - mods are broken without extra attention
    
  - 2. finishing small overload guide, ask some people to write about how to use some of the weapons
    + help newcomers catch up with the knowledge of people that played this game for years
    
  - 3. Cloning trackerdata
    + perfect sql project
    
  - 4. Visualise tracker data
      1. Idea: how did general map/weapon preferences change over time
      2. Idea: how did player weapon preferences change
      3. Idea: Use the matches to calculate a player ranking and experiment with elo
      
  - 5. Wrap up the Autoorder mod:
      1. Add Tomcatts ideas
      2. Add Bens ideas
      3. Select on spawn
      4. Dont select after manual swap
      5. Overwrite pre/next function
      6. Figure out the server bug that prevents to flawlessly change to the next highest missile
         after the current one got shot empty
         
   - 6. Add the Automap in multiplayer (main thing to figure out is how to change the controls)
       + make it a present for yoshi
       
   - 7. Fix the 120hz input in a non cheesy way    
   
   - 8. Change the damage/creeper color to their respective team colors
   
   - 9. Replace team color in 2 team scenarios with enemy color and friendly color
   
   - 10.Check out how the Light code changed in the pre/after console release versions

