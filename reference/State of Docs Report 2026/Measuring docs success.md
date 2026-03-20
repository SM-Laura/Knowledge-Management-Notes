## Data only makes sense in combination

CT Smith is a technical writer at Payabli, a payments startup. Every month, she produces an internal “State of the Docs” report combining data from PostHog, Google Analytics, chat logs, git statistics, and Linear ticket data, semi-automated with a Claude skill.

### “Almost nothing needs to mean anything by itself. The meaning is in the connection.”

That philosophy shapes how she interprets every metric. A high bounce rate on a reference page means someone found what they needed quickly; the same rate on a getting-started guide means they gave up.

### “I would caution people against trying to set it and forget it. Documentation metrics have to be understood in their context. It is not just revenue.”

One early finding reshaped her entire approach: 68% of users go straight to search rather than browsing the table of contents, which drove a major IA restructuring. She also tracks outbound clicks from documentation to signup and sales pages — a direct line from docs to conversion.

Smith reads every AI chat session on the docs site and creates tickets for bad answers. She monitors cost-per-story-point across projects and tracks component usage to justify resource allocation. Surprisingly, though, the feedback widget has been less useful: zero external users have used the thumbs up/down button.

**Sandeep Medikonda at ServiceNow has built measurement at an entirely different scale.** He created the content analytics function from scratch at a company with 250 to 350 technical writers, 12 websites, and over 60 content types. He’s built sophisticated analyses on top of even some simpler metrics like page views.

### “When you walk into an ER, one of the first things that the nurse would do to you is check your basic vital signs. When it comes to digital content, a count of page views is one of those vital signs.”

But a page with low views might document a feature with a small but dedicated user base — in which case the engagement rate might actually be excellent.

### “None of these metrics on their own make sense. You need to overlay them with the context of your product.”

One of his most powerful metrics is “content not viewed.” When the data showed 30% of documentation in a product area wasn’t being consumed at all, it forced hard conversations.

### “Content not viewed is a very touchy topic. You have writers who spend time creating some really cool documentation around some amazing features, but then the report comes back and says, hey, 30% of what you’ve written wasn’t even consumed.”

His advice for teams just starting out is simple: don’t wait for the perfect analytics stack.

### “See what data you have. Get some basic stuff around the number of people coming in. What are they consuming? What are your top areas? Just starting off with that data will start pushing out the creative juices to all of your peers.”

Even before analytics, there’s value in just making the scale of your work visible. Most engineering and product peers have no idea how much content you manage.

### “One of the best things you can do is gather a snapshot of the size of your repository. Many times, your development peers or product managers don’t understand the full size of the context you’re working with. So it helps them respect you even more for the work that you’re doing.”

The payoff comes with consistency. Share data regularly, and the organization develops its own questions.

### “Once you put it out consistently for a few quarters, that’s when the deeper questions get asked. This is a data literacy journey — as everyone involved gets used to the numbers that they see, they start asking questions from their specific perspective.”

Shahed Nasser at Medusa adds a different layer: measurement through the AI assistant itself. When her docs assistant can’t answer a question, that gap gets logged as a content issue. Sarah Moir at Sigma Computing cautions against over-relying on the numbers: “You cannot directly derive intent reliably from quantitative data.”

Vinay Payyapilly at New Relic is experimenting with AI agents that ask standard questions against the documentation and score the answers. And Liz Argall cuts through the complexity: **“My number one measure is: how many hours am I giving back to my developers?”**.

Whether it’s a two-person team or a dedicated analytics function, the practitioners making progress share a trait: they build measurement into their workflows from the start and interpret data in context.

25%

**don't track any documentation metrics** at all

![](https://framerusercontent.com/images/Kb72W46uzTfT3V60v4OgIGRWts.svg?width=80&height=80)

74%

rate docs as **somewhat or very effective for self-service troubleshooting**

![](https://framerusercontent.com/images/6kyu6svowosIojPrumDKtWEKvM.svg?width=80&height=80)

Documentation measurement is widespread but shallow. Most teams track something, but the metrics they rely on most are losing their explanatory power.

_The clearest illustration is a story Ian Alton at Airbyte recounts about Tailwind CSS: their documentation became so good that AI agents could write Tailwind code on users’ behalf. Page views collapsed — not because the docs had failed, but because they'd succeeded in a way the metric couldn’t see. Tailwind depended on human viewership to provide leads, and its revenue model was unprepared for this massive and sudden shift toward agentic users._

_It’s a preview of a problem the whole industry is heading toward: as AI mediates more of how users consume documentation, the signals teams have always used to prove value **a**nd contribute to business results will increasingly point in the wrong direction."_

The paradox this section keeps returning to is a familiar one: teams believe docs drive business value but struggle to prove it. What’s new in 2026 is that the proof problem is getting harder and the teams finding real answers aren’t looking for a universal metric. They’re building measurement programs that interpret data in context, connect documentation to outcomes leadership already cares about, and stay honest about what the numbers can and can’t tell them.

## What metrics teams track — and don’t

The top metrics are usage indicators, not business outcomes:

![Company Size Year-over-Year](https://framerusercontent.com/images/ie7zp4A6BAYcWurSlsL76lcNlAc.png?width=2264&height=1176)

![Company Size Year-over-Year](https://framerusercontent.com/images/u4H17LgSua6gvuO3mxYYRlfyWTI.png?width=2265&height=1162)

A quarter of respondents don’t track _any_ metrics, and 35% don’t track internal process metrics. The business-outcome metrics (revenue, conversion, lead generation) hover around 11–12% — a fraction of teams.

- ### “We track tutorial completion not just through page views but by monitoring repository clones and Docker Hub image pushes — concrete product actions as documentation effectiveness signals.”
    
### “There’s no universal docs metric — you have to map your work to whatever metrics your leadership already cares about. That’s how you prove value.”
    
### “We’re working on a system of rating our docs. We'll use AI to read our content on the basis of how well it can answer customer questions. Then we'll do an audit and take up improvement.”
### “We have analytics for our top searches and click conversion, but we also get results for queries without results. One of the top queries consistently was Docker. So we realized, okay, users want a guide about setting up Docker.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

## The measurement gap scales with company size

![Company Size Year-over-Year](https://framerusercontent.com/images/CaDGpc0snoVdMhWfyoKQQY2DHk.png?width=2462&height=1268)

The measurement gap scales with company size. Medium companies (51–300 employees) are the worst at measurement — 32% track nothing, and those who track average just 1.7 metrics. Enterprise companies (301+) are the best with only 18% of teams tracking nothing. But even this segment measures an average of just 2.7 metrics for their docs.

## Docs in the sales cycle

As explored in **Purchase decisions and business impact**, half of respondents say docs are important or essential for closing deals — but 57% don’t track leads from documentation, and 39% believe docs generate fewer leads than marketing. That disconnect is a symptom of the broader measurement gap this section describes.

### “Time to live is a great metric for docs — the first day someone looks at it to when they start actually using it with a fee behind it. If you can decrease that time, you're going to make more money.”
    
### “There’s no magical formula. I’ve been in this industry for 15 years and I haven’t found it yet.”
    
### “One of my favorites is when I can get the support team to track the number of tickets they answered with a link to the docs. That is just a fantastic way to prove value.”
    
### “For me, the most reliable form of measurement is still personal anecdotes. Everybody wants something much more quantitative, but the attribution is really hard to measure.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

## Troubleshooting: a quiet strength

![Company Size Year-over-Year](https://framerusercontent.com/images/onSAVGsZSFvAKJHv2QPPieW0g.png?width=2264&height=1176)

![Company Size Year-over-Year](https://framerusercontent.com/images/KrXdPUMtRlDaoNUOkOPyPZHnLw.png?width=2265&height=1162)

**74% rate their docs as somewhat or very effective** for self-service troubleshooting. This makes sense considering that support ticket deflection is one of the more frequently mentioned value props of docs that can be measured. But similarly to the role of docs in the sales cycle, **more than a third of respondents don’t measure the success in any way.**

### “If we're not getting any value that leadership can see, that engineers understand, or that users can actually perceive — the documentation isn't doing the work it needs to be doing.”
    
### “We’re successful if we've reduced support tickets on something we overhauled documentation on. Some of the flags we see in support tickets are, ‘I went and looked at the documentation on this’ — that shows us if there’s a gap.”
    
### “Trust in documentation can be quantified: count the total assertions of product behavior, count how many are actively tested and passing. That ratio is your trust score.”
    
### “Using support data as a forcing function to improve quality based on literal input — what is support getting asked about most, to know where to put the effort into the docs.”
    

![](https://framerusercontent.com/images/6tTbkXggWgQCAJ4DO2QEdXXmgM.svg)![](https://framerusercontent.com/images/11KSGbIZoRSg4pjdnUoif6MKHI.svg)

The metrics everyone wants — did the user succeed? did they understand the concept? — require knowing what happened after they left the docs page. Most teams don’t have that visibility and may never get it.

## Year-over-year comparison

Individual metric adoption rates shifted as the 2026 survey introduced new options (conversion rate, time to value, “I don’t know”) that weren’t available in 2025, making direct option-by-option comparisons less straightforward.

But the rate of teams that are not tracking or unsure remains similar for external success metrics.

![Company Size Year-over-Year](https://framerusercontent.com/images/nUBqc6RmZZUxvqu1DrV5M8C1I.png?width=2240&height=1275)

![Company Size Year-over-Year](https://framerusercontent.com/images/j7yeeWc8KoAQEoWls3xxFj81Ms.png?width=2240&height=1275)

For internal measurement, the addition of categories makes an apples-apples-comparison difficult. Still, there’s been some moderate improvement in the rate of measurement, with a **7pp reduction in teams not tracking any metrics**.

## Strategic implications

**The measurement gap is the biggest missed opportunity in documentation.** Nearly half of respondents (49%) still aren’t tracking internal docs metrics — down from 55% in 2025, which shows progress, but it’s still the most common answer. The teams that figure out measurement — connecting docs to conversion, retention, and support deflection — will have a significant strategic advantage in justifying investment and headcount.

**Start with vital signs, not a full analytics stack.** As Sandeep Medikonda at ServiceNow puts it, page views are like checking a pulse — basic but essential. Teams don’t need sophisticated tooling to start. Inventory your content, track what people are consuming, and share the data consistently. The real insight often comes not from any single number but from seeing how the numbers change — a spike in page views after a launch, a drop after a reorganization, a steady climb in search-driven traffic. That fluency develops over time, and it only develops if you start tracking.

**But don’t stop at page views.** As LLMs consume documentation content and users arrive through AI-powered tools, page views alone capture less and less of the picture. Teams should layer in new measurement approaches — conversion tracking, AI referral metrics, engagement depth, and product-action signals (like Docker tracking repository clones from tutorials) — to build a fuller understanding of how documentation is actually being used.