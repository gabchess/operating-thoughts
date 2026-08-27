# How I think about GTM

People ask me what GTM means once you get past the acronym, past the funnel diagram everyone draws on a whiteboard. What it means for me is the daily work: building the pipes between marketing, sales, and data, and having the taste to know what a screen should even ask a person to do. So here's how I think about it, the way I'd explain it if we were sitting down together with a whiteboard between us.

## Remove the step, don't add the button

Picture someone cooking dinner. Every tool they own is already out on the counter: three peelers, a garlic press, a mandoline, two pans they never use. They only need to chop one onion. They pick up three gadgets before they touch the knife, and dinner is late because they spent it choosing instead of chopping.

I've watched that same pile show up on a screen. A product that can do a lot still makes the person hunt for the one thing they came to do. The extra steps are the product, even when nobody planned it that way, and people feel the delay even when they can't say why.

I use one word for that pain: a step. A step is anything a person has to notice or remember before they can do the next useful thing. Clicking counts. Reading a label they didn't need counts. Waiting on a field that should already be filled in counts too, and that one's the quiet kind, which makes it worse.

Before I add a field or a button, I ask one question. Do we know where the person gets stuck, or do we only know what we wanted to build? What we wanted to build is easy to defend in a meeting. The stuck point only shows up when you sit with a real person and watch them use the thing without talking. I've shipped whole pages that answered what we were curious about and never touched the actual freeze point.

A stuck point is the place someone stops because the next useful move isn't clear. They've got the onion in front of them and can't tell which tool is for chopping. On a screen that's a long form with a tiny submit button and copy that talks past the job.

Whoever built the screen already knows where the knife is. They skip past the extra tools without noticing, because the path is muscle memory for them. A new person picks up the wrong tool because they're reading the counter the way it got laid out for them, not the way they'd lay it out themselves. I try to sit as that new person.

So I start with what the person needs to decide. Book the call, or leave. Keep this company on the list, or throw the row out. I write that decision as one sentence I could say out loud at a table. If I can't say it that plainly, I don't get to add a control to the screen yet.

Then I take things off the counter. A field that doesn't change the decision gets deleted. I've cut help text explaining a button whose own label was already a verb. A second path added for some rare visitor has cost more build time than that visitor will ever bring back.

Whatever's left has to be obvious. That's the primary action, the one useful thing the screen exists to let someone do. Make it big. Put it where a tired eye lands without searching. Give it a verb someone would say out loud, like book the call or keep this company. If a person has to hunt for it, that's a step you added by accident.

I design the empty state before I design the full one. An empty state is what a person sees before any of their own data has shown up. A blank table lecturing about power features is the counter with every gadget already out. Show the one move that puts the first real thing on the table. Demo data is a kitchen where someone already chopped the onion for you. If a new person can't start from nothing, all you've built is a walkthrough of a counter you already understand and they don't.

Here's a test I run for real. Hand the laptop to someone who's never seen it. Count about five seconds in your head. Don't coach them. A stranger standing behind your shoulder should be able to say what to click next. The moment they hesitate, I take a tool away and try again.

Some rows should never reach a human at all, and that's what a gate is for. A gate is a check that throws a row out before anyone spends real time on it. A dead website ends the work right there. I once dropped a lead because the only public email on the site was info@, and nobody's ever going to answer that mailbox. If I can't find a person who owns sales at that company, I stop, because there's no next move for that row.

I've opened forms that wanted a person's life story before they wanted a name. I've seen a lead row ask someone to visit a website and write notes on it, and nobody had even checked whether the company was still alive first.

The pull is always to add. A stakeholder asks for a field, the field ships, and the old one never gets removed. I've watched a team ship a whole product tour because the first screen confused people, so now a person has to dismiss a popup before they can find the knife. I've been the one who added that popup, once. What moves things forward is deleting until a stranger can chop the onion on their own, without reaching for a peeler first.

## GTM is the pipe between rooms

Now picture a small kitchen with three stations. One person chops. One stands at the stove. One plates. They never look at each other. The onions sit while the pan burns. The plate goes out with the wrong garnish on it. Nobody in that kitchen is slow. The meal fails in the gap between the stations.

I've watched companies run that exact kitchen. Marketing writes the page and buys the attention, in one room. Next door, a seller works off a calendar and a list of names somebody handed them. Further back, someone's still holding last week's spreadsheet. Each room can look busy on its own clock. The lead still dies in the doorway between them.

Growth happens where those rooms meet, and that part is easy to miss from inside any single room. A campaign can look loud while the seller is still typing names out of a PDF by hand. I've watched a clean list of leads show up a week late, after the seller already guessed and moved on without it.

Companies buy AI tools hoping it fixes this on its own. Most of the time it doesn't, because nobody rebuilt the handoff. I've watched a team buy a writing tool so a marketer could ship twice as many pages, and the extra pages just piled up in the same doorway, still attached to the same spreadsheet nobody trusted.

I've got a name for the whole path those rooms share: GTM. Go to market is the stretch from we built this to the right person can find it, buy it, and use it without a scavenger hunt. That entire stretch is GTM. Building the pipes so marketing, sales, and data can hand work to each other without a meeting for every single row is GTM engineering, and it's the craft I spend most of my time on.

I've sat on calls where a marketer pastes a row into a chat and a seller asks what the columns mean, while someone from data is on the same thread saying the export's from last Tuesday. That call is the pan burning. The point of building real pipes is that Tuesday's export shows up already named, dated, and ready for a tired person to open at 4pm without asking anyone anything.

What those pipes produce is a pipeline: the ordered set of jobs that turns a raw source into a row the next person can use without asking you what the columns mean. I collect from a source I've already measured. The next job gates the row, throwing out what doesn't qualify. Enrichment only runs on what survived the gate. Packing is the last job, the one that writes a sheet a seller can open without needing a legend to read it.

Every job in that chain ends in a handoff, the moment work leaves one station and lands at the next one already in a state someone can run with. A good handoff carries a date and a reason the row is still alive. The next action should be obvious to someone who's tired. A zip file named final_v3 still needs a meeting to figure out what it is. I want the next person to pick up the plate and walk.

Before I spend a seller's morning on a company, I look for a signal, a dated, checkable sign that the company might care right now. I want to open a URL and see a real date on it. A hiring post from this month I can check with my own eyes. A page that loaded this week is another one.

I shipped this for real once, on a project called ScaleFlow. It was a 48-hour take-home: build a list of about 100 high-ticket leads for agencies and B2B companies doing $500k to $20m in ARR. I shipped the list. I want to be straight about what this was: a take-home assignment, so there's no business result to report.

I started with an orchestrator, the agent that runs the whole sequence so jobs fire in order and a dead step can't quietly pretend it finished. Scrapers came next, the jobs that pull companies from a source you've already picked. Eval gates sit on top of the rows as plain yes-or-no checks that throw a company out. I shipped an MCP last, a live connection so the next person can run the same pipeline from a chat window instead of digging through a private notebook.

I'll say this plainly because it matters: the MCP scrape tools read an already-normalized CSV. They don't open a browser. I'm naming that because a demo can look like live browsing when it's just a file read, and I don't want that ambiguity to slide.

The mix I shipped was 71 leads from Clutch and 29 from Crunchbase. Clutch lists agencies, and that's where most of the shipped mix came from. Crunchbase lists funded companies, and I pointed the scraper at it like it was the main well, which was the wrong call. Seventy-four percent of that Crunchbase pull had already raised over $20 million, outside the band I was supposed to be targeting. The lesson is simple: measure the source before you build the scraper around it. I built first and measured after, which is backwards.

Out of 357 companies, only 7 cleared intent as a hard filter, where intent meant a dated public sign, a hiring post or a page asking for that kind of work. That 357 is its own separate pass from the shipped 100, and I keep those two numbers in different pockets on purpose so nobody blends them into one slide that sounds better than what happened.

The mailbox check was MX-only, meaning it confirms the domain publishes a mail server. That's the whole claim, and I leave those exact words on the sheet so a later version of this doesn't quietly upgrade what got verified.

New spend on Apify for the whole run was $4.12. I write that number down because a cheap run can still burn two full days if you pointed it at the wrong well to begin with.

The system drafts, a human approves, and nothing went out to a real lead. If a source blocked the scraper, the job stopped. A CAPTCHA got the same treatment. Stopping means the gate is doing its job. The whole pipeline ends in a queue a person can read and decide on.

I build the pass so the next person can cook without me standing there pointing at the onions the whole time.

## Every platform is a different room to walk into

Same stew, three different serving moments. Across a crowded bar you get one sentence and maybe a glance at the bowl before someone's attention moves on. That's X. At the first bite, someone decides whether to keep eating in about a second and a half. That's TikTok. On the table, the bowl is also a picture of who you are, for whoever scrolls back to it later. That's Instagram.

On X I treat the fast glance as a take: one sentence over a screenshot, judged in minutes. I write the line I'd throw across a bar and then stop. Extra text under the screenshot is a second serving nobody asked for, and the timeline's already moved to the next bowl. I've deleted lines I wouldn't say out loud to a person standing two stools away holding a drink. Timing's the other half of it. A take that lands at 2am in a dead room is the same sentence, wasted in an empty bar.

I sit with the replies for about five minutes after posting. Silence tells me the sentence failed, and I've pulled a take at minute six once I could tell it had missed the room.

On TikTok I'm writing a hook, the first slice of attention, the actual first 1.5 seconds. I put the character or the world in frame from the start. Someone who already has the spoon at their mouth isn't going to wait for a title card explaining the stew. The camera starts on a face, or on a pot that's already moving. I've opened a video on my own face mid-sentence, already talking, because the world has to be in the shot before anyone decides to stay. I've cut intros that were completely true and watched the bite disappear because the world arrived too late.

Instagram asks you to leave the bowl on the table. That's composition, how the thing sits on the screen. Reels are how a stranger who's never sat at your table finds the kitchen at all. The feed itself is identity: someone scrolling later is looking at the bowl as a picture of who you are, deciding in a glance whether this table is theirs too.

A private joke sits cold on a feed. Carousels still work, because people will swipe a sequence when each card earns the next one. The first card has to be a claim a tired thumb will stop scrolling for. I've built a long carousel where the card I cared most about sat too far in, and people left before they got there.

I spend real time on the still image, because the still is what's left once the Reel has finished traveling. If I copy someone else's table setting, people notice. The grid is what a guest sees when they come back later looking for the kitchen again.

The bowl on the table is also a handshake. I call that brand, and brand is every human touchpoint, including the ones with no pixel attached. The way a seller says hello on a call is one. So is the error message that pops up at 11pm when nobody from marketing is even in the room to see it.

I think about four things a touchpoint can do. Keeping people informed means someone can find the next fact without sending a message into the void, a date on a page does that job quietly. Inspired is the heat that makes someone stand up after reading a post and go try the thing themselves. Involved means there's a door back in, a reply a tired person can answer at 4pm. Interested is the one that lasts past the sitting, meaning next week they still want to look at the next bowl.

I look at numbers, but a number only earns a seat at the table when it changes what I do next. A view count I can't act on is a bowl I'm still staring at after I already decided to eat. I dropped a chart from a weekly review once because nothing about next week would've changed no matter which way that line moved.

I've rewritten the same idea for a fast glance and watched the words go quiet the moment I set that same bowl down on a table meant for something slower. I'd kept the sentence and forgotten which serving it was for. Write for the physics of whichever window you're standing in.

## Two crowds want two different things

Picture a night stall that sells to people who already know the cook. They come for the smell and the usual bowl. You can fill that stall on a good night and still not meet a single new person. Down the street there's a supermarket aisle, jars with labels, picked by strangers who've never heard the cook's name. The stall is where money and belief show up first, among people who already speak your language. The aisle is where daily users come from.

I've spent years cooking for the stall. I call that crowd CT, Crypto Twitter, the public crypto conversation on X. People there already know the words. A new bowl can travel on a thread before morning, because the cook's already in the room with them.

I've stood in that room with a product that was still half-built, and people asked for the usual bowl anyway. The conversation was already happening, and my job that night was to be in it.

The stall is good at bootstrapping liquidity, money that can move into a market or a token. Someone who already speaks the language will put money in motion after watching the cook work for one good night. The same stall is how I raise capital too, money committed to the project that sits once it arrives, because a person who already trusts the cook will commit after one conversation in the language of that room.

Those are two different jobs, and I pick CT when the job is getting liquidity moving or getting capital committed, because the people who can do that already live in that conversation. I write the job as one sentence I could say out loud: get a commitment that stays. If I can't say the job that plainly, I haven't earned the right to pick a crowd yet.

The aisle is a different crowd. I call it Web2, the ordinary internet where most people already spend their day. They pick up a jar because the label told them what's inside, and they've never heard the cook's name. They came because they were already walking that aisle for something else.

What I want out of the aisle is a DAU, a daily active user, someone who opens the thing today. That's the whole claim. Most of the internet already lives in that aisle, reading labels on the way to whatever they came for. If I want someone to open the product tomorrow morning, I put a jar somewhere they're already walking. A label has to stand on its own without the cook there to explain it. The stranger's only got the jar in front of them, so it has to say what's inside in words that person already uses, on a shelf they already pass every day.

I name the job before I pick the crowd. Bootstrapping liquidity and capital is stall work, done among people who already speak the language. DAUs grow in the aisle, one stranger at a time, from someone who found a jar while walking somewhere else entirely. Mixing the two jobs wastes both.

I watched a team once take a stall sentence and print it straight onto a supermarket jar. The cook left the stall to go stand in the aisle instead. The usual crowd waited on an empty street that night, and the jar in the aisle still talked like a night stall, so the strangers kept walking past it. Both rooms lost a night's work over that one call.

A cook only gets one night. I spend it on the job I named ahead of time. If I walk to the supermarket instead, the stall sits empty, and that's a real choice, one I make on purpose.

## The person who stands in both rooms

In one room, people can make a model fetch a page, write a script, fill a sheet. In the other room, people know who's buying, what scares them, and exactly which promise would get a company sued. I've watched both rooms nod at each other politely in a meeting and then go right back to work as if the other room were basically a rumor.

The first room is fluent in demos. The second room has sat with a buyer long enough to know which sentence gets a company in trouble, and they carry that knowledge into every meeting even when the demo in front of them looks finished. The job in the middle is translation: standing in that doorway long enough to turn a demo into words a seller can use on a Tuesday, then into pipes a team can rerun without the person who built the demo hovering over their shoulder forever.

I walked out of an engineering sync once thinking, wait, what. By the time I hit the hallway the question had changed shape: how do I use this thing. The room had shown me something exotic and I'd nodded along. By the elevator I still couldn't have handed that demo to anyone else.

So one job after a sync like that is making the exotic thing sound familiar. I take the new object and say it in the language of the floor. A seller already opens a sheet every morning, so I tell them this is that same sheet, with a gate that throws a dead company out automatically, sitting in a queue a tired person can read at four in the afternoon. Once it sounds like work they already do, they can pick it up without a second explanation.

Plumbing is a different afternoon of work entirely. I mean agent plumbing, the pipes that turn a live walkthrough I click through in my own chat into something a team can rerun without me. A demo I run live in front of people is still private the moment I close the laptop. Plumbing is what lets the next person press the same sequence on Thursday, when I'm nowhere near the room.

In the meeting itself I try to say the demo in one spoken sentence. Something like, you can run the same list from chat now, and so can the next person after you. I keep working that sentence until it comes out of my mouth in words a seller already uses on their own.

I keep something called a CLAUDE.md for a sequence like that, a note Claude reads before every session. I write the job, the kind of company we're spending time on, the gates, and the voice I want showing up on the sheet. The next morning starts already knowing the kitchen, without me re-explaining it from scratch.

A hook in this room is a different tool from the TikTok kind. Here a hook is an event rule: something happens, and the agent starts on its own. A new row lands in the sheet and the eval runs automatically, so nobody has to remember to press a button at 9am every day.

I shipped the ScaleFlow pass as a take-home, and again, there's no business result to report on it. An MCP is a live connection between Claude and the rest of the stack, the thing that lets a chat reach the sheet without me copying cells by hand one at a time. A plugin is a packaged workflow a team can install on their own machine, so the demo leaves my laptop entirely and Thursday doesn't depend on my memory of how I built it.

When the translator's missing, the backlog fills up fast. The technical room keeps shipping demos nobody on the sales floor can run. Tickets go cold while both rooms stay busy on their own separate clocks. I've sat in that exact meeting, where everyone nodded along and nobody in the room could run the thing come Thursday.

People chase what I'd call a fake pipeline: fake clients and fake code paired with big names and bigger confidence. It's easy to chase because it photographs well for a deck. What I look for sits quieter than that. I want curiosity, someone who'll open the product and press on it until something breaks. I want accountability in that same person, the kind who'll answer for a row that went wrong. The people worth hiring already use the product themselves and will tell you, live, what failed this morning.

Skills can be taught. A system can be learned by anyone who'll sit with it. The scarce part is the person who shows up and does both, someone who can stand at the pass, hear a demo in the technical room, and say it back in words a seller can cook with. A fear from the sales floor becomes a gate the model will respect, once that person's translated it.

A human still has to decide whether the row lives, and whether the promise is safe to print.

## Still the director

Too many companies stack steps onto the register without noticing. Three tickets, three different physics. A handshake instead of a logo. A kitchen pass sitting unattended between marketing, sales, and data. Two rooms that badly need a translator between them.

You still pick the ICP, the kind of company you're willing to spend time on, and I make that choice before any script runs. The gate is the same kind of choice. So is the window you choose to stand in tonight, X or TikTok or Instagram, stall or aisle.

I still have to name what good looks like. A standard is a sentence I'd say out loud about a row, a company, or a window. The model can multiply whatever I hand it, so I have to hand it the right job to begin with.

I use AI as an assistant, and as a coder when a pipe needs a script written. That's where the real workflows live for me. I've used it for health questions, and for rehearsal before a conversation I was scared to have, the kind where I need to hear myself answer out loud before I'm in the room for real. I barely use it for writing. Grammar's the one exception, because English isn't my first language.

AI still isn't great at sentences. Pile on extra instructions and you still get a paragraph that reads like a model wrote it. It does decent work if you already know what you're doing going in, so I'll take help fixing a comma. The paragraph itself still has to come from me.

When I want help drafting, I interview myself first. I pull out my own ideas, my own tone, the stories I'd tell a friend across a table, and then I type it. I stay the director of my own sentences, the same way I stay the director of the gate, the window, and the ICP. The model can multiply the work. It was never going to be the part that carried the judgment.
