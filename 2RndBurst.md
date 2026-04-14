# Week 1: Your First Mod: 2Rnd Burst

## Download Tutorial Material

Please find the tutorial material on Github or [click here to follow the documentation.](/DownloadResources.md)

### New Project
[Create a new project](/newProject.md) and call it `MyFirstAK`. Make sure to leave no spaces.

  Exit the workbench and then restart. When you arrive at the `Launcher.`  right-click on your new project and select `open with addons.`

  ![alt text](/images/image-14.png) 

  when you select `open with addons` a smaller window with all your projects and mods will appear.

  ![alt text](/images/image-15.png)

 If you cannot find your downloaded mods, press cancel and select `+ Create New`   then `Scan for Projects`  This will open a familiar load window. 

Navigate to your downloaded tutorial files - which should be in your `Arma Reforger Workbench` folder.

### Making a New AK-74

To create a new AK-74 with an additional firing setting (2 round burst), we will need to create a child. To do this we need to find `Rifle_AK74.et in the `Resource Browser`.

Now right-click🖱️ to open the context menu and select `inherit in MyFirstAK` It will be in the vicinity of `Duplicate in ...`  and `Override in ...`

![alt text](/images/image-16.png)

>The small image above shows `inherit in >`. This is because the image was captured with multiple addons. The small chevron (>) offers a sub-menu. You should see `inherit in MyFirstAK.` 

You should now have a modded AK-74 in your `MyFirstAK` folder under `MyFirstAK/Prefabs/Weapons/Rifles/AK74.`

![alt text](/images/image-17.png)

### 2 Round Burst

Now. we will learn how to make a 2 round burst setting on the safety of our AK74.  To do this we will need to access the `World Editor` - to access the World Editor:

1. Double-click on your modded AK74 file (the one in the image above). A 3d model of the rifle will appear in the window.
2. On the far right will be an empty panel with a long button labelled `Edit Prefab`  (first image below). Click it. If it is greyed-out, check to make sure you are clicking on the `Rifle_AK74_Modded.et` and not the `Rifle_AK74.et` If in doubt, use the navigation window and click through your `MyFirstAK` folder and find your AK.
3. You are now in the `World Editor.`  On the right is your component panel. in the middle of the panel is a large drop-down box with `Entity Instance` selected (check the third image below) select `Rifle_AK74_modded.et.`  Now when your save, all changes will be done to your AK.

![alt text](/images/image-18.png)
> This is the button to the World Editor

![alt text](/images/image-19.png)
> This is the World Editor. On the right its where all the magic happens.

![alt text](/images/image-20.png)

We will be spending most of our time in the window with the green and yellow icons. These are `components`

These components can be thought of as visual interfaces that let you change logic in the game. Basically, you check the box and a line of code is altered, added, or deleted. This let’s you focus on modifying the game and not memorising Enfusion Workbench code (Enforce) syntax.

So when we check a box, the logic changes.

Let’s Start by changing the name of our AK, so we can find it in the Arsenal.

Find `SCR_WeaponsAttachmentsStorageComponent`.  Components are always moving around in the hierarchy, so try to find it by sight first. It is normally the 7th component. just below the yellow-coloured icon. But this could have changed.

Best to search for it in the filter box above the component window.

![alt text](/images/image-21.png)

Give your mouse wheel a wiggle to ensure you are at the top of the component. `Name` should be at the top of the parameter window.

![alt text](/images/image-22.png)

Name your AK something that can be recognisable - I went will `AK74-2-round-burst` and I also changed the `Description` to `AK74 with a 2-round burst firing mode.` The description is directly below `Name`.

Further down the components list (the window with the green icons etc) look for `WeaponComponent`  This will open to a sub-directory of components. Look for `MuzzleComponent.`

![alt text](/images/image-22.png)

Near the top, you will find a head `Fire Modes` This is a drop-down menu. there will be a blue chevron that will let you open/close the tree.

![alt text](/images/image-24.png)

You can see three `BaseFireMode` sub-directories.

In the image above they are neatly closed. It is likely they will be open and unrecognisable like the image below.

![alt text](/images/image-25.png)

Take a moment to close them up to look like the first image. Focus on finding 3 `BaseFireMode` headings and close them so the chevron is >.

If you can’t find them, your `Fire Modes`  directory could be closed.

To add our new fire mode, we need to add a `BaseFireMode` to this list. To do this we need to click the + button located on the right of `Fire Modes.`  This is where beginners get stuck, so check the image below.

![alt text](/images/image-26.png)

This will add a new `BaseFireMode.` It is the bottom one. It should be highlighted. 

Open it to reveal the detail. 

We want to `name` the fire mode so lets put ‘Burst’ into `UI Name.` 

The first parameter is `Max Burst` lets set that to 2. It is a decimal, so it will change to `2.000.`

>**Europeans!** This is the Engish version of `2,000` so `2,000` is equal to `2.000` in English Decimal. Where half of one is equal to `0,5` for you, in English half of one is `0.5`. `2,000` in English is Two Thousand. We love you, and we are sorry that we changed it. 

And now we have modded our first weapon. We have made a 2-round burst AK74.

Let’s Test it.

The next thing we will do is make a world and spawn in and try it out.

So that we don’t over shoot our level of knowledge and start building out a world, we will spawn into an already build virtual world pre-build by the guys at Bohemia.
So let’s save everything by going up to `File/save all` just to make sure. and then exit the Workbench.

Restart and this time, Right click on your `MyFirstAK` and select `open with addons.`  search of `main` and select the `sample mod - main addon.` Yes you may already have your addons, but it is good practice to shut down and reopen to add your `Main Sample Mod.`

![alt text](/images/image-27.png)
![alt text](/images/image-28.png)

This will let us open a world via the world Editor.

To do this, head up to `Editors` which is located next the `File`

World Editor is the first selection.

Once clicked, a new window will open.

To access the virtual world, we need to `Load World` Do this via the `File` menu or click thee folder icon in the tool bar.

Then select `SampleMod/Worlds/Modding` folder and `Assests_Showcase_Base.ent` file.

Hit `OK`

 Now use the view to “fly” to the squares in the centre of the virtual world. Then drop your AK onto one of the boxes.

To find your AK, look for the image of your MODDED rifle, click and drag it into the world.

![alt text](/images/image-29.png)
![alt text](/images/image-30.png)

You should be able to walk up to the AK pick it up and then equip it using 2.

Press V to cycle through fire modes. 

Fire at will.

[Return to Main](/README.md)