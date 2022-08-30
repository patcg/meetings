# August 2022 Virtual Meeting

The Private Advertising Technology Community Group's meeting will be meeting two days for 3 hours at the same time both days.

## Schedule

### Day 1 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 07:00         | 10 Wed | Tokyo         |
| 08:00         | 10 Wed | Sydney        |
| 15:00 (03 PM) | 09 Tue | Seattle       |
| 18:00 (06 PM) | 09 Tue | Boston        |
| 23:00 (11 PM) | 09 Tue | London        |
| 24:00 (12 PM) | 09 Tue | Brussels      |

### Day 2 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 07:00         | 12 Fri | Tokyo         |
| 08:00         | 12 Fri | Sydney        |
| 15:00 (03 PM) | 11 Thu | Seattle       |
| 18:00 (06 PM) | 11 Thu | Boston        |
| 23:00 (11 PM) | 11 Thu | London        |
| 24:00 (12 PM) | 11 Thu | Brussels      |

## Joining Information

[Zoom](https://mit.zoom.us/j/95356244879?pwd=NDBwZmxleTMwcHFpZG1MZW1tUXhVUT09)

## Agenda

### Day 1 Agenda

- <= 10m: Intro, Google Doc, Call for Scribes
- == 10m: Brief notes on CG Charter led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)
- <= 10m: TPAC Update led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)
- <= 1h: [Threat Model Update](https://github.com/patcg/meetings/issues/69) led by [@eriktaubeneck](https://github.com/eriktaubeneck) [Slides from session](Aggregate-Measurement-Threat-Model-Draft-PATCG-Issue-69.pdf)
- ~= 1h 30m: [(CPA?) Composable privacy-preserving architecture to support more flexible x-platform use cases](https://github.com/patcg/meetings/issues/65) led by [@rmirisola](https://github.com/rmirisola)

### Day 2 Agenda

- == 5m: Intro, Recap Q&A, Call for Scribes
- => 1h 25m: [IPA Status Update](https://github.com/patcg/meetings/issues/70) led by [@eriktaubeneck](https://github.com/eriktaubeneck) [Slides from session](IPA-August-2022-Update-PATCG-Issue-70.pdf)
- <= 1h 25m: [Further MVP Discussion](https://github.com/patcg/meetings/issues/56) and Setting up MVP Survey led by [@aramzs](https://github.com/aramzs) (and hopefully others)
  - Intro / Overview
  - <= 30m: Absolutely Required
  - <= 25m: Nice to have / Advanced Capabilities
  - <= 30m: Survey Design
- == 5m: Closing

## Minutes

[Minutes document in Google Docs](https://docs.google.com/document/d/1jzUzPFH9BgkGUGTedSF8pk_GuJD_EZeggxn-UMVLZ90/edit#)

## Scribes

**Willing (Tuesday):** Erik Taubeneck (when not presenting), kleber while Erik is presenting

**Willing (Thursday):** Nick Doty, Graham Mudd

## Day 1

### &lt;= 10m: Intro, Google Doc, Call for Scribes

**Sean Turner:** [W3C: Read All About It!](https://docs.google.com/presentation/d/1uahuT9ugb79YDEmpcYz3R4ymjCQg1G3S1JfhVpYVFrM/edit?usp=sharing): Links to W3C FAQ, Process, Code of Conduct, Contributor Licenses Agreement, etc.


### == 10m: Brief notes on CG Charter led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)

**Aram:** Briefly walk through open PRs on the charter - adding the threat model. #19. Any objections? (None raised.)

**Sean:** Normally would just merge it, but want to give a heads up.

**Aram:** This just says that we intend to produce it.

**Sean:** #20. Might be premature, could wait to make sure it’s aligned.

**Aram:** Let’s ask people to review it.

**Aram:** Wendy provided a small editorial review for the PATWG, which we merged (https://github.com/patcg/patwg-charter/pull/40). We didn’t believe it alters intent, but wanted to raise the change to everyone’s attention.

**Aram:** That’s all we have for the charters.


### &lt;= 10m: TPAC Update led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)

**Aram:** **We are running a session. There was a question**: right now some of our sessions overlap with FedID. We know that we have shared participants between PING, PrivacyCG, but wanted to ask about FedID.

**Wendell:** For many of us who aren’t closely involved, but want an update, it would be nice to not overlap. 

**Aram:** We’ll pass that along, and do what we can. See a +1 from the chat.

**Sam W:** FedID will have two sessions; at least one (the first, according to the current plan) will not overlap with PAT CG.  Sessions will not be recorded. 

**Aram:** We have a space, we have a session.. We should have enough space. If you have any questions, we wanted to leave some time now to address those. Also good to start adding agenda items as issues now. Will be great to see people in person who can make it.

(No questions.)


### &lt;= 1h: [Threat Model Update](https://github.com/patcg/meetings/issues/69) led by [@eriktaubeneck](https://github.com/eriktaubeneck)

**Erik:** There is an open PR we're working on.  I've summarized things that are new, need input, or where people are likely to have comments.  Happy to take questions as we go, or at the end.  High-level outline of today: status, formal threat model, All The Parties (First, Embedded, Delegated), Aggregation / Anonymization, Input Needed.

**…:** Draft has been submitted today as a PR to the PATCG docs-and-reports repository.  Not in final state at all, very happy for feedback if anything provokes reactions.

**…:** Threat model is similar to the way it looked at the last meeting.  Outlined actors, and capabilities and mitigations for each of them.  Addresses both aggregator collusion and outside attackers.

**…:** Use cases involve two (or more) distinct first parties (since with only one first party, browser storage and cookies already do the job).  Considering both one first-party embedded in another first-party, and probably more common, one delegated party embedded in both first parties.  Aiming for APIs that support this embedding capability, and want to avoid incentives for first parties to give elevated privileges to embedded parties.  This comes with complications: Multiple embedded delegated parties, who might therefore be in a position to disable or corrupt one another's data; depleting some global budget at the expense of a competitor; sneaky use of multiple delegated parties to get more Differential Privacy budget.

**…:** Scope is data collected from individual clients or users and then gets aggregated.  Want to avoid revealing information about individuals.  Want to aggregate as much as possible, and ensuring that the information you can infer about a person is limited even across queries — that is what is limited by imposing a Differential Privacy requirement on the output.

**…:** Requirements for DP are bounding the contribution of any one contributor, and noising output in a way somehow proportional to that bound.  Noise parameterized by epsilon.  Users will want to run various queries multiple times, and you need to add up the epsilon-noise from those queries.  Need some total epsilon budget per unit time, e.g. per week.  Allowing less epsilon per epoch, or letting epochs be longer, are ways to control information leakage over time — but note that over infinite time this still leaks all data

**…:** There is a question of what scope this budget is over.  Could manage budget per first-party, or per first-party first-party pair.

**…:** Need input on what is the epoch, what is the epsilon, what is the unit of privacy (e.g. per 1p or 1p*1p pair).

**Martin Thomson:** There is also some notion of epsilon-delta DP, where delta when nonzero represents the size of a slice of data that is exempt from the epsilon budget, small amount of data that may escape aggregation protection.  May need total query budget also.

**Erik:** Please open PRs against document once it's merged.  Great to talk now about things people have thoughts on.

**Nick Doty:** Will file issues / written feedback later, but happy to chat now.  A few things that I'm not sure are in this threat model already:

**…:** 1. Some kind of *group* privacy model.  You won't get information beyond epsilon about whether this individual visited this website or whatever.  But if a classroom teacher finds out "at least three of my students have visited this website about abortion", then the fact that the teacher can't tell which ones they are might be cold comfort.  Does DP cover this, or is there some notion of group privacy that we can augment it with?

**Mariana Raykova:** DP baseline is focusing on individuals.  There are extensions that focus on groups, but often trades off heavily with information available.  Figuring out to what extent it's possible to address this depends on the adversarial model?  DP is focused on "adversary who already knows what everyone did except for me".  Is that the right model from group privacy?  Probably not.  Minimum aggregation thresholds help, but not enough to address this.

**Erik:** DP is a measure of information released from a system.  You could have a DP system with very high epsilon, and it would just not be very private.  We need to use it as a measurement tool and be comfortable with how much is released.

**…:** Part of the goal here, and in the charter, is exactly to release group information instead of individual information.  DP makes promises about what kind of inference you can make, including about large aggregates, not just about individuals.

**Brain May:** A lot of the language you're using is relatively opaque to me.  I know what I'd want to do do report on an ad campaign, but I don't know how to translate that to your talk about threat models.  Can you offer any way to translate what you're working on into the intended uses for advertising?

**Erik:** Not in this document — that would belong inside individual proposals, while this doc is about describing the threat models that cut across all examples.  This is certainly something that we should be doing with each proposal as it comes about, while this doc is deliberately very abstract and should apply to future proposals.

**Brian:** Also, if you bound the input domain of an aggregation, the result can be very revealing, so it lets you find out something substantial about a class of people.

**Erik:** This is what Nick was getting at also.  We want to make these APIs purpose-constrained and want to narrowly define what that purpose is.

**Brian:** Seems like you cannot allow arbitrary queries?  Can only allow queries that are known to be privacy-preserving.  I can't imagine how arbitrary data and arbitrary aggregates could not be privacy-invasive.

**Erik:** That is indeed what the goal is.  The threat model is slightly different: Given that there is a proposal that claims to have some limits on its use, to what extent could the parties using it violate those expectations and get more out of it than the system intends?

**Martin:** I think Nick's concerns are highly relevant.  We have a system where we pretty much understand the ways the system can protect the information about an individual.  Over infinite time, we give out infinite information.  We'll need to ensure that epsilon is not proportional to sensitivity not just in a single epoch but over many.  Right now, privacy of one person over 10 weeks is the same as the privacy of 10 people over 1 week — this gives us some intuition of how things scale over time and population size.  I don't know how we're going to get comfortable with that.

**Mariana:** Defining over what attributes you can aggregate to begin with gives us protections beyond DP.

**Martin:** Unfortunately we don't get to choose — the proposals all assume that the 1p has some sort of information about visitors (directly, inferred, purchased, etc), and they will be able to choose whether individual users are participating.  If a malicious website wants to target a particular person, they can do so.  The information they don't have is what that user did on other websites, but they might know lots of other things, including global things like demographics.  I've been operating under the assumption that all the information is maliciously constructed, which is the DP standard.  Would like to hear from others.

**Mariana:** There is no golden value for DP epsilon.  It's good to quantify in other ways what we are releasing — including bits of entropy, not to replace DP but as a sanity check on the number of bits you're releasing.  Coming up with the exact epsilon that will satisfy us, we'll need help.

**Martin:** Probably a case where we might be better informed by thinking of a target epsilon, and a target period over which it's released.  For an individual user, when their epsilon reaches x, their privacy is destroyed, and we think about time.

**Mariana:** What does epsilon 3 vs 4 vs 5 mean

**Martin:** I'm thinking about 0.1.

**Benjamin Case:** Could have transparency reporting about the types of aggregate queries that are getting run.  If you have a query over 100M users and only have 20 breakdown keys, there are only so many things you could do.

**Erik:** Nick, please do open an issue after the mtg, should have more discussion.

**Raimundo Mirisola:** What sort of decisions are we making around privacy units?  Different units for different use cases?  Information in the privacy unit may have implications for who can enforce.  May think some use cases are more sensitive than others.  Sensitivity over larger time period is higher than over a particular day.  Health care data may be more sensitive than seeing random advertisements on the internet.  How do we build that flexibility into the system? \
**Erik:** This doc for now is addressing the measurement use case — would expect some things to change if we were considering other use cases.  Some stuff is transferable, but surely would need some changes.

**…:** Good call-out on the privacy unit in particular.   This may be more about a way to compare different proposals, rather than a privacy setting within one proposal.  

**Aram:** Did that answer your questions?

**Raimundo:** Defining the epsilon is not enough, defining the dimensions of privacy is important also.  That choice will affect where the privacy unit can be enforced, who can do that enforcement.  I think we need to consider that about any proposal.

**Erik:** Agreed.  We're going to have to get into that with the various proposals.  Not necessarily something we'll decide beforehand; different proposals may address it differently (e.g. IPA in the aggregation system, other proposals client-side.)

**Nick:** Larger area that maybe hasn't been part of the threat model: How will the user understand the system they are participating in?  Threat: if the user doesn't understand the system and what its privacy features are, then maybe users will turn it off / decline to participate, or contrary-wise maybe the system will do something that makes them unhappy and then they will lose trust in other such systems in the future.  Have we thought about this?  Is it an appropriate thing to add to the threat model?

**Erik:** We have thought about this in individual proposals.  Hasn't come up in this threat model exercise yet, seems non-traditional, but I'm not opposed.  Delicate balance here: Aggregation is something most people understand, but it's very attackable; DP can be much more private but loses a lot of explainability for normal people.  By the same token, most people don't understand TLS, but users have some idea that my browser is more secure because of https instead of http.

**Sean:** We can wait for the marketing department to come up with cute, approachable videos.  We can't always get there, but there is something to be done.  User can't understand everything and definitely can make mis-decisions.  But we can evaluate the proposals, and then other people can evaluate them and see if there's stuff that we missed, and if so they will write papers about it and get Ph.D's.

**…:** From experience and based on the authors, the threat model contains what’s needed.

**…:** One question — For some of the def's, like "first-party", we'll point back to privacy principles, right?

**A:** Yes.

**Martin:** I don't think Nick's point about explainability is a fit for the threat model, which is focused on other actors in the system and what they can find out.  Maybe capture this in our principles document instead?  I don't want to lose sign of it, even if it doesn't go here.

**Brian:** Adding the user to the threat model seems really worrying because there are so many users and so mucht they might do.  But can't evaluate this in the same way.

**Erik:** To be clear, the _user_ is in the threat model, but the user _understanding the system_ is not.

**Aram:** User seeking greater privacy is not a threat.  Maybe address it in principles, maybe elsewhere, we should indeed consider it.  Hard to figure out, especially at the early steps of these proposals, but having additional explanations is going to be very useful.  Even when there are additional explanations, people misunderstand things, especially how they improve privacy.  I don't want to lose this; let's figure out how to apply it as part of our proposal process.

**Mariana:** Whatever we will be doing to make users more confident in these designs will be at least one level removed from the designs themselves.  People can understand the benefit of encryption in some way even without understanding the underlying cryptography.  What we want them to understand is not about the technical details of the proposals — we could have lots of different implementations that enable the same abstract functionality, and the functionality is what we want to explain, independent of the nitty-gritty design choices.

**Brian:** Users use a lot of things they don't understand, starting with "a computer" and "a browser".  We should identify someone who takes into account the user's well-being.

**Aram:** Wrap-up comments?

**Erik:** If no objections, I'd like to merge the current PR and then take up various PRs against it — easier to track discussions that way than in PR comments threads.

**Sean:** It's a Work In Progress, there's no harm in merging it and addressing anything later.

**Aram:** I'll add a note about WIP-ness, and hearing no objections, I'll merge it during the break.

~~ 12-minute break, until **:25 ~~


### ~= 1h 30m: [(CPA?) Composable privacy-preserving architecture to support more flexible x-platform use cases](https://github.com/patcg/meetings/issues/65) led by [@rmirisola](https://github.com/rmirisola)



* **Raimundo**: 
    * Follow up from the conversation from the WFA cross media measurement system, and adding composable privacy preserving architecture. We thought this framework could be a bit more general and useful in this group.
    * **Key takeaways**:
        * WFA system is hoping to meet strong privacy guarantees to deliver valuable ads use case
        * Composible privacy preserving architecture
    * Requirements that needed to be meet from the market. It was clear that while we wanted to support more advanced measurement, the key use case was “reach and frequency” measurement.
    * Main problem to work with was cross media measurement, counting unique people across multiple platforms. It’s not enough to solve for web, also need to include TV, mobile apps, etc. 
    * Very difficult to build a unified ID space. People share devices.
    * Solution was to use a model. Use a trusted calibration panel, then use that to translate how many people saw the ad.
    * Use that model with data collected on different device types.
    * **Example**:
        * Panel label tells us what attribute we believe a person has, and that is used with the data collected on the web site. This assigns a “virtual person ID”.
        * Once we collect enough VIDs, we can construct the reach curve based on the model.
        * When you add it all together, your VID reach is very close to true reach.
    * In this problem we don’t care who watched the add, just how many people in a specific demo saw the ad.
    * There is published research ( [https://research.google/pubs/pub45353/](https://research.google/pubs/pub45353/) ) around the accuracy of this approach.
* Martin Thomson
    * I don’t understand this curve. What does it do? I understand what you’re doing in the abstract, but not sure what the graph is.
* Raimundo
    * We’re trying to map how many cookies we see to the number of people that actually saw the ad. We have a source of truth (panel), that we can use to fit this curve. As more cookies accumulate for a particular segment, how many people that corresponds to.
* Martin
    * How does this work in a context where tracking is no longer possible.
* Raimundo
    * When we lose 3PC, we’re going to lose cross publisher behavior across websites. We’ll only be able to build this curve for individual publishers. As the number of publishers grows, the dimensionality gets too high to train these models.
    * One of the reasons that we are here is to figure out if we can mitigate the some of these losses.
* Aram
    * So the curve represents the effectiveness of identifying a person. 
* Raimundo
    * Advertisers want to know how many people they show ads to. On the Y axis, you have how many people saw the ad, and the X axis shows how many cookies were observed.
* Aram
    * Ok, so this is about trying to build a model that is effective in understanding that a user is likely to be a user we’ve already seen before? [for use in unique views or frequency capping]
* Martin
    * You’re building a model that will give you some ability to take information you have about disparate information to predict how many people are reached. What sort of information is that trained on? People who form your panel give you information because they are being paid, but how else is that gathered.
* Raimundo
    * Panels recruited by 3rd parties, and have different instrumentation installed to get more accurate information, including TV.
* Bosko
    * The panel we’re referring to is used for the ground truth to build this curves?
* Raimundo
    * Correct.
    * We can think of this curve as a virtual person space. We can think about one per person, and then we create a random process to assign these IDs so that it maps in the way that the model is trained.
    * If you count the number of virtual IDs, then the count of VIDs is a good approximation of the unique number of real people.
    * The challenge is that VIDs are derived from cookies. From a privacy perspective, they are as bad as cookies. They are somewhat consistent overtime.
    * We cannot send them in the clear, we need to aggregate them in a privacy preserving way.
    * So far we’ve designed an MPC protocol where publishers participate in the system, get the trained model, (which is trained by a panel company), publishers use that model to assign VIDs, and when we want to count reach and frequency, each publishers sends these to the MPC that will guarantee that the outputs are differentially private.
    * I’ll also tell a bit about how we are using sketches.
* Aram
    * Before you get into the MPC, there is a question about how the VIDs work. How are they stored and assigned?
* Raimundo
    * The cookies are hashed into the VID space, and it may turn out that these get assigned the same IDs.
    * If the model says that users have a lot of cookies, then you will find multiple cookies that map to the same VID.
* Aram
    * Are these stored as a cookie, or are they generated on the fly?
* Raimundo
    * Each publisher gets their server side logs and applies the VID model.
* Aram
    * VIDs are not intended to be privacy preserving but the MPC processing is?
* Raimundo
    * Yes
* Graham
    * You mentioned that the VID is applied randomly, which should provide some privacy? But if two publishers apply the same values and get the same output it wouldn’t be. How is it random?
* Raimundo
    * There is a random seed, but the process is deterministic. Given the same data, they are likely to get the same VID, with different data, the probability of getting the same VID depends on how the model is trained.
    * 
    * Main challenge we have is that there is a large volume of impressions (100Bs a day.)
    * Solution is to compress the data. The way we compress the data is by using a sketch (e.g. a bloom filter.)
    * The sketch has a fixed size, so that the size doesn’t leak information. This is a lossy process. This works for reach and frequency.
    * Threat model is that we should only need to trust one of the nodes.
    * Everytime you run the protocol, you have an epsilon differential privacy loss.
    * So far, about 2 years of collaboration. End of the year, proof of concepts with real data.
    * 
    * **Reason why we are here**: we’re going to lose information which we can use in the VID model. 3PC is going to be limited, and that will prevent our ability to see cross media information, especially as the number of publishers increase.
    * We’ve started thinking about how we could leverage new systems that are coming up, and still preserve privacy.
* Bosko
    * Could you clarify a little more in the setup. There’s this part where you do VID assignment. It seems that the entity that does this needs a lot of data. Can you explain who are the parties involved, who’s doing the VID assignment, who’s exchanging information, etc?
* Raimundo
    * The party that does the assignment is the not he party that trains the model. The party that does the VID model application needs to have some data, for example could be data collected on the publisher server. The panel needs information to train the model, so they collect some publisher data as well. Once they train the model, it can be used by the publisher to assign VIDs. Today, that can be done with 3PC, but in the future it could be 1PC.
* Bosko
    * You sketch this MPC with inputs and outputs, but the VID assignment is done by some sort of God like entity that can see all the data? Does it only need the panel data?
* Raimundo
    * Yes, it’s only the panel data.
* Graham
    * If it’s only the panel data, how is it likely that the model will provide the same outputs? Is it only the panel members privacy that could be compromised?
* Raimundo
    * The panel allows us to train the “curve”. When we train that curve in the panel, and then we want to apply it on the entire population.
* Graham
    * That much I understand. Supposed provider A and B have the same email address, there’s a reasonably high chance that given the same input, it will have the same output.
* Raimundo
    * Yes, if the model was trained consistently, then yes it should have the same VID. As the input space grows, you’ll start to have collusions.
* Graham
    * So the VID is essentially just a hash of the email, but the VID also gives the probability of collision and some demo data.
* Aram
    * Presumably we are moving towards a future where 3PC aren’t available. In that case, what is fed into that model?
* Raimundo
    * The model already deals with disparate ID spaces, but as you have more of those spaces, you need a larger sample size to understand how this works.
* Aram
    * If I can generate a unique ID, why can’t I feed that in? What is needed from the VID model?
* Raimundo
    * Why not just count cookies? You can think of this as a “corrected” cookie. There could be multiple people behind the screen. The demographics could be incorrect. The VID corrects for this.
* Aram
    * So you’re trying to resolve an ID that would be more accurate, based on some inputs.
* Raimundo
    * That’s correct, and we want to do this consistently across publishers.
* Aram
    * From a publisher POV, this seems somewhat uncomfortable about having a 3rd party assign an identifier that is distinct from the identifier that we as a publisher have.
* Martin
    * There’s probably two ways this could go, and curious what the research into this goes. One is that the ML is good enough to predict people based on information collected. The other potential outcome is that there is a cohort on one side and the other side to which the model essentially assigned randomly. You gain the ability to learn about people holistically, but not about using it as a tracking identifier.
    * Which situation this would be in is not something I can reasonably assess from this presentation.
* Raimundo
    * The way the model is segmented is by age and gender attributions. If two publishers don’t agree on attributes, it’s only by chance they’d be assigned the same value.
    * VIDs aren’t meant for targeting, only for measurement.
* Martin
    * Given that it’s only used on 3PC now, do we know which case were in? Can it be used for tracking?
* Raimundo
    * Primarily using 1PC cookies now, but without 3PC it will be difficult to add new publishers and to train models. Are there ways to use what we are building here to retain some of the quality, and add a larger number of publishers, but maintain a level of privacy.
* Martin
    * I don’t see how you’d move this into the browser.
* Raimundo
    * Good segway into the next topic.
* Aram
    * Quick question. Will entities with more data about individual users be more capable of generating useful models? [since in the post-3p world models will need to be recalculated using new types of input data] 
* Raimundo
    * More data used results in higher quality models.
* Mariana
    * Want to discuss some of our thoughts about how the WFA system is designed, and some of the APIs discussed in this venue, and if this can be used to support the R&F use case. Moving VIDs on device would mean they’d only live on the device, and then it’s a question of how do you use it in a privacy preserving protocol, where before you were assuming the providers have all the data and can generate sketches, to now where each user could be viewed as an independent data providers (and requires the system to deal with **many** more data providers.
    * Now the first step, instead of having an impression log, you’ve have to do this on device. 
    * Let’s think about the proposals for aggregation that we’ve seenL Chrome attribution API and IPA. Both of these have the underlying functionality of computing differentially private histograms from browsers used by users.
    * The type of differentially privacy noise were adding is for each bucket, because we want to reveal this count or aggregate bucket.
    * Looking again at CMM R&F, a little abstract, we have 3 phases:
        * Generation of aggregate sketches for each data provider
        * In the MPC phase, we can split it in to 2 phases
            * First is aggregating the sketches which is pretty much just additions
            * Once we have 1 aggregate sketch, then we have pro-processing: collision detection, extract reach/frequency counts.
            * Reach is the number of registers with a value, and frequency is the count with a specific value. This post processing is done on one aggregate sctech, independent of the number of data providers.
    * Without 3PC (and other identifiers) the only place we could apply the VID model is on the device. We have two options for applying privacy preserving APIs:
        * **Option 1**: require functionality to be directly supported in the browser APIs
        * **Option 2**: understand how to integrate between browser APIs and CMM API
    * The way we broke down the cross media protocol, the first phase looks quite similar to other proposals. Can we aggregate on the device, and then obtain the sketch from each data provider, and then use that with the CMM protocol?
        * Answer is both yes and no. The aggregate API let’s you compute these aggregate sketches, but no because if we look a bit deeper into the differential privacy coming out of the browser APIs and treat them as inputs, we’ll have an explosion of noise.
    * The first step of the CMM protocol is to aggregate sketches. And if we’re aggregating across all browsers, the noise increases significantly, much more than needed to hide individual users.
    * The other issue is that the browser APIs give a differentially private histogram. But the CMM protocol is looking at the frequency histogram, i.e. how many values with value 1, value 2, etc. We then just make the frequency histogram differentially private.
    * **There are two routes**:
        * Make the histogram into a frequency histogram, and make the frequency histogram DP. This will have better composiblity.
        * Other route is to make the histogram a DP histogram, and then convert that to a DP frequency histogram. This causes the noise to compound.
    * One way to resolve this issue is to compose the two APIs without revealing any intermediate input. We could aggregate across users, but encrypt that, and then send this to the MPC directly.
    * We will have this computation on-device that applies the VID model, which then converts this into a sketch. These are shared to the Aggregate API, which distributes this to the workers.
    * One conceptual way to think about this split is that the Aggregate API will be doing the work to deal with aggregating users, then the Cross Media protocol would then do the post processing and add the differential privacy.
    * This requires a trust transition to the other workers in the CMM system.
    * You can use the output of different Aggregation APIs to provide input into the CMM protocol.
* Nick
    * Is this two MPCs?
* Mariana
    * I’m thinking of the Aggregate API as a black box. Maybe it’s MPC, maybe it’s not. The proposal is just to have the aggregation, and then outsource the DP to the CMM system.
* Nick
    * You’re suggesting that the output will be aggregated without DP, and will go to some actor who just has an aggregate, but that’s ok because it promise to only put it in to the CMM system.
* Mariana
    * No, there will be no party, it will go directly to the CMM workers.
* Nick	
    * But someone needs to split up the shares.
* Mariana
    * Could do it in a smarter way, and create shares.
* Nick
    * Would be helpful to have that in the diagram.
* Raimundo
    * Composable Privacy Preserving Architecture (CoPPA)
    * There’s a problem around trust and privacy that we’ve discussed. Different data controllers may have different opinions around who is trustworthy operators of these systems. We want to support multiple user cases, and the computational graphs could look different. 
    * A CoPPA node, which takes an input and can only output into other nodes, or a differentially private information.
    * **Examples of a node**:
        * User device
        * MPC service
        * Single user
    * Trust and Privacy Principles
        * Node controllers are responsible for deciding their privacy
    * Example
        * This is how we could think about taking browser device data into the system. Could have Browser A that applies a VID model, which goes into an MPC network. Could also have Browser C that applies a VID model, which trusts Secure Enclave D. 
* Erik
    * Browsers/apps (other user agents) need to trust everything to the right. These seems way further ahead of where we are at. 
* Raimundo
    * Some of these systems are ready and might help us scale.
* Micheal
    * Going to agree with Raimundo. Most of what’s being asked for is not a technology change, but using this new technology to make a policy change. As we’ve been thinking about this space, we’ve been talking about a number of techniques to do privacy preserving processing. With those, we’re willing to take data (secret shares, etc) so that the later output is sufficiently private. It seems like the big ask here is about composability about packaging up data and send it for aggregation, which it not necessarily about providing DP, but maybe be itself about packing up data.
* Erik
    * The work item we’ve set out to build is a single purpose, so my feedback is that we should focus on that before concerning about supporting a great deal of purposes.
* Martin
    * Less concerned about the composiblity explosion and more about the practicality. There’s two things being asked: we put some information into a system which then puts it into another system that does some work. We can reasonable the entire chain of custody.
    * I would be interested to know who is operating the MPC systems as a browser, and we may want to talk to them about operating the MPC.
* Raimundo
    * We’re in the process of spinning that up. They may not be the long term operators. We’re in a dishonest majority, so you only have to trust one.
* Martin
    * The other concern is the VID, and understanding how that would work. This is similar to IPA, where you have an externally injected ID. Here you’d have an externally injected model, and then all the inputs to the model. This is where I start to have concerns, where the information used with the model could come from multiple websites. 
* Raimundo
    * It could be useful to use something like IPA, and use some sort of post processing to use the VID model.
* Martin
    * In this cases, it’s likely the inputs I’d be concerned with.
* Craig
    * I’m worried about revealing pieces of IDs.
* Nick
    * This seems like a good test of our threat model. And then also our user comprehensiveness, and who the user has to trust. If we want to talk about composability, we should apply the threat model to this; does the user have to select and trust each step in a composable pipeline? Or trust any downstream composition of aggregations? 
* Erik
    * Could also flip this, removing the VID model and instead using IPA matchkeys with offline events.


## Day 2


### == 5m: Intro, Recap Q&A, Call for Scribes



* IRC Minutes from last meeting - [https://www.w3.org/2022/08/09-patcg-irc](https://www.w3.org/2022/08/09-patcg-irc) & [https://www.w3.org/2022/08/10-patcg-irc](https://www.w3.org/2022/08/10-patcg-irc) 
* 

Reminders about policies. Nick and Graham to scribe. IRC Chat. Please sign in on the Participants list.

Tuesday’s meeting on Composable Privacy Architecture, Threat Model, TPAC (open thread on github issue).


### => 1h 25m: [IPA Status Update](https://github.com/patcg/meetings/issues/70) led by [@eriktaubeneck](https://github.com/eriktaubeneck)

**Ben Savage (Meta):** 



* updates to Interoperable Private Attribution proposal. [https://github.com/patcg-individual-drafts/ipa](https://github.com/patcg-individual-drafts/ipa) 
* Fleshed out in more detail. 
* Simpler client APIs which only needs to share the match keys.
* Formalization of helper party networks
* Meeting all security goals, previous version was leaky, where helper nodes would learn the number of events generated per person.
* Helper server could learn with high confidence that most of the events were connected to a single person, and so learn something about their activity or their matchkey.
* Goal is to preserve privacy even from malicious helper servers. Tried a few possibilities, including generation of fake events or capping number of events.
* In new proposal, helper nodes learn nothing about the number of events. Malicious helper nodes should not learn anything, even in collusion with the source site or match key provider.
* With 3 MPC helper nodes, rather than 2, can be efficient even if one of them is malicious. Lots of academic research on highly efficient techniques for this configuration. Honest helpers can abort the computation if something goes wrong.
* **Additive secret sharing**: start with a secret number, pick two random numbers, and shares are the two random numbers and mod(secret-share1-share2,p). Even with two of the three shares, you learn nothing about the secret.
* **Replicated secret sharing**: by providing two shares each to three different helpers, none can learn the secret, but multiplication is now efficient.
* Can add secret sharings together (each helper adding together their local shares), where in aggregate the answer is the sum of the two secret numbers. Can follow a protocol to get an aggregate multiplication of the secrets. Use shared random number generators.
* With addition and multiplication, can accomplish many complicated arithmetic circuits.
* Bottleneck is communication between the MPC nodes (needed for multiplication), not the CPU computation. For semi-honest, 1 number exchanged per multiplication, for malicious, 2 numbers exchanged.
    * Helpers receive a large list of secret shared events (no distinction between source and trigger).
    * Sort events by the match key (while the events remain secret).
    * You submit a time sorted list to the MPC as an optimization. 
    * Run an oblivious attribution algorithm over events.
    * Cap the max contribution of any individual person.
    * Sum up the trigger values per breakdown key.
    * Helpers add some amount of random noise.
    * Helpers reveal their totals to the API caller, and the caller combines them to get the value.
* Sort is the most expensive part. Expect new research to make it more efficient over time.
* Oblivious attribution algorithm can be almost any type of attribution heuristic.
    * Equal credit up to the last 3 touches, for example.
    * Attribution is cheaper if only involving addition and multiplication.
    * Shared algorithm of last-touch attribution.
* Capping per user contribution
    * Makes the result less accurate, but necessary to provide differential privacy, for cases where a single person spent a very large amount of money, for example.
    * API caller can decide what the cap is, trading off between bias and random noise, depending on the use case (e.g. app installs vs ecommerce purchases).
    * **How to do capping**: stop taking events once reached or scale total numbers.
* Simple privacy budget in current proposal, query-level
    * The API caller decides how much privacy budget to use in any query, and when you run out of budget, you can’t make any more queries that week.
    * Could be more complex, welcome input from the group.
* Implemented a simple research prototype
    * MP-SPDZ compile code into an MPC program, but will keep optimizing
    * **Open source code Prototype at**: [https://github.com/martinthomson/raw-ipa/tree/main/research-prototype](https://github.com/martinthomson/raw-ipa/tree/main/research-prototype) that you can compile and test yourself
    * Likely efficient enough for many advertisers
        * For 1 million source and trigger events, 
            * at CPM of $14.40, would cost $7,200
            * At CPC of $0.35, would cost $175,000
            * Cost of attribution MPC would be less than $50 on AWS, 100 minutes, 390GB of communication traffic.
            * Egress cost is the most significant.
        * Current literature suggests that it could be significantly cheaper, maybe ~$20
* **Benchmarks**: 
    * time and network usage go up linearly with the query size
    * Multiplicative depth of the circuit goes up logarithmically
    * Cost is driven by sort, complexity of the attribution piece is not very significant
    * Queries with more breakdowns are a little more expensive, but not much

**Alex Whitworth:** who would the parties be?

**Ben:** IETF standardization of a measurement protocol ppm. Some services running at scale, DivviUp, Prio, etc. Might be similar vendors.

**Martin:** ISRG is operating a very similar service. Some others, but would let them announce if they want to.

**Kleber:** model is three, independent non-colluding helpers. Benchmark is assuming they are at three different public cloud providers, and egress is the cost of sending data between those different providers.

**Erik:** we ran our test internal to AWS, but calculated cost as if egress of the full data.

**Kleber:** not just the egress cost, but privacy/security problems of running multiple helpers in a single cloud provider. Shouldn’t have any two in the same cloud.

**Erik:** yes, that’s the assumption we’re making.

**Benjamin:** latency would also be higher with different cloud providers.

**Chris Wood:** 

* Cloudflare likely interested in doing experiments of interop with this, similar to the MPC tests for dap/ppm.
* Capping per user contribution may be the most difficult part, especially across client devices or over long periods of time. Likely need to be very conservative to protect end user privacy, but that could impact utility.

**Erik:** trade-off can be provided back to the API caller and their particular use case. Caller can decide whether bias or accuracy is more important.

**Chris:** DP lets us reason about that trade-off, but correct enforcement of the cap could be difficult. Reasoning about caps _across_ (independent?) queries is tricky.

**Brian May:** could you test this in a domain where privacy is less of a concern? Would that save a lot of the cost?

**Ben:** Charlie Harrison proposed an optimization related to sort: you can pay the sort just once, after you’ve paid the cost to sort by match keys. Amortize the cost across multiple queries. Could run five different queries on the same set of events with different breakdowns, and the cost would be similar.

**Erik:** reach and frequency could be a calculation of count-distinct, which could happen all with the same expensive sort on matchkey.

**Ben:** running several queries on the same events also makes it more efficient on use of differential privacy budget.

**Martin:** distinguish between money budget and privacy budget (which is spent when you do multiple queries no matter what).

**Justin Li:** timing of benchmarks, does that include the time to generate the source and trigger events?

**Ben: no, just the time of the MPC network. Erik:** may go up with latency of using different cloud providers.

**Martin:** matchkeys are encrypted to each of the helpers. This information will come from multiple websites, so it will take time for the API caller to gather, sort and annotate.

**John Delaney:** appreciate the simple slides. For oblivious attribution algorithm, want to attribute conversions only to ads that displayed the particular product – is that possible/easy?

**Ben:** “attribution grouping id” – you just make up a number and sort by matchkey and then the grouping id.

**Erik:** performance-wise, it extends the matchkey.

**Benjamin Case:** you can do a pre-sort by timestamp and grouping id.

**John:** if you want to match on either of two groupings. Ben: an arbitrary number, so you can use for many complex uses. Prepared by the API caller.

**Mariana:** do different queries need different matchkeys or different ids? Do you have to determine beforehand what kind of query you will later do?

**Ben:** if you just have constraints on what could be an attribution.

**Mariana:** how do I specify different queries or breakdowns?

**Ben:** each source event contains a breakdown key, which is secret shared/encrypted into the MPC.

Please file issues and we can have threaded discussions on different topics.

**Alex Cone: set-up:** source and trigger events would need to be in the same helper party network during the seven-day epoch. Scenarios include one advertiser and one source (like Meta/Facebook), or one advertiser but many sources. Advertiser maybe uses multiple ad providers, attribution providers, and running ads on thousands of websites. Do all of those entities have to be part of the same network? Sounds tenuous.

**Ben:** proposal requires committing to a configuration for a particular week/epoch. Lots of entities involved in advertising, and all of them want some kind of reporting. Publisher wants to know how many ads they showed, and DSP wants reporting of ads across websites, and advertiser wants reports about wherever the ad is shown. Each of the parties should be able to get a batch of events, and they can decide what helper party network and match key provider. For one website that serves ads for multiple advertisers and each advertiser is running ads on multiple websites. For either source or trigger event, can call get_encrypted_matchkey multiple times: can generate source events for different helper party networks. Can forward to the advertiser whatever encrypted events. On trigger website, can call get_encrypted_matchkey many times, for my own website and for possible advertiser/source, forward the reports on to Meta.

**Alex:** advertisers have to run code to call the get_encrypted_matchkey, or coordinate with the publisher to make sure they run this code configured for your helper party network. As long as you can execute code on their site … can’t be blocked by a publisher’s policy.

**Erik:** should be able to run embedded, not in the top-level context.

**Ben:** publisher can decide just by not letting them run their code

**Alex:** code can execute just when a creative is delivered.

**Aram:** Agreed that this would be a nice option

**Charlie:** how does attribution work in a malicious secure system? Oblivious sort across all reports and all users. How does this change for last-touch-attribution vs other kinds of attribution? What is the performance cost? Logarithmic across all the reports? 

**Ben:** if events are submitted in a sorted order, and if you’re willing to make some guess about the maximum number of events for a particular user, just do oblivious match of a row with each of the following hundred rows, for example. For last-touch attribution, optimization by having every row compare against the row below it. O(N log N). For more complicated multi-touch, might be linear.

**Charlie:** would want to avoid quadratic factor of comparisons in complex attribution.

**Ben:** imagine a spreadsheet, doing sort on multiple columns, so each event is close to what it is nearest.

**Daniel Masny:** multi-touch is more complicated, but think of it as a last touch to the best matching source event, and then redistribute that value across N source events. Could involve another sort operation, or a linear scan. Exponential decay would be more costly than just evenly distributed across multi-touch.

**Charlie:** time decay was my ultimate question. Harder to do with simple sorting.

**Ben:** if the timestamp data is available in the events, you can do some calculation based on time-decay.

**Charlie:** could augment the data with timediffs beforehand.

**Ben:** raw timestamps in the encrypted event, and then do an MPC calculation.

**Mariana:** have you looked at dishonest majority?

**Ben:** we haven’t run it under that assumption, but we could and update.

**Daniel:** efficiency of running under dishonest majority. Would be pretty expensive.

**Kleber: re:** permission to run these APIs. Chrome is giving new APIs/capabilities in Google Privacy Sandbox, all of which come with permission policy. Web browser mechanism so that the top-level page can define what actions embedded parties can run. Moving away from the old model where any embedded third-party script can do anything. Browser can have a technical mechanism where the APIs are limited to particular iframes, in a transitive way if necessary. We would extend that to get_encrypted_matchkey. Permissions policy would be transparent to the embedded third party. So an advertiser could assert we only show our ads if we have this attribution capability.

**Ben:** should probably follow that.

**Nick:** vendor will choose the helper party network, but the vendor might have an incentive to choose a network that intentionally colludes and decrypts the very sensitive matchkey.

**Martin:** intersection of the party network that the browser vendor/user trusts and the party network that the site wants to choose. Centralization risk as well.

**Nick:** that increases the number of parties the user has to trust, maybe by a lot?

**Erik:** not users deciding case by case, but can trust or disable altogether. Browser vendor making a trust decision that’s hopefully in your interest.

**Ben:** but want multiple networks, because otherwise lack competition and increased costs of doing the operation itself.

**Aram:** performance risks to publishers by letting ads create iframes or run code on the page. Would prefer a configuration object that was just configuration, not providing open-ended running of script or iframe. Could decrease the performance concerns, and network connections. Advertisers can push stuff onto publishers. 

**Aram:** would prefer not to have advertisers only realize after they’ve won a bid that they can’t use the service that they want. Could be expensive for the publisher.

**Alex:** for privacy budget with a finite resource, market dynamics may push towards fewer calls.

**Erik / Ben:** these questions apply generally, not just IPA.

**Ben:** +1 for configuration without requiring random scripts. Could also collect reports on your own server and then forward later.

[https://github.com/patcg-individual-drafts/ipa](https://github.com/patcg-individual-drafts/ipa)


### &lt;= 1h 25m: [Further MVP Discussion](https://github.com/patcg/meetings/issues/56) and Setting up MVP Survey led by [@aramzs](https://github.com/aramzs) (and hopefully others)



* Intro / Overview
    * We will think through how to gather requirements.  Goal isn’t to gather all requirements during this call.
* **&lt;= 30m**: Survey Design
    * Maybe push towards simple explanations of things?
    * Charlie put together a list of requirements that might serve as a starting point.
        * Aram agrees this could be a good starting point. Will need to bring less technical people in the discussion to gather requirements.  We need to use less technical terminology to do this.  Focus should be getting what the participants, then sort them into the categories we’ve put together.  
    * **Erik**:  Yes, we should start with higher level questions.  Challenge is that not everyone agrees on the basic definitions of things like MTA or R&F.  
    * **Aram**:  Yes, we should push for the simplest possible descriptions instead of relying on terminology that isn’t well defined.  Wished we had more ad tech participants here to provide feedback.
    * **Brian**: Couldn’t we ask companies that publish reports.  Go to major ad platforms (Google, TTD, etc) and ask which reports are most important to their end customers.
    * **Alex**:  +1  People will probably say they want everything.  Asking for stats on the reports that are most popular.
    * **Aram**:  We should ask narrow questions if we want specific answers. There will be reports that just won’t be relevant any 
        * What needs to be available to support the majority of your clients?
    * **Graham**: dimensional questions, stack rankings? What type of attribution models are most popular last click vs mta? Otherwise may diverge to everyone wanting everything.
    * **Aram**:  Yes, but want to be careful not to exclude anyone. 
    * **Ben**:  Agree with Alex that people will ask for everything.  Also need to careful that just because people ask for it or receive it doesn’t mean they use it.  Could frame it questions in the negative:  What would happen if X report was no longer available.  For example:  What if in the future we couldn’t do cross device conversion counting – what would that do to your business?  What if MTA wasn’t available?
    * **Nick**:  Also curious what the MVP should be for users?  What types of things are acceptable to end users from a privacy perspective?
        * **Aram**:  Agree that it would be interesting but very different audience.  Maybe we should reach out to consumer reports. 
    * **Erik**:  Are we scoping this to the private measurement work item?
        * **Aram**:  Yes, for now.
    * **Wendall**:  Yahoo is putting something like together internally.  Have two big questions.  1) Does any of this work?  Will it operate in practice?  2) How on earth do I sell this?  Very easy for us as tech platform/publishers to do this, but not clear that advertisers have the appetite to participate.
        * **Aram**:  On 1) Work for what?  What is the output that is most desired?  What we want out of this survey is to understand what is most important.  On 2) Good question. How can we make it easy to sell?  In our next session we have a buy-side panel discussion.  We have an issue open – we should add questions for this audience to this.
    * **Craig**:  Only including a limited number of attribution models will bias against certain publishers just like it biases against some advertisers.  Number of folks on the call could leverage relationships with advertising trade bodies, like the WFA.
        * **Aram**:  Concern is that when we’ve asked this questions in the past we get very extensive questions so we need to have very structured questions. 
        * **Craig**:  What are the set of MTA algos you support?  
        * **Aram**:  But we are talking about the MVP.  Question is whether the MVP needs to go beyond last touch.
        * **Craig**:  Well at least it would show it works.
    * **Mariana**:  Could go the other way around.  Think about the solutions that have been proposed and ask if they would be useful as an MVP given what they can provide.  Important to say that this isn’t just academic.  There are startups that have been acquired that do this.
    * **Brian**:  We should be careful that the candidate set of attribution models are willing to participate in the testing once it’s available.
    * **Wendall**:  Getting anything out there at all will flush out the operational/business problems.  Dreaming of exotic features may not be worthwhile.  When I say something is academic, that’s because that’s what’s getting thrown back to me.  Let’s demonstrate viability by producing something that can be run in multiple companies/labs.
        * **Aram**: Goal is here it to flesh what needs to be included.  Still have conversations with folks in ad tech that don’t believe anything is going to happen.
    * **Alex**:  Demo day!  Because the CMA is now blocking Google from ending cookies, it’s hard to know if it really works.  Everything will do less than what we can do today.  Let’s just show folks demos to prove that it works.  
    * **Erik**:  Let’s start with the proposals we have and get reactions.  Let’s ask people to evaluate the tradeoffs.
        * **Aram**:  Here’s three versions of the MVP and how they work. Which of these would be the most useful.
    * **Wendall**:  At Y!, there will be reduced functionality at some indeterminate point in the future.  Preparing for that is interesting and worthwhile.  Trick is how much functionality there will be and how much it will cost.  IPA and PPM (DivvyUp folks have a working prototype) are viable candidates.
        * **Aram**:  Apple’s web and app solution (SKAdNetwork) and the Chrome Privacy Sandbox one in origin trial, we're looking at both of those at Washington Post
    * **Graham**:  Need to include degree of privacy, utility and cost ($ and implementation cost)
    * **Brian**: We have companies with good resources. Can we tap into them? Can we use that to evaluate proposals? We have representation, can we use the resources we have?
    * **Mariana**:  PPM and IPA more or less the same in terms of functionality if we set aside cross device.  Difference will be mostly about cost side.  In terms of implementation cost:  Think it will be mostly borne by big tech companies – not particularly challenging for customers.
    * **Erik**:  Agree with Mariana on the functionality point - but different privacy levels.
    * **Martin**:  Reasonably fixed in terms of the system build, but we do need feedback on the integration/deployment costs.  Shipping something is the way to really understand this.
        * **Aram**:  If there components that we think will be taken care of by intermediaries, we may want to set those up so that work isn’t borne by end customers.
    * **Aram**:  Let’s establish three potential MVP versions.  These three versions – we could ask how this would restrict you.  This would give us a narrow focus but also a pragmatic approach.  Then we can use this to make a decision on which MVP to move forward.
    * **Martin**:  List the proposals, then list a limited number of question.  
        * Would this be useful
        * What 3 additional functionalities would be helpful
        * What types of changes would you suggest
    * **Aram**:  +1  Next step is for proposal owners to develop MVPs.  In issues we can discuss the question we want to ask.  Then we can distribute them.
        * **Erik**:  What’s the ask in terms of developing the MVP?  Do we want a generic framework to use for evaluation?  
        * **Martin**:  We need a quick brief describing the proposal.  
        * **Aram**:  An ad-tech style document, not an eng paper.
        * **Mariana**:  Most important thing we get away from "match based on keys" and talk in a way that ad tech understand
    * **Graham**: some differences are technical, but should we also describe the Differential Privacy limits/budgets? Will that affect advertisers and their use cases?
    * **Brian**:  Need to be able to provide comparison on a similar set of dimensions.  	
        * Yes, but we can do this after we have the descriptions.
    * **IRC**: How will we decide?
        * Need participation from browser and MPC providers. Then there will be a consensus process.
    * This is focused on the IPA family of proposals, not the attribution API or browser based approaches.
    * **Notes**:
        * **Buy Side conversation**:  In October.  Plan to spend a whole day on that.  Typically under represented, so very important.
        * TPAC is our next meeting.  Have room for everyone.  Can participate virtually. Add questions in the Issue.  Will form agenda in the same way as others.  Need to lock agenda earlier.
            * **Brian**:  May make sense to offer tutorials since we’re colocated.  Add ideas to the TPAC wiki.  Wednesday is the breakout day and is a good day to do these sessions.  Can add requests to the wiki.  If you do, post an issue about this to this group.
* &lt;weiler> The call for breakout session proposals will open on August 16, 2022. There will be 45 slots available, scheduled during 3 one-hour slots on the afternoon of Wednesday September 14. Anyone with a W3C account will be able to join breakouts that are requested to be public, free of charge or registration."

**CLOSE**

**NOTES from Aram towards a survey:**

* What are the currently most pulled reports? What are the stats that are most looked at? Starting with the actual practice?
* "what needs to be available to support the majority of your clients." 
* Dimensional questions - attributions - attribution rankings - stack rankings? 
* What type of attribution models are most popular last click vs mta? 
* We don’t want ‘would you like x y and z’
* Reporting that is currently used is not always useful in terms of actually impacting buying decisions 
* Frame things in the negative? What happens if X doesn’t exist. What would it do if it wasn’t there? What would happen to biz, costs, sales, etc… ? 
* Do we want to survey users? Which of these things do you think advertisers should know about? 
    * Consumer Reports? 
* How do I sell this? 
    * **To sales people**: what do you sell on? Might be useful. What is the most common metric agencies use to sell? Our next call has Buy Side people - might be good to go in with some questions on this? 
* What are the advertising use cases that people have and how are they impacted by this. 
    * WfA report - bring questions to them to answer. 
    * MTA algos we want to support 
    * Last Touch not going to cut it? Good POC would be for MTA
* Demo day 
* Make people give feedback on the existing proposals - form current tech into proposals 
* Illustrate the privacy utility trade offs? 
    * Utility, privacy, ease of implementation, and cost
        * Ease of implementation by whom
        * Integration costs for website developers / publishers  \

* “IPA and PPM proposals are pretty much the same” 
    * How we manage the budgets between the 2 proposals is very different 
* **martinthomson>** I'm hearing a survey along the lines of "here is a description of a system that can be used for measurement: ... **1) would this system be useful in your business? 2) what 3 additional capabilities would make this system more useful to you?  3) what 3 changes would you suggest for this system in order to make it better for you?"**
* **martinthomson** repeat for each proposal
* About 3 grafs 
* Some comparison of proposals 


### == 5m: Closing

## Participants Day 1



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Brian May (dstillery)
4. Nick Doty (Center for Democracy & Technology)
5. Justin Li (Optable)
6. Andrew Pascoe (NextRoll)
7. Sean Bedford (Meta)
8. Heng Tang(LinkedIn)
9. Chris Wood (Cloudflare)
10. Don Marti (CafeMedia)
11. Kyle Hogan (MIT)
12. Martin Thomson (Mozilla)
13. Xiaoqian Wu (W3C)
14. Daniel Masny (Meta)
15. Erik Taubeneck (Meta)
16. Michael Kleber (Google Chrome)
17. Jay Kishigami (W3C)
18. Davis Gilton (Microsoft)
19. Christine Runnegar (PING co-chair)
20. Sam Weiler (W3C/MIT)
21. Wendell Baker (Yahoo)
22. Craig Wright (VideoAmp)
23. Bosko Milekic (Optable)
24. Benjamin Case (Meta)
25. Mariana Raykova (Google)
26. Joel Pfeiffer (MSFT)
27. Sashidhar Jakkamsetti (Meta)
28. Russell Stringham (Adobe)
29. Rachit Sharma (IAB TL)
30. Abida Haque (Meta)
31. David Hong (IAS)
32. Sid Sahoo (Google Chrome)
33. Aditya Desai (Amazon)
34. Graham Mudd (Anonym)
35. Braedon Vickers
36. Leon Yin (Microsoft/LinkedIn)
37. Wendy Seltzer (W3C)
38. John Delaney (Google Chrome)
39. Lisa Markou (Ford)
40. Yoshifumi Takeuchi (Dentsu)
41. Amandeep Aggarwal (Amazon)
42. Tamara Yaeger (IPONWEB)
43. Garrett Johnson (Boston University) 
44. Raimundo Mirisola (Google Ads)
45. John Mooring (Microsoft Ads)
46. David Dabbs (Epsilon)
47. Alex Cone (IAB Tech Lab)
48. Richa Jain (Meta)


## Participants Day 2



1. Sean Turner (sn3rd)
2. Jay Kishigami (W3C)
3. Daniel Masny (Meta)
4. Brian May (dstillery)
5. Aram Zucker-Scharff (The Washington Post)
6. Nick Doty (CDT)
7. Wendell Baker (Yahoo)
8. Chris Wood (Cloudflare)
9. Heng Tang(LinkedIn)
10. Ben Savage (Meta)
11. Erik Taubeneck (Meta)
12. Abida Haque (Meta)
13. Sid Sahoo (Google Chrome)
14. Xiaoqian Wu (W3C)
15. Alex Whitworth (Pinterest)
16. Rachit Sharma (IAB TL)
17. Alex Cone (IAB TL)
18. Andrew Pascoe (NextRoll)
19. Joel Pfeiffer (MSFT)
20. Betul Durak (MSFT)
21. Mariana Raykova (Google)
22. Davis Gilton (Microsoft)
23. Bosko Milekic (Optable)
24. Justin Li (Optable)
25. Erik Anderson (Microsoft Edge)
26. Leon Yin (Microsoft/LinkedIn)
27. John Mooring (Microsoft)
28. Michael Kleber (Google Chrome)
29. John Delaney (Google Chrome)
30. Don Marti (CafeMedia)
31. Aditya Desai (Amazon)
32. Richa Jain (Meta)
33. Sam Weiler (W3C/MIT)
34. Graham Mudd (Anonym)
35. Braedon Vickers
36. Russell Stringham (Adobe)
37. Benjamin Case (Meta)
38. Wendy Seltzer (W3C)
39. Siddharth Sharma (Microsoft)
40. Craig Wright (VideoAmp)
41. David Dabbs (Epsilon)
