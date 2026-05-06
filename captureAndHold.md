# Setup Capture & Hold PVP.

Start by navigating to `ArmaReforger/worlds/CaptureAndHold.`  and select `CAH_BaseWorld.`This is the Everon map. You can swap this part of any map - for example, Fallujah map. Fallujah is a community mod so you will need to download it and make sure to open your project with the mod as an addon. Better still, make it a `Dependency`.

![alt text](/Capture-And-Hold/image.png)

Go to File/New World and make sure the Sub-scene (of current world) option id selected.

![alt text](/Capture-And-Hold/image-1.png)

Now we need to Save World As in the File context menu. You probably saw it when you made the new world.

![alt text](/Capture-And-Hold/image-2.png)

Give it a name that resembles your gamemode. - `CAH Everon by WillowSaysWhat` Make a `worlds` folder in your mod. Just understand that your Gamemode id will also be called this.

Pick a place to build your capture and hold.

We picked St Pierre.

![alt text](/Capture-And-Hold/image-3.png)

You will see that the locked layer has about 8 entities already available. These are things like preloaded items in the world, the chat channels, building destruction manager, Item preview, AI nav and perception.

![alt text](/Capture-And-Hold/image-4.png)

Below these default entities will be our layer. `CAH Everon` in this demo.

We can place other necessary prefabs here.

In the resource browser below the preview window, find `Prefabs/MP/Modes?CaptureAndHold` drag `GameMode_CaptureAndHold.et` into the world. It is not import where. It affects the whole world wherever it is.

![alt text](/Capture-And-Hold/image-5.png)

from `Prefabs/MP/Managers/Factions` drag the `FactionManager_USxUSSR.et` into the world.

![alt text](/Capture-And-Hold/image-6.png)

And in `Prefabs/MP/Managers/Loadouts` drag `LoadoutManager_USxUSSR.et` into the world.

![alt text](/Capture-And-Hold/image-7.png)

Just check to make sure all 3 entities are in the world. To do this, look at our layer on the left.

![alt text](/Capture-And-Hold/image-8.png)

Let’s create a capture point.

![alt text](/Capture-And-Hold/image-9.png)

Find `Prefabs/MP/Modes/CaptureAndHold/Areas` and drag it onto the map. Drop it in your desired location. Let’s drop it on the church

We can change the shape of the point in the blue `Unsorted` drop-down menu.

![alt text](/Capture-And-Hold/image-10.png)

`Trigger Shape Type` lets you pick a shape and `Sphere Radius` lets you expand the sphere to the desirable size.

![alt text](/Capture-And-Hold/image-11.png)

`Draw Shape` makes the capture radius visible. Untick the box to make it invisible.

You can make multiple points in this area.

Now let’s add a spawn point so we can jump in and test.

Find `Prefabs/MP/Spawning` and drag `SpawnPoint_US.et` and `SpawnPoint_USSR.et` to the map. Place them in the desired location.

Save.

![alt text](/Capture-And-Hold/image-12.png)

To Test. Make sure `Play From Camera Position` is not selected. Then hit the green Play button. ESC will end the simulation so try to use the on-screen button to exit menus. 

In `CAH` Your point will increase the longer you hold a position.

![alt text](/Capture-And-Hold/image-13.png)

The blue squares (here it is A) indicates that our team holds the A point.

You are welcome to add more points. 

This is the basis to King of the Hill and some of the smaller PVP gamemodes.

But to be able to play this in Arma Reforger, we need to add a `Mission Header`.

But first we must make the points invisible.

Select `SCR_CaptureAndHoldArea` from your layer. see the image below.

![alt text](/Capture-And-Hold/image-14.png)

On the other side of the screen, untick `Draw Shape` it near to where you chose the shape of your capture point.

![alt text](/Capture-And-Hold/image-15.png)

Okay - Mission Header.

Close down the `World Editor.` 

In the main window, we need to make a folder called `Missions.`

![alt text](/Capture-And-Hold/image-16.png)

You can make a new folder by clicking the `Create` button at the bottom of the window. See image. Make sure to have your mods root directory selected. 

![alt text](/Capture-And-Hold/image-17.png)

Now we need to make a `Config` file. To do this need to right-click inside the lower window and select `Config File` 

A menu window will apear.

Pick a name for your `MissionHeader` This one is called `CAH_StPierre_Church.`

![alt text](/Capture-And-Hold/image-18.png)

Then select `SCR_MissionHeader.`

![alt text](/Capture-And-Hold/image-19.png)

It will now be in the Missions folder.

![alt text](/Capture-And-Hold/image-20.png)

Open it up by double-clicking the file.

![alt text](/Capture-And-Hold/image-21.png)

In the `World` field, click on the browse button ..  and navigate to our world file `CAH Everon.ent.`

![alt text](/Capture-And-Hold/image-22.png)

Fill out `Name` and `Author` , and change the `Game Mode` to `Capture and Hold` give the `Player Count` a max number.

Let’s go back into the world and change some game parameters.

In the `SCR_BaseGameMode` located in the layer.

![alt text](/Capture-And-Hold/image-23.png)

Find `SCR_ScoringSystemComponent` and change the `Score Limit` in `Score: Actions` then open `Actions/EndGameActions` there you will find `Score Limit.` 

Above this in the blue `Scoring: Multipliers` we can change a range of other score multipliers that could assist in winning or losing the match.

![alt text](/Capture-And-Hold/image-24.png)

# Kill Feed

Check out `SCR_NotificationSenderComponent` in `SCR_BaseGameMode`

Right now, the kill feed will show `unknow player` to `group only`.

![alt text](/Capture-And-Hold/image-25.png)

We can change this to `Full` and `All.`

![alt text](/Capture-And-Hold/image-26.png)

# Activate Unconsciousness

By default, this is deactivated. Goto `Gamemode_CaptureAndHold`  and in there find `SCR_GameModeHealthSettings` tick `Permit Unconsciousness` you may allow players to talk while down by ticking `Permit Unconsciousness VON` 

# Spawn Areas - Safe Zones

To make a spawn point, you will need to drop `CaptureAndHoldSpawnArea.et` and `CaptureAndHoldSpawnArea_USSR.et` into the world. They are located in `ArmaReforger/Prefabs/MP/Modes/CaptureAndHold/SpawnAreas.` Drop them into the world. Make sure to place them next to your spawn points. 

Select one of the spawn areas and scroll down to the blue `Unsorted` menu. 

Change the `Trigger Shape Type` to `Sphere` and give it a radius of `23`

find `Draw Shape` and tick it.

The spawn area is now ready to be added to the map.

We need to add a component from the `+ Add Component` button.

![alt text](/Capture-And-Hold/image-27.png)

Filter for `Map.`

![alt text](/Capture-And-Hold/image-28.png)

we want the `SCR_MapDescriptorComponent` click to add.

Make sure `Visible on Map` is ticked. And change `Scale` to the size of the sphere in `SCR_CaptureAndHoldSpawnArea.` 

Change `Main Type` to `Icon (Generic)`

Save and Test.

