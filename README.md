## Instructions on how to interact with the work

Open to see the interface effect without any manual clicks

## Details of your individual approach to animating the group code

### Drive
I chose to use Perlin noise to drive my code

### Properties of the image
I will use Perlin noise to adjust the position and color of patterns to create animations

### Inspiration
When I was investigating this artwork, I found that it was influenced by the New York Broadway and the Rhythmic style of Boogie Woogie When I listen to boogie wooogie on YouTube and watch this artwork, I think of the mechanized rhythm of Charlie Chaplin's assembly line in Modern Times. Inspired by this connection, I plan to incorporate the concept of assembly lines into the interpretation of artworks.

The entire artwork is divided into multiple areas by yellow lines. The larger squares are like workers wearing different colored clothes, while the smaller squares on the yellow lines are like items that move endlessly



### Coding Technique Exploration

1. First, introduce the attribute `this.t` in the Element Class as a parameter to calculate the movement speed of the graphic. Its initial value is obtained from `random(-3,3)` to ensure that it can move in both directions; also use `this.flag=random(-1,1)` to determine whether the graphic moves forward or backward. If `flag` is greater than 0, it moves forward; otherwise, it moves backward.

2. In each iteration update of the pattern, if a child element's `t` is less than 0, then decrease the value of `t` by `random(0.01,0.02)` to make the child element move backward; if `t` is greater than 0, then increase the value of `t` by `random(0.01,0.02)` to make the child element move forward.

3. The movement speed and position of the element are calculated using `noise(this.t)*2-0.5`.

4. When a child element moves to the boundary, it returns to the starting point and randomly changes color, symbolizing the end of one express delivery and the start of another in the delivery process.

