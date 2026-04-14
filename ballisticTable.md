# AI Ballistic Table

Now we will have to create a ballistic table.

Save your progres and close this window. You will return to the main view.

For the next part we will need to create a `Configs` folder.

To do this, highlight the root directory of our mod. That’s the `MyFirstAK` folder.

in the bottom of this panel is a `Create` button - see image below.

 Make sure the bottom window is also returned to `MyFirstAK.`  If you accidently make the folder inside the wrong folder, just drap it from the bottom window and drop it into the `MyFirstAK` folder in the hierarchy in the top window.

![alt text](/Ballistic-Table-Images/image.png)

Make a new folder. Call it `Configs`. 

Make another folder inside of `Configs` call it `Weapons` and then make another inside `Weapons` and call it `AIBallisticTables` That’s `AI Ballistic Tables` all-one-word.

Inside `AIBallisticTables` create a Config file, but finding `Config File` in the `Create` button you used to make the folders.

call it `AIBT_545x39_Ball_Modded` and select `BallisticTableArray.`

![alt text](/Ballistic-Table-Images/image-1.png)

This lets the AI fire the rounds accurately.

Now we need to go back into the Bullet Prefab using the `edit prefab` button. select `ShellMoveComponent` and add our ballistic table to the `Ballistic Table Config.`

![alt text](/Ballistic-Table-Images/image-2.png)

Open the browse feature using the two dots (..). Navigate to `MyFirstAK` and select our modded config file.

![alt text](/Ballistic-Table-Images/image-3.png)

If this was done properly, we should now be able to generate data for the ballistic tables by Right-clicking on the `ShellMoveComponent.`

![alt text](/Ballistic-Table-Images/image-4.png)

![alt text](/Ballistic-Table-Images/image-5.png)

And that is the completed explosive round.

Now Let’s make a [high-cap Magazine](/200RndMagazine) to put them in.

[Return to Main](/README.md)

