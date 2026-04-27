# Modding Car Damage

## Inherit a car

To start modding a car, we need to inherit it from the base game using the same method as the Weapons Mod. We will inherit the `UAZ469.et`. Remember to add the `_MODDED`  postfix.

Next we need to `dupicate` the materials so we can change the color of the car. Search `UAZ469_body.emat.` Name it `UAZ469_body_moddded.emat.` 

open  `UAZ469_body_moddded.emat.` and change the `class type` to `MatPBRMulti.`  We will discuss this further when we make a new car - later in the course.

![alt text](/Modding-Car-Damage/image.png)

We will need to add it to the car. `UAZ469_body_moddded.emat.` 

![alt text](/Modding-Car-Damage/image-1.png)

Find `MeshObject` in the `Object Properties` window.

Change the `UAZ469_Body` to your modded material.

![alt text](/Modding-Car-Damage/image-2.png)

Hot-Key back to the main window using ALT-TAB and open `UAZ469_body_moddded.emat.` You can place the two windows side-by-side as shown in the image below.

![alt text](/Modding-Car-Damage/image-3.png)

For now, try playing around with the sliders in `Material 1 (Base)` to come up with some interesting colours. To find `Material 1 (Base)` you will need to scroll past `Material 3`  and `Material 2.` 

Click on the colour box. It is circled in the image above.

Play with the colour wheel and see the car body change in real-time. You may choose any colour for your car.

You can also play with the other masks, but we will be looking into materials at a later date.

# Side note.

There are so many more components in a vehicle compared to a weapon.

Each icon represents a type of component.

E = Engine component - Implemented deep in the Enfusion Engine Codebase.

G = Game Component - Implemented in game code - may vary from game to game.

H = Hybrid Component - component is handled by engine and by script

S = Scripted component

▶️ = (green) Editor scripted component.

# Modify Damage

In this chapter the following topics will be explained

- How to increase armour on vehicle
- Make it super fragile to collisions!

Open the modded UAZ469 via the `Edit Prefab` button like we have done previously. It is possible that you already have this open.

Let’s navigate to the `SCR_WheeledDamageManagerComponent.` It is best to use the filter.

![alt text](/Modding-Car-Damage/image-4.png)

Head down to `Unsorted` and change `Max Health` by adding more zeros. It will reset to default max health which is 65535. 

Check that `Collision Multiplyer` is set to 100000. This will destroy the car on any impact.

Then at the bottom of the window - `Collision Velocity Threshold.` Change it to 1.