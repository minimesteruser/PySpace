# Step 2: Add Scenery

Let’s start by adding a background to the game scene. This can be done with a couple more `screen.blit()` calls.

At the end of section #3, after loading the player image, add the following code:

```python
sky = pygame.image.load("resources/images/sky.png")
```

This loads the images and puts them into specific variables. Now they have to be drawn on screen. But if you check the grass image, you will notice that it won’t cover the entire screen area, which is 640 x 480. This means you have to tile the grass over the screen area to cover it completely.

Add the following code to game.py at the beginning of section #6 (before the player is drawn on screen):

```python
    for x in range(width/grass.get_width()+1):
        for y in range(height/grass.get_height()+1):
            screen.blit(grass,(x*100,y*100))
```

As you can see, the for statement loops through x first.
Then, within that for loop, it loops through y and draws the grass at the x and y values generated by the for loops.

[<<< Last Step](./step1.md) | [Next Step >>>](./step3.md)