# Week 1 Your FirstMod: Explosive Rnd

## Inherit a Bullet

Let’s open our project `MyFirstAK` with the `sample mod - main addon` This will give us access the orb wrap.

Inherit the `Ammo_545x39_ball_7N6.et` file so we can make modifications.

![alt text](/Explosive-rnd-images/image.png)

Remember to rename with `..._Modded.`

Once done. click the `edit prefab` button and find `Project Model` it is one of the lare grey panels with a small image in it. Actually it is the first one with the image of a bullet with a red band.

![alt text](/Explosive-rnd-images/image-1.png)

Here we are going to swap the bullet out for a red orb. Just for fun.

![alt text](/Explosive-rnd-images/image-2.png)

click the browse button on the far right (red circle) and find the orb.xob file in the `SampleMod_ModdedWeapon` folder. Check the image for the full folder tree.

![alt text](/Explosive-rnd-images/image-3.png)

select it and click the OK button.

![alt text](/Explosive-rnd-images/image-4.png)

To make the round visible we need to change `Projectile Visible Time Scale` to 2. This will let us see the ball of ‘fire’.

Now we want to add and explosive effect to the round.

# Explosive Effect

We will now delve into adding Components to our bullet, or round as it is offically called.

This will give the round and explosive effect on impact.

We will add `CollisionTriggerComponent` and `BaseProjectiveComponent`

To do this we must head to the bottom of the screen and click the `+ Add Component` button.

![alt text](/Explosive-rnd-images/image-5.png)

It is best to search for the Component via the filter box. check the image below.

![alt text](/Explosive-rnd-images/image-6.png)

In the `CollisionTriggerComponent` add an `ExplosionEffect` by clicking on the plus (+) of the `Projectile Effects` heading. Check the image.

![alt text](/Explosive-rnd-images/image-7.png)

A drop-down menu will appear. Pick the `ExplosionEffect` module.

Now use `CTRL + TAB`  to hotkey to the other window. You should see the blue floor in the 3d window.

Go to the Resource Browser panel on the left and search for `Warhea_Grenade_He.et` in the same way that you found the AK and the 5.45 bullet.

Inherit the warhead file into your mod folders by picking `MyFirstAK` 
We are going to make changes in this warhead before returning to the round.

Open the prefab via the `edit prefab` button.

In `BaseTriggerComponent`  and then `ExplosionImpulseEffect`- change `Damage Value` to 25

change `Damage Distance` to 5. This is located 3 heading down the list from `Damage Value`.

The heading for these values is `ExplosionImpulseEffect`- close the chevron. This will make it easier to search for our next heading.

`ExplosionFragmentationEffect` is the next heading down in the list.

![alt text](/Explosive-rnd-images/image-8.png)

Let’s change the `Damage Distance` to 40. This is the 4th heading inside `ExplosionFaragmentationEffect`.

We are looking for `Damage Framentation Count` it is set to 300 by default.

We want to reduce this to 200.

This will lower the amount of frag coming out of the round, as 300 is a little high for a bullet.

Now we need to click on the `HitEffectComponent` back in the Component Window.

![alt text](/Explosive-rnd-images/image-9.png)

Here we will find a `Partical Effect` panel where we will need to place the `Explosion_AK74_Modded.ptc in the `SampleMod_ModdedWeapon` folder.

Save

Return to the `Ammo_545x39_ball_Modded` World view viw the `edit prefab` button. In the `CollisionTriggerComponent` browse the `Effect Prefab` and select our Warhead.

![alt text](/Explosive-rnd-images/image-10.png)

Select warhead here.

![alt text](/Explosive-rnd-images/image-11.png)

From here we will add a `Ballistic Table.` [click here to continue](/ballisticTable.md) on to the Ballistic Table tutorial.

[Return to Main.](/README.md)

