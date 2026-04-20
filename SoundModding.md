# How to change the sound effects.

In this part, we will now modify the sound of the rifle. 

To do this we will need to `Duplicate` a sound file into our `MyFIrstAK` folder.

Search for `Weapons_Rifle_AK-74_Shot.acp` in the search bar. You might have to keep an eye on the filtering as you type this in, as the `AK-74` format might empty the window. Try checking the `ArmaReforger` folder when you get to `Weapons_Rifles...`

![alt text](/Sound-Images/image.png)

Right-click and duplicate to `MyFirstAK.`

![alt text](/Sound-Images/image-1.png)

Name it `Weapons_Rifle_AK-74_Shot_MODDED`

Without going too deep in the audio structure, a typical weapon sound uses multiple **sound banks** and **sound shaders** to create a final mix. Shaders are affected by **various signals** like distance from camera, environment around shooter or current weather conditions.

![alt text](/Sound-Images/image-2.png)

In this tutorial, only smart part of the audio project will be modified - bodies & tails sounds.

Some of the shortcuts used in audio project files might be confusing at first glance. Please refer to following table in case something is not clear:

| *AL* | Add Layer |
| --- | --- |
| *FP* or *1p* | First Person |
| *EQ* | Equalizer |
| *EL* or *EnvLayer* | Environment Layer |

We will start with the red box, which is labeled `Bodies`. It has 10 boxes in them that are all joined by lines.  We want to focus on:

- Body FP (Body First Person)
- Body Mid (Body medium range sound)
- Body Far (Body far range sound)

We will add some sample auto files to these small boxes. Known as `Banks.`

>You can close the white `Listener Setup` window with the red sphere in it. This will allow you to better view the `Item Detail` window.

Let’s search for the samples in the Resource Browser on the top-left panel. You can close down many of the window on the left panel so it looks like the image below.

![alt text](/Sound-Images/image-3.png)

Click on the bank named Body FP.  It will highlight in yellow.

In the blue `Sample drop-down menu, there are 5 samples already available. Let's remove them.

To remove the samples. click on one of the samples, then click the minus (-) button. check the image below.

Remove all the samples so we can add fresh ones.

![alt text](/Sound-Images/image-4.png)

Let’s search for `Prototype_Cannon_01_Discharge_0` so we can drag-and-drop the following samples into `Body FP`:

- Prototype_Cannon_01_Discharge_01.wav
- Prototype_Cannon_01_Discharge_02.wav
- Prototype_Cannon_01_Discharge_03.wav
- Prototype_Cannon_01_Discharge_04.wav

![alt text](/Sound-Images/image-5.png)

If you have filtered correctly, you can select them as shown in the image above, then drag them into `Body FP` where they will automatically populate the blue `Samples` menu.

Do the same for `Body Mid`, which is located below `Body FP.` Remember to remove the original files.

Finally, search the following `.wav` files and drop them into `Body Far`:

- Prototype_Cannon_01_Discharge_Distant_01.wav
- Prototype_Cannon_01_Discharge_Distant_02.wav
- Prototype_Cannon_01_Discharge_Distant_03.wav
- Prototype_Cannon_01_Discharge_Distant_04.wav

Remember to remove the original samples first.

> All new WAV files need to be `Registered.` To register a file, right-click on it and select the `register/register and import` option. If they are greyed out, it is already done. **Our samples are already registered.**

To test the shot, you can move over to the bundle of banks shown in the image below.

![alt text](/Sound-Images/image-6.png)

Once zoomed in, look for `Sound_Shot.`  This is the blue coloured bank that is highlighted in the image below.

![alt text](/Sound-Images/image-7.png)

Once highlighted, you can “Fire the Shot” but pressing Space Bar.

We can further modify by zooming out and finding `Tails Meadows Far,` `Tail Hills Far,` and `Tail Houses Far` in the large blue box labeled `Tails.` remove the current samples again and drop in:

- *Prototype_Cannon_01_Tail_Open_01*
- *Prototype_Cannon_01_Tail_Open_02*
- *Prototype_Cannon_01_Tail_Open_03*
- *Prototype_Cannon_01_Tail_Open_04*
- *Prototype_Cannon_01_Tail_Open_05*

Now navigate back to `Sound_Shot.` Highlight and press space bar.

# Apply Sound to Weapon

Once all adjustments in ACP are done, it is now possible to link those new firing sounds to the **Rifle_AK74_Modded** prefab. Remember to save.

Let’s open our modded `AK74` Prefab. 

Edit the prefab by clicking the `Edit Prefab` button (you should know where that is by now).

![alt text](/Sound-Images/image-8.png)

In the `WeaponSoundComponent` under `Filenames` you will find the index for our modded shot. it is at the zeroth (0) index.


![alt text](/Sound-Images/image-9.png)

Search for our new sound by clicking on the browse button (..)

![alt text](/Sound-Images/image-10.png)

Click `OK` to add it to the List of files.

Your Modded rifle now has a more futuristic sound profile. Congratulations.

Let’s test it out.

Exit out of your prefab and return to the main window. open the world editor via the menu bar at the top.

![alt text](/Sound-Images/image-11.png)

Load the sample world via the Modded_Weapon folders.

![alt text](/Sound-Images/image-12.png)

Drag-and-drop your modded rifle into the world.

![alt text](/Sound-Images/image-13.png)

Press the green play button to start the world.

![alt text](/Sound-Images/image-14.png)

Just remember that ESC will end the session. This is a huge pain because muscle memory will force you to continually exit the world when you least expect it. It is a huge complain within the Enfusion modding community.

Now Fire at will.