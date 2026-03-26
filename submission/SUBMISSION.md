## Tinkercad Circuit Link

```
https://www.tinkercad.com/things/cjiWyJmyByb-swanky-blorr?sharecode=4udTVf_bfonKHtLPoxTf221k02vOViH6yGrz9TKm_ZU

I tried to change to public visibility, but it stated that it was pending review. I didn't want to risk y'all not having access, so here's a share link instead!
```

## Program Explanation
```
Assumptions/design choices made:
-> The feedback blink was implemented as 3 blinks as 1 blink is not very obvious in what feedback it's giving.
-> Serial monitor output is published for both valid and false starts.

In my design, I've used an arduino, a pushbutton and an LED to create the reaction time tester. 
I started with implementing the pulsing of the LED once armed. The fade in and fade out was implemented using analogWrite. The duration was calculated using the random function within the given range of 2-10. If a false start was detected, the rapid blinking function was run, and the false start recorded.

I put all of this in an armedState function with a boolean output to indicate if a false start occurred or not. If all is good, it moves on the reaction testing step. The millis() function was used to calculate the reaction time. I trialled and errorred my way through different pattern delay times for the three different states and implemented 3 blinks to give feedback appropriately.

Following this the system returns to idle.
```
