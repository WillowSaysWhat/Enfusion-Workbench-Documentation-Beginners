# Modding Driving Behaviour

Following topics will be covered in this paragraph

- Basics of wheeled simulation
- How to change engine parameters
- Changing of driving characteristics

# Wheeled Simulation Overview

Wheeled vehicles simulation is contained in **`VehicleWheeledSimulation`** component. In that component, after expanding **Simulation** list, you can find five major categories:

- **`Engine`** - responsible for engine simulation
- **`Clutch`** - contains all parameters controlling clutch simulation
- **`Gearbox`** - here you can change gearbox settings like amount of gears, gear ratios or gearbox latency
- **`Differentials`** - differentials controls
- **`Axles` -** contains definition of each axle together with wheels and tyres

# Changing Engine Parameters

We can change the `Engine` power by increasing the value of `MaxPower`.

If all Chevrons `>` are closed. Open `Simulation.` It sits 3rd in the list - below `Animation.` 

Here you will see the sub-lists for `Engine,` `Clutch,`  `Gearbox,` `Differentials,` and `Axles.` 

Open `Engine.`

![alt text](/Driving-Behaviour/image.png)

Find `Max Power` it is 2nd in the list, below `Inertia.` 

Change `Max Power` to 255.

Also, Change `Max Torque` to 272Nm.

This should make the vehicle excelerate faster.

# Modding The Steering

Expand the `Axles` chevron `>` This is a car, so there should be 2 `Axle` chevrons `>` inside.

![alt text](/Driving-Behaviour/image-1.png)

Open the first `Axle` in the list. This is the front axle.

Inside this list we will find `Suspension.` The first value is `Max Steering Angle.` Set it to `48.`