# Make a GameMode_Plain

To start coding in the Enfusion Workbench, we need to set up a simple world for our script to manipulate.

We can’t just press a play button like a normal coding editor.

Let’s set up a world like we did during the capture an hold video.

Go to `ArmaReforger/worlds/Eden/Eden.et` and double-click on it.

![alt text](/beginnerScripting/image.png)

This will open the `World Editor.` 

Now click on the white page symbol to `Save` the world. Call it `OurScriptingWorld.`

Rename the `default` layer to `A_Managers`

![alt text](/beginnerScripting/image-1.png)

Add the list of prefabs in the image below by searching for them in the `Resource Browser.`  Drag and drop them into the window, then they will appear in the layer.

![alt text](/beginnerScripting/image-2.png)

Let’s add a script to the `GameMode_Plain` prefab. Add an `OnGameStart` and a `UserScript` script to the prefab by going to the blue `Script` dropdown menu and clicking the `+` add button.

Just close the Script Editor after selecting `OnGameStart` This will return you to the blue `Script` drop-down where you can select the `UserScript`

Now, when you click either `edit` button, both will lead you to the `UserScript`.

A `UserScript` allows you to access the area of the class that is outside the `OnGameStar()` method.

If we didn’t have a `UserScript` we would be unable to click outside the Method. This prevents you from writing good code. The image below is the `UserScript`

![alt text](/beginnerScripting/image-3.png)

This is without the `UserScript.`

![alt text](/beginnerScripting/image-4.png)

The software will not let you click outside the method. You must access the `UserScript` to do so.

# Now we can start…

The first thing to learn in programming is “Hello World”. Let’s do it.

Enforce (Enfusion Workbench Script Language) is based on C-Sharp (C#). Except for the very first thing we learn.

To print something to the console in Enforce, it is just `Print();` 

In C# it is `Console.WriteLine();`

Our way is better and easier.

Let’s give it a go.

To make it easier to see in the `World` console, let’s add 3 `Print` statements.

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart() // let's the original logic run.
	{
		
		super.OnGameStart();
		Print("==========");
		Print("Hello World");
		Print("==========");
	}

};
```

Now save and close the `Script Editor`

You should be in the `World Editor`

Don’t forget the semi-colons (`;`).

Pres the play button. It is the green play button on the top menu bar.

![alt text](/beginnerScripting/image-5.png)

Select `Yes to All` when this dialogue box appears.

![alt text](/beginnerScripting/image-6.png)

Scroll the `Log Console` up using your middle mouse button and find your `Hello World.` 

![alt text](/beginnerScripting/image-7.png)

Congratulations, you have made your first `print to console.`

Press `ESC` and return to the `World Editor.` 

Press the `edit` button on your `UserScript` again to open the `Script Editor.` 

We can also do this locally within the `Script Editor.`

 Type `Print("Hello World");` into the `Remote Console.` It is located in the bottom-right of the editor.

 ![alt text](/beginnerScripting/image-8.png)

 While this is a great learning tool, it will only delay the introduction of scripting complexities and the skill of browsing through the `World Console.` So instead of using the handy `Remote Console`, we will be coding in an actual script that can be executed in the `World Editor.` 

 ## Print Format

There is a second `Print` statement in Enforce. It is the `PrintFormat()` statement. Most languages have this. It lets you write out a string of words and place a placeholder in to so you can fill it with a whatever you want, whenever you want. for example:

```csharp

class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart() 
	{
		
		super.OnGameStart();// let's the original logic run.
		
		Print("==========");
		Print("My name is Willow!");

		PrintFormat("My name is %1","Willow"):
		Print("==========");
	}

};

```

In this example you can see the thing added is `Willow.` 

Coding has these primitive containers known as `Variables (vars).`  These are many different types, but for now we will utilise a particular type called a `string`  because we are stringing words together. 

We can create a `string` variable and place `willow` into it.

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart() 
	{
		string myName = "Willow";
		
		super.OnGameStart();// let's the original logic run.
		
		Print("==========");
		// we now use the variable.
		PrintFormat("My name is %1", myName);
		Print("==========");
	}

};

```

Let’s save and exit back to the `World Editor` press play.

This should give you the same output. The change is programmatic.

We can print a whole range of different types of variables. We can change the string of letters to a whole number.

This is known as an `integer` or `int` in Enforce.

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart() 
	{
		int myAge = 45;
		
		super.OnGameStart();// let's the original logic run.
		
		Print("==========");
		// now we change to a number instead.
		PrintFormat("My age is %1", myAge);
		Print("==========");
	}

};

```

We can also do this using the `print` statement too.

To do this we must use `Concatenation` This is the joining of strings and variables to create a finished sentence structure. 

We concatenate a `"string"` + `Variable` together to create a sentence. Try the one below. 

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart()
	{
		
		int myAge = 45;
		
		super.OnGameStart(); // let's the original logic run
		
		
		Print("==========");
		// we now use the variable.
		Print("I am " + myAge + " years old.");
		Print("==========");
		
	}

};
```

You can also do mathematical operations inside a `Print` statement.

```csharp
Print (5 + 5);
```

You can also do the same with variables.

```csharp
int five = 5;
Print(five + five);
```

You can do slightly more complex concatentation using maths.

```csharp
int myAge = 45;
int mykidsAge = 6;

Print("I was " + (myage - mykidsAge) + "when my kids was born.");
```

Math won’t work

```csharp
int myAge = 45;
int mykidsAge = 6;

PrintFormat("I was %1 when my kid was born",(myAge-myKidsAge) );
```

Other Variables

```csharp
string aWordOrSentence = "this is a string";
int aWholeNumber = 5;
float aDecimal = 5.5;
bool isTrueOrFalse = true;
```

You can use both in a `Print` or `PrintFormat` statement

```csharp
string sEntity = "Infantry";
float  fDistance = 150.5;

PrintFormat("%1 is at %2", sEntity, fDistance;
```

# Conventions

When we write `Variables` we start them with a small letter and then every word inside the name is capitalised.

`myKidsAge,` `isReadyToFire,` `distanceInMeters.` 

This is called `Camel Case.`

Booleans (`true/false`) usually start with `is.` 

`isMapOpen,` `isBroken.`

Most variables in Enscript are prefixed with a lowercase letters:

- s for strings, `sPlayerId.`
- i for integers, `iPlayerId.`
- f for floats, `fPlayerId.`

Here is the Bohemia Interactive cheat sheet. For now, ignore the `m_` as this is a prefix for class parameters. We will look at them later.

![alt text](/beginnerScripting/image-9.png)

# Conditionals

Conditionals are your `if/else if/ else` decisions that are the basis for most scripting logic.

Here is an example of an `if` statement in Enforce.

 

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart()
	{
		
		int iPlayerHealth = 100;
		
		super.OnGameStart(); // let's the original logic run
		
		Print("============");
		
		if (iPlayerHealth > 50)
		{
			PrintFormat("Player is %1.", "Healthy"); 
		}
		else
		{
			PrintFormat ("Player is %1.", "Wounded");
		}
		
		Print("============");
		
		
		
	}

};
```

There is also and `Else if` statement that allow you to choose this or that, otherwise this - where before it was this, otherwise that.

```csharp
class GameMode_Plain1_Class: SCR_BaseGameMode 
{
	// user script
	// code here

	override void OnGameStart()
	{
		
		int iPlayerHealth = 100;
		
		super.OnGameStart(); // let's the original logic run
		
		Print("============");
		
		if (iPlayerHealth > 50)
		{
			PrintFormat("Player is %1.", "Healthy"); 
		}
		else if (iPlayerHealth > 30)
		{
			PrintFormat("player is %1.", "Stable");
		}
		else
		{
			PrintFormat ("Player is %1.", "Wounded");
		}
		
		Print("============");
		
		
		
	}

};
```

# Arrays

An array is a container that holds multiple slots of data. 

```csharp
array<string> letters = {"Alpha", "Bravo", "Charlie"};
```

Then we can print them to the console by using the this syntax.

```csharp
Print(letters[0]);
Print(letters[1];
```

You will notice that our array has a index value of zero `letters[0].`

In coding, all lists, vectors, and arrays start with an index of zero. One `1` is the second index place. Confusing yes? 

we can `insert` new data.

```csharp
letters.Insert("Delta");
Print("letters array has " + letters.count() + " indexes");
```

Here is an example using an array with conditionals

```csharp
// Create an array of numbers
		array<int> numbers = {1, 5, 10};

		// Check specific values using if statements
		if (numbers[0] == 1)
		{
			Print("First number is 1");
		}

		if (numbers[1] > 3)
		{
			Print("Second number is greater than 3");
		}

		if (numbers[2] == 10)
		{
			Print("Third number is exactly 10");
		}
```
# For Loop

A for loop repeats instructions a specific number of times. 

```csharp
for (int i; i < 5; i++)
{
	Print("Count: " + i); // prints ("Count: ") 0, 1, 2, 3, 4 then leaves (i < 5)
}
```

A for `foreach iterates over an array. 

```csharp
array<string> weapons = {"rifle", "pistol", "Grenade"};

foreach (int i, string weapon : weapons)
{
	print("weapon: " + weapon);
}
```

If you need to modify the element, use the `for` loop. A foreach is read only.

Foreach is great for displaying data from an array.

Here is an example of modifying an element using a for loop.

```csharp
array<int> numbers = {1, 2, 3};

		for (int i = 0; i < numbers.Count(); i++)
		{
			numbers[i] = numbers[i] * 2; // modify value
			Print("Updated value: " + numbers[i]);
		}
```