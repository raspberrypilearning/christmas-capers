## Falling Presents



+ We now need to add in the presents for Rudolph to collect. Add the **Present** sprite to the project (use the **Present.png** file).
+ __Create a new variable__ by clicking the `Data` and make it for this sprite only, then uncheck the box next to it to remove it from the stage. This will be used to control when the present should be removed from the game.
+ __Create another variable__ and call it `Speed` and make it for this sprite only, then uncheck the box next to it to remove it from the stage. This will be used to control the speed that the present falls down the screen.
+ Add the following script to the **Present** sprite to allow it to fall from the sky. Note that we will use `pick random` to make the present appear in a different place each time.
+ By using the `touching [ Rudolph ]` block we can make the present disappear when touched. We can use this later to keep a score.
```blocks
    when FLAG clicked
        forever
            set [Finish v] to [0]
            go to x: <pick random (-230) to (230)> y: <pick random (50) to (170)>
            set [Speed v] to [-1]
            repeat until <(Finish) = [1]>
                change y  by (Speed)
                if <(y position) < [-160]> then
                    set (Finish) to [1]
                end
                if <touching [Rudolph v]?> then
                    set (Finish) to [1]
```

## Test Your Project

__Click the green flag.__ Do the presents fall from the sky? Do they disappear when Rudolph touches them or they hit the ground?



+ Let’s make the game more interesting by changing the colour of the presents each time they fall. Do this by using the `change colour` block.
+ Change the speed of each present by replacing `set Speed to -1` block. Try different values such as **-10** to **-1**. Your script should now look like this.
```blocks
    when FLAG clicked
        forever
            set [Finish v] to [0]
            go to x: <pick random (-230) to (230)> y: <pick random (50) to (170)
            change [color v] effect by <pick random (1) to (-160)>
            set [Speed v] to <pick random (-10) to (-1)
            repeat until <(Finish) = [1]>
                change y  by (Speed)
                if <(y position) < [-160]> then
                    set (Finish) to [1]
                end
                if <touching [Rudolph v]?> then
                    set (Finish) to [1]
```

## Test Your Project

__Click the green flag.__ Do the presents fall at different speeds and colours?



