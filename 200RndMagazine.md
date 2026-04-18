# Week 1 Your First Mod: 200 RND Mag

## Inherit a Magazine

Okay! You know how to do this now. 

Search for `Magazine_545x39_AK_30rnd_Base.et` and Inherit it.

Name it `Magazine_545x39_AK_30rnd_Modded.` 

let’s edit the prefab via the `edit prefab` button.

Inside of `MagazineComponent`  change the `Max Ammo` to 200. This is the Magazine Capacity.

Next we need to make a new ammo config. 

To do this we need to hotkey back to the main view.

We need to add another folder inside `Configs/Weapons` This folder will be called `Ammo`

![image.png](attachment:06f51853-7a67-46a7-9cfc-2586edb38ffb:image.png)

Now head back to the `Create` button and make a `MagazineConfig` in the same way you did for the Ballistic Table. call it `Ammo_545x39_Modded`

![alt text](/Magazine_Images/image.png)

Now head back to the Create button and make a MagazineConfig in the same way you did for the Ballistic Table. call it `Ammo_545x39_Modded.`

![alt text](/Magazine_Images/image-1.png)

Double-click on our new Ammo Config and add our modded round to the 0 slot. Remember to use the `..`  button to browse and `save` too.

![alt text](/Magazine_Images/image-2.png)

Head back the the Magazine window and add the config to the `Ammo Config` slot below the `Max Ammo` heading.

![alt text](/Magazine_Images/image-3.png)

Make sure to add 200 rounds to the Ammo Mapping. Currently there are 30 in the image and there could be zero (0) in yours. Click the `+` at the right of the textbox with the (30). That will add +1 to rounds to your mag. if you all slots at zero (0) they will fire your explosive round. If you change it to 1. It will either not fire a round, or it will default back to a normal round.

Now that we have a mag full of explosive rounds, we need to adjust how the AI use it.

click on the `AICombatPropertiesComponent` and change `Priorities Against Vehicles` to 35.

This will allow AI to use these rounds against vehicles.

Also, tick the `Vehicle Medium` in `Used Against` . So they will fire on bigger cars and Armoured vehicles.

Also, select `Infantry` in `Indirect Used Against` so the AI will utilised the splash to injure large groups of soldiers.

# Apply Mag to Weapon.

Open your `Rifle_AK74_MODDED` and edit the prefab.

in `MuzzleComponent` You will find `Magazine Template` I recommend searching for it in the filter.

![alt text](/Magazine_Images/image-4.png)

Change your Template by clicking on the the 2-dot button and selecting your modded magazine.

![alt text](/Magazine_Images/image-5.png)

And that is how to mod a Mag.

[Return to Main.](/README.md)