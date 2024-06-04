# Entry 5
##### 6/3/2024

### How I have been learning my tool?

At first I and my team wanted to make a game thats a 3rd player view. So then I started to look at videos that could help me. So I started with this [youtube series](https://www.youtube.com/watch?v=-FhvQDqmgmU&list=PLwyUzJb_FNeTQwyGujWRLqnfKpV-cj-eO) it tought me a lot of how mixamo (mixamo is a platform to get characters and animation from for free) and how to code and use the animation that I got from mixamo in the character. After getting my charecter and animation I had to import it to my unity game. I then had to add a animator component to the charecter game object. Then, an animator controller is created and assigned to the controller of the animator component. In the animator controller it is a window that has 2 sections in that window. The first thing you would noitice is the grid pane that is where the animation states are created, modified and connected. An animation state represents a single animation, like walking, idle, or running. To add the animtion to the grid you first check the loop box and then drag it to the grid and it will place it on the grid. I added the idle and walking animation you have to add a transition between them. I had to set the idle animation state as the deafult state so that will make it if nothing is happening the idle state will keep on playing. He then teaches me how to use boolean values to change between animation states. So then if you remember I talked about there was 2 sections in the animation controller. This is the second one, you could add parameters in the to use for coding in the transtions. So then I added a `iswalking` boolean. The expectation is that the `iswalking` boolean will be true when the player presses `w` to move forward. and false when the player stops holding the `w` key. But at this point the `iswalking` boolean does nothing. YOu then press the the transtion line that connects the two animtions states and add the boolean. But the way to grant your player the control over the value is with code. I added the animation state controller to my charecter and this will script the control of the animation state. 



[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
