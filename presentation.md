# IMPROVING PERFORMANCE BY HACKING THE USER
 - perface
## Monolouge
Performance isn't really about milliseconds and kilobytes, it's about perception. If you are waiting for a bus for 15 minutes, but it feels like 30, does that make it better? People hate waiting.

Amazon.com feels like it loads in about 2s - 3s, but it isn't fully loaded for ~15s. Performance is not the same as perception.

## LET'S DO AN ACTIVITY
Give everyone a post-it note and pen, tell them we will all be waiting and the writing down how long they think they waited for. Participants shouldn't mentally keep track of the time, or watch a clock (that's cheating). At the end of some time between 30s - 2min have the participants write down how long they waited and compute the average. 

- distribute post-it notes & pens
- we will be waiting a period of time, then recording how long we *think* we waited
    - no cheating (counting, clock-watching, etc.)
- after 30s - 2min stop the activity, collect the papers and calculate the average.

## STORY TIME
### THE AIRPORT & THE BAGGAGE
In [2009 the Houston Airport](http://www.nytimes.com/2012/08/19/opinion/sunday/why-waiting-in-line-is-torture.html) regularly recieved a large number of complaints about the time it took for checked bags to reach the luggage carousel. On average, it would take bags 8 minutes to make their way to the carousel. Passengers would spend 1 minute walking to the baggage claim, and 7 minutes waiting for their luggage to arrive. The executives at the Houston Airport were able to basically stop these complaints by parking planes further away from the baggage claim area, and by sending passenger's luggage to the furtherest carousel. This caused passengers to spend 6 minutes walking and 2 minutes waiting. 
### WHERE THE MAGIC HAPPENS
Disney is a master of having people wait in lines, and have been working on this issue for decades. There are several tricks they have in their toolbelt for waiting customers. At the entrances to every ride is an estimated time of how long it will take to go through the line (often overexaggrated). Every line is filled with things to look at, mini-games, and visits from disney characters when a line becomes exceptionally busy. Each line is long and wound up, there is a steady stream of forward motion with only short stops every so often. 

## ACTIVE PHASE VS. PASSIVE PHASE
Waiting can be divided into 2 phases, the active phase and the passive phase. The active phase is is characterized by the user's mental activity, usually some sort of mental or physical activity like riding a bike or solving a puzzle. The passive phase is the period of time in which the user has no choice or control over the waiting time, such as waiting in line. Research has shown that, on average, people in the passive phase overestimate their waiting time by about 36%.

 - Reveal results of activity. What was the wait time, what was the average estimated wait time?

## JUST NOTICABLE DIFFERENCE (20% RULE) ([Weber-Fechner Law](https://en.wikipedia.org/wiki/Weber%E2%80%93Fechner_law))
Some of you may have worked on increasing performance before, only to send it to the users and be told "doesn't look different to me", here is a rule-of-thumb to help prevent that in the future. Most users what notice any changes in performance unless there is a 20% change. That means if your page loads in 5 seconds, a user likely won't notice a difference unless you suddenly drop that down to 4 seconds. This pendulum swings both ways, if there is a resource intensive feature that ends up increasing pageload times, it is unlikely that many users will notice, so long as you keep the increase under 20% of what it was previously doing. 

Bear in mind that noticable does not equate to meaningful, users may begin to notice a difference with a 20% improvment, but they won't be amazed by any means, more work is required.

## REFLECTING
### THE AIRPORT & THE BAGGAGE - REVISITED
This story highlights that waiting is what users had a problem with, not the total amount of time it took their luggage to reach the carousel. By having users spending more time in the active phase (walking) and less time in the passive phase (waiting) they were able to reduce the number of complaints they recieved to nearly 0.

### WHERE THE MAGIC HAPPENS - REVISITED
Disney attacks waiting on multiple fronts. By providing an overexaggrated wait-time estimate, they are setting user expectations, and then surpassing them. By providing distractions they are helping to decrease the amount of time their patrons spend in the passive phase. By keeping one line that makes a steady trickle of progress, their users feel they are progressing and getting closer to their goal.

## WHAT ARE OTHER TECH COMPANIES DOING?
Youtube makes an effort to get users into the active phase as quickly as possible. They could spend 30 seconds downloading the full video to your browser before playing, thus putting the user in the passive phase for that length of time. They instead only download the first few seconds before playing the video (switching the user to the active phase) and continue downloading the rest of the video in the background.

The Safari browswer for iOS provides a "Top Hit" selection whenever a user is inputting a new url into the search bar. The top hit is the website safari thinks is the most likely one you are trying to type in. As soon as any website appears as an option for the Top Hit, Safari will begin downloading the website in the background. If the user does chose that site, their website will already be loaded on the phone.

## What can you do?
Knowing the difference between the active and the passive phase, you can optimize your site so that it places the user is the active phase as quickly as possible (thusly minimzing the amount of time in the passive phase).

### Preemptive Start
The most time-intensive part of nearly every website is the amount of time it takes to load a page, an about 90% of that time can be attributed to getting all html, js, css, and other assets to through the network to the user's computer. By smartly requesting the resources your webpages need you can drasticaly increase load times. Take a look at the following.
    
    dns-prefetch
    preconnect
    prerender
    prefetch
    preload
    async
    defer

### REDUCE PROJECT SIZE
The smaller you make you make each page (focusing on the resources loaded) the faster it will load. Fewer loaded resources is better, and smaller loaded resources is better.

Another option is to load a minimal amount of css and javascript, and use javascript to load the remainder of your scripts and styles once the bare essentials are fully loaded.

### Early Completion
The most practicle case of this is to only html and necessary resources for content loaded in the viewport onLoad. Once that has been achieved, loading will begin for the rest of the page's content. Amazon and eBay are experts of doing this. A similar example of this technique is when youtube loads part of their video and begins playing it, and downloads the rest.

### Progress Indicators
You should try and optimize as much as possible so that the user doesn't have to wait on progress bars/spinners, however there are times when you're doing a process heavy task that needs time. Here are things you can do so the wait doesn't feel as long
 - Make the progress indicator show actual progress
 - Allow users to perform a task while waiting, such as completing a form while uploading files or playing a mini-game while waiting.
 - Explain what is happening during the wait time
 - If they are waiting in a shared queue, tell them where they are at in the queue. Shared wait times feel shorter.
 - make the user feel comfortable

## Conclusion
"The dominant cost of waiting is an emotional one: stress, boredom, that nagging sensation that one’s life is slipping away. The last thing we want to do with our dwindling leisure time is squander it in stasis. We’ll never eliminate lines altogether, but a better understanding of the psychology of waiting can help make those inevitable delays that inject themselves into our daily lives a touch more bearable" - Alex Stone, The New York Times

## ADDITIONAL INFORMATION
 - [Psychology of Queueing: A Case Study of Universal Studios Singapore](http://www.iaapa.org/news/funworld/funworld-magazine/psychology-of-queueing)
 - [Why Performance Matters, Part 2](https://www.smashingmagazine.com/2015/11/why-performance-matters-part-2-perception-management/)
 - [prefetch & friends slides](https://docs.google.com/presentation/d/18zlAdKAxnc51y_kj-6sWLmnjl6TLnaru_WH0LJTjP-o/present#slide=id.g33211238_0_2)
