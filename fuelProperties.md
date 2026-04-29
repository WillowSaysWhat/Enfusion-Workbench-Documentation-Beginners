# Increasing Fuel Consumption

In  `SCR_FuelComsumptionComponent` and locate `Fuel Consumption.`
![alt text](/Fuel_Properties/image.png)

In the image below, you can see that `SCR_FuelManagerComponent` has 2 Fuel nodes. Your component probably has its `SCR_FuelNode` open. Find the chevrons `>` and close them so your component look like the image below. 

You can see that our car has two fuel tanks (`nodes`), This is common in military vehicles.

![alt text](/Fuel_Properties/image-1.png)

Open the first `SCR_FuelNode` and change the `Fuel Type` to `Diesel.` Do the same in the second `SCR_FuelNode.`

![alt text](/Fuel_Properties/image-2.png)

Change `Max Fuel` to 69  and `Initial Fuel Tank State` to 60.  You may need to close the chevron `>` on `Fuel Cap Position` to replicate the image below.

![alt text](/Fuel_Properties/image-3.png\)

# Increasing Fuel Consumption

In  `SCR_FuelComsumptionComponent` and locate `Fuel Consumption.`

![alt text](/Fuel_Properties/image-4.png)

The `Fuel Consumption` value is the amount of `Litres` consumed at max power RPM per hour. Let’s change the value to `145.` This will cause the car to consume fuel very fast.