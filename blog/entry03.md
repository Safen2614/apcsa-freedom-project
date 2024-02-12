# Entry 3
##### 2/12/24

# How I added animation

I used a [video](https://youtu.be/FF6kezDQZ7s?list=TLPQMTEwMjIwMjSsCN0sWIbRhQ) first to help me start this journey.

What I first did was to make a new project to test out this animation thing. After that, I added the same model he had which is the [Ybot](https://www.mixamo.com/#/?page=1&query=Ybot&type=Character) from the website called Mixamo. Mixamo also has many other things like animation so I then downloaded a walking and a running animation. I then needed to add an animator controller that would allow us to use animation in our model. I then had to open up the model package and duplicate the idle animation inside it because it wouldn't allow me to move it anywhere. Then I made it the default state so it will be played the second I press play. So then it worked!

## How I used the animation when the player presses the key w

What I had to do was to make a boolean animator parameter and it was true when the player pressed w and false when they let go. I figured out that I have to uncheck the exist time because it puts a little delay when pressing w. I then added a condition that if `iswalking` is true it is because what we gonna do now is use that in our code. In the code, I just wrote   

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
        Debug.Log(animator);
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


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
