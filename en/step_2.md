## Make Rudolph fly



+ Start a new Scratch project. Delete the cat by right-clicking it and selecting Delete
+ Replace the background with **SkyBackground.png**.
+ Add the Rudolph sprite to the project (use the **resources/Rudolph.png** file)
+ Make Rudolph follow the mouse by using the following script:
```blocks
    when FLAG clicked
        go to front
        forever
            go to [mouse-pointer v]
```

## Test Your Project

__Click the green flag and move the mouse.__ Does Rudolph follow the mouse?



+ To make the game more interesting we will add some moving snowy hills to make it look like Rudolph is flying. Add the Snow sprite to the project (use the __SnowHills.png__ file).
+ Rename the sprite to __Snow1__.
+ Create a new variable by clicking the *Data* tab and then **make a variable**. Call it `ScrollX` and make it for all sprites, then uncheck the box next to it to remove it from the stage. This will be used to control how the hills move.
+ Add the following script to make the hills move:
```blocks
    when FLAG clicked
        set y to (0)
        forever
            set x to (ScrollX)
            change [ScrollX v] by (-1)
            if <(ScrollX) < (-480)> then
                set [ScrollX v] to [0]
```

## Test Your Project

__Click the green flag.__ Do the hills move? What happens as the hills move to the side of the screen?



+ Let’s fix the issue with the snowy hills suddenly reappearing. Add a second set of hills to the stage. Use the __new sprite from file__ button to add the Snow sprite to the project again (use the **SnowHills.png** file).
+ Rename the sprite to __Snow2__.
+ Add the following script to the Snow2 sprite to allow the second set of hills to follow closely behind the first:
```blocks
    when FLAG clicked
        set y to (0)
        forever
            set x to <(ScrollX) + [479]>
```

## Test Your Project

__Click the green flag.__ Do the hills move? Has the issue with the reappearing trees been fixed?



