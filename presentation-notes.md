# Preface
  - I'm a very "by-the-numbers" person, this talk is based on pyschology.

# Intro
 > Performance isn't really about milliseconds and kilobytes, it's about perception. If you are waiting for a bus for 15 minutes, but it feels like 30, does that make it better? People hate waiting.
  - Who uses Amazon? Load time?
  - 13s to fully load. But 1.7s to start rendering

# Activity
  - Pass out sticky notes & pens
  - People will wait, then write down how long they *think* they waited

# Stories
## Houston Airport
  - customers complained about wait-times for checked baggage
    - It took bags 8 minutes. 
    - Customers walked 1 minute, and waited 7
  - the solution was to park planes further away
    - bags still took 8 minutes
    - customers walked for 6 minutes, and waited for 2 minutes

## Disney
  - You have to wait at disney, no way around it (yet)
  - They are upfront with how long people will be waiting (they often overestimate)
  - Lines are filled with mini-games and things to look at (keep people busy)
  - Disney characters dispatched to overcrowded lines

# Active Phase & Passive Phase
  - Active Phase - Waiting with some kind of mental or physical activity
    - riding a bike
  - Passive Phase - Waiting with no sense of choice/control
    - waiting in a line
# Just Noticable Difference (20% Rule)
  - performance increases need to be %20+ to be noticable
  - the reverse is true
  - noticable != meaningful

# Examples
## Cross Walks
  - Most city cross walk buttons don't function
  - They are there to give the pedestrian a sense of control
    - passive phase -> active phase

## Houston Airport
  - Passengers: 1m active & 7m passive --> 6m active & 2m passive

# What can you do?
  - Optimize for the active phase
  - 90% of page load times is attribuatable to the network

## Get content ASAP
  - Get content painted on the browser ASAP
    - Small initial page load (with defered scripts, styles, images)
    - use cacheing
    - optimize how assets are loaded (`prefetch`, `preconnect`, etc.) [best bet]
  - Improve Waiting (if you *really* can't remove it)
    - Show actual progress in the progress bar
    - what's happening during the progress bar
    - unique/creative 'progress bar'
    - Task the user while waiting (form on file upload) (mini-game)

# Conclusion
 > The dominant cost of waiting is an emotional one: stress, boredom, that nagging sensation that one’s life is slipping away. The last thing we want to do with our dwindling leisure time is squander it in stasis. We’ll never eliminate lines altogether, but a better understanding of the psychology of waiting can help make those inevitable delays that inject themselves into our daily lives a touch more bearable
 > - Alex Stone, The New York Times
