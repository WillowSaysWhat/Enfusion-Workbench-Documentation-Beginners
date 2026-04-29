# Changing Exhaust Effects

 Lastly, we will try to do some modifications to particle effects to get some sparks going out of exhaust tubes. To do so, we will learn about

- Adding additional emitor to particle effect
- Changing exhaust particle effects

First, we will need to `Duplicate` the particle effect and modify it.

Let’s close the world editor and return to the main window. REMEMBER TO SAVE!

Filter the `Resource Browser` for `Vehicle_smoke_car_exhaust_normal.ptc.`

![alt text](/Exhaust-Effect/image.png)

`Duplicate and add `_MODDED` to the filename.

Open the Particle Editor via the `Editors` menu next to `File` on the top menu bar.

Load the modded effect.

Now we want to add a spark effect to the exhaust. To do this we need to add a particle effect the add button is at the bottom of the Particle Effect window. 

See Image.

![alt text](/Exhaust-Effect/image-1.png)

The spark effect will need to be designed from this default effect.

Go through the image below and make the necessary changes.

![alt text](/Exhaust-Effect/image-2.png)

Now it is time to place this effect on the car. 

Save! then close the `Particle Editor.` 

Jump into the car prefab by clicking the `Edit Prefab`.

FInd `SCR_MotorExhaustEffectGeneralComponent` in the `Object Properties window` This Component hads a yellow `H` icon.

![alt text](/Exhaust-Effect/image-3.png)

Replace the `Particle Effect` with `Vehicle_smoke_car_exhaust_normal_MODDED.ptc`.

Save.

Let’s test it out.

