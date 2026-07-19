# Reflection – Daily Schedule Simulator

## What was your approach to designing the schedule?
I ended up going with a condensed version of what the most straightforward approach to this assignment
\- calling setTimeout() 24 times with their times being set apart by n seconds. I used a loop to 
get all 24 calls at the same time, using 2500 * i to space out their executions to be once every 2.5
seconds. Doing this also let me write out my schedule in an array, and I had to make a function to 
properly convert i to the right 12-hour time, which did also allow me to print out whether it was 
AM or PM. The alternate method I assume you could approach this assignment is by having a recursive 
async function, have a index variable set outside of it, and use await to ensure everything got displayed
at the right time. But I didn't try that method since this felt easier.

## What was one challenge or unexpected behavior you encountered?
Nothing to surprising or challenging from this assignment, but to be fair, I took a simple and 
straightforward approach, so it was pretty simple to get the logic down. I did make the mistake that I
saw warnings about, and that is that I wrote some code outside of the setTimeout function that didn't
seem to effect the display, and that's just because those calls happened immediately and now when the 
code was actually being executed due to the setTimeout delay.

## What does this assignment teach you about async code?
It would be insanely difficult to create code that behaved like this without async code. The only idea
I can think of it to have the computer do an arbitrary work to delay the execution of 
output.textContent calls, but that would be a complete waste of computing power and time. When we need
code to be timed properly, async code will be greatly useful.

## What creative element did you add?
I decided to add a chance at a random event and a changing background color. The random event I had
a good idea on how to do. I just generated a random number, and when the loop hit that number, instead
of printing out the event that's correlated with that time, it displays that I took an "unexpected nap"
instead, because I do sometimes just fall asleep during the day. The background change involved more
research on my part. I figured from seeing that we can use document.getElementById() to get parts of
the html document that I could do the same with the body, so that was the first thing I had to search up.
I then just added that inside the fucntion passed into setRandomTime so that each call would also chnage
the background color, but the syntax for that differs from retrieving text content from a &lt;div&gt; 
element. That last obstacle was just going backwards in an array, and figuring out the right math to make sure
it was working properly.

## How does this project simulate or differ from real-world schedules?
For one, it only runs for a minute instead of a 24 hour day. Two, it can only list a defined set of 
activities that don't accurately describe my day. Never once does my simulator mention when I eat, but 
I do have that scheduled in my day. It'd just be odd to have an hour of my simulated schedule dedicated
to a meal, but that's because I made the simulation change every hour. Plus, I had to actually thing 
about the structure of my day and jazz it up to be more exciting to see play out. The truth is that I
have no hard set schedule, and most of the day is spent doing nothing productive.
