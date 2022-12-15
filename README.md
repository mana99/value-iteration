
Value Iteration
===============

This applet shows how value iteration works for a simple 10x10 grid world. The numbers in the bottom left of each square shows the value of the grid point. The blue arrows show the optimal action based on the current value function (when it looks like a star, all actions are optimal). To start, press "step".

There are 4 actions available: up, down, left and right. If the agent carries out one of these actions, it have a 0.7 chance of going one step in the desired direction and a 0.1 chance of going one step in any of the other three directions. If it bumps into the outside wall (i.e., the square computed as above is outside the grid), there is a penalty on 1 (i.e., a reward of -1) and the agent doesn't actually move.

In this example, there are four rewarding states (apart from the walls), one worth +10 (at position (9,8); 9 across and 8 down), one worth +3 (at position (8,3)), one worth -5 (at position (4,5)) and one -10 (at position (4,8)). In each if these states the agent gets the reward when it carries out an action in that state (when it leaves the state, not when it enters). You can see these when you press "step" once after a "reset". If "Absorbing states" is checked, the positive reward states are absorbing; the agent gets no more rewards after entering those states. If the box is not checked, when an agent reaches one of those states, no matter what it does at the next step, it is flung, at random, to one of the 4 corners of the grid world. \[Does this make a difference? Try the non-discounted case (i.e., where discount=1.0).\]

The initial discount rate is 0.9. You can either type in a new number or increment or decrement it by 0.1. It is interesting to try the value iteration at different discount rates. Try 0.9, 0.8, 0.7, 0.6, (and 0.99, 0.995 and 1.0 when there is an absorbing state). Look, in particular, at the policy for the points 2&3-across and 6&7-down, and around the +3 reward. Can you explain why the optimal policy changes as the value function is built? Can you explain the direction in the optimal policy for each discount rate?

You can also change the initial value for each state (i.e, the value that value iteration starts with). See if changing this value affects the final value or the rate that we approach the final value.

You can also change the contrast (the mapping between non-extreme values and colour); this is mainly for showing in classrooms where often we couldn't see the colour changes. You can also change the size of the grid (this makes most sense if you are using the applet viewer).

This is the same domain that is used for the [Q-learning applet](https://www.cs.ubc.ca/~poole/demos/rl/q.html).

---

You can get the code: [VIgui.java](https://www.cs.ubc.ca/~poole/demos/mdp/VIgui.java) (which provides the GUI) and [VIcore.java](https://www.cs.ubc.ca/~poole/demos/mdp/VIcore.java) (which actually does the value iteration), or the [javadoc](https://www.cs.ubc.ca/~poole/demos/mdp/index.html). This applet comes with ABSOLUTELY NO WARRANTY. This is free software, and you are welcome to redistribute it under certain conditions, see the code for more details. Copyright © [David Poole](http://www.cs.ubc.ca/spider/poole/), 2003-2007. All rights reserved.

Copyright © 2006-2010, [David Poole](http://cs.ubc.ca/~poole/) and [Alan Mackworth](http://cs.ubc.ca/~mack/)
