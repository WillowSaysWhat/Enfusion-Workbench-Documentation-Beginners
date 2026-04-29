# Adding a Turret to a vehicle

### Using the Slot Manager

Time to add some extra firepower to our vehicle! In this chapter we will learn how to add working***** turret our vehicle

- Adding turret via **SlotManagerComponent**

While it might look quite advanced at first glance, adding turrets to vehicle is not that complicated if you want to use one of the already existing turrets. Whole procedure can be done in two steps:

## Adding Component

We will need to add the `BaseSlotComponent` via the `+ Add Component` button at the bottom of the Objects Property window. see the image below.

![alt text](/Adding-Turrent/image.png)

click the button and filter for `BaseSlot.`

![alt text](/Adding-Turrent/image-1.png)

This is the one we want.

Select it. Check the list of components and we should find it. You can filter `base` to minimise scrolling.

![alt text](/Adding-Turrent/image-2.png)

Our `BaseSlotComponent` should have a simple layout. Like the image below.

![alt text](/Adding-Turrent/image-3.png)

We need to change the Attach Type to `RegisteringComponentSlotInfo.`

![alt text](/Adding-Turrent/image-4.png)

It will ask you to name the object. call it `M151A2.`

![alt text](/Adding-Turrent/image-5.png)

Now we must assign the `M15A2_gun_mount_M2HB.et` to the prefab slot. Click on the browse (`..`) button and search for the `gun mount`. Use the one in the `ArmaReforger` folders.

The mount should appear on the vehicle. But, it isn’t in the correct place.

![alt text](/Adding-Turrent/image-6.png)

Let’s use the `offset` parameters to move it. changing the offset `y` to `1` should lift the mount onto the roof.

![alt text](/Adding-Turrent/image-7.png)

![alt text](/Adding-Turrent/image-8.png)

