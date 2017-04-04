# Deconstructing Performance

The Oscars happened, they messed up.
16.5 seconds for lalaland site to load
13.2 seconds for moonlight site to load (and that is why they won (a joke) )

Web pages have gotten bloated over the years, but with each year, we are expected to have faster and faster page loads
in 1999 4s page loads was ok, now we need 1s page loads.

**People hate waiting**

In some countries with corruption, there are jobs where people will wait in line for you, so you do not have to wait.

Performance is not mathematics, it is about perception. It is ok if the complete page load takes 15 seconds, so long as the user is not waiting that long. Amazon.com is an example of this.
100ms delayed video was not noticible, 400ms delay was noticiable and was annoying. 

Weber-Fechner Law defines JND (just noticeable difference), for web development this can be simipliefed into 20% rule. 

Noticeable difference != meaningful difference

### 20% Rule
If a new feature slows down anothoer feature, it is fine so long as it slows it down by 20% or less.

People complained waiting 8 minutes for luggage to get off plane. 1 minute to walk from plane to luggage, 7 minutes waiting. The solution was to park the planes further away, people walked for 6 minutes and waited for 2 and the number of complaints dropped to 0.

People in **passive phase** (not doing anything, waiting) over estimate the time in this phase by %36 on average. The passive phase can be reduced by increaseing the active phase. An example is video streaming, you do not wait for the full video to be loaded, only a little bit.

**Optimistic UI** 1-3% of API request reutnr failure, the rest are success. This is my 'smoke and mirrors techniuqe'. Twitter and Facebook both use this. If there is an error, the button goes to a success state then reverts back. 

**resource hints** `dns-prefetch` `preconnect` `prefetch` `prerender` `preload`

**critical path** is the longest path that sits between the user and the resources, you want to reduce this as much as possible. 

Many cross walks have a placebo button to fix a psycholog problem. Waiting is a passive phase and providing the illusion of a button is moving the user to the active state. 
While uploading a file, slideshare provides a form users can fill out about the form while the file uploads, this puts the user in the active phase.

Speaker uses local tools to try and optimize the performance of the LaLa Land website.
The main reason the site is load is because it is JS driven and generates everything on the page it, waits for everything to be generated then loads it. 
After about 2 hours of work, he was able to get content displayed in 2s. Rendering started in 0.921s.
Under the hood, the site takes 15+ seconds to completely load, but the user gets meaningful content in 2s.

## Q&A
Medium.com has low-quality images at first, then comes into focus as the page loads. is that better?
The answer depends on how long you have to wait. In general, the images are totally fine to show in bad quality, users are not coming for the content, not for the images.

Where is the fine line between fast and too fast?
Being too fast does exist, banking sites do not have an expectation of working instantly, users expect a delay. if you provide a __service___ then you want the user to feel the value of the service, so you may want to use a placebo slow-down. 
