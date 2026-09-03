---
layout: post
title: To be an AI Service Giant, be a Network Bureau
---

Since writing software features has become close to free sometime in early 2026, everyone building an AI Service is worried about defending their business in the long run. And rightly so - building a 100B company over >10 years clearly requires market power; even the most beautiful castle will fall to the enemy if the gates are open and the surrounding lands flat and clear.

While technology is changing rapidly, the free markets we operate in have not. So, many of the [original "7 powers"](https://www.nfx.com/post/seven-powers), which are really all ways to put a moat around the castle, still apply. The question is which are attainable for an AI service, and which are not.

We have run Heron as an AI-native services firm for 2.5 years, and what we have learnt suggests that most of the moats will not survive long-term, except for one.

### Most moats won't work…

Two are close misses - sound right, but we can already see they won't hold this early in the game.

Take counter-positioning. It sounds extremely favorable to an AI services company. The start-up undercuts prices compared to incumbent firms using humans, and those firms often operate on a per-hour model, so *them* cutting *their* humans directly cuts their own revenue. While this is true, it has a fatal flaw: It only works against incumbents. The next AI services company will follow your positioning, has nothing to lose, and the moat is gone.

Switching costs are similar. Automating a workflow that has direct financial implications (e.g. touching money movement) introduces some. But they are a friction, not a way of offering an entirely differentiated product. We know this because we win from incumbents deep in a sensitive decision flow all the time. The type of incumbents that would have likely cited this moat in their favor. Switching costs make these deals much harder to win, sure, but win them you will once your offering is significantly cheaper, better or faster. Switching costs can provide some medium term protection, but they are no long-term match to the overwhelming forces of technological change.

### ...or be too small...

There are two powers that seem more durable and intuitive for an AI service: Scale economies and network effects. We have found they are both real, but scale economies are too feeble and run out too quickly to afford the market power for a truly huge company.

Simply put, they exist where a company providing the same service at scale can do so more cheaply than one that does not. And this is indisputably true for many AI services: A firm seeing 10,000 units of work a day and receiving feedback on incorrect inference will have better evaluation sets, and hence inference, than a firm seeing 100 cases a day. Being better on first inference lowers human review costs and even increases product quality. There are also cost savings in buying inputs in bulk.

But, the [marginal value declines quickly](https://a16z.com/the-empty-promise-of-data-moats/): Intuitively, there are only so many cases before one has seen the vast majority[^1] of ones that matter. So, while it matters to get to *enough* scale, in practice many companies will get there, and it's unclear how much going from 10,000 to 100,000 cases really adds after that. Even worse, this scale effect is strongest on inference and inference gets better all the time, so the value of having more evals than your competitors will also structurally decline.

[^1]: There's an exception here if the underlying data has to be extremely fresh for the scale economies to kick in. I haven't seen this in reality, but I'd love to hear about any cases of this. In this case, scale economies could be much more defensible.

So, the protection afforded by scale economies is too feeble, and stops compounding too quickly, to ensure a fast-growing AI service transforms into a giant company.

### ...but most people underestimate network effects

Network effects are different. They exist when the value of a product increases with the number of users of that product because there is some direct interaction between them. Customer 1's data making customer 2's inference better is a broad scale effect, customer 1 and customer 2 interacting more directly is a network effect.

To illustrate a network effect, take Heron. We offer an AI service that underwrites financial products for businesses. Historically, this work would have been done by humans. In fact, we estimate that if we handled all underwriting we do in software by hand instead, Heron would consist of ~2000 people sitting in a big office underwriting 8 hours a day (the real number is 60, and only 5 of them underwrite day-to-day).

Now imagine for a second that these 2000 underwriters had borrowed two things from science fiction: A Harry Potter style time-turner, allowing them endless time to underwrite each deal, and Star Trek-style mind meld, the ability to perfectly share thoughts with each other. Immediately, the underwriters would underwrite with substantially fewer losses than before:

For one, they could stop a lot of fraud. They could flag to each other a company applying to 20 lenders at a time. They could transmit to each other a stray thought ("seems weird - I swear this owner applied to us before"), and have it confirmed by an underwriter at a different company ("Yes, this owner applied to us with a different company just this week"). All of these are clear fraud patterns. We estimate that fraud just in short-term business credit costs lenders in the US billions a year, and a network of AI agents can tackle this problem in a way 2000 underwriters sitting across all of our customers never could.

If the same underwriter or same lender sees a company twice over time, they can see a broader trend - are revenues falling or rising over the years? With the time-turner and mind-meld in hand, underwriters would compare notes, build a picture of the company much richer than before, and make more accurate offers taking into account the trajectory of a business.

Now, *this* has the potential for a durable moat: [Cross-customer signal](https://menlovc.com/perspective/software-finally-gets-to-work-the-opportunity-in-vertical-ai/) that increases with the number of customers, allowing whoever holds the effect to not just automate a workflow, but to augment the existing workflow.

It's worth being precise on quite how different this is to the scale economies above: Scale economies as we see them in AI services deliver a lot of increased value when you overcome the "cold start problem" - building a competing AI service for insurance claims when you don't have a single insurance claim and the adjusted outcome is very hard - but then flatten out.

Network effects are the opposite. They do not exist until two customers send the same applicant, so they stay close to zero for a while and then increase quadratically relative to market share. So, unlike the scale economies, their value increases rapidly right around the time where a company starts winning a market.

![Network bureau signal chart](/images/posts/network-bureau-chart.png)

### AI Services will capture the full potential of network bureaus, or even create them from scratch

The above begs a question: If it makes economic sense to share this data today and create some network signal, it would have made sense to share it 30 years ago. Why hasn't it happened?

The answer is simple: The economic pressures for these organizations accumulating and sharing cross-customer signals (call them "**network bureaus**") have indeed existed in many sectors for a long time. But, network bureaus tend to be hard or impossible to set up if the underlying workflow is manual and has unstructured data, because the contribution to the network is very high friction. Take my example from above: Fraud signals need to be fresh, so a manual workflow for contribution would need to be a highly-staffed effort to share all cases in real-time, which would be prohibitively costly. A network bureau tracking the trajectory of a business over time would fall down because historical performance data on a business has always been unstructured: Bank statements, quickbooks exports, and whatever the business said on their application form. This is far too unstructured to share and compare easily.

This reality has led to a lot of "thin" network bureaus that are below their potential: In business lending, very few lenders trust the existing business credit bureaus, in large parts because batch uploads of data from members are incomplete and very slow. In insurance claims, shared claim databases (e.g. Verisk) give a cross-customer view on a claimant, but because the adjuster's findings are in (unstructured) prose, they don't make it into the network bureau, which is much "thinner" than it could be.

There's an interesting case where in some places, contribution is so high-friction that network bureaus that one could easily imagine making sense economically don't exist at all. One such place would be a deep understanding of a person's past work performance when hiring, but data on a person is so non-standard and hence subjective that, understandably, the legal hurdles to contributing to such a hypothetical network are prohibitive. Another is accounting. There's surely value for a restaurant in Cleveland to see if it's overpaying for HR software relative to all the others. This has not happened because bookkeeping is historically so manual and data so non-standard - every business has a custom ledger of accounting categories - that a network bureau pooling them all and making comparisons has not been practical. AI services will change that.

### And network bureaus at full potential are *very* valuable

The flipside of this logic also holds. Looking at workflows that were automated with structured data *before AI* allows us to see "the future" and grasp the type of network effects that AI service companies will be able to harness.

Consumer credit underwriting is an obvious example: It turns out the character of a person is fairly stable, a good way to determine that character is to capture their repayment history, and this data can be captured in a few simple integers and booleans, leading to Experian, Equifax and TransUnion sharing cross-customer signals for >50 years and a combined market cap of ~$70B as of Aug '26.

The example of cybersecurity is even more encouraging: Computers mostly describe themselves in structured data and telemetry is automated, so CrowdStrike (~230B market cap) and others have created a strong network bureau out of sharing telemetry data across customers, allowing a network to detect and block anomalies found for one customer across many, on the premise that attacks will often target multiple companies.

| Workflow & Data | Contribution | Network Bureau Quality | Examples |
|---|---|---|---|
| Automated + Structured | Rich & Automated | High | Crowdstrike, Consumer Credit Bureaus |
| Manual + Unstructured | Thin & Batched | Below potential, maybe non-existent | Business Credit Bureaus |

The core insight is that **AI services structure data and automate workflows, turning contributions to network bureaus from high friction to very low friction. So, in any market with a below potential network bureau caused by high-friction contribution, AI services can create valuable, defensible network bureaus.**

### So, which way, AI services founder?

The above outlines a roadmap for AI services founders who'd like a moat.

The first order of business is to focus on one market, so that there's actual overlap between the cases of work. No network effects can occur where two customers don't send the same case. Focussing on one thing tends to be good advice for many reasons. Mental clarity about network effects just adds another. AI services also lack the historic downside of focus: small addressable markets. AI services sell into labour budgets that appear [6-10x larger than IT budgets](https://foundationcapital.com/ai-service-as-software/), making the move to focus a no-brainer.

The failure case here is clear: Going horizontal to grow revenue faster and focus on scale economies, which at first will come true - note that scale economies don't necessarily need you to serve a market with overlapping applicants - before realizing that the company sells into multiple use cases, without the critical mass for network effects in any of them. Next thing you know, Anthropic is coming for you.

The second is to build towards the network effect that will make the biggest difference in a given market. One can do this either by looking at what old, thin network bureaus were trying to do and see if low friction contribution allows to 10x that, or by imagining what economic pressure for a network bureau always existed but has stayed unserved because of prohibitive contribution friction.

AI services that do both have a chance of winning big. Over time, there will be cross-customer signal network bureaus in many new places, and they will generally be owned by the AI services companies doing the work: AI Services will have an easier time building the network bureau to provide cross-customer signals than (below potential) network bureaus building the AI service to do the manual work.

AI services that stay horizontal or are not able to clearly articulate what network effect creates economic value for their market may be able to fly high for some time, but will eventually have to rely on weaker economics of scale or switching costs as a way to defend themselves.
