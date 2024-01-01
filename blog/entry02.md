# Entry 2
##### 12/18/23

I have been continuing to work on learning kaboom.js and the elements I need to know to be able to complete my freedom project. I focused on a lot of movement because in my last entry I learned how to make the sprites move using the "wasd" keys. In this blog I will be focusing on how I learned how to allow for my sprite to do continuous movement. First thing you have to do is set the scene, then you would create the character and name them whatever you want. You also have to define the players velocity, after that you have to make the code able to handle continuous player movement. The last two steps I had in my piece of code was to normalize the direction to keep a constant speed and then move the player based on the speed. Putting all of that together the code looks like this 
```java
kaboom.scene("game", function () {

  var player = kaboom.add([
    kaboom.sprite("player"),
    kaboom.pos(12, 12),
    {
      y
      speed: 120,
      dir: vec2(1, 0), 
    },
  ]);

 
  player.action(function () {
    var moveDirection = vec2(0, 0);

    if (kaboom.keyIsDown("right")) {
      moveDirection.x = 1;
    }
    if (kaboom.keyIsDown("left")) {
      moveDirection.x = -1;
    }
    if (kaboom.keyIsDown("up")) {
      moveDirection.y = -1;
    }
    if (kaboom.keyIsDown("down")) {
      moveDirection.y = 1;
    }

    
    moveDirection.normalize();

    
    player.move(moveDirection.scale(player.speed));
  });
});
```

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
