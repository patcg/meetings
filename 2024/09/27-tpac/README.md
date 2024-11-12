# September 2024 TPAC Meeting

The Private Advertising Technology Community Group will be meeting at [TPAC 2024](https://www.w3.org/202409/TPAC/) in Anaheim, California in a hybrid format, in-person and on Zoom. One session is [scheduled](https://www.w3.org/2024/09/TPAC/schedule.html#friday).

## Schedule

### Session Start

The session is scheduled from 09:00-16:00 (09:00 AM - 04:00 PM) local time. Two breaks are scheduled: 1030-1100 (snacks) and 1230-1400 (lunch).

| Time             | Day    | Location      |
| ---------------- | ------ | ------------- |
| 02:00 (02:00 AM) | 28 Sat | Syndey        |
| 01:00 (01:00 AM) | 28 Sat | Tokyo         |
| 18:00 (06:00 PM) | 27 Fri | Brussels      |
| 17:00 (05:00 PM) | 27 Fri | London        |
| 12:00 (12:00 AM) | 27 Fri | Boston        |
| 09:00 (09:00 AM) | 27 Fri | Anaheim       |

## Joining Information

[Zoom Link](https://www.w3.org/events/meetings/6fe0ca25-56c5-4ac4-8a87-bd1e231d24ae/)

## Agenda

(Times local)

### Section 1 

- (9-9:30) Welcome, Hellos, Intros, Policies, Google Doc, Call for Scribes
- (9:45-10:15) What DSPs need [#190](https://github.com/patcg/meetings/issues/190) @tprieur
- (9:30-9:45) Updates from taskforces/sub-groups 
	- [#184](https://github.com/patcg/meetings/issues/184) @npdoty
- (10:15-11:15) Attribution Level 1 (Part 1) ([#191](https://github.com/patcg/meetings/issues/191)) - @martinthomson 
- (11:15-11:20) Break
- (11:20-12:20)Attribution Level 1 (Part 2) ([#191](https://github.com/patcg/meetings/issues/191)) - @benjaminsavage 

- (12:20-1:30) Lunch

### Section 2 

- (1:30-2:15) Updates on Chrome's Attribution Reporting API [#193](https://github.com/patcg/meetings/issues/193) - @hpatoski 
- (2:15-2:45) Attribution Level 1 (Part 3) ([#191](https://github.com/patcg/meetings/issues/191))
- (2:45-3:15) Learning using aggregation APIs [#192](https://github.com/patcg/meetings/issues/192) - @mvono
- (3:15-3:45) Learning inside a trusted server ([#187](https://github.com/patcg/meetings/issues/187)) @fhoering 
- (3:45-4) Working Group update

## W3C Read All About It!

[W3C Policy Slide](https://github.com/patcg/meetings/blob/main/W3C%20Read%20All%20About%20It!.pdf)

## Minutes

[Minutes](https://docs.google.com/document/d/1iWE_GGHkJKMQHO9zbwBjM-yag_3nI3PSq0OVdHMVKsk/edit?usp=sharing)

## (9-9:30) Welcome, Hellos, Intros, Policies, Google Doc, Call for Scribes

Scribe: Charlie Harrison



* Sean: need more slides
* Introducing Tara, privacy lead of the W3C. Staff been assigned to us. Two sessions, one before lunch and after lunch. Break at 11:15. There’s a chance we might have free time at the end. At the end Phillippe will give a working group status.
* W3C read all about it slide. Policies etc, process, code of conduct. Keep it professional.
* Moving Nick’s item to the bottom since he is not here.


## (9:45-10:15) What DSPs need[ #190](https://github.com/patcg/meetings/issues/190) @tprieur

Slides [PATCG2024-What_DSPs_need.pptx](https://criteois-my.sharepoint.com/:p:/g/personal/t_prieur_criteo_com/EfIUSqyby3dFoC5zBJBuS4UBC2gl7wwe1tRHfSwDpl_Y3Q?e=ebnrXH) // https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/PATCG2024-What_DSPs_need.pdf 

Scribe: Charlie Harrison



* Thomas: Work as a product manager at Criteo, ad tech company (DSP). Focus on display advertising on the web. Famous for performance marketing. Our clients expect us to deliver good performance, **revenue over ad spend**. This is a short presentation so feel free to stop me any time.
* Context:
    * We are in a position heading somewhere with the privacy preserving measurement APIs. Making good progress. Just take a moment to take a step back and ensure we take the right decisions. That is the goal.
    * We have different measurement APIs
        * Apples Ad Attribution Kit
        * ARA - Attribution Reporting API
        * Firefox - Privacy Preserving Attribution
        * Etc
    * These APIs all have different capabilities, that’s why we wanted to take a step back
* Measurement & Machine Learning & budgeting
    * We all have different POVs on what measurement is & what we need as a DSP
    * **Attribution to a specific impression**
        * Have a display on the pub, click on it. Have a conversion event. This is typically relying on 3PC. It is really important to have the link between one *specific* impression and the conversion for our algorithms. They need all the features for that impression.
    * **Attribution to a channel**
        * On the other hand, the marketers use measurement to attribute a channel
        * Not linked to a specific impression
        * Link decoration (not linked to a specific impression) - utm_source=criteo
        * Only requires consent on the advertiser website. Does not require 3PC
        * Can see users coming to the website and check the utm_source, can see where people are coming from (traffic analysis)
        * Used by marketers to prove value of advertising to steer budgets across channels
        * Primary vendor → Google Analytics. Gives dashboards of traffic sources / conversions. Measure through utm_source.
        * More money → to channels with better performance
        * Each channel needs to learn and innovate.
    * DSP brings value through learning. Marketers *can* do measurement without impression level information, but the DSP needs impression level attribution to learn.
* **What an advertiser needs**
    * Accurate billing (not in scope)
    * Estimate of audience reach (not in scope)
    * Performance in a global source of truth (50%+ is GA)
    * Ability to check if a channel is a channel delivering as expected
    * Short term rough estimates (debug + find issues) and long term accurate figures (budget allocation)
        * Need to requery
    * Deduplicated performance across channels
* **What does a DSP need**
    * Reach the right person with the right message at theright time
    * Optimization is key
        * Run ML algorithms at scale, with decent costs
        * Access to a truth set fully granular & noise free
            * Could be hidden in a TEE
            * Need to learn from a *granular* truth set
        * Run any sort of models, not just logistic regression but also deep learning with GPUs
        * (slightly out of scope) need to learn *what good features* are. But we can only leverage this if it is accessible at bidding time. Need to connect ML outputs to a bidding API, then we cannot leverage anything
    * Reporting is important, but can be
        * Modelled, aggregatted, post-view or post click
    * Need to re-run queries
        * More accurate long term data + noised granular short term data
        * Ability for advertisers to delegate to DSP (most of Criteo’s customers are small)
        * Support 10ks of pubs for any given campaign
    * We need to keep in mind these requirements to ensure adoption in the long run. Don’t do any design choice that precludes us from satisfying these capabilities in the long term.
* Aram: wanted to rewind to a specific requirement - attribution to a specific impression. This requirement is not achievable is the common agreement. What is the next step past that for Criteo? Almost all the proposals we deal with are aggregating the information, so you will not get this specific data. How do you talk to your buyers, move forward from that requirement.
* Thomas: All the APIs do an attribution to a given impression, once they are available to the DSP they are aggregated. 
* Roxana: we should support ML training
* Thomas: once they are available in the clear, should be able to run private ml training. The system itself should have the capability to do this. Based on this data in a private manner.
* Aram: ML is something we have wanted to support, introduction of noise. If we are retaining attribution to specific impressions people will be confused.
* Thomas: Doesn’t mean DSP has access to this
* Aram: concerned about how this sounds
* Roxana: training an ML model is a form of aggregation. Can be done privately. The training of the model will need the inputs to be individual attributions.
* Thomas: without going through our systems in the clear

	(scribe notes; as opposed to utm_source)



* Isaac: marketing point
* ARam: reality point. If I’m a buyer / seller / regulator, that wording is going to be confusing to me in ways that are undesirable. Let’s move on
* Ben: Thomas is trying to say is contrasting the two use-cases, one internally it’s important that we understand which impression drove conversions so the correct features get aggregated (vs. channel). Internally an important characteristic of the system
* Max: Push back on: if we’re making an allowance that this info we allow (before noise addition)t them to run ML models on that information. From the standards position we’ve lost control of saying there is privacy enhancements here. If we set this precedent that this information is accessible, there will be players that say they will be private. The incentive is to break the privacy guarantee.
* Thomas: I didn’t explain myself. We have an aggregation service that collects impression-level attributions. That is no different from what I explain here. THat aggregation could just be a ML algorithm. The goal is not to trust the DSP, the goal is to build the APIs to allow the use-case to ensure the privacy.
* Max: don’t intend to pigeonhole, let’s chat more later
* John Wilander: my understanding is the proposals we are working on don’t support modeling on a per-impression basis. I agree that sounds problematic. I don’t think apple’s proposal supports that.
* Roxana: Let’s take ARA or PAM. The way it works is a report goes out to the ad tech and is encrypted. It is batched to some trusted aggregation service, which sums and adds noise. That sum is calculated with differential privacy. What is being proposed here is to not only support SUM function, but also support ML training, also with differential privacy in this ML training. Also done in the trusted aggregation service. Same privacy guarantees, a different function.
* Thomas: goal is to ensure we don’t preclude this to close the door on this use-case.
* John: I don’t think any of the proposals are considering this. I am not expressing any support for this idea.
* Isaac: It seems like we’re talking about input privacy vs. output privacy. We are not asking for a change to the level of output privacy. We are already allowing individual inputs to go into this gate. It is a change to the function in the box (instead of a SUM), not fundamentally different.
* Ben: John I think we’re all aligned on this, it is a communication issue. What Thomas is saying is we should add central differential privacy, not local. The DP sum could be used to power your bidding model. A simple ML model could be powered by a SUM.
* John: Acknowledge that the difference between local and central DP is a good one.
* Charlie Harrison: Similar to Ben, if we’re concerned about function in box vs privacy of output, we need to take a step back and ask if we’re actually comfortable with sums. Training an ML model is basically taking a world model of human behavior. If you’re not comfortable with learning human behavior, then DP won’t help you. Slippery slope to saying that you don’t want the system to be able to learn anything, that doesn’t feel like a rigorous position we can protect
* Aram: Good discussion. I keep coming back to this as a communication issue. Emphasize our need to gain trust of stakeholders, it is tenuous. We don’t want to mis-describe this. The phrasing that was brought up is worth reconsidering before it goes out to any buyers or anything like that.
* 


## (9:30-9:45) Updates from taskforces/sub-groups


### [Issue 184](https://github.com/patcg/meetings/issues/184) @npdoty

Scribe: Charlie Harrison



* Nick Doty: I don’t have much to present. I am impressed with our enthusiasm
* [https://npdoty.github.io/patcg-docs/principles/#measurement](https://npdoty.github.io/patcg-docs/principles/#measurement) 
* Link in the slack and the minutes ^. There is a PR in my repository, let’s review it.
* This document is the private ad technologies **principles**. Collect consensus positions about the privacy principles we are trying to satisfy with the deliverables from this group. Covers a lot of topics. 
* Area we have new text and want review: first principles in measurement
* Some debate in public about opt-in, opt-out, safety level of an aggregate measurement API.
    * Measurement should be private for safe widespread usage but under user-control
    * Should not reveal personal data. Ensuring de-identified data
    * Reasoning: if something works across many users, it will be hard for users to make that decision, do you want all the implications of 3PC, inappropriate question
    * We cannot ask all users to do that
    * We don’t want it sharing personal data
* Charlie: What is the notion of de-identified data? Many proposals h ave reports that are tied to a specific context, but the relevant cross site data is encrypted. Would we consider that de-identified, since it can be tied to an individual?
* Nick: We have a definition. 
* Charlie: In ARA, you call a function, it generates a report, it can be linked to an individual. API isn’t revealing anything new. The cross-site info is hidden, but there’s an identifier that ties back to the first party context that called the API.
* Nick: First party has lots of data. Output of the API could still have an ID. That doesn’t sound de-identified.
* Michael Kleber: Every HTTP request could contain non de-identified data.
* Charlie: The goal here is cross site information. We want to avoid mixing across sites. I think it should be a non-goal to say a first party cannot have access to first party identifying data.
* Aram: Problem in these systems is that any user can submit anything, and the API doesn’t account for that being PII
* Charlie: One example.
* Aram: Important to identify here is that no one is creating an identifier for a user where they wouldn’t otherwise have one.
* Charlie: I think we need something different from this principle.
* Michael: a 1P identifier from a single context that cannot be linked to a 1P identifier from another context cannot be used for x-site identification.  The problem happens when you can tie two different 1P identifiers together
* Martin: Suggest we don’t try to fix the problem right now, Charlie should comment on the pull request (or others). This seems important & I agree with Charlie + others. It’s very important to get this very clear.
* Nick: It could be the confusion is about “revealing”. 
* Charlie: gives a thumbs up
* Aram: figure it out on the PRs.
* Nick: Opting out should not be visible. Even if the goal should be for the API to be safe, users always need to opt out and opting out should not be visible.
    * Measurement should not significantly re-enable cross context recognition
    * “Significant” , DP + parameters
    * Measurement should not significantly enable inferences about individuals, from their participation in the measurement. We might allow inferences about individuals, but you shouldn’t get the inference from the fact the individual participated.
* Thomas: The opting out should not be visible. To whom? To be clear, publishers need to be paid for giving an article for free. Usually he is paid by advertising. Requires measurement. If opting out is not visible, cannot say you don’t want to pay me through ads, pay me differently. You don’t let publishers monetize websites the way they want.
* Nick: To whom: we say to the sites they visit. That’s different from blocking ads (which might be visible). Choosing not to participate in an aggregate measurement would not be visible.
* Max: Understand the concern that Thomas is raising. As a publisher, I will push back. If you imagine an ecosystem wide question, I think it gets baked into how things work. Opting out around the same rates, in general the market will adjust and I’m not particularly worried about it.
* John: raising this particular point a few times over the years. Always in favor of hiding this for exactly this reason. To ensure users have a choice and cannot be pressured. It is a *feature*. It will help us. We say the benefit to users is indirect, to monetize the web. Users are not clamoring for ad measurement. Ensuring they can disable it and still use website is important.
* Erik Taubeneck: Not to pile on but I think it’s a good principle. Useful for us to explore learning opt-out rates in aggregate and to learn effects on the entire system. I agree with the arguments for hiding.
* Isaac: join Thomas under the pile. There is a 1st order concern which is free content. These are two first order concerns in tension. We aren’t going to solve this here but I am in favor of not hiding. Competing priorities
* Michael Kleber: If someone has an agg measurement API turned off in the browser, then there are two possible impacts when a pub or advertiser / adtech tries to understand what happened
    * They just don’t know what happened at all for this user, measurement has a larger error bar
    * The aggregate report treats a user who turned off as if it is a non-attributed conversion (no this user did not see an ad). This one seems worse!
    * If a user has the API turned off, you don’t know anything.  We should try to design APIs that reflect that, rather than the risk of explicitly giving incorrect information
* Don: if the user did not have an “official” undetectable opt-out, a bunch of tools would spring up to avoid the system. Some of these tools would be honest, some would try to generate fake data, some would take the opportunity to find users who are trying to opt out and use their browsers to create hard-to-detect fraud. From a practical standpoint, it seems having an official undetectable opt-out avoids a lot of moderation of sketchy privacy extensions and other tools
* Max: To kleber’s point, it is an interesting question to ask. Worth discussing but not in response to this particular principle. What we have seen as publishers is that the bargain over time wrt behavioral advertisers worsened for publishers … . As behavioral advertisers gained traction, it led to paywalls. In theory, we would see more free content if we were less extractive. Disagree that this principle would move more content behind paywalls.
* Charlie: A tension that I don’t think has been raised yet behind hiding the opt in or out of the API and the users perception of privacy. A lot of the ideas are if the user opted out of the api we send a report but it is null so they don’t contribute to the end output of the API so that is a common design idea. To a user who doesn’t understand the system, they are seeing a report outputed from the browser and it will be difficult to explain to them that this is a null ‘safe’ report esp when the user can’t decrypt it. I’m not making a normative … I think there is a tension between user expectations and what they see 
* Aram: closing the queue
* Nick: I think we already closed this. One thing to point out is that if we’re open that, publishers have a guarantee that they know a user participates in the system to coerce them. How would we go about building that? Quite difficult. Advice we give to other working group is don’t ask a browser to make a promise on behalf of a user, it doesn’t work very well. Make sure users are telling the truth.
* Isaac: Max I’m not clear on what you said aligns w/ your preference.
    * Specific q about enabling a specific opt-out
    * Broader point (John), one 1st order principle. I think that is wrong, there are 2 first order principle (as we see people move towards paywalls)
    * If we don’t recognize that we will move to a place where pubs find workarounds. If we don’t consider the user’s first order concern (free content) we will…
    * Push for 2 things
        * Recognition of the principle
        * Nuanced API, allows us to balance the two principles
* Max: There is a lot to unpack in this, I will do my extended Robin at lunch
* Thomas: solution to have an opt-out *rate*. If we know the rate, we could model that. The person that opted out might behave similarly to non-opted out. Free choice for the user but also provide some measurement. Could be an easy solution. 
* Roxana: that aggregate can be done privately (the opt-out rate)
* Ben S: To Nick’s quip earlier, we did have a consensus call on this point, and we did align on it. We agreed the opt-out should not be visible. If folks disagree with consensus call, we should revisit but I’m aligned. Wanted to thank Nick.
* Aram: moving to accountability
* Nick: very briefly, wasn’t planning on it. Goals here are aspirational.
    * Users should be able to investigate how they are participating
    * Capability for researchers / auditors can investigate if there is possible for abuse.
    * Some privacy risks are not at the individual level, we want other parties to investigate
    * Comprehensibility: users to learn and understand the implications. Open work on realizing that
* Aram: process-wise discussion?
* Nick: hoping to merge the PR, but I think we need to keep talking about it.
* Aram: Next step, merge it into our repo?
* Nick: Discussion on the PR next
    * https://github.com/patcg/docs-and-reports/pull/61


## (10:15-11:15) Attribution Level 1 (Part 1) ([#191](https://github.com/patcg/meetings/issues/191)) - @martinthomson

**Github repo: **[https://github.com/private-attribution/api](https://github.com/private-attribution/api)

**[EARLY DRAFT] Proposal text: **[https://private-attribution.github.io/api/](https://private-attribution.github.io/api/)** **

Slides: [https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/Privacy-Preserving%20Attribution%20Proposed%20Roadmap.pdf](https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/Privacy-Preserving%20Attribution%20Proposed%20Roadmap.pdf) 

Scribe: Arpana Hosabettu

Martin: [dramatic walking around the room]



* Like the fact that we are doing the work. 
* 
* More interested in shipping code. So here we can set down a starting point addressing very basic needs but provide a platform to improve and expand. Ship something and demonstrate whats possible.
* Proposal: Look at problems and focus on addressing basic use cases. Maintain privacy throughout, identify gaps, and goal to know the gaps and work on them in parallel and fix them.
* It's a strawman proposal but not going to be perfect. Take a note of those and start to put them down in a tracker and prioritize.
* Starting Point: PAM
    * This is what Aggregate ARA is anyway.
    * Individual DP that Roxana proposed on Wednesday is also central to ARA does 
    * Proposing to drop hard stuff
    * Find the things that can fit into the scope that is not going to delay shipping something that is maximally useful
* PAM recap
    * Impressions are saved in the browser. 
    * Conversion happens, which is attributed and aggregate reports are generated that produced DP reports
* Overview
    * Imp goes in the db, conversion goes in db, aggregation service produces dp reports
* Save Impressions
    * Basic information is added to the db: filter-data. Ben suggested numbers are enough. 
    * Where you expect the conversion to occur. We can late talk about conv that occurs in multiple sites 
    * Timestamp etc 
* Store
    * Associated with the target site where the conv might occur
    * Includes all the information discussed above
    * At conv occurs this is the browser end: query made of db. 3 main blocks
        * How much privacy budget is going to be consumed. Which aggregation service is going to 
        * How you perform attribution logic: last-touch, multi-touch etc
        * Size of histogram, Value
        * Finally: how you select the impression, how far back in time, which sites did they occur on and so on
* Delegation
    * Use something like permission policy, so adv can delegate a party on their behalf
    * Little difficult on conv site, since we want to do budget allocation which will largely be a browser choice. How much budget can be possible and how much budget in total.
    * ARA uses 10 delegations each getting X budget. Google can talk about this but you can imagine other browsers dividing the total budget by 10. Here we want to discuss the bounds on that. It would be unreasonable if only 1 was possible or if 10K was possible
    * Conv report itself will be an encrypted blob suitable for the aggregation service chosen. In working through IPA there is a core chunk of info that is small, and data associated with it can support quite large data,details will need to be worked upon 
    * Blob will be given to adv or delegates and those are collected and submitted to agg. Service. Yet to be specified either MPC system or the TEE based system used in ARA - a choice a browser would make. This would be built into the API that allows adv can choose based on choice of the browsers. 
    * We will need to work out details on all these options 
* Aggregation
    * How to submit things to aggregators etc 
    * DAP -  so some work on differential privacy and also anti replay already happening in IETF and we should use it.
* MPC
    * Scalability of this and submitting in a batch fashion
    * DAP is currently structured as 1 by 1 submission as well as budget tracking and we will likely want to batch as on this scale it may be an issue
* TEE
    * Similar constraints, lot of work has been done by folks at Google and we will need to sit down and put those details down
* Safeguards
    * DP
        * Central DP uses budgeting at the device level and application needs to happen in MPC. There are open questions but general direction is good ( [https://arxiv.org/abs/2405.16719](https://arxiv.org/abs/2405.16719) ). In short term - there are 2x noise but can be optimized 
        * Anti replay: Need to be specified, the way report is structured will need to support better anti-replay to ensure no duplicates, the same report does not appear in multiple queries. 
    * Transparency: accountability plan needs to be worked on: agg,service need to publish queries and this many budget and this many reports has been consumed.this is to ensure there are no abusive patterns in the queries. 
        * If you find 50 ppl with 10K buckets it might be concerning; Cannot determine exactly what the buckets are and what values are etc so there needs to be reasonable expectations.
    * Propose to defer:
        * Solid ideas for ML to support logistic regressions but we propose to set it aside until its ready
        * Also for multi-touch attribution 
        * Late binding: good properties managing fraud but require fancy MPC - we’d like to work on but right now keep thes
        * Ben - We should not put this in initial launch but continue to work on them
        * Massive histograms - DAP is not able to produce very large histograms there may be a need for other systems but cannot deliver it right away.
        * And defer anything else that requires a fancy MPC. 
        * All this is possible and many here might say we know how to do it - we need to get to a state on we can make this happen- Deferral is not rejection
    * Bunch of stuff not included in this presentation - adtech/publisher/DSP reports. We thought this was ‘easy stuff’ but ends up not; so if something fits and timelines won't be badly impacted then lets just do it. Like http-requests we may consider easy enough to specify in addition to javascript api then we need to specify
    * Suggestion: take the list of disappointments and have a discussion, capture them and put them on issues list and track them/prioritize them and shipping on main thing and have a list of items so we know what we can do. Love to hear disappointments and encouraging items. 
    * Started working on the spec for this, and hopefully this is a WG by the time we start and people can start contributing to move this quicker. 
* Questions 
    * Charlie: Request on task the group can do about massive histograms-how massive is massive. PCM supports 1000s of buckets, it has been found to be lacking across few users, so where we think the limits are; Other one - push back a little bit on things that slide say are easy they are not - biggest callout are publishing counts across all queries/metadata for strategies from system. This seems to be biting a lot more than we can chew, like leaking a lot of proprietary data. Final question - while going through js it not clear who the calling entity is, is it the origin of iframe or did you envision arbitrary origin 
        * Martin - Any origin permission policy permitting can write to the db.
        * Charlie - On the impression we wont have permission wont be from adv. 
        * Martin- db can record and adv from conv side can then add preference to from where it needs to be chosen. 
    * Ben - 
        * Which repo/tag should we use to add the list of items for tracker
        * [https://github.com/private-attribution/api/issues/](https://github.com/private-attribution/api/issues/) 
    * Nick
* Does the proposal enable interoperability of data across browsers, collect form across browsers and submit to a single Aggregation Service?
* Ben Case - Basic case - No if each browser choses different aggregation systems. In the long term it may be possible to break down different pieces to different browsers but not much value right now.
* TEE can take in the data assuming an MPC already has added noise then aggregate, there is a long term path there
* No technical limitation as per Ben said 
    * Max
        * Biggest thing from a publisher perspective is there could be unintended consequences if different browsers are using aggregation services -single browser would be able to provide different systems - this puts publishers at a disadvantage. So would be good if all could agree on 1 
        * How do we handle which one to take on from the tracker if there is a lot on the list
        * Martin - If its big but very important and delivers ton of value then we pick that one and discussion 
        * Michael - Simple answer to single browsers supporting multiple agg service Chrome allows TEE and MPC, but firefox is only going to do MPC only. Outcome of Chrome allowing 2 is that if you need to do across different browsers it becomes possible.
        * Max- that's not a problem, but if Google provides both and set of publishers with distinct users and some unindexed on Google. Using different models benefits different partners and create problem/disparities  in market accounts 
        * Output of the system is same irrespective of TEE/MPC system
        * Max- I doubt it can be that perfect and it can be exploited. If it becomes a fact great we can support both or many
    * Erik - It’s important there be many supports so there can be competitive markets rather than a monopoly so you can choose which one you want to work with. 
    * Joey - Some companies might show ads only in browsers, others show a lot of their ads in apps -  if this is browser only then we cut off a lot of folks. Add that to the disappointment list and it becomes difficult to put in the Operating system
    * Martin - Don’t have any influence on the platform that operate the OS 
    * ErikT - It’s worth pointing out that nothing in the proposal that would not work on app 
    * Michael - ARA has a precedent browser to work with OS and delegate when available 
    * John Delaney - Word of caution on simple implementation to start with- Continue adding 1 field, change the string to int etc, so we should stop and look at where we want to be.
    * Martin - We just have to keep on top of it, the price we pay for delivering something. We have to rely on lot of people with ton of experience and draw on that to build this. 
    * Chris Patton - Work on DAP stuff, comment of size of histogram. People are thinking of PRIO - one of them is linear in the len of histogram and another is constant size. Quickly plug a new protocol [Mastic](https://datatracker.ietf.org/doc/html/draft-mouris-cfrg-mastic) (also: [https://eprint.iacr.org/2024/221](https://eprint.iacr.org/2024/221) )-  trading communication cost with cpu time. Size of report is no longer linear in the len of bucket so it needs to be predefined
    * Isaac -  Am i right in understanding that goal here is 2 things - 1)  something that is acceptable as starting point (Isaac addition) to all the major browsers 2)More than 1  production use case for ads/marketing/measurer’s  supported, i.e. this might not address CPA but addresses something generic like conversions on top of CPM 
        * We are just saying not now but work towards here are the list of things but would be good to at least say yes/no.
        * Martin- Nothing stops us from collecting the stuff, there are things that we can do now, and things that are aspirational and would be good to know
    * Andrew Pascoe (very supportive, should keep in mind “build one to throw away,” perpetual refactoring, requirements changing over time, etc.)
        * Testing Privacy sandbox - huge value in building against something and testing, it helps develop things. Kind of tying to what John and Martin were saying with agile development, we might have to build something to throw away. Requirements change over time, we want to learn and adapt. So embrace perpetual refactoring etc might be good put in principle. And finally - no disappointments, i am sure those will be deferred and will come up.If anything starting point might be complex and willing to start something sooner.
    * Thomas P - love the choice between TEE vs MPCs & the aggregator choice, and “things to tackle later”. The payload should be flexible, and we should allow some replay
        * We like the TEE vs MPC choice and also love the fact that ML thing in feature list and will be good to start shipping so love that approach
        * Shared the payload that could be something that can be sent to MPC - is this fixed? 
        * Martin - DAP has a protocol , that might be something we’d ship. TEE has something else. So ultimately this is about contributing to an aggregate histogram, so it can be flexible needs to be worked on
        * Thomas - We should prevent replay, but its the key so should not limit it, but allow coarse grain data and later allow fine grained data
        * Martin - 1) If you  know you want to be using multiple queries then ask for multiple reports, we had some discussion about taking 1 report and submit multiple times and say I have X epsilon and want to spend y amount out f it,
    * John Wilander (Thanks for this proposal, looks good to us high level, love to see actual API shape. The terms report collectors and aggregators – who is the recipient of the aggregated data and the recipient of data to aggregate? Are you envisioning a menu of supported aggregators per browser or a site choice from some central menu?)
            * Starting to shape into a real thing - I love that. Thank you Mozilla and Martin for putting this together and Ben's help.
            * Roles of delegator -  Merchant site picked an aggregator . Are you envisioning that they know a menu which one to pick from, are these browser menu or default it falls back to
            * Martin - Proposal we are working towards,each browser are working on an aggregator and trust and list would be provided via API. Go to the API and say pick from the list. Its sufficient since you need to arrange to pay/contract with that provider. As a merchant - develop business relationship and then hard code to the website. 
            * John W Confused a little bit of terms - would there be multiple and would they pick more than 1 in MPC?
            * Martin - you only interact with 1 party (DAP ) you are unaware there are other parties involved.
            * John W - We should make this clear in specification and the roles of them
    *  Christina Ilvento (Simplifying server side discussion, how much needs to be in scope for the initial version)
        * Echo John W. We want to think about how much server side decisions we need to make now, suggest deferring those and focus on the client side unless we think it changes the decisions we are making on the client side.
        * Martin - Yeah, if Apple is telling me that's the case, then that might be good. 
    * Martin - Good discussion, would like to put an official stamp and have some more folks contributing to this and put together a team. Come and talk to me if you want to be involved. 


## (11:15-11:20) Break


## (11:20-12:20) Attribution Level 1 (Part 2) ([#191](https://github.com/patcg/meetings/issues/191)) - @benjaminsavage

Scribe: Ben Case

Slides: [https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/Privacy-Preserving%20Attribution%20Proposed%20Roadmap%20(continued).pdf](https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/Privacy-Preserving%20Attribution%20Proposed%20Roadmap%20(continued).pdf) 



* Aram: Ben on next section 
* Ben Savage:  more consensus than expected already.  Some more detail on things we have a good idea how to build.  How to actually build these Level 1 things. 
* Delegation
    * Many Advertisers will need to delegate, collection of reports, submitting queries, and viewing results
    * View delegation as a must have for level 1
    * Slide measureConversion.  Could have one or more iframes on the website and you can provide them permission (permission policy) to call this API and spend their budget on their behalf. 
    * How could this work.  Googler’s have asked to support multiple measurement partners.  Multiple parties can call on the advertisers behalf.  Browsers can make different decisions about how to configure options for delegation.  Can bound the total to all delegates, can bound the budget for any one.  We don’t need to specify in the spec just how the browser can specify these parameters. 
* X-pub attribution 
    * Another thing we think works out of the box is x-pub attribution.  We saw earlier the basic use case of advertiser explained how they want to see how much they are spending on different channels where they are buying ads.  
    * As charlie has suggested having conversion side breakdown keys. We can let this leverage data in the impression database. The browser can add things automatically to the database (tld, iframe, intermediary). 
    * So could do a breakdown by the intermediary site, the site that actually served the impression.  
    * This seems easy. 
* Anti-replay protection 
    * We have a good design for this already that scales without storing all the records.  Can store a timestamp. Likely can lift the same replay design as ARA.  
    * As Criteo folks talked about you will want to run multiple queries on the same attributed value (e.g. daily and 30 accurate query). 
    * We can have separate segments or pipelines with replay protection enforced on for them.  You submit a batch of reports and it updates the timestamp in the anti-replay protection 
* Dp noise
    * When measureConversion is called epsilon is passed to the device to spend. Checks to see if you have enough budget to get a legit report. The epsilon gets bound to the conversion report in the associated authenticated data. 
    * The aggregation service can check that the same amount of budget has been requested for all reports in the query. 
    * Martin: you might tell the device epsilon of 5. The aggregation service needs to know that epsilon of 5 was bound to each.  If one has epsilon of 2 then they will need to drop it. 
* Ben: now we can discuss. Any issues people see? 
* Charlie: question on delegation proposal on adv site.  You mentioned permissions policy but I guess open to others. What do we consider the root of trust for adv opt-in?  Java script in top level on adv site.  Do we think that is the model? Do we want a strict root of trust? Something not tamperable by java script running in the top level. Instead http header or ping to advertiser. 
    * Martin: if you include java script from other sites they will be able to set permission. Also in header bits on page if you want to prevent scripts from changing the permission. 
        * Charlie: question about defaults. Enthusiastic consent from adv or anyone on top site? 
    * Ben: suggestion?
* Charlie: want to raise the issue of possible race to spend the adv budget if many can give themselves permission.  In tension with needing it to be done on Adv server, when is a “turn key” approach which wouldn’t work as smoothly with all current deployments
    * Michael: suggest a .well-known file for adv to avoid the race condition and simplify deployment
    * Nick: we talking impression or conversion side? 
    * Martin: the contention is on the conversion side where request to spend the budget occurs. 
* Charlie: we talk about adv consent to this. When we talk about x-pub queries, we need to also consider the opt-in of the caller of the impression api.  If i participate in this system but don’t want some other party to use data from ads that i served for their measurement, we may want to require a reverse handshake that requires the impression site to option
    * Ben: specifically don’t want us to do this.  Channeling Robin, we don't want to introduce a point of control that prevents the advertiser from measuring their ads.   Otherwise there will be incentive to continue status quo of not supporting letting the advertiser query their data just because some DSP don’t have incentive to let adv measure their ads against other ads the advertiser is buying.  We should see as the adv’s data that they can measure. 
    * Aram: but still let the top level site serving the ads opt-out? Be able to say don’t participate in this API.  can not allow other scripts on their site showing ads to call this API
    * Ben: yes, martin has said we shouldn't do that
    * Michael: are you asking to design something that deliberately doesn’t support the status quo? That seems odd
    * Erik:  you could still support the status quo. 
    * Ben: yes you could still filter to support the status quo measurement of one publisher.  
    * Erik: but would also allow the advertiser to decide to do more than the status quo of measuring across multiple places where they are buying ads. 
    * Erik: specifying the default of how privacy budgets are allocated here will need to be considered. 
* Aram: breakdown key question. Could breakdown by other things like tldr of where the ad is shown. So this is not already shown? 
* Ben: you might want to do funnel analysis. You know what conversion type you are calling about (cart, purchase). And in histogram you could have multiple of these in the measurement.  But you could also add breakdown about which DSP saved the impression. 
* Aram: breakdown key is extremely useful to have in level 1
* John D: on conversion side it would be interesting to see how much we can use for histogram.  Want to push back on ownership model. … one thing we’ve seen in ara is a state across conversions, in this case there is a state across impressions and we don’t want other ad techs to influence other ad techs impressions. 
* Martin: have some ideas but see as a layer on top
* Roxana: relevant for user time dp?
* John: about influencing another ad tech’s budget to your advantage. 
* Ben: agree we should consider how to prevent this
* Arthur: how to deal with bias in multi-channel. Tammy talked about before.  You may time out at different points depending on what sites you visit. More bias for sites that people visit more.  How to allocate budget for sites.  Need some way to measure bias. 
* Ben; no budget is consumed by just showing an impression. And we have a path forward to measuring the amount of budget.  Michael also mentioned about incorporating the error bars into the system. If we can have someone increase the error bar due to having someone out of budget. Yes we should do. 
* Issac: thought you said including more impressions sites and privacy budget? 
* Ben: not sure
* Issac: i’m on the adv site and looking for an impression, is the breadth of sites going to consume the amount of budget that I am consuming? 
* Ben: no is the epsilon you are passing in.  you need to also tell it the max value. 
* Issac: impression is site or who showed the ad? 
* Ben: we can do both. You can filter by different characteristics of the database. Filter to do status quo measurements. 
* Issac: so you could look for all ads of one DSP even if showing on many sites. And not spend more budget?
* Ben: yes, 
* Roxana: when running on multiple epochs you pay for impressions you select.  You might select from multiple epochs and then you do attribution value assignment. x`
* Issac: what if i’m looking for last impression that occurred but 3 occurred in other epochs? 
* Roxana: right now we need to deduct from all epochs even if you don’t attribute to. We are thinking if we can optimize more.  
* Issac: you could make separate queries for different epochs. 
* Martin: maybe … we can look into.  We can keep working on better understanding the analysis 
* Max qq: ridgid math can be good, but there can be a way people work issue here for how people plan to spend their budget.  People do things like loose reports or query the time period and they might do that after they have spent all their budget. They will want to re run
* Roxana: people will need to change how they think about the resource of privacy. 
* Max: I don’t disagree but you will get push back on this when it goes into the real world. It will be a bigger issue than you expect. 
* Charlie: we have some experience on this in ARA. 
* Issac: some of your concerns would be handled by saving the result of the query. 
* Max: yes, but there might be people who change their minds after you set up the result of the query.  I’m okay to hear that its fixed but you will hear feedback on this. 
* Daniel: here we have early binding which late binding would help to address. 
* Aram: our messaging here will be important and the UI we give to users will be important. It would be good to see the vendors involved in generating reports perhaps show some UI examples on how to make this clear to users. 
* Ben: people make mistakes.  So we make sure the epoch length is not too bad. Shorter will let you resent more often. Suggest a week. 
* Miguel Morales - Purpose of impressionSites, knowledge of impression universe by advertiser, purpose of breakdown key (bit limit?) 
    * Filter is a field and if you leave blank you get data from all publishers.
* Ben: yes
* Miguel: other question on breakdown…?
* Christina: having multiple impression sites – we will want to explain to users and the scope of what is covered. Will want to understand if you give your demographics on one site that other publishers can not get access to my demographics.  Glad aligned on using DP.  In goal of simplicity might be good to put some constraints on this. 
    * Ask to John or Haley if they have feedback on how impressions saved
* Ben: Charlie talked about saving impression under who is storing it so that we can make sure they can’t fill up the storage and we can evict them first
* Don: what size of the impression site list?  Be good to be able to filter out bogus sites. 
* Ben: on impression sites, you will want to list intermediaries and maybe could also add some filters to exclude bogus sites. 
* Erik: privacy benefit of short epochs. Less to spend at one point. 
* Charlie: two ways we could do breakdown key. One joined in encrypted payload. But if just a conversion side one we don’t need to hide it so we could put in authenticated data and partition replay protection by it. 
* Ben: sum of add to cart and purchase? 
* Ben: yes sounds useful. 
* Issac: epsilon and epoch length operational considerations.  Could it be configured at browser level? Could it be configured by the site with different types of campaigns? 
* Ben: sound complicated
* Roxana: epoch length has meaning for the privacy to the user. Would suggest fixing both. Adv can still query wider than the epoch length. But from budgeting the length and epsilon both impact privacy. 
* Issac: entity updating impression store, could there be a way to mutate? Replace based on a key. This way you can query just one query.
* Ben Case: sounds interesting way to address your problem. Don’t have an immediate answer. 


## (12:20-1:30) Lunch


## (1:30-2:15) Updates on Chrome's Attribution Reporting API[ #193](https://github.com/patcg/meetings/issues/193) to- @hpatoski

Slides: [https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/ARA.Updates.%40.TPAC.2024.pdf](https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/ARA.Updates.%40.TPAC.2024.pdf) 

Haley Patoski - Learning from testing we have done so far.

Small sampling of people who are testing shown.  Broad range of participants from all aspects of the industry.  

Seeing a 23% of page loads call the ARA

Broad Learnings



* Engage and get Feedback.  Not just from 1-2 partners but a wide range of testers and industry players and users of the API to understand how the API is being used.
* Flexibility.  Helps accommodate more use cases.  Instead of building purpose built solutions, leaving implementers flexibil;ity works
* Testers need help to understand privacy principles.  Big shift.  Helping the understand how that impacts implementation and strategy, how to set up their systems etc. important

Learning #1



* Deploying and monitoring private APIs is difficult for developers.  Hard to compare to the status quo.  Need to understand that the setup of their private API is compared to how it works today  Initially built transition debug reports for this transition.  To enable this on web traffic, we built in a debug solution to help with that
* Provides an example (in the slides).  In the debug solution, store impression, use up conversion, budget has been exhausted 0 does this conversion get attributed to anything (priori question).
* We have built aggregate debugging so they can set aside a slice of their budget to set aside for debugging purposes.
* Now they actually receive a debug report to help them understand what is happening

Aggregate Debug Reporting



* Same supported use cases as verbose debug reports.
* Allows creation of histograms of various browser-defined debug events
* Very similar to aggregatable attribution reports - like those today -0 requires using the aggregation service
* Reports are sent unconditionally
* Shows example of what report looks like

**Learning: One size does not fit all**



* Doesn’t work for all use cases 
* This is where flexibility help users to achieve their specific goals
* Example: ad tech may want to aggregate different types of contributions on different cadences - example counts vs. values
* SOlution is flexible contribution filtering.  Looks like the way the original design says the whole report has to be sent to all contributions - no ability to look at one contribution early and one let
* With flexibility contribution filtering allowing an ad tech player to submit different timings on a single report

Flexible contribution filtering (example)



* Each contribution can only be used once
* Each contribution can be done at a different cadence

**Learning: Latency and delays break critical flows like monitoring and optimization**



* Example: Reports are scheduled to be sent with a delay..  The user closes their browser and report does not get generated
* Solution: instant aggregate reports.  Reduces transmission loss and more easily verify reports and filter out unwanted reports

**Learning: Engagement with the industry helps to uncover unique business needs.**



* A marketplace site is running ads for different vendors on their site and they only want sources from that site in their reporting
* Exampole: Previously, the wrong source could be attributed.  So with the new model is “pre-attribution” filtering.  We allow them to add a filter for which impressions that can be applied for certain conversions
* They can still do post-click attribution.(
* Attribution scopes - allows filtering of sources before attribution takes place, giving flexibility to only considered sources

ARAs Latest Features



* Slide showing a matrix of features and descriptions (put chart here)

**Question and Answer**

[Ben] Earlier, the code that I shared suggested filtered data for exactly that kind of intended use case and I was trying to think why I would need more than ---- - seems to me each vendor can give a hint and at run time you can provide vendor’s hint.  So wondering why you need strings?  Is there a different use case where you need a list of strings.

[John] - In a lot of cases, hints would work.  If you think about bigger advertisers like a department store like Macy’s - I might have multiple customer aIDs - multiple different campaigns targeting multiple audiences.  So it can’t be just one single thing.  I may run two campaigns and I want to convert either of those.  

Example - two different ads for shoes - for the same shoe - and in those cases we have to determine who that is attributed to.

[Aram] - This is the multiple product in a single example.  I think what is causing this confusion is that I have two people running ads both of which show ads for shoes and shirt and the conversion being tracked is the version where someone clicks on on the shoe in the ad

Not quite.  

SPecific example:

The reason here is because we have multiple dimensions - this ad related only to advertiser 1.  And advertiser is selling 7 products.  How do I attribute that?

[Ben]  DIfferent browser could have different retry logic - varies how and when a report is being sent - from browser perspective- how much of this part do we think we can standardize?  I’m sure there is some kind of retry logic in ARA obviously?

[Charlie] - These instant reports don't need to be as complex.  I am not sure we need standardization - kinda like Fetch - would happen right away.  I think it is less critical - all the complicated logic is when you have to delay 10 minutes- 1 hour when the user isn’t on the site and has closed their browser.

[Ben] Every time we have a high entropy ID - every time we have it and I have to explain it - people get confused

[Charlie] What this is trying to accomplish is what you tried to accomplish - you can use Fetch API to send it off to some endpoint.  The reason we have this is we are at the http layer and there is no javascript variable that we can associate with it.  That;s why it is there—to allow for that connection with context.

[Ben] Are we married to name filtering ID here?  This is more like clustering for different types of queries.  How did you come up with this name

[John] These names are the names of the histogram - -----.   That gets bundled in a set of contributions.  The way the aggregation service filters out the ----. 


## (2:15-2:45) Attribution Level 1 (Part 3) ([#191](https://github.com/patcg/meetings/issues/191))

Request: what do we do next.  The chance for the chair to lead on this one

[Aram] We have some fairly high interest in this approach.  There is a lot of interest in moving forward on it.  Not a working group, but we will have one soon so we will move forward as if it exists.

What we can do is to ask this group if they are ready to bring this into the group for more work.

[Sean] We know it isn’t perfect.  You have to get over that.  We know the general direction we want to go, but if we wait before it is completely done it will never show up.  (Editor’s note: Good lean principles).  We need a consensus call - get back together, judge how to proceed.

[Martin] This is a starting point.  Once it becomes a working group, you get together and you can throw it all out and do something different but it is time to get started.

[Eric] What do you mean by bringing it in?  Martin and Ben have started - we can move it to the formal repo or the draft repo - which are you proposing?

[Aram] Idea is to bring it into formal repo.

[Martin] When we have a working group we can move it into the W3C  area.  This is the timeframe we are talking about.  That is a pretty common path.  The community group doesn’t have formal standing.  But once it is a working group, then it has formal standing.

[Aram] Are we aligned? 

[Ben] Was wondering if we should use this time to create to-do lists. Example: I really love the transparency and accountability idea, but from what I am hearing it would derail other elements of the proposal

[Aram] - We can move that in a little bit.  Still have organizational stuff to do

[Nick] Do we want to talk about continued work on the CG?

[Aram] - There will be additional candidates for the CG to work on.  More along the lines of measurement - there will be additional features once the measurement spec is done that the CG will work on.  Also opens up an opportunity for the CG to consider proposals that have not typically been on our radar but now could be.

[Nick] I like approach of starting with measurement but want to see us incubate other ideas.  Other parts of online advertising that need to be more private and need our attention

[Sean]  Specifically in the working group charter - it will ask for working group feedback and determine whether CG group is still needed and how meetings will go.

[Aram] Additionally important to acknowledge that not every stakeholder has an interest in all topics.

[Thomas] Mentioned MVP - we need a place where the list is outlined because we need a place where we can say what we can contribute.

[Aram] Put this to Ben’s point - the PRs issues and github activity.  If you want something to persist or a conversation on what we are talking about, make it a github issue.  Talking about moving that into PATCG so people can get more visibility into it.

[Thomas] - Do we need more meetings?

[Aram] We are going to have the meetings that are pre-scheduled for this year.  For next year, can be updated/changed.  Up to editors of doc to work on changing the groups schedule.  In this case, Martin and Andy.  

[Martin] -- Listed at editors because we have done the work but happy(!) to step aside.

[Aram] In terms of adding this to PATCG and github organization, let’s do that now and let’s do a consensus call.  And if we agree, that moves us closer to an active working group.  

[Sean]  Need to have people not here have time to have input - need a consensus call in a week or two to do this?  Our folks aren’t shy and will be willing to speak up

[Aram]** Formal consensus call:** 



* Proposed: Are there any objections to move the proposal discussed here today to move this into the PATCG github organization?
* Response: No objections. ** We consider the call for consensus successful.  **People have a week to give input.  Put on agenda to move into PATCG github

Things we want to defer and include;

Would be happy to go through remainder of this time to go through that list

[Ben] At end of this session, put a document into our repo with both lists to simplify how we have this discussion about.  

[Max] Like idea of getting out ahead of this.  Want to propose that in developing this list if it is possible to look at things that we would like to defer in batches, 1st batch and 2nd.

[Arthur] - Happy to document roadmap discussion

[Ben Savage] Messaging and setting expectations correctly is very important.

List

[Ben Case] Things to defer - list is fine, but not always easy to do the combinations correctly.  Think it is good for everyone to give input on the hybrid proposal so we can get a better feel to what is important to have both short-term and long-term.

[Nick] If we want to debate

INCLUDE:



* Transparency for two reasons
    * Design input from builders and users of the system
    * Users have learned, from decades of experience of abuse by online advertising ecosystem, to distrust everything they hear.  So we want to give users confidence about how this works by being transparent, in order to give them some reason to accept.

[Ben Savage]

INCLUDE



* Trigger Context (Filter) IDs
* Instant reports - necessary if you are using http
* Difference scopes - filtering done by the server?   - filtering ID - including a 	breakdown key in the ARA.  
* (Seems like an easy thing to include

[Isaac]



* D0 you think there would be room for shaping how that is available and how that would get pushed out.
* With reporting, I have done things where you have simple static metrics to start just to get to MVP

[Nick]

That’s what we can have in short form.  We certainly can do that in the short-term and we should continue to iterate.

[Isaac]



* Basically something quick but with limited capability sooner is better

[Roxanna] May be multiple aspects of transparency.  In V1, the real privacy control is in this device.  That’s where the limit is imposed.  You can provide transparency by providing some data in a tab showing what has been sent - which report went to which advertiser - a simple UI could be part of this .  The user agent is the control of your privacy loss - so put the information there.

[Joey]

I want to understand why this is difficult?  When I heard this I thought of something like the chrome settings page that provides some simple, straightforward info for the end user.  What is the difficulty?

[Ben]

Two separate transparencies



1. The one you describe is easy and it goes on level1 list
2. The other one - idea that secure aggregation service publishes public information about how many queries were run, how many records were in them -0 so the public could get transparency in how the data is being used  - in privacy principles Nick had some items that resonate well with that - that potentially reveals information about how many ads were served on your website over time.  That is considered business private information and not wanting to have the whole world know about it.  That would potentially slow down our adoption.  So we have to think about this - and I suggested a couple of ideas for how this could be done.  For example, controlling access to that information in some way - so it stays private.  Or what if some aggregation services published these reports and some didn’t.  So this isn’t as easy to solve.
3. 

[Don] Definitely agree with Nick’s pont about transparency being essential.  I believe we are talking about making free riding free and undetectable—you can choose not to participate in the system.  And not every page visited and seen by a user where an ad is shown is from a publisher that the user wants to support (common to visit pages accidentally).  Some people will be given information on transparency and how the information they choose to provide will help the sites they visit, and that may be a negative considering the overall trust level.  This issue needs to be addressed early.

[Thomas] 



* Delegation as a must
* choice of TEE and MPC
* Delegation and choice between the TEE and h---
* Need viewthrough and clickthrough support - somewhat obvious to folks here.  You can choose to attribute to last ad seen

[Ben C]  ( we can also choose transparency metrics which show something about privacy properties (e.g. average amount of aggregation) but not revealing the total number of impressions.  For example revealing the ratio of number of breakdowns and number of input records to queries. 

[Ben] I don’t think it effects the client-side web.  Should be interaction between the server and what the client-side spec looks like.  We can make movement there and keep talking about what server-side transparency metrics are needed

[Andrew] For Nick: when we talk about transparency metrics - when we talk about them - it sounds like it will reveal a lot of company information.  But not sure how that gives trust to the consumer?  What are you thinking about specifically.  What metric would increase trust.

[Nick] Haven’t figured that out yet.  

[Andrew] Does anyone else have ideas about that?

[Nick] SOme high level about how much information is getting used.  Some patterns or signals that are unexpected that would signa; a ‘dangerous’ use.  Example - one query had a small number of users - that should get flagged.

[Roxanna] the differential privacy guarantee is the same no matter what the size of the underlying database.  Main value of a DP guarantee

[Nick] Is that true even with information outside the system?

[Roxanna] Completely independent of outside data

[Ben] In traditional barebones DP, but empirical DP there is a significant difference.  If you run a query on 100,000 unknown variables and dont know if conversion has happened on any of them, the leakage can be large and yet you learn nothing.  Analyzing this usage - large aggregations over huge number of people

Talking about using empirical DP on real data from real people, aggregation is very meaningful

[Roxanna] The challenge with empirical DP is composition.

[Ben] For same IDP guarantee on my device - if you analyze the output of the same IDP system then that is problematic.

[Aram] So traditionally we have not talked about UIs, but talking about trust within the browser, but it may be interesting for implementers to share thoughts among UIs.  People who are concerned about trust to give feedback on this.  Putting it out for discussion.

[Don] The pitch for getting users to leave the system turned on - is likely to be something like: this is a system that supports the sites that you actually like  As long as intermediaries are in a position to advocate for the system with users the disclosures that they make need to reference something about the sites that are actually participating in this.  One useful metric:  certain sites that are able to see views and collect clicks but add little value to users, make it clear how much attribution “credit” is flowing to problem sites.  In this case, it would be useful for intermediaries to disclose that that intermediary dropped for a policy violation (not just privacy, also copyright issues, malware, etc)

[Aram]  Ad tech provider is intermediary?

[Don] Yes

[Charlie] If we want to have some other formal notion of privacy beyond IDP, we should schedule a tech session to discuss this.  There is a lot there to unpack. Might tie it back to the anonym workstream on this. 

[Ben] 

DEFER



* Publisher/AdTech queries - unless revolutionary breakthroughs, this is complicated.  Put it on the ‘soon’ list, not ‘less soon’ list
* Having one conversion that contributes to multiple buckets in a single report - Short term, suggest there is a workaround by using filterID and registering multiple conversions for each real conversion to do that instead of having a single conversion.
* Multi Touch - Proposing to defer.

[Isaac] We are talking about this in terms of level 1 and 2.  We are trying to achieve two things

1. What can browsers / ad techs support?

2. What is real world

Shouldn’t number two guide our decisions?

Am I understanding correctly that we want our first cut to support something?  Eg. CPM conversion measurement where billing doesn’t matter.

Talking about needs in the abstract is problematic

Is level 1 the consensus between browser consensus and usability

[Ben] It is what we want versus level of effort.

[Aram] You will find that some items will be Level 1 but there are things we want to move forward on that will either move forward because they are required to deliver level 1 or are deferred because the items in Level 1 are needed to deliver them.

What do we absolutely need?  

[Isaac]  Would Criteo and XandR - we have uses cases for this and that would guide our decisions.  

[Aram] We will open a PR and gain a consensus or add to next meeting agenda.


## (2:45-3:15) Learning using aggregation APIs[ #192](https://github.com/patcg/meetings/issues/192) - @mvono

+

## (3:15-3:45) Learning inside a trusted server ([#187](https://github.com/patcg/meetings/issues/187)) - @fhoering

Executed benchmarks and sample code [https://github.com/criteo-research/dp-sgd-ad-click-prediction](https://github.com/criteo-research/dp-sgd-ad-click-prediction) 

[Slides](https://github.com/patcg/meetings/blob/main/2024/09/27-tpac/PATCG_Learning_Via_Aggregation_Servers.pdf)


* [Fabian] 
    * Follow up from this morning. Motivation first, then ML learning.
    * Motivation: hybrid proposal is the right direction. Important to move forward and test. Also important to look at future features and not get stuck. Scope is mostly attributing impressions to conversion. Possible to use static urls that enables aggregated metrics.
    * Campaign optimization use case. Hybrid has a lot of complexity, added value is limited. Important to activate more use cases.
    * ML
        * Input: features + conversion label
        * Goal: optimize ad campaigns
        * How: learn probabilities
        * Execute: see same features, maximize probabilities
    * Privacy Sandbox CMA test
        * 3 populations. Status quo, cookieless, and privacy sandbox.
        * Large impact on publisher revenue. (~ -50%)
        * [link to Garret Johnson’s paper]
    * Looking into including targeting data in a privacy preserving way. Applied for Contextual Optimization as well.
* [Maxime]
    * 3 options for ML
        * 1. Noisy event level
        * 2. ML w/ global dp via aggregation API (sum/counts)
        * 3. ML w/ global dp via trusted server
    * Local DP
        * Pros: 
            * is agnostic to reporting downstream tasks
            * Very easy to use with current stack
        * Cons
            * Learning is biased
            * More noise than global DP
            * Adding feature privacy further hurts performance
        * Future steps
            * Dense vectors
            * De-bias user features
            * 
    * ML training via aggregation API
        * Pros:
            * Less noise
            * Aggregate statistics are partially reusable
        * Cons:
            * New learning paradigm
            * DP budget scheduling. Constantly balancing utility and privacy
    * ML training from label proportions
        * Ad tech companies do not have access to left side of the data (see slide). 
        * Access to back propagation
        * Two main routes
            * Try to predict label proportions. Minimize discrepancy between aggregated label and aggregated prediction.
                * Want to predict accurately the probability of clicking on an ad.
            * Label proportions:
                * 1-1 mapping with binary classification. Label DP makes debiasing possible.
                * Estimate with larger variance, need more data.
    * ML training vai gradient querying with DP
        * Gradient is an aggregate statistic. Can query this. Online learning problem. One stop of gradient descent.
        * Global DP amounts to un-biased gradient estimates with larger variance.
        * Better results than local DP (~ -10% in LLH vs -25% with ε = 5)
* [Fabian]
    * Seen that it’s possible but it’s complicated.
    * Current workflow. (see slide). Looks very similar to hybrid. Reports would include full feature vector and label (could be positive or negative)
    * Collected and sent to trusted server. Trusted server can see everything, as it works today. 
    * Apply global DP. Then could do whatever you like with the model.
    * Pros:
        * Much less noise than local DP.
        * Very close to current design.
    * Cons
        * Likely higher trusted server cost
        * To limit noise, more data, less models, etc
    * Encrypted report is not a breakdown key, it’s full feature vector. It may include user data. Needs positive and negative values.
    * Output is not a histogram.
    * Could be injected with Protected Audience API. contextual optimization also applies
    * Experiment
        * Logistic regression with SGD
        * Criteo ML challenge dataset with 171 features
        * 15 epochs
        * Estimated to train ~10 models. Can not train a model on the full dataset.
        * With A/B test, that 2x the models. Usually more than 1 A/B test.
        * May want to compare offline metrics. With 1 day of data, ~50 such experiments. Full model can live in the trusted server, only the aggregate metrics come out of the server with DP.
        * Source code is on github [[Link here](https://github.com/criteo-research/dp-sgd-ad-click-prediction)]
        * Noise is Gaussian. Impression level DB budget. Dataset doesn’t have user id. Epsilon scales to the square root. 
        * Less models, re-learnings, or features → less noise
        * Benchmark: target epsilon 5. Data set is 100m lines. Higher the batch size, the more noise you get. Only worked with 1m.
        * Used reference metric for offline experiments. For ε = 1, -4%. ε =5 … even ε=1 is acceptable.
    * Conclusion
        * It’s possible to apply global DP. 
        * ε = 28 is well above DP recommendations.
        * There is an advantage to larger players with more data.
    * Next steps
        * Could do more experiments
        * Utility / privacy tradeoffs. Room to get both.
        * Levers to pull, epochs, # models, etc
        * Measure user level DP
        * Publish extensive benchmarks
* [Charlie]
    * How high priority is this with / without Protected Audience.
* [Fabian]
    * Important in both. Contextual optimization outside of Chrome is still very useful.
* ..
    * Optimizing for first party data is also very important.
* [Ben]
    * Thanks for the presentation. At the beginning, you led with how important it is for model training to have access to private features. Do you have any proposals for how we’d get access to private features? 
* [Fabian]
    * Private features means user and advertiser data. Could be previous impressions. Maybe shared storage? Maybe someone else can add other ids?
* [Ben]
    * Possibly something the CG could keep talking about.
* [Roxana]
    * Batch size are recommended.
* [Fabian]
    * For performance, the larger the batch size the better.
* [Roxana]
    * Availability of data. Only cases where large scale models can be trained with DP. Is there that availability?
* [Fabian]
    * It won’t be a deep model. It will be shallow with limited features due to DP SGD.
* [Christina]
    * Are you describing that you are adding noise per contribution, or to the gradient?
* [Fabian]
    * No to the gradient.
* [Christina]
    * Confused as to why we’d have less noise.
* [Fabian]
    * Complicated, take it offline.
* [Isaac]
    * Roughly the idea: input into box. Might be encrypted results from a protective auction. Run model, then have noise. Able to run the thing you want to run, but what comes out obeys the noise constraints.
* [Fabian]
    * Also, code is open source so folks can replicate it.
* [Isaac]
    * In the system, the thing that’s coming out is being released back to you, and into your bidding algo?
* [Fabian]
    * Model is DP, so I can take it back and use it.
* [Isaac]
    * Did you play around with the idea of the model coming out encrypted and into a protected auction?
* [maxime]
    * …
* [Isaac]
    * Could go back to the K/V server. Expanding the box to be 2 boxes.
* [Michael]
    * We’ve thought about this a bunch and it doesn’t seem feasible. If part of the story is that the weights are too private to take out the box, then you would also need a budget to run inference on the model, otherwise you can exfiltrate the weights.


## (3:45-4) Working Group update

Philippe Le Hegaret

We had a formal objection on the [formation of the] working group and the formal ETA is before the end of October for this to be done. I’ve been talking with the AB and they and the Team are working as fast as they can. 

This is still happening. Working Group by the end of October is the schedule. 

Sean: 



* Two questions
* We earlier had a call about adopting a document and then moving it to the WG 
* Do we get the w3c/pat-wg repo automatically? 

Philippe:



* There’s not a set thing yet, but we will figure it out, likely after the next two weeks. 
* We have an example of the FedID WG
* I try to get a little bit ahead 

Sean:



* How long is the time to wait for the first meeting and official adoption of the document?

Philippe:



* The lawyers for companies are a little less fast - that is out of our control. 
* Some have already approved, but it is slow. 
* The good news is that the staff withdrew from changes to the charter and that should help. 
* How do we transition a proposal from CG to WG. 
* Look at process from FedID working group 
* That shows how to move from CG to WG
* Look into it and you may get good ideas 
* Also have it in place for future things that might get passed from CG to WG. 
* 

Nick: if we were to have another Formal Objection in the future, what will W3C do differently in processing objections? 



* PLH: Parallelizing our responses. Not relying on blockers. As in other groups, we are moving way way faster. 


## Future Meetings 



* Meta - Seattle or London might work without NDAs
* Let’s get it on people’s budgets now. 


## Participants



* Sean Turner (sn3rd)
* Aram Zucker-Scharff (The Washington Post)
* Alex Koshelev (Meta)
* Aloïs Bissuel (Criteo)
* Andrew Pascoe (NextRoll)
* Andy Leiserson (Mozilla)
* Arpana Hosabettu (Google Chrome)
* Arthur Coleman (ThinkMedium)
* Aykut Bulut (Google Chrome)
* Ben Kelly (Google Chrome)
* Benjamin Case (Meta)
* Benjamin Savage (Meta)
* Brandon Maslen (Microsoft Edge)
* Cathay Li (Meta)
* Charlie Harrison (Google Chrome)
* Christian Berkhoff (Meta)
* Christina Ilvento (Apple)
* Christine Runnegar (PING co-chair)
* Christy Chen (Meta)
* Daniel Masny (Meta)
* David Dabbs (Epsilon)
* Don Marti (Raptive)
* Elias Selman (Criteo)
* Erik Anderson (Microsoft Edge)
* Erik Taubeneck (Meta)
* Ethan Leeman (Google Chrome)
* Fabian Höring (Criteo)
* Fatma Moalla (Criteo)
* Graham Mudd (Mozilla/Anonym)
* Haley Patoski (Google Chrome)
* Isaac Foster (Microsoft Ads)
* James Honaker (Mozilla/Anonym)
* Jay Kishigami (W3C)
* Joey Knightbrook (Snap)
* John Delaney (Google Chrome)
* John Wilander (Apple)
* Jolyn Yao (Google Chrome)
* Kannan Vijayan (Meta)
* Laszlo Gombos (Samsung) 
* Lionel Basdevant (Criteo)
* Mark Blunk (Apple)
* Martin Thomson (Mozilla, TAG)
* Max Gendler (News Corp)
* Maxime Guerreiro (Cloudflare)
* Maxime Vono (Criteo)
* Michael Kleber (Google Chrome)
* Nick Doty (cdt)
* Phillipp Schoppmann (Google)
* Pierre Tholoniat (Columbia University)
* Richa Jain (Meta)
* Risako Hamano(LINE Yahoo)
* Roxana Geambasu (Columbia University)
* Sam Weiss (Meta)
* Sandor Major (Google)
* Sarah Jennings (HM Government)
* Sarah Murphy (Microsoft Edge)
* Shinta Liem (Meta)
* Sid Sahoo (Google Chrome)
* Tammy Greasby (Mozilla/Anonym)
* Tara Whalen (W3C)
* Tatsuya Igarashi (SONY)
* Theresa O’Connor (Apple, TAG)
* Thomas Prieur (Criteo)
* Tris Southey (Google Chrome)
* Wendy Seltzer (Tucows)
* Vikas Sahu (Google Chrome)
* Chris Patton (Cloudflare)
* Miguel Morales (IAB TechLab)



