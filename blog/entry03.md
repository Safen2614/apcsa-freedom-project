# Entry 3
##### 2/12/24

# How I added animation

I used a [video](https://youtu.be/FF6kezDQZ7s?list=TLPQMTEwMjIwMjSsCN0sWIbRhQ) first to help me start this journey.

What I first did was to make a new project to test out this animation thing. After that, I added the same model he had which is the [Ybot](https://www.mixamo.com/#/?page=1&query=Ybot&type=Character) from the website called Mixamo. Mixamo also has many other things like animation so I then downloaded a walking and a running animation. I then needed to add an animator controller that would allow us to use animation in our model. I then had to open up the model package and duplicate the idle animation inside it because it wouldn't allow me to move it anywhere. Then I made it the default state so it will be played the second I press play. So then it worked!

## How I used the animation when the player presses the key w

What I had to do was to make a boolean animator parameter and it was true when the player pressed w and false when they let go. I figured out that I have to uncheck the exist time because it puts a little delay when pressing w. I then added a condition that if `iswalking` is true it is because what we gonna do now is use that in our code. but before that there are animation states and you have to add a tranistion to each one to connect it that you have to add before coding this stuff in. This is a tranistion, it connects both animations so it can switch inbetween each other.

<img width="167" alt="Screenshot 2024-02-11 at 10 46 14 PM" src="https://github.com/Safen2614/apcsa-freedom-project/assets/91745058/e4d105f1-3b36-4eea-9c13-745e65228ac5">
In the code, I just wrote   

```java
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class animstionStateConstroler : MonoBehaviour
{
    Animator animator;
    // Start is called before the first frame update
    void Start()
    {
        animator = GetComponent<Animator>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKey("w")) {
            animator.SetBool("isWalking", true);
        }
        if (!Input.GetKey("w"))
        {
            animator.SetBool("isWalking", false);
        }
    }
}
```
the `void Update()` and the `void Start()` are already added when I started coding. I think its pretty easy to understand the code it just reads when the player hits the w key and lets go. 

### Skills
the skills I gained is embracing failure because I had a lot of errors trying to fix the animation just stopping but all my solutions failed. I also had the Growth mindset because I needed to have patience and persevere. 

#### EDP
in the engineering design process I am making a prototype of my game.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
