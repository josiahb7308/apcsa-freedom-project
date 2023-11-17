# Entry 1
##### 11/7/23

  I have decided on my tool because I want to be able to create a video game using code and kaboom is a good gateway to be able to do that. I tinkered with Kaboom by messing with sprites and making code that causes the sprite to move in different directions depending on which button out of "wasd" is pressed. I did this because it allowed me to get a better feel for things that I would be doing a lot in a game which is pretty much making certain actions and inputs correspond to certain actions and outputs using sprites. I want to make a platformer inspired by games like "Hollow Knight" and as an extreme "Ratchet & Clank". These games both capture the platformer genre on a more simple side and on a more complex side. This is the code that I came up with to make a sprite move when w,a,s, or d are pressed:

  ```js
keyDown("right", () => {
  player.move(player.speed, 0);
});

keyDown("left", () => {
  player.move(-player.speed, 0);
});

keyDown("up", () => {
  player.move(0, -player.speed);
});

keyDown("down", () => {
  player.move(0, player.speed);
});
```
I learned this code from Kaboom(https://kaboomjs.com/#isMouseDown). This code is pretty popular in most platformers to allow the sprite to traverse the map.

### Tools Considered: 
I considered hacksplaining(https://www.hacksplaining.com/features) and Unity(https://unity.com/). I considered them because hacksplaining sounded and looked very interesting to me and my partner but we could not think of a project that we would both want to do that would involve hacksplaining. I considered Unity because I saw the projects that were made using it and I was very interested into that but the thing is that Unity is mainly a 3d library and most platformers are 2d so it didnt make sense for me to use Unity.


## EDP and Skills
EDP: I am in stage 2 of the EDP which is the research stage because I am learning the code and looking at other examples of games similar to what I want to create to get inspired on how I want to make my game look and run. 

Skills: I am using the skills How to google, and How to Learn, I am using these skills because I need to use the How to google skill to get the best search results that can help me learn and get inspired. I am using the How to learn skill because with the things I google I need to effectively learn them so I can use them well in my own project.


[Next](entry02.md)

[Home](../README.md)
