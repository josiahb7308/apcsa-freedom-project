# Entry 4
##### 4/30/2024

I have been making progress in the application of my learning of kaboom.js, I have been doing this by making a MVP of my game that has player movement, collisions, score tracking, as well as a game over function and random generated "apples" which work as coins. The official Kaboom.js(https://kaboomjs.com/) website has been my biggest helper through working through the error messages and everything else.

Starting with the apple counter that appears on the screen this is the code behind that.

```java
let appleCounter = 0;
const counterLabel = add([
  text("Apples: " + appleCounter, 12),
  pos(12, 12),
```
This code causes a counter to stay on the upper left corner of the screen which displays the amount of apples collected when the player collides with them. I got this idea from looking at other Kaboom games and how they kept track of the score while the game is running. 

#### Apple Generator and collector

The following code generates apples randomly every 1.5 seconds on the screen.

```js
function spawnApple() {
  const apple = add([
    sprite("apple"),
    pos(rand(0, width() - 16), rand(0, height() - 16)),
    area(),
    "apple",

loop(1.5, () => {
  spawnApple();
```

This code registers when the player has collided with an apple and then it registers it to the apple counter. It also checks if there have been 10 apples destroyed, if yes then it will set `isGameOver` to true and start the game over function which congratulates the player and ends the game.

```js
bean.onCollide("apple", (a) => {
  destroy(a);
  appleCounter++;
  counterLabel.text = "Apples: " + appleCounter;
  if (appleCounter === 10) {
    gameOver(true);
  }
```


### Next Steps
I want to go further than the MVP and proceed to add the following things: platforms, obstacles, apple generation that isnt random, and hopefully enemies because I think that would elevate the game by a lot if we were able to do that. There is so much more work to do but I am glad that I am understanding what functions to use when and how to make ideas I have in my head into a reality in the game, even though the execution isnt great as of now.

### EDP & Skills
I would say I am still in both the 3th stage and 4th stage of the EDP which are imagining and planning. I am imagining how my game will work while taking actions towards learning things that I will need. I am planning how I will use these things that I am learning to make an intriguing and interactive game. I am starting on stage 5 which is creating a prototype because I started to make a barebones prototype using the things that I learned. The next chunk of my time will be spent on making this prototype better and closer to a finished product. I am using the skill How to learn by learning the skills I need to make my game the way I want to. I am also using the skill of creativity by imagining how I want my game to be and taking steps towards it.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
