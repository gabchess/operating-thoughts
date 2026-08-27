# How I think about building with AI

People ask me all the time how I actually work with AI, day to day. Not the buzzwords. The real mental model, the one I use building agents, running a content pipeline, doing security research on the side. So here it is, the way I'd actually explain it to a friend, not the way a whitepaper would.

## Graphs, not just prompts

Start with a kitchen. Tell one person to clean it and give them one vague line, they wipe the table and call it done. Give them a checklist, they do more. Split that checklist across three people, one washes dishes, one hits the stove, one puts food away, and someone checks the room before everyone leaves. That's basically graph engineering, and it's less scary than it sounds.

Most people still use AI the old way: prompt engineering. You type an instruction, the model spits out an answer. Fine for a short email. Falls apart the moment the job has real parts, because now you're asking one tired assistant to hold the groceries, the recipe, and the calendar in its head at the same time.

Next step up is an agent. It takes a goal, picks up tools, checks files, keeps working through steps instead of answering once and stopping. A worker with a task, some tools, and a little room to act. That's it.

Add a loop and the system stops trusting its first answer. It drafts, checks itself, finds the weak spot, tries again. You already do this. You write a message, read it back, fix the line that sounds rude, then send. A loop is just that habit, built into the machine.

Graph engineering stacks structure on top. A graph is a map of the work. One branch researches. Another checks facts. Another turns notes into a report. Branches that don't depend on each other run at the same time, then everything comes back together at the end. Same as the kitchen: you don't need one person doing every job in sequence if three jobs can happen in parallel.

I use this for content research constantly. I don't ask one model to browse, remember every detail, decide what matters, write the post, and grade its own homework. That's too much weight on one pass. So I split it. One branch hunts for examples. Another checks whether those examples are actually relevant. A third groups the patterns. Then a reviewer asks the only question that matters: did we prove this, or are we guessing?

That reviewer is a second checker, scoring the work against the goal and kicking it back into the loop if it's weak. I've seen setups use a threshold around 85 before anything moves forward. I wouldn't treat that number as gospel for your project. The number matters less than having a bar at all instead of a vibe.

Generation and judgment want different people doing them, even inside a machine. The part writing the answer wants to finish, it gets attached to its own draft. The part checking needs a completely different posture: what's missing, what's unsupported, what breaks in the real world. Separate those two jobs and the whole system gets easier to trust.

Parallel work saves attention too. Send three agents after three independent topics and none of them need to carry the same giant pile of context, each one only carries what it needs. Don't make every worker haul the whole warehouse when they only need one shelf.

Tokens are the small chunks of text a model reads and writes. Load too many and you pay more, run slower, lose focus. So graph engineering is also attention management. You decide what each branch needs to know, what it hands back, and how the final answer gets checked.

None of this means every task needs a graph. Need a recipe idea? A normal prompt is fine. Renaming a file doesn't need five agents and a reviewer. Graphs earn their keep when the job has independent pieces, real risk, or a quality bar you actually care about. Match the structure to the work, or it turns into theater.

## The pipeline, not just one shot

Now zoom out to a real pipeline. Think factory, minus the machines and smoke. A content pipeline: each step takes one input, does one job, hands the result to the next step. Short-form video is the clean example.

The pipeline finds topics that already performed well, filters for brand fit, writes an original script, generates audio and an avatar, edits, schedules, posts. Research isn't writing. Writing isn't editing. Editing isn't scheduling. Keep the jobs separate and each one gets better at its one thing.

Say you and I are making beginner cooking videos. We don't copy another creator. We ask what beginners are actually struggling with: burnt rice, cutting an onion wrong, buying too many gadgets they'll never use. A research step surfaces topics that got attention. A filter step asks the harder question: does this fit our voice, our audience, our standards?

That filter earns its spot because a loud topic that performed well somewhere else can still be wrong for your brand. A trend gets popular by being exaggerated, plenty of the time. So the pipeline needs taste baked in as rules: no fear-mongering, no promises we can't back up, no copying someone else's style line by line. Original output, even when the topic idea came from research.

Then the script, the spoken plan for the video, still built in your voice but grounded in evidence. If a source reports an account grew fast, I can say that source reported it. I can't promise you the same system gives you the same growth. One demo's numbers are not a law of physics.

From there, audio: a real recorded voice, or a generated one if you've actually got the rights and setup for that. Then maybe an avatar, a face or character speaking the script. Then editing, cutting dead air, matching visuals, adding captions, making it watchable. Then scheduling, which just queues the post for later.

Some setups chain coding agents, avatar tools, voice tools, rendering, browser automation, and a scheduler to do all this. The point isn't which tool. It's that each tool does the one job it's actually good at, and the handoff between steps stays clean.

Triggers matter more than people think. A trigger is just whatever kicks off a process, a morning alarm, a calendar time, whatever. Research, production, and posting should each start on their own trigger, because they need different context. If posting only needs the finished video, caption, and time, it doesn't need to reload every research note. If editing only needs the script and audio, it doesn't need every topic you rejected. Split triggers cut repeated context, and they make failures cleaner: if posting breaks, Monday's research is still sitting there fine.

Concrete version: Monday's research trigger surfaces twenty topics, the filter keeps five. Tuesday's production trigger turns those five into scripts, audio, video drafts. Friday's posting trigger publishes whatever got approved. If the avatar generation blows up on Tuesday, Monday's research doesn't disappear with it.

I want to be careful with the word automatic here. I've seen strong claims about automation, follower growth, revenue, hours saved. Treat those as one source's example, not a promise for your setup. A system running many steps by itself still needs human review, especially the moment it speaks under your name to your audience.

The safer version: automate the boring handoffs first, let software move finished pieces between steps. Keep a human on claims, tone, approvals, brand risk. The word automatic stops sounding good fast if the pipeline publishes nonsense while you're asleep.

Research tells you what people care about. It can't tell you what you stand for. A script generator drafts. It can't know when a line crosses a boundary unless you've given it the rule and someone actually checks the output.

## The harness around the model

Graphs and pipelines are the shape of the work. The next question: what surrounds the model so it actually behaves? That's harness engineering, and despite the name it's a simple idea.

A harness is the control layer around the model, the rules, files, tools, memory, permissions, and checks that keep it on track. Think of a car seat for a kid. The engine moves the car. The harness keeps the kid safe. The model is the engine. Everything I build around it is the harness, and that's what keeps the work useful instead of dangerous.

Layer one is the prompt, the instruction itself. "Write an email to a client." Fine for something small, but it carries almost no structure.

Layer two is context, the information the model actually needs. Client name, the problem, our tone, what we already promised, what to avoid. Skip the context and the model guesses. Feed it in and the answer usually gets better fast.

Layer three is the harness proper. It tells the agent what it's allowed to read, which tools it can touch, which rules it has to follow, how to check its own work, and which actions need my sign-off first. That's the difference between a clever answer box and an actual work system.

Say I want an agent to help build a landing page. The prompt: make a landing page. The context: the audience is beginners, the product teaches AI workflows, keep the tone calm, no income promises. The harness goes further: brand notes, design references, a folder where the source material lives, a rule that every claim needs evidence, a test command, and a deployment step that waits for my approval.

Guardrails live inside the harness. A guardrail is a hard boundary, don't delete files, don't send emails, don't touch billing, don't publish without approval. Not a moral lecture, just an operating rule that stops the system from taking a step nobody authorized.

Tools too. A tool lets the agent do something past plain text, search files, open a browser, read a calendar, build a slide deck, run tests, ship a page. Tools make agents useful and they raise the stakes at the same time. Anything that can act in the world needs permissions and checks wrapped around it.

Memory is the system remembering stable facts, this brand avoids hype, this codebase runs its tests with this command. Memory goes stale fast, though. If a fact might have changed, the agent should go check the current source instead of trusting last week's note.

Skills are reusable instructions for one kind of task, how to build a slide deck, how to review accessibility, how to draft a report. Think of a skill as a recipe card. It doesn't cook the meal itself, it tells the worker how this kitchen wants the dish made.

Deployment belongs here too, putting something where other people can actually touch it. A real harness spells out what gets checked before release, who approves it, and how you confirm the live version matches the plan.

Verification is what keeps everyone honest. Did the output follow the rules? Did the tests pass? Did the page load? Did the script avoid claims it can't back up? Did the agent only touch the files it was allowed to touch? Skip verification and the harness is decoration.

I'll say this plainly: the harness around a model can matter more than which model you pick, once the model is already good enough for the job. I wouldn't turn that into a universal law. A strong model with zero harness can still do real damage, waste real money, and cause real confusion.

Stories about coding agents doing wild things make the tools sound safer than they are. I'm not going to turn any one story into proof that a specific tool is safe. The actual lesson: put boundaries around anything before it touches files, inboxes, calendars, deployments, contracts, or money.

Same logic applies to review. Whoever builds the thing wants to finish it, and if that same agent also grades its own work, it defends its own choices. A separate reviewer catches blind spots because its whole job is different from the start. Ask an agent for a ten-slide lesson plan, a separate reviewer checks whether slide one assumes too much, whether the examples fit beginners, whether any claim needs a source. Then the builder fixes only what's actually weak. That's a harness doing real work: roles, checks, a path back to correction.

The model is one part of the system. I get better results with a harness wrapped around it: context, tools, memory, guardrails, a reviewer that isn't the builder, and human approval on anything that actually matters.

## Five gaps that aren't the model's fault

Every tool has gaps. A coding agent can feel unstoppable and still whiff on basics. I think about five common ones: video understanding, research depth, project memory, visual design, token cost. Framing it this way stops me from treating one agent as one magic brain.

Video understanding first. A text-based agent handles a transcript fine. A video is more than words, it's frames, timing, faces, slides, cuts, captions. Give the agent only the transcript and it can miss what's actually on screen. Hand me a transcript of a cooking video and I'll understand the recipe. I won't know if the shot was blurry, if the knife technique looked dangerous, if the caption covered up the ingredient. Video needs visual evidence, not just words.

Research depth is next. A quick browse comes out shallow. A heavy research run gets slow and expensive. The middle ground routes different research tasks to different tools or document systems depending on what's actually being checked. Checking a company needs broad search. Checking a contract needs close reading. Checking a technical claim needs primary docs. One research mode for everything either wastes time or misses what matters, so the routing has to match the risk.

Project memory is third. Big projects scatter the important facts across a hundred files. Load everything and you burn tokens without necessarily keeping the thread. Load too little and the agent starts guessing. A project map, basically a guide to what lives where, fixes this by letting the agent navigate before it acts instead of stumbling through the whole codebase first.

Fourth, visual design. Coding agents ship interfaces that function and still look plain, sometimes awkward. Design needs taste: spacing, hierarchy, contrast, motion that helps instead of distracting. Design-focused skills and an actual look at the rendered screen help here, though I wouldn't call either one a guarantee. Ten buttons that all look equally important, and you have no idea where to look. Random spacing makes a page feel cheap. Animation that moves too much gets tiring fast. A real design fix hands the agent references, standards, and a way to look at the actual screen, not just the code behind it.

Fifth, token cost. Long context costs money and slows the agent down. I've seen one cost-saving setup report something like a 20% reduction in token use, in its own tests. I wouldn't bank on that number for a different project. The number is less useful than the habit: don't load what you don't need, summarize what's stable, split independent work, keep reusable instructions in skills, use project maps, route research to the right tool, check if a cheaper step solves it before handing the model everything.

These five gaps stop lazy diagnosis. Coding agent fails, and the problem might not be the model at all. Maybe it had no visual access. Maybe the research path was wrong. Maybe nobody built a memory map. Maybe the design brief was vague. Maybe the context was bloated and expensive. Find the missing layer instead of blaming the whole tool. No video access, add visual evidence. Can't remember the project, add a map. Design comes out bland, add references and an actual screen check. Spending too much, cut the context and split the work. Match the fix to the actual failure.

## Four agents I actually use

Now bring it down to an actual day. Four practical agents, built around coordination, creativity, clarity, and conversation. I like that order because it starts with the day you already have, not some fantasy office where everything's clean.

Coordination first. It stops your day from leaking through interruptions. However you feel about the exact numbers on workplace interruptions, emails, and chat pings, the everyday point stands on its own: if messages and meetings run your attention, you need something that makes the day visible.

A coordination agent reviews yesterday's unread email, sorts it into urgent, informational, ignore, then lines up the urgent stuff against today's and tomorrow's calendar. Sounds small. It's not, because email and calendar usually live in separate parts of your head. One shows demand, the other shows time. The agent puts both in one view.

Draw the line clearly here. The agent can draft an urgent reply. It should not send anything without you looking at it first. Reading is one level of trust. Drafting is another. Sending is higher still. Scheduling gets even higher, especially once the calendar touches clients, family, travel, anything sensitive. Earn the trust step by step, don't hand it all over on day one.

This is where connectors come in, giving the agent access to something like Gmail or your calendar. Read the permissions slowly before you connect anything. Grant only what you're actually comfortable granting, and keep manual approval on sending email, changing calendar events, or acting under your name.

There's a shape that works well for this kind of prompt: task, tool, categories, output, boundary. What to do, where to work, how to sort it, what you want back, what it must never do. Review unread messages, use Gmail, group by urgency, give me a short plan, don't send anything without my say-so.

Creativity is the second agent. It doesn't mean the machine becomes the artist and you vanish. You bring the rough material, it helps shape something you can actually judge. Rough notes turning into a beginner lesson with eight or ten slides, the agent asking follow-up questions before it fills any gaps, that's the shape.

That last part matters more than it sounds. If the agent doesn't understand your notes, you don't want it inventing the missing piece. You want it asking. A good creativity agent turns confusion into a question first. Then it builds a real draft, a deck or a document, and you edit from there. You're still the director. It just hands you a starting point that beats a blank page.

Skills help here too. A presentation skill teaches it to build an actual slide file instead of dumping text in chat. A brand skill teaches it your colors, fonts, layout rules. Still check the result yourself, because a file that exists isn't the same as a file that teaches anything.

Clarity is third. It helps when something's too spread out or too dense to hold in your head. Two modes I actually use: telescope and microscope. Telescope looks wide. Microscope looks close.

Telescope mode when information is scattered, say you want to understand a company before a partnership call. The agent gathers public information, reviews past messages only if you've deliberately connected that account for research, and hands you a tight brief. Ask it to verify and stay concise, because broad research turns into a pile of interesting noise fast if you let it.

Microscope mode when the risk lives inside one document. A contract's the obvious example. Ask for a summary and a confusing contract just gets shorter while the dangerous clause hides in plain sight. Better ask for a five-column table instead: what the clause says, what it means in plain language, why it matters, how risky it is, what question to ask before you sign.

Sensitive data needs real care here. Don't bring private names, account numbers, client secrets, or personal terms into the agent if it doesn't need them. Mask or strip what it doesn't need to see. Clarity shouldn't cost you exposure you didn't need to take on.

Conversation is the fourth agent, and it's the one people underestimate because it feels less technical. Might be the most human of the four. It lets you rehearse out loud before something high stakes: a client closing call, an interview, teaching a live class, a negotiation.

Voice is the whole point. Type the answer and you might think you know it. Say it out loud and your mouth finds the weak spots. You hear yourself hesitate. You notice the price answer going defensive, or the explanation running too long. The agent plays the other person, asks one question at a time, pushes back, then flips into trainer mode once the simulation's done.

Trainer mode is where the real work happens. After the role play: what went wrong, where did I ramble, how do I answer that better next time. The goal was never memorizing one perfect line. It's building the judgment to improvise when the pressure's actually on.

Start with one of these that makes your work visible before it starts acting for you. Let it coordinate, create, clarify, or rehearse. Keep the approval gate around email, scheduling, connectors, contracts, and anything sensitive.

## Still the director

All five pieces connect. Graph engineering teaches me to arrange work into branches, loops, and verification. The content pipeline teaches me to keep research, writing, production, editing, and posting from blurring into one blob. Harness engineering teaches me to build the control layer around the model itself. The five gaps teach me to diagnose the missing layer before I blame the whole tool. The four practical agents bring all of it back down to an actual Tuesday.

Underneath all of it: structure around the model. The model is strong and still needs direction, the right context, the right tool, the right boundary, the right check. Feed it your confusion and it multiplies confusion. Give it a clear job and it multiplies clear work.

Human judgment doesn't go anywhere in this. I decide the goal. I decide what counts as good. I decide which permissions are safe to hand over. I decide when a source is strong enough, when a claim needs softening, when a draft stays private. The agent speeds up the work. Speed was never the part that required judgment.

Strip the hype off any of this and it gets almost boring. A graph is a map of work. A loop is a check and a retry. A harness is a control layer. A trigger starts a process. A skill is reusable instructions. A verifier is a second checker. None of it needs the machine to be magic.

I stay the director on all of this. I set the boundaries and hand the model tools that actually help. Then I verify what comes back and keep judgment sitting exactly where a mistake would cost something real.
