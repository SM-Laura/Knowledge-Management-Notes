https://www.stateofdocs.com/2026/ai-and-documentation-consumption## 
“Good for humans is not good for agents”

Dachary Carey is a “programmer writer” at MongoDB, where she’s doing something few documentation practitioners have attempted: systematic, empirical testing of how AI agents actually consume documentation. Not theory — hands-on experiments across multiple agent-model combinations, tracking what agents do when they hit real docs pages.

Her findings challenge several widely-held assumptions. The first: that llms.txt files reliably guide agents to structured content.

### “It turns out lots of agents don’t even know about llms.txt. It’s non-deterministic. It sometimes has this idea in its model training data that there is this file somewhere it can work with. And sometimes it doesn’t.”

The second: that agents consume full pages of documentation.

### “A page might be 20,000 characters. But some agents have a mechanical limit of how much content they can view. Sometimes the agent knows that truncation happened. Sometimes it has no idea, and it’s just silently not serving you 15,000 characters of your page.”

The third — and most provocative: that writing well for humans automatically means writing well for agents.

### “I don’t think what’s good for humans is good for agents. Tokens are expensive and context is a public good. Agents need the smallest possible unit of docs that will help them complete their task. And that is probably not what we consider good for humans.”

She’s found that the specific agent-model combination matters enormously, and that some agents delegate tasks to smaller models behind the scenes, compounding the problem. MongoDB is already addressing this in a cross-functional way — the Education AI team runs behavioral evaluations, works with an Information Architect to make documentation changes, and then monitors for improvements. Changes to docs improve model answers in weeks, not months.

### “Agents are a new kind of user.”

She’s also created [afdocs](https://github.com/agent-ecosystem/afdocs), an open-source tool that audits documentation pages against her Agent-Friendly Documentation Spec.

**Bekah Hawrot Weigel has been testing the other side: whether you can actively optimize documentation for AI consumption and see measurable results.** Given a target of moving “cloud agents” from ranking position 26 to 10 in three weeks, she started with auditing existing content and updating it for LLM consumption.

### “I was like, I’m one person and that’s wild — this is not going to happen. But at one point we hit number eight.”

Documentation had a structural advantage for this optimization.

### “Blogs are kind of seen as almost like ephemeral content. But documentation has a bit more credibility because it’s meant to be a lasting resource.”

But Weigel is equally clear about where AI features don’t pay off. She turned off an expensive AI-powered search because users just treated it as basic search.

### “If I’ve done my job and presented the information in a way that’s readily scannable, then they can have their answer in five seconds.”

And the cost picture is sobering. A colleague was paying $100/month for an AI subscription but consuming over $3,000 in compute.

Christopher Gales observes that the shift has reversed conventional wisdom about content formats: “FAQs were on their way out. Nobody in the doc community liked them. But it turns out they’re almost the perfect format for machines — clear question, clear answer, easily parseable.”

The question of whether documentation teams are writing for two audiences — or whether writing well for one serves the other — remains the central tension. The practitioners who are testing rather than guessing are the ones finding real answers.

38%  have **deployed conversational AI interfaces** — the most-shipped AI feature

![](https://framerusercontent.com/images/q8VnUgmonDwP62jKo3YoPoCXxSA.svg?width=80&height=80)

67% say **AI has made docs better;** only 7% say worse

![](https://framerusercontent.com/images/kbzIw80FZYS8XOkC7SZpXheYElc.svg?width=80&height=80)

[The previous section](https://www.stateofdocs.com/2026/ai-and-documentation-creation) was about AI making docs. This one is about AI delivering them, and the difference matters more than it might seem.

When a user reads documentation, they can compensate for a confusing instruction, skip ahead, or search for a better explanation. When an AI agent consumes documentation, it follows what’s written literally, may only see a fraction of the page, and has no way to signal that something felt off. The stakes of documentation quality are higher when AI is the intermediary, and most teams are only beginning to reckon with that.

What this section surfaces is a profession in transition. Most teams have shipped at least one AI-powered feature, the majority say AI has made their docs better, and investment in chatbots, AI search, and MCP servers is accelerating. But the question Dachary Carey keeps asking — whether writing well for humans automatically means writing well for agents — doesn't have a settled answer yet. The teams finding real answers are the ones running empirical tests rather than assuming the two audiences want the same thing.

## AI features currently deployed

![Company Size Year-over-Year](https://framerusercontent.com/images/dznm4e0HURyRDEq3IZhBAU.png?width=2264&height=1176)

![Company Size Year-over-Year](https://framerusercontent.com/images/wJa7Z6JzRFiyoeTvj79PV6A6A5E.png?width=2859&height=1275)

The most-deployed features are **conversational AI interfaces (38%)** and **AI-enhanced search (36%)**, but **26% haven’t shipped any AI features yet**.

Organizations with formal documentation teams ship significantly more AI features. **41% of organizations with no formal doc team have shipped zero AI features**, versus 19–21% for centralized or hybrid teams.

## “There’s a shift happening where a lot of product companies are lagging. Your users are just telling their agents to build them something, not mentioning your product. If you’re not in the agent’s frame of reference, you’re never going to come up.”
    
## “With humans, when you break trust, you get frustration, you get churn. With AIs, when you break trust, you can get some pretty gnarly results — a failed implementation or a customer environment doing things it shouldn’t be doing.”
    
### “llms.txt is pretty much table stakes at this point, and most platforms will just automatically generate that for you.”
    
### “If I have done my job and presented the information in a way that’s readily scannable, then they can have their answer in five seconds.”
    


## Has AI made docs better or worse?

![Company Size Year-over-Year](https://framerusercontent.com/images/i5oeSRpqBpzOlciDsbkNQr45w.png?width=2265&height=1176)

The verdict is positive: **67% say AI has made their docs better** (40% slightly, 27% much better), while only **7% say worse**. Among those who’ve implemented AI features, the strongest perceived impact is on **findability — 47% agree or strongly agree that users find information faster**. But impact on business metrics (docs usage, sign-ups) is less clear, with large “neutral” and “don’t track” segments.
### “What's more valuable for AI agents is conceptual understanding. A human doesn't want to know how the system works before using it — they want to get to the solution faster. An AI agent might prefer to understand the system first, and configure everything after.”
    
### “You want to make sure you have all the context baked into the page, because if one page is consumed at a time and you’re making assumptions that a user will have read something else first — the AI won’t have read the other thing first.“
    
### “I don't think what’s good for humans is good for agents. Tokens are expensive and the context window is a public good. Agents need the smallest possible unit of docs that will help them complete their task. And that is probably not what we consider good writing.”
    
### “At the end of the day, people explain stuff and write stuff for other humans, even though there is this AI layer in between.“
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

The stakes of documentation accuracy are higher when AI is an intermediary. A human might recognize a confusing instruction and work around it. An AI agent will follow it literally.

## How teams think about AI optimization

The profession is in transition:

![Company Size Year-over-Year](https://framerusercontent.com/images/QSHfX9ozOeQ2Grnfj1apeb9jvRE.png?width=2265&height=1162)

![Company Size Year-over-Year](https://framerusercontent.com/images/o3gO9GKlzqzWt6iPAn6H39nfRys.png?width=2265&height=1176)

The top optimization techniques — **adding explicit context (30%)**, **making pages self-contained (30%)**, and **investing in structured data (26%)** — are practices that make documentation better for everyone. As multiple interviewees put it: the best AI optimization may simply be better writing.

### “We really need to keep feeding good quality knowledge and information to the language models. Otherwise, their ability to help us degrades.”
    
### “If you want to make your documentation accessible for LLMs, you have to directly answer questions like 'What is the purpose of this documentation?'. The subtext and literary analysis that humans grab automatically — you need to make it super explicit.”
    
### “If you’re laying off your entire docs team and you’re using AI to write all of it, you might actually be paying a whole lot more for it. And what’s going to happen if they’re not subsidizing this thing anymore?”
    
### “You still need to get your basics right. What Google looks at as a good quality website is still going to be essential in a world where you're writing for both humans and AI.”
    

This deliberately counterintuitive observation highlights the tension: sometimes optimizing for AI consumption does require specific structural choices that differ from human-centered documentation design.

## What’s planned for next year

![Company Size Year-over-Year](https://framerusercontent.com/images/outbpBHq6ocmvlCY136212IiI.png?width=2265&height=1176)

AI chatbots (32%) and AI-powered search (29%) lead the planned investments. **MCP servers** (25%) are a fast-emerging category. Only 15% have no plans to add AI features.

## Security: moderate concern, not a blocker

![Company Size Year-over-Year](https://framerusercontent.com/images/luyIAKtOermgNgEcRrPMCMd9g.png?width=2265&height=1155)

**56% are comfortable** with external AI integrations (26% very comfortable, 30% somewhat). **16% are blocked or very cautious**. Top concerns: data privacy (51%), compliance requirements (36%), and data retention by AI providers (35%).

## New for 2026

This section is new for the 2026 survey. In 2025, AI and documentation was treated as a single topic focused primarily on creation. The rapid growth of AI-powered delivery channels — chatbots, enhanced search, MCP servers, AI-powered onboarding — warranted a dedicated section. Most questions here (AI feature deployment, perceived quality impact, optimization strategies, security concerns) are entirely new. Two questions carried over from 2025 and are compared below.

## Year-over-year comparison

![Company Size Year-over-Year](https://framerusercontent.com/images/ZzaBz6ZUYvAErTIIred0VZ2ttiM.png?width=2462&height=1472)

When asked which contextual formats will play a larger role in documentation’s future, every category grew — but the AI-adjacent ones grew fastest. **Context-aware assistance** jumped from 51% to 62% (+11pp), and **chat-based assistance** rose from 51% to 59% (+8pp). **Interactive tutorials** held steady (51% → 53%), while **user-defined custom-generated docs** grew from 39% to 45% (+6pp) and **voice-based assistance** from 19% to 26% (+7pp). The profession’s expectations are converging on AI-powered, context-aware delivery as the future of documentation.

![Company Size Year-over-Year](https://framerusercontent.com/images/aPwUoLebAYhyJTFWUXKs3FagY.png?width=2462&height=1472)

The belief that **AI will become the primary tool for creating and maintaining docs** nearly doubled, from 19% to 35% (+16pp). The 2026 survey also added new options that weren’t available in 2025: **59% now say teams should consider AI/LLMs when formatting docs**, and **41% believe docs should adapt to users’ needs** in real time. Only 14% think AI will not have a major impact.

## Strategic implications

**Documentation is becoming AI infrastructure.** Every AI-powered feature — chatbots, search, AI onboarding wizards — depends on the quality of the documentation underneath. Good docs power good AI; bad docs power bad AI.

**Writing well for humans is mostly writing well for AI — but not entirely.** 
The top optimization techniques (explicit context, self-contained pages, structured data) are good documentation practices regardless of audience. But practitioners like Dachary Carey at MongoDB are finding real tension at the edges: agents have hard token limits, silently truncate long pages, and may need smaller, more atomic content units than human readers prefer. The question isn’t settled — it’s an active area of experimentation, and the teams testing empirically are learning the most.

**The AI consumption landscape is shifting faster than teams can adapt.** Tools and standards that practitioners invest in today may behave differently tomorrow — agent capabilities, model context windows, and discovery mechanisms are all moving targets. This isn’t a reason to wait, but it is a reason to build flexible documentation architecture and measure what’s actually working rather than assuming.

**To innovate on AI features, treat documentation as a function — not a one-off.** Teams with dedicated documentation functions lead on AI feature adoption, while 41% of organizations without formal docs teams have no AI features at all. The advantage isn’t just about headcount — it’s that dedicated teams can learn from each other, build programs, share what works, and iterate. Innovation in AI-powered documentation requires the kind of institutional knowledge and cross-pollination that only comes from treating docs as an ongoing discipline.