# How I think about building with AI

I came to AI through marketing. I'd spent years researching audiences and writing for other people, so I was already used to asking whether something made sense to the person reading it. Ghostwriting made that personal. I had to understand how someone thought before I could write a sentence they'd want to put their name on.

That experience shapes how I use AI. I can generate more versions of an idea than I'll ever need, which puts more of the work into choosing. I need to know what I'm looking for and be able to explain why one version works.

## What I mean by taste

After fifteen years in marketing, I've developed a feel for when a message reaches someone. Sometimes a technically accurate sentence still gives the wrong impression. A product explanation can answer every question the team had and leave the customer confused about what to do next.

I pay attention to those reactions. They tell me something about the work that a grammar check misses.

When I say taste matters, I mean the judgment behind those choices. I bring examples to an agent and explain what I like about them. If the spacing helps me understand a page, I say that. When a draft sounds like me, I point to the words I'd use in conversation. The more specific I can be about the choice, the more useful the feedback becomes.

I still read the result aloud. That's often where I find the sentence I couldn't say to a friend.

## I start with the work

Before building an agent, I want to understand what a person is trying to finish. I ask them to walk me through the current process, including the copying, waiting, and checking they do along the way. Those details tell me where software could help.

A feature launch is a useful example. The team has release notes and a walkthrough, but someone still has to turn them into a campaign. Different people need different versions of the message, and the person reviewing everything has to check what each version promises.

That's the work behind [Launch Factory](https://github.com/gabchess/launch-factory). The agent prepares drafts from the sources. A local builder renders the assets and puts them in a review page, alongside the source evidence and proposed campaign dates. The reviewer can open the video, read each email, and check the claims in one place.

I want the result to be something the team can pick up and use. That means paying attention to the reviewer's time as well as the time spent drafting.

## How I arrange the agents

I split a task when its parts need different information or can run independently. Someone checking product facts needs the source material. An editor needs the draft and enough context to judge whether it says what we mean. Giving each one a clear job helps me see where the work went wrong.

For a small edit, I keep the process small. Larger jobs benefit from a separate review, especially when a mistake would reach a customer or affect money.

I also save the useful output from each stage. If a video render fails, I want to fix the render with the approved script still available. Repeating the research would waste time and introduce another chance to change the message.

A retry needs a reason. I read the error, make a specific correction, and check again. Repeated failure is a reason to investigate the step or ask for missing information.

## The instructions around the model

I spend a lot of time on the context and tools an agent gets. The project needs a clear place for its sources, rules about what it can change, and a way to check the result. I also need to know which version we're reviewing.

That's what I mean by a harness. In my own work, it includes reusable skills and checks that run with the workflow. I keep stable instructions there so a new session can continue without another long explanation. Facts that change still need a fresh source.

When I correct the same behavior repeatedly, I look at what would make the correction stick. A writing preference belongs in a voice guide with an example. A file-handling mistake can need a test. Some actions need an explicit decision from me before they happen.

## Looking at what came back

For Launch Factory v2, verification included rendering a real video and opening the review pages at desktop and phone sizes. I also checked what happened when source files changed during a build. Those checks answer different questions, and I want to know which ones ran.

The same applies to writing. A paragraph can cite a source and still stretch its meaning. I read the source and the sentence together before I'm comfortable using it.

I'm interested in how much of that review I can make easier for the next person. If they have to search through a conversation to find the relevant file or figure out which draft is current, there's still work for me to do.
