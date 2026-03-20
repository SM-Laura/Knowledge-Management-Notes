

### Featured Voices
## “We didn’t build it with code. We built it with context.”

Sarah Sanders works on documentation at PostHog, where the four-person docs team operates more like a product engineering team than a traditional writing group. They build custom React components, manage a Gatsby-based platform, and run AI agents that are reshaping what documentation work looks like.

Her defining contribution is **context engineering** — the idea that the future of documentation isn’t about writing faster, but about providing AI systems with enough product knowledge, style conventions, and structural examples that their output is worth refining rather than rewriting.

### “I’ve heard this term multiple times… something like ‘context engineer’. Being someone that becomes a master of crafting context for either users or robots or both. And I think that’s where the future is for technical writing.”

The most concrete example is PostHog’s AI onboarding wizard: a one-line CLI command that installs PostHog, identifies events in a user’s codebase, and creates dashboards — compressing days of setup into about eight minutes.

### “90% of the implementation of that onboarding wizard is actually example apps that we’ve written, documentation pulled from our MCP server, and then just really good testing with prompts.”

### “Engineers often want to solve AI workflows with code, but you can create an entire AI workflow with mostly just docs and very minimal code.”

Sanders’ team also builds agents that generate first-draft documentation PRs from engineering changes. The target isn’t perfection — it’s a useful starting point.

### “We want [the agent] to enable PostHog engineers to own documentation from start to finish, ideally getting them 60% of the way on the first try.”

But context quality is everything. Without it, the AI output created more work, not less.

### “When we weren’t giving it good context, it was just all over the place. And it actually, in my opinion, would have created a backlog that was way more hard to review and keep up with.”

**Ian Alton at Airbyte has built an equally sophisticated system, but focused on verification rather than creation.** As the sole dedicated technical writer, he’s spent a year developing an agentic QA loop with two phases: pre-release, an AI agent reviews open PRs and proposes documentation updates; post-merge, a QA agent validates documentation against source code and flags inaccuracies.

### “Pretty early on, I started building an agentic loop where — after we have a commit in the platform — a background process will spin up an AI to review that documentation and make a proposition for any changes we want to make.”

The system has caught real problems:

### “It can be as major as a third-party API that we’re connecting to and we’ve gotten the scopes for their permission model totally wrong. Anyone using the docs would not have had a good time in that situation.”

But without human guidance about user needs and product context, the AI produces technically correct but practically useless content.

### “If I tell it to look at a PR and just document it, it will produce some very great, probably technically accurate information that is not of use to anyone.”

As mentioned in [Docs and product](https://www.stateofdocs.com/2026/docs-and-product) Mirna Wong at dbt Labs automated a different piece of the pipeline — an agent that **analyzes code changes, detects customer-facing updates, and auto-creates documentation issues**. And Marco Spinello at Booking.com found a use for AI in batch operations: applying a documentation template across 30 to 50 articles. “80% was good. I had to go through a couple of iterations to tweak my prompt and break it down into multiple steps so that Claude could move incrementally. But once I got the process, **it did a huge amount of work that would have been very, very tedious and error-prone.**”

None of these practitioners are using AI to simply “write docs faster.” They’re **solving specific bottlenecks** — information gathering, change detection, QA verification — and **keeping human judgment where it matters most**.

76%

**use AI regularly for documentation creation** — up 16pp from 60% in 2025

![](https://framerusercontent.com/images/qesZVfNdAqtGIccjQD9RE6bgBAA.svg?width=80&height=80)

64%

**believe AI will be "extremely impactful"** — up from 49% last year

![](https://framerusercontent.com/images/ZxgqRKt0PlR5F3JMTyessZMEMCc.svg?width=80&height=80)

AI adoption for documentation creation has crossed the mainstream threshold. Three-quarters of practitioners now use it regularly, and the profession is more convinced than ever that it will reshape the work. But the headline numbers obscure something the featured voices make clear: the teams getting real value from AI aren’t the ones using it most broadly. They’re the ones using it in the right places.

The bottleneck in documentation has never really been the writing. It was always the information gathering, the change detection, the verification — everything that had to happen before and after a draft existed.

That’s where the practitioners in this section are finding leverage: agents that surface what writers need before they have to ask, QA loops that catch inaccuracies before they ship, batch operations that would otherwise take days. The writing itself, it turns out, is often the part AI helps least. Technical writers report the smallest time savings of any role, because experienced writers were already fast at writing.

What hasn’t kept pace is governance. Most teams are using AI without guidelines in place, and documentation carries a higher accuracy bar than almost any other content type. A wrong instruction not only confuses, but it breaks someone’s implementation and erodes trust in the product. This section covers who is using AI, what they're using it for, where time savings are real and where they aren’t, and why the gap between adoption and governance is the most urgent problem in the field right now.

## AI adoption: the numbers

![Company Size Year-over-Year](https://framerusercontent.com/images/AgLDg0xceLrVAzUGyHTT1ThCYDo.png?width=2265&height=1176)

**76% of respondents use AI regularly** (always, often, or occasionally) for documentation creation. Only 11% never use it. The shift toward AI is dramatic and consistent across the board.

![Company Size Year-over-Year](https://framerusercontent.com/images/X909GsIkFbsZAlX8OsmTQHMC4.png?width=2265&height=1176)

![Company Size Year-over-Year](https://framerusercontent.com/images/RnjxnIRovXrSkscgjibngOp7QA.png?width=2265&height=1176)

Three-quarters expect to increase their AI usage further next year, and 64% **believe AI will be “extremely impactful” for documentation.**

## What AI is used for

![Company Size Year-over-Year](https://framerusercontent.com/images/11bZDRxnjtIVZFNpyUAJi4PqU.png?width=2264&height=1176)

The top tasks are **drafting (62%)**, **brainstorming (58%)**, and **proofreading (58%)**. Style guide matching (50%) is also substantial. Only 25% use AI to write the whole thing. **General-purpose LLMs** dominate tool usage at 73%, far ahead of code assistants (39%) and documentation-specific AI tools (26%).

### “The primary way I use AI is for editorial assistance. I combine a linter, Vale, with a large language model to enforce our style guidelines and suggest rewrites that bring content into alignment with those standards.”
    
### “The biggest value AI gives me isn’t faster writing — it’s faster information synthesis. I can throw a spec, a Slack thread, and a Jira ticket at it and get a coherent summary in seconds.”
    
### “For us, it looks like being editors and reviewers when people who aren’t tech writers are using agents to open a first draft. It’s like ‘context engineer’ — being someone that becomes a master of crafting context for either users or robots or both.”
    
### “We are suffering from a little bit of AI slop. I've put some issues out and I've had so many people submitting PRs — I think I've got about eight duplicate PRs for the same issue.”


## Time savings: real but role-dependent

![Company Size Year-over-Year](https://framerusercontent.com/images/AzVqZ1mCWsQovXNjJYF7vMN2o.png?width=2265&height=1176)

**78% report AI makes documentation faster**, with 35% claiming 50%+ time savings. But these gains aren’t evenly distributed:

![Company Size Year-over-Year](https://framerusercontent.com/images/c1pUxHSi7RRLF2hkWe1kekq7Ynw.png?width=2660&height=1385)

Technical writers — the heaviest documentation producers — report some of the smallest gains. The people closest to the writing report the smallest time savings — as Sarah Moir at Sigma Computing puts it, “it’s often faster for me to just do the thing than it is to try to tell an AI to do the thing for me.”

### “When you try it, it looks like you should be getting these 500% efficiency gains, and then when it actually comes down to it, it’s maybe like 20%. Verification is still really hard.”
    
### “Typically, if I can get an AI to get me 80% of the way there, I can do some final edits. But that’s only possible if we’ve done the work from the beginning to really express what we want.”
    
### “People’s expectations of tech writers have shifted — ‘this should be faster because of AI, so why aren’t you being faster? Let me load more stuff on you.’ They don’t recognize that good content does require a human in the loop.”
    
### “I used Claude Code yesterday to rename 600 files in my IA. I was able to cut six days of work down into an afternoon. That’s kind of the way I’m using AI — not for content, because I have found that I have to edit too much.”
    


## Governance lags adoption

![Company Size Year-over-Year](https://framerusercontent.com/images/B6NwIxmO32vi3YX1zlTlNvPshgE.png?width=2265&height=1166)

Only **44% have formal or informal AI guidelines**, and 22% have no plans to create them. There’s a clear gradient: 55% of “always” AI users have guidelines versus 30% of “rarely” users. But even among the heaviest users, **15% have no guidelines and no plans**.

### “We need technical writers more than ever because of AI. Right now is the time for companies to double down on documentation.”
    
- ### “When we talk about an agent that is hallucinating, we’re really talking about an agent that's starving for context.”
    
### “I’ve semi-automated things — and I say ‘semi-automate,’ because I included a human-in-the-loop aspect so that AI doesn’t automatically rewrite anything. The writer has the ultimate say.”
    
### “We’re preparing our own guidelines for how to write content for AI, but we don’t yet have any benchmarks. I’m not sure if anyone has universal benchmarks yet.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

## Concerns: hallucinations dominate — and vary by role

![Company Size Year-over-Year](https://framerusercontent.com/images/nHhsrVrr9q9gyckWrZ5bwUb0uw.png?width=2265&height=1176)

When it comes to concerns about AI documentation, **hallucinations** lead at 62% overall — but the worry is dramatically role-dependent. The concern profile varies significantly by role:

![Company Size Year-over-Year](https://framerusercontent.com/images/YLdlXjuAnRGHznMn07gKguuAUH4.png?width=2663&height=1673)

Writers worry most about accuracy and skill erosion. Engineers worry more about cost, legal issues, and user trust. The two groups that work most closely on documentation see fundamentally different risk profiles.

## New for 2026

The 2025 survey included basic questions about AI usage for documentation. For 2026, we significantly expanded the AI creation section to cover governance, concerns by role, the executive-practitioner priority gap, and the relationship between AI adoption intensity and team practices. The rapid pace of AI adoption — and the governance gap emerging alongside it — made this deeper coverage essential. Questions that carried over from 2025 are compared below.

## Year-over-year comparison

The AI adoption numbers show the most dramatic year-over-year shifts in the entire survey.

![Company Size Year-over-Year](https://framerusercontent.com/images/gTtc1Ey3veJ3YVM0H4x1dx3k0.png?width=2265&height=1275)

Regular AI usage (always, often, or occasionally) jumped from **60% to 76%** — a 16 percentage point increase in a single year. “Never” users were cut in half, from 25% to 11%. AI for documentation creation has crossed the mainstream threshold.

![Company Size Year-over-Year](https://framerusercontent.com/images/bXneElYsK5f9ocuuw3Gng833m5Y.png?width=2265&height=1275)

Belief that AI will be “extremely impactful” rose from 49% to 64% (+15pp). The profession isn’t just using AI more — it’s more convinced than ever that AI will reshape the work.

## Strategic implications

**AI is delivering real value — in the right places.** Seventy-eight percent report AI makes documentation faster, and the top use cases — drafting (62%), brainstorming (58%), proofreading (58%), and style enforcement (50%) — reflect practitioners finding genuine leverage. The teams getting the most from AI are the ones that have identified specific, repeatable tasks where AI excels, rather than trying to apply it to everything.

**Context is what separates useful AI output from noise.** As Sarah Sanders at PostHog found, AI without good context “was just all over the place” and created more work, not less. Or as Ian Alton at Airbyte puts it: “When we talk about an agent that is hallucinating, we’re really talking about an agent that’s starving for context.” The teams seeing real results aren’t just prompting — they’re building context systems: product knowledge, style examples, and structural patterns that make AI output worth refining rather than rewriting.

**Governance needs to catch up with adoption — because accuracy and trust are non-negotiable.** AI usage is at 76% but guidelines exist for only 44% of respondents. Documentation carries a higher accuracy bar than most content: one wrong instruction can break a user’s implementation and erode trust in the entire product. AI tools are genuinely useful for creation, but organizations need quality checks in place — not to slow adoption down, but to protect the trust that makes documentation valuable in the first place.

**The biggest AI wins aren’t in writing — they’re in the rest of the workflow.** The obvious use case for AI in documentation is drafting, and it is the most common (62%). But practitioners are finding that the deeper leverage is elsewhere: gathering information from engineering tools, detecting product changes, running QA against source code, enforcing style at scale. Technical writers — the heaviest documentation producers — report the smallest time savings from AI (31% at 50%+), in part because experienced writers were already efficient at the writing itself. The bottleneck was never the words.