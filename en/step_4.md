## Scoring and Sound Effects



+ __Let’s change our script to keep track of a score within the game.__ We can then use this later to work out when the game over message should appear.
+ Create a new variable. Call it `Score` and make it for all sprites. Leave this variable ticked so it appears on the screen.
+ Change the script behind the **Present** sprite to look like this. Note we have both added sound effects with the `play drum` when Rudolph touches the present.
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
                    play drum [57 v] for (0.25) beats
                    set (Finish) to [1]
                end
                if <touching [Rudolph v]?> then
                    play drum [39 v] for (0.25) beats
                    set (Finish) to [1]
                    change [Score v] by [1]
```

Let’s add some music to the game:

+ Import the sound file **Jingle_Bells.mp3** to the __Stage__.

+ Add the following script to the __Stage__. This will `set score to 0` when the game is started. It will also play Jingle Bells while the game is being played.
```blocks
    when FLAG clicked
        set [ScrollX v] to [0]
        set [Score v] to [0]
        play sound [Jingle_Bells v]
```

Note, if at first the music sounds ‘choppy’, save your project, close Scratch and then open your project again.

## Test Your Project

__Click the green flag.__ Does the score change when Rudolph touches a present?



