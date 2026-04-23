In this last chapter the weapon's particle effects will be affected through the following operations:

- Create new particle effects for muzzle flash & explosion using one of the existing effects as a base
- Link those particle effects to the modified weapon

We will be duplicating this file in a different way. We could call this a traditional `Save As` method where we will `Load` a pre-existing file, make changes, and then saving it under a different name.

So let’s `load` `Muzzle_AK74.ptc` from the `ArmaReforger` folder.

Start by opening the `Particle Editor via the icon on the dashboard or main screen.

![alt text](/Particle-Effect/image.png)

There will be a sample animation running. It’s smoke and it is crap.

Let’s `Load` `Muzzle_AK74.ptc` from the `ArmaReforger` folder.

![alt text](/Particle-Effect/image-1.png)

You are welcome to make extend to full screen.

Particles Editor opens on the new window with five main sections visible:

- **Particle effect** tab - allows to manage particle effects playback as well as add new emitters
- **Emitter Properties** tab - contains all possible parameters that can be used with selected emitter
- **Particle-Lifetime** **Graphs** tab - visualisation of emitter changes over time
- **Log Console** tab - listing all errors that Workbench detects
- **Preview window** - the final particle effect can be seen there

![alt text](/Particle-Effect/image-2.png)

You can play the animation by clicking the pause button. click the loop button so you can see it running. You might have to zoom in and lift the animation out of the floor to see it.

![alt text](/Particle-Effect/image-3.png)

Now we will multiply the muzzle effect by 10 and change the color to green and blue.

To do this we need to adjust the `Size Multiplier` in the blue `Particle Appearance` tab to 1.5.

![alt text](/Particle-Effect/image-4.png)

Changing color is a little more difficult to start.

First find `Color` in the blue `Particle Lifetime` tab.

When you select it, the space below the preview will change to a graph.

![alt text](/Particle-Effect/image-5.png)

Current, the `red,` `greeen,` and `blue` lines are hidden at the top of the graph. click-and-hold one of the dots that is just visible and drag it down. Replicate the image below. 

You will notice that I have unticked some of the boxes to the left of the graph.

![alt text](/Particle-Effect/image-6.png)

Let’s Save our Effect.

head up to `file/save as` 

using the `New Folder` button at the bottom of the `save as` window, make the new folder structure `MyFirstAK/Particles/Weapons` and save your effect as `Muzzle_AK74_Modded`

Now we add it to our modded AK.

Exit back to the main screen and open your modded rifle.

![alt text](/Particle-Effect/image-7.png)

Open the prefab via the `edit prefab` button.

Find the `MuzzleEffectComponent.`

![alt text](/Particle-Effect/image-8.png)

And change the `Particle Effect` property to our modded muzzle effect.

Save the prefab and close down the prefab window.

You have now completed the lessons on modding a weapon!

You can now test it out in the world editor using the `Showcase World` like we have done throughout this modding tutorial.

See you in the next lesson.
