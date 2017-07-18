## Game over

+ Let’s use our score to work out when the game over message should appear.
+ Change the script on the __Stage__ so when the `Score` a __GameOver__ message.
```blocks
    when FLAG clicked
        set [ScrollX v] to [0]
        set [Score v] to [0]
        play sound [Jingle_Bells v]
        forever
        if <(score) = [10]> then
            broadcast [GameOver v] and wait
```

+ We now need to add in our GameOver message. Add the __GameOver__ sprite to the project (use the **GameOver.png** file).
+ __Add the following script to the GameOver sprite.__ This will `hide` it when the GameOver message is received.
```blocks
    when FLAG clicked
        hide

        when I receive [GameOver v]
            go to front
            show
            stop [all v]
```

## Test Your Project

__Click the green flag.__ Does the score change when Rudolph touches a present?



