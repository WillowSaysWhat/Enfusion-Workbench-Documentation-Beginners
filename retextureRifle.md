# How to Retexture a rifle

## How to Make a New Material

To make a new material, right-click on the `resource browser` window (the bigger one) and select `Materal` this will make a new, empty material. However, we will be duplicating materials for this tutorial. We are doing this to keep this at a beginner level.

![alt text](/Retexture-Rifle-Images/image.png)

# How to make a duplicated Material.

So, the M16A2 has multiple camo variants. However, we will make another one so we can understand how to retexture a rifle.

To `Duplicate` an `emat,`  we need to navigate to the M16A2 `Data` folder. The best way to do this is to search `emat M16.`

![alt text](/Retexture-Rifle-Images/image-1.png)

we need to Duplicate the following `.emat` files:

- `AK74_Barrel_01.emat`
- `AK74_FrontSight_01.emat`
- `AK74_Grip_01.emat`
- `AK74_Receiver_01.emat`
- `AK74_Reveiver_02.emat`
- `AK74_Stock_01.emat`

rename them with `_Camo.emat`  at the end.

These should now be in your `MyFirstAK` folder under `Assets/Weapon/Rifles/AK74/Data`

Now lets place a new camo into each one of these `emat` files.

It is up to you which camo you would like to use, but I will use this one.

Camo can be found in `ArmaReforger/Common/Textures/Camouflage`

![alt text](/Retexture-Rifle-Images/image-2.png)

Now open the emat `AK74_Barrel_camo.emat` in your `MyFirstAK` folder. It is located in `MyFirstAK/Assets/Weapons/Rifles/AK/Data`.

At the top for the window (image below) is a button that says `Change Class`

![alt text](/Retexture-Rifle-Images/image-3.png)

Once clicked, it will open a small window. Search `Camo` in the Class Drop-down menu and click `OK`.

![alt text](/Retexture-Rifle-Images/image-4.png)

If an error is thrown, check to see if the class is already `MATPBRCamo`. You don’t need to change it if the Camo class is already selected. This can happen when duplicating a camo `emat` 

Scroll down to the bottom and find the blue `Camo textures` drop-down menu.

![alt text](/Retexture-Rifle-Images/image-5.png)

Now return to the `Camouflage` folder located at `ArmaReforger/Common/Textures/Camouflage` and drag-and-drop your camo .edd into the `Camo Albedo Map.` The sphere should change to reflex the drop.

![alt text](/Retexture-Rifle-Images/image-6.png)

Now do the same for all other `.emat` files.

This should include.

- `AK74_Barrel_01.emat`
- `AK74_FrontSight_01.emat`
- `AK74_Grip_01.emat`
- `AK74_Receiver_01.emat`
- `AK74_Reveiver_02.emat`
- `AK74_Stock_01.emat`

DON’T FORGET TO SAVE ALL!

We can now drop these `.emat` files onto our AK.

Navigate back to our `AK74` and locate `MeshObject` in the `Object Properties` window.

![alt text](/Retexture-Rifle-Images/image-7.png)

Drop the correct `.emat` into its place and you should see the rifle change colour.

Find your `camo` emat using the `resouce browser` below the viewing window.

The `Camo-Roughness-Metalic (CRM) Map`  can be thought of as a heat map for where textures should be located. Here is an example of a CRM Map.

![alt text](/Retexture-Rifle-Images/image-8.png)

- **Camo Normal Map** - Optional. Classic normal map. It can be used to add additional bumpiness like some mud smudges or deep scratches
- **Camo CRM Map** - CRM stands for **C**amo/**R**oughness/**M**etallic. Textures per channel:
    - **Red** = Mask - white color defines where all Camo textures are applied
    - **Green** = Roughness - classic roughness
    - **Blue** = Metallic - classic metallic

**Camo Albedo Map UV Transform** is quite a useful transform, since it lets control the size of the camo texture.

"**Camo modifiers**"  contains opacity controls of each mask. If no **Camo Normal Map** is provided then **Camo Normal Opacity should be set to 0**.

Below is an example of **Camo CRM Map.** Roughness and metalness were copy pasted from base material but custom maps can be exported to these channels easily if that mask is created in a program like Substance Painter.

![alt text](/Retexture-Rifle-Images/image-9.png)

Camo CRM Map channels

Texture that have been created should be in **RGB Color** mode with **8 Bits/Channel** and saved in **.tiff format with following settings.** 

You can make simple colors in [Canva.com](http://Canva.com) and drop them into the Workbench. The best import type is `.TFF` but `.PNG` is also accepted.