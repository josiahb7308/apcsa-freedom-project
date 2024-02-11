# Entry 3
##### 2/11/24

I have been continuing to work on learning kaboom.js and the elements I need to know to be able to complete my freedom project. I focused on basic game mechanics necessary for an entertaining and interactive game. The first mechanic was collisions and how to implement that. For example:

```java
// Check for collisions between the player and an enemy
player.collides("enemy", function () {
  // Put what you want to happen when they collide
});

```
This code is definitely going to be used in my project but I will most likely make it so after the collision the player loses health or a life to make it interesting.

The next basic game mechanic I started learning was keeping score to add a challenge and a motivation. This code will make it so when a player picks up a collectible its score goes up which I think is pretty neat. 
```java
let score = 0;

// Increase score when player gets a collectible
player.collides("collectible", function (collectible) {
  collectible.destroy(); // Remove collectible from the screen
  score += 10; // Increase score
  // Update score display on the screen
  scoreLabel.text = "Score: " + score;
});
```
This code will also be used in my project but im not sure if it will be a collectible or like maybe jumping on an enemy im still coming up with the applications for it.

The last one I touched on was making the enemies move and I thought this was really cool because you can make them chase after the player which makes the game more challenging. The code for this is :
```java
// Move enemy towards the player
enemy.action(function () {
  enemy.move(player.pos.sub(enemy.pos).unit().scale(80));
});
```
### Next Steps
I would like to continue learning these basic game mechanics that I am going to need for my project. Some ideas for my next mechanics are adding obstacles and then after that I would like to put them all together within a scene and test it out to see the compatibility of my ideas with each other and with the idea I have for my game. 

### EDP & Skills
I would say I am still in both the 3rd stage and 4th stage of the EDP which are imagining and planning. I am imagining how my game will work while taking actions towards learning things that I will need. I am planning how I will use these things that I am learning to make an intriguing and interactive game. I am using the skill How to learn by learning the skills I need to make my game the way I want to. I am also using the skill of creativity by imagining how I want my game to be and taking steps towards it.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
