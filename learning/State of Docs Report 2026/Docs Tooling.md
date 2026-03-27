## “It doesn’t have to be about just writing lots of words”

Chris Ward leads documentation at Supabase, an open-source Firebase alternative. His team dogfoods the company’s own products — search runs on Supabase vectors, and the feedback widget feeds into Supabase. He also manages a three-tier contributor model: internal staff, a paid external contributor program, and open-source community contributors.

### “We have workflows and tools — the process is to help people at all varying levels of involvement with the company and the project to be able to contribute as easily as possible.”

The tooling decisions are constant. Supabase uses MDX — a nonstandard corner of Markdown — and the team built custom linting tools because existing options didn’t support it. They’re now migrating to Vale.

### “[The custom linting setup] works quite well, but it makes less sense to use it now because we can switch to Vale and we don’t have to maintain our own stuff. We can leverage that community.”

But a bigger architectural challenge is emerging:

### “All our different products are separate projects, so it’s important to modularize our documentation around each one, while also making sure that it comes back as a cohesive whole.”

Ward also sees documentation people expanding beyond writing into the broader developer experience — onboarding flows, CLI tools, interactive experiences.

### “I’m a big believer in interactive experiences, or good onboarding or CLI tools. As documentation people, we could influence all of those — it doesn’t always have to be about just writing lots of words.”

**Delfina Hoxha comes at tooling from a different angle — not platforms, but the structure underneath them.** As an information architecture consultant, she’s spent years working with companies whose tools are fine but whose content organization is broken.

### “There’s no AI without IA (information architecture).”

Every AI-powered documentation feature — chatbots, search, MCP servers, content APIs — depends on well-structured content underneath.

### “People who say ‘just throw it on the docs site, AI will make sense of it later’ are wrong. AI will also have an easier time making sense of stuff if you have decent information architecture going in.”

She advocates for audience-based path differentiation and the principle that **“every page is page one”** — users arrive from search, AI tools, and deep links, so docs can’t assume a linear reading path. She’s also seeing companies create new roles at the intersection of content and AI: positions focused on prompt creation guidelines and AI interaction design policies.

Marco Spinello at Booking.com captured the shift in a single anecdote: after installing a Vale MCP server and piping it through Claude Code, he “went from ‘why would I want an MCP server for Vale’ to ‘there’s no other way now.’”

The tools are changing fast, but the lesson is consistent: the tools only work when the structure is sound. Or as Hoxha puts it — **there’s no AI without IA**.

70%

**factor AI into information architecture decisions** at some level

![](https://framerusercontent.com/images/CSkAHzKDWaiq51fkJqwXwbYJEUs.svg?width=80&height=80)

53%

use **self-created guidelines for information architecture** (the top approach)

![](https://framerusercontent.com/images/kbzIw80FZYS8XOkC7SZpXheYElc.svg?width=80&height=80)

Tooling decisions in documentation used to be mostly about publishing: which platform, which format, which workflow. That's still part of the picture, but the questions teams are asking have expanded.

Chris Ward’s team at Supabase is building modular documentation architectures that hold together a growing family of products and projects. Delfina Hoxha's consulting work starts with information architecture — the structure underneath the tools — because she's seen how many teams hit the same wall: the platform is fine, the content organization is broken, and no amount of AI will fix the output if the input is incoherent.

That last point is showing up in the data. Nearly 70% of teams now factor AI into their information architecture decisions, a jump of 11 points from last year. The teams building the most effective AI features have learned that documentation quality is what determines AI output quality — which means tooling decisions and structure decisions are increasingly the same decision. This section covers how teams publish, how they organize, and how AI is changing both.

## How teams publish documentation

![Company Size Year-over-Year](https://framerusercontent.com/images/X6aAAi0aJ4kpz01CPZyVe5jcUMQ.png?width=1714&height=1119)

**Dedicated documentation tools** lead at 45%, followed by **open-source platforms/Git repos** at 21% and **website publishing platforms** at 9%.

### “We set up a GitHub workflow that analyzes an engineer’s code changes, and if it detects it’s customer-facing, it’ll automatically add a ‘needs doc’ label. When the PR is merged, it opens an issue in our repository so we know about it.”
    
### “I've built automated testing for docs several times, including code snippet testing and Playwright tests for UI flows. Testing reduces inaccurate information in your docs. It's essential for both human and AI readability.”
    
### “I like to offer multiple contribution paths — WYSIWYG editors, docs-as-code PRs, AI writing agents in Slack — so contributors can use whatever tool they’re most comfortable with.”
    
### “Outdated information is the oldest documentation problem since the Stone Age. AI can definitely help, but no one’s fully cracked the code yet.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

## How teams structure information

![Company Size Year-over-Year](https://framerusercontent.com/images/8VapTiG1ChTdPWMEB12yhUByc4.png?width=2265&height=1159)

When it comes to structuring information, self-created guidelines are the top approach at 53%, followed by **established frameworks** like Diataxis and DITA at 28%. **Intuition-based approaches** account for 32%. Documentation teams are professionalizing their information architecture.

### “I think there’s less appreciation for information architecture. People look at AI tools and say, ‘Docs topics? We can spit those out all day.’ There’s less understanding of the extent to which IA affects customer experience, compared to software architecture where everyone immediately gets that it’s complicated.”
    
### “When I’m writing English these days, I treat every single sentence as though it’s being quoted out of context.”
    
### “If people can’t find the page, then the words on the page never mattered anyway. You have to break it down into useful chunks so that people can find what they’re looking for.”
    
### “Information architecture will always matter. And I say that even though 68% of our users just went to the search — no one used our table of contents. The TOC matters less than people think nowadays, but it also matters more than you might expect.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

## AI’s influence on information architecture

![Company Size Year-over-Year](https://framerusercontent.com/images/MkXbIfGPhsVs5gMkyGVvEY2wVIM.png?width=2264&height=1176)

Nearly **70% of teams now factor AI into their IA decisions** at some level (“Consider” or “Primary focus”). Only 20% say they’re not thinking about AI when making information architecture choices — and 46% are actively considering it, even if it’s not yet a primary focus.

- ### “Five years ago you’d ask, ‘how do we structure this information and how does the search engine work?’ Today you need to ask, ‘is there an agent interacting with this product? Do we need LLMs.txt? Do we need an MCP server?’”
    
### “We’re not writing completely different content because of AI. It’s more about organizing content — we’ve added more FAQs to help LLMs, working with our SEO team on schema markup, and we recently shipped an update where agents get raw Markdown instead of HTML.”
    
### “I’ve taken great pains to ensure our standards are upheld programmatically — so I don’t have to keep telling people. Use AI tools to make suggestions or even direct edits.”
    
### “Your concepts need to be concepts and not have reference or tasks mixed in. Your tasks need to be tasks, your tutorials need to be tutorials. You need to have things consumable by human users and by AI crawlers and consumers.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

The teams building the most effective AI features understand that documentation quality is the input that determines AI output quality.

## New for 2026

This section is new for the 2026 survey. While the 2025 survey asked about publishing tools, the 2026 version significantly expanded its coverage to include information architecture approaches and — critically — how AI is influencing IA decisions. We added these questions because our interviews revealed that tooling choices are increasingly driven by AI readiness: teams aren’t just picking tools to publish docs, they’re building information architecture that powers AI features. Some questions carried over from 2025 and are compared below.

## Year-over-year comparison

Where questions carried over from 2025, some of the shifts are meaningful.

![Company Size Year-over-Year](https://framerusercontent.com/images/xc1NpW9YXsyjhknYlSLoN3vYYgo.png?width=2265&height=1275)

The changes in information architecture are not drastic, but they are visible in the data: **self-created guidelines** grew 4pp to 53%, **established frameworks** (Diataxis, DITA) grew 4pp from 24% to 28%, while **intuition-based approaches** declined 4pp from 37% to 32%.

![Company Size Year-over-Year](https://framerusercontent.com/images/L0oqrOxfijH6wFV9PIedpYuhxic.png?width=2264&height=1275)

The most dramatic shift: the “not thinking about AI for IA” group shrank from 31% to 20% (-11pp), while “considering AI but not as a primary focus” surged from 36% to 46% (+10pp). In just one year, AI went from something most teams weren’t considering in their IA decisions to something nearly 70% factor in at some level.

## Strategic implications

**Information architecture is the foundation for AI features — and for AI context.** As Delfina Hoxha put it, “There’s no AI without IA.” Every AI-powered documentation feature — chatbots, search, MCP servers — depends on well-structured content underneath. And as AI tools increasingly rely on documentation as their source of product context, the quality of your information architecture directly determines the quality of AI output. Teams investing in IA now are building the foundation for everything that comes next.

**The professionalization of IA is accelerating.** Documentation teams are thinking more systematically about how they organize information, with established frameworks gaining ground and intuition-based approaches declining.

**Style guides can be operationalized with AI.** Marco Spinello at Booking.com piped a Vale MCP server through Claude Code and went from skeptic to convert: “there’s no other way now.” When style enforcement becomes tooling rather than a document people are supposed to read, consistency scales beyond the docs team.