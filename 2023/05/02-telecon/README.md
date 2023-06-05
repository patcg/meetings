# May 2023 Virtual Meeting

The Private Advertising Technology Community Group's meeting will be meeting two days for 3 hours at the same time both days.

## Schedule

### Day 1 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 23:00 (11 PM) | 02 Tue | Sydney        |
| 22:00 (10 PM) | 02 Tue | Tokyo         |
| 15:00 (03 PM) | 02 Tue | Brussels      |
| 14:00 (02 PM) | 02 Tue | London        |
| 09:00 (09 AM) | 02 Tue | Boston        |
| 06:00 (06 AM) | 02 Tue | Seattle       |


### Day 2 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 23:00 (11 PM) | 04 Tue | Sydney        |
| 22:00 (10 PM) | 04 Tue | Tokyo         |
| 15:00 (03 PM) | 04 Tue | Brussels      |
| 14:00 (02 PM) | 04 Tue | London        |
| 09:00 (09 AM) | 04 Tue | Boston        |
| 06:00 (06 AM) | 04 Tue | Seattle       |


## Joining Information

Zoom: https://mit.zoom.us/j/95356244879?pwd=NDBwZmxleTMwcHFpZG1MZW1tUXhVUT09 

## Agenda

### Day 1

- <= 10m: Hellos, Intros, Google Doc, Call for Scribes
- <= 15m: [Review WG Charter PRs](https://github.com/patcg/meetings/issues/108)
- <= 60m: [Private measurement of single events](https://github.com/patcg/meetings/issues/112)
- == 5m break
- => 45m: [Private Conversion Optimisation](https://github.com/patcg/meetings/issues/117)
-- Moved to Day 2
- => 15m: [TPAC Review](https://github.com/patcg/meetings/issues/116)
-- Moved to Day 2

### Day 2

- <= 10m: Hellos, Intros, Google Doc, Call for Scribes
- <= 15m: [Review WG Charter PR#59](https://github.com/patcg/patwg-charter/pull/59)
- => 45m: [Private Conversion Optimisation](https://github.com/patcg/meetings/issues/117)
- <= 30m: [Private measurement of single events](https://github.com/patcg/meetings/issues/112) (conitnued)
- [Continue Baseline Requirements Review](https://github.com/patcg/meetings/issues/91)
- <= 15m: Future Meeting Planning
o [TPAC Review](https://github.com/patcg/meetings/issues/116)

## Read All about It!

[Slides to Read All About It!](https://github.com/patcg/meetings/blob/main/2023/05/02-telecon/W3C%20Read%20All%20About%20It!.pdf)

## Minutes

gDoc: https://docs.google.com/document/d/1XjRCMrdZrsf876oBjPhst9mkuBMU99yiCbegzht150g/edit?usp=sharing

## W3C Read All About It!

[Policy Slides](https://github.com/patcg/meetings/blob/main/2023/03/21-telecon/W3C%20Read%20All%20About%20It!.pdf) 


## Day 1


### Hellos, Intros, Google Doc, Call for Scribes

&lt;= 10m

[Policy Slides](https://github.com/patcg/meetings/blob/main/2023/03/21-telecon/W3C%20Read%20All%20About%20It!.pdf) 


### [Review WG Charter PRs](https://github.com/patcg/meetings/issues/108)

&lt;= 15m (actually went 50m)

* Aram: Closing the longstanding thread [https://github.com/patcg/patwg-charter/pull/18](https://github.com/patcg/patwg-charter/pull/18)
    * James who submitted the request, is he on here? Not seeing him
    * Posted a letter that he published / sent to W3C. Part of the ongoing lawsuit “movement for the open web” is part of. Wanted us to note any advice we received from general counsel. We haven’t received general advice related to this PR.
    * Sean: agree
    * Aram: Note no specific advice and no changes to this thread. I think we can close this PR without merging. Any objections?
    * Closed
* Aram: Deweaponize “all known” [https://github.com/patcg/patwg-charter/pull/60](https://github.com/patcg/patwg-charter/pull/60)
    * Not a major change here
    * Any feedback for this change?
    * Sean: could open the possibility that some security and privacy implications could “get in”, but I’m not that worried.
    * Aram: (missed)
    * Martin: Concern is the implication that we must document everything
    * Sean: It’s a way to stop proceeding. It’s an ok change
    * Nick: I don’t care strongly, but it’s in the template. If we think this is a likely problem for lots of charters. I would appreciate if someone filed an issue on the charter template so this isn't just a one-off on our group. I am fine if someone is willing to do this.
    * Aram: Volunteers to put in the PR  [https://github.com/w3c/charter-drafts/blob/gh-pages/charter-template.html](https://github.com/w3c/charter-drafts/blob/gh-pages/charter-template.html)
    * Consensus to merge? Merging
* Aram: Proposals should clearly state business factors and user risks [https://github.com/patcg/patwg-charter/pull/59](https://github.com/patcg/patwg-charter/pull/59) 
    * We discussed this needs reworking
    * Recently a proposal from Martin
    * Open up the queue (no one queues up)
    * How about the last change?
    * Martin: the last one is the result of the discussion and feedback, slight preference for that one
    * Shivan: Does not feel comfortable “balancing” privacy risk with business use-cases.
    * Charlie: I think this is fine. I want to disagree with Shivan, anything this group is going to do will release some amount of user information. I think the question is how much. Obviously zero is the most private but we need to ask ourselves why we are in this group and what we are accomplishing. What we are accomplishing, I think, is a privacy utility tradeoff where it is benefiting the ecosystem and the utility to the ecosystem is derisking other potential harms like fingerprinting or other covert techniques. Mby we can reframe this to a privacy privacy trade off but nothing will be more private than zero. We have to reason through what level of privacy loss is acceptable. If you think that any privacy loss is bad then maybe you should oppose the charter. 
    * Shivan: This is pretty unusual in the w3c to say that we are balancing something in regard to privacy. With differential privacy, I see your point, this is a fundamental tradeoff and this is embedded into the proposal. I also am opposed to using DP in this proposal
    * Aram: question for Shivan: are there specific privacy mechanisms that are not a tradeoff? 
    * Shivan: a technical proposal that necessarily balances privacy as a tradeoff is not acceptable. I don’t know if there are proposals that don’t have that tradeoff, but this road is not one we want to go down.
    * Brian: This is an important aspect of any proposal. They may want to make decisions about. In terms of privacy, I don’t think we should think about it that way, instead information release. This is subjectively a privacy violation. INformation release is objective.
    * Martin: When I think about balance, I don’t think about “they are balanced”. We are not necessarily giving equal weight. User privacy weight can have more weight. It’s not 50/50 split kind of thing.
    * Aram: While we do always want to increase privacy as much as possible, the mission of this working group / CG is to allow specific business practices to occur, less private than a world where these mechanisms do not exist. If this is something you’re uncomfortable with, you are uncomfortable with the WG entirely. For every browser other than Chrome has moved to a more private state. An API that allows some tracking to happen in an anonymous way, etc. It’s more information about user behavior leaking than would have happened before. Goal is still to follow the priority of constituencies, but the nature of the proposals and our objectives is going to require some level of balancing. More data than 0 is going to be coming out of these APIs. Understanding is this creates a more desirable outcome for the web. If you hope 0 data will come out of these proposals, that won’t happen and it won’t happen in a WG PR.
    * Don: Going back to Charlie’s point about private ad technologies displacing fingerprinting. If a particular non-fingerprinting technology is available, then parties will use that instead of fingerprinting. That point needs to be filled out a little more. I don’t understand how that fits in with how a lot of these tracking technologies are modular and can be run at the same time. Still a concern that there will be fingerprinting one way or the other. Fingerprinting + PATCG data collection or fingerprinting on its own. If there is a way to explain that displacement of fingerprinting is going to work, we need to explain how.
    * Nick: a little off track in a deep philosophical discussion. This section is the “success criteria” section. Security and privacy implications sections could be addressed and mitigated. Original impetus of this paragraph was to document this business factors as success criteria and how that interacted w/ decreasing user risks. Not clear what that means exactly. I think the “balancing” is not going to be useful for us in decision making. Document the advertising business use-cases and maybe how they exist in current status quo we could document that.
    * Aram: These concerns were raised in the formal objections process. Maybe your proposal could address them better? The idea is that where we make decisions that balance less privacy for particular business interest vs. absolute privacy which make business objectives impossible, document this balance. More than one specific request that where these tradeoffs were considered, documented in the specified
    * Charlie: I just wanted to quickly say that when we’re talking about balance I’m very opposed to the PR making some sort of objective claim for how much we balance one over the other or which thing is favored. Mostly because we don’t have an objective criteria for these things or these tools and 2 people can take very different looks at the same thing since we don’t have comparable units. We should try to find a way to address the comments without a normative claim in the working group. We should find a way to document these things. 
    * Aram: Would you oppose the addition of the priority of constituencies to the paragraph in the way we are considering?
    * Charlie: Yes, I think the high level thought of this group can reference the priority of constituencies but how it matters for this group is very complicated. It has to deal with first and second order effects. If we have to say that we have to always err on focusing on the user thing we’ll miss the 2nd order effects. I feel if we take this to the extreme and you are not looking at 2nd order or ecosystem effects we will end up not building anything. We would consider that any API would be an issue, at every step we’d be making a decision not to continue. 
    * Brian: I think this group is different from other groups - we want to explicitly identify cases of information sharing w/ other parties. Taking it out of context to compare to other technologies. We want to share technology and make explicit what is shared. We should not be making the case for whether a specific user agent “should” implement. Not something the working group charter should mandate. We should also mention the privacy principles document if we’re building that since it should apply.
    * Martin: Originally going to say that most working groups make privacy worse over time. Fingerprinting surface, etc. Most of them don’t do anything special although they do document the privacy implications of that. We will do that. Detailed security / privacy implications for implementors web authors, and end users. We should document more thoroughly. Might spend a few mins to try to revise this text.
    * Wendel: To get Yahoo’s voice on the record. The important thing is to get on with it. We’re overthinking. The success criteria is “does it work commercially”. It has not been shown. Get something working, then iterate and refine.
    * Aram: Sounds to me not consensus to merge any version of this. Let’s put a pin and try to come back to it thurs. Seems we need something like this, beyond just privacy risk. Not hearing consensus.
    * Sean: Advocate people to think about this before thurs.
    * Aram: Agreed, want WG submitted as soon as possible
* Aram: making explicit that proposals should detail the data they intend to use and return [https://github.com/patcg/patwg-charter/pull/36](https://github.com/patcg/patwg-charter/pull/36) 
    * Lots of back and forth and no significant discussion since then
    * Goal is to express what data is coming into the API and output of the API should be part of the proposal as a distinct section
    * Some feel this could be very useful for the type of work we are doing.
    * Brian: Advertising is a domain where we are explicitly allowing the sharing of information, we should say something about what is being shared. We are providing this piece of information to this party for this purpose. Should be enough so someone can consider whether to participate.
    * Nick: Didn’t especially see the need, but if we do want to document data inputs / outputs, it’s a weird place for it in the sentence. Instead add to a next sentence that the privacy/security section should contain documentation of input and outputs of data.
    * 
    * Charlie: I was going to +1 to Nick. Privacy and security sections often include this information and it seems a natural fit in that section. Brian: Do you feel this text is more coming from the benefit it gives the user considering privacy considerations or the biz participant achiving their use cases?
    * Brian: more from the perspective of users.
    * Charlie: more strongly agree with what Nick said then.  
    * Aram: quick question to Nick. Are you looking for a specific paragraph?
    * Nick: &lt;typing>
    * Nick proposes edit
    * Brian: looks good
    * Aram: going to commit to branch
    * Brian: “should” or “must”?
    * ARam: generally always should
    * Brian: Probably “must” is better, since we are explicitly exfiltrating data.
    * Aram: “should” is considered strong enough
    * Martin: I’m not convinced we need to do this at all. We need to specify things. This dilutes the requirements.
    * &lt;Brian> agrees?
    * Aram: Close without merging? Consensus to close. 
    * Closed
* 


### == 8m break


### [Private measurement of single events](https://github.com/patcg/meetings/issues/112)

&lt;= 60m



* Charlie has [slides](https://docs.google.com/presentation/d/1Cc8_S46m4-z8o_dM4egYSSEyHxc-bGinSw_Say_93uA/edit#slide=id.g21ee318a45e_0_0). 
    * References in speaker notes
    * Will make into a pdf for repo
    * Private measurement of single evnents – vague title for several API proposals
    * Definition of single is event is if out can observe output of single events. 
    * Did source lead to a particular outcome
    * Most API support, in particular event-level in ARA.  ARA summary and IPA also support of craft the aggregation keys to query slices of size one.  Could references a single event.  PCM has limited support, but has information protection so can’t do it at scale. Could learn about a small number of individual events
    * Question for today is if this is okya.  Most aPIs haven’t added protections against it. Would need to be modified to prevent.  Are we okay with just DP? Do we need aggregation?  If we disagree would need an action item to figure out how to enforce additional mitigations and hard to enforce
    * Point 1
        * DP can protect event individual events
    * Point 2:
        * Works for utility 
    * Pint 3
        * Hard to actually enforce if we don’t want it
    * Started as an issue I opened on IPA for supporting this more structurally.   Also issue in the patcg repo to see if we are okay with 
    * What is DP for single events. Why can it protect individual users
        * Ask question did source lead to conversion – a binary question. Real answer 0 or 1,  here real answer1.  What you see is noised added to this answer
        * Laplace, centered at true answer.  Mass closer to 0 than 1 gives plausible deniability. 
        * RR: coin flip and pick random answer. 
            * Graphs look similar if you take an integral of the left graph
            * General principle is the same of introducing some plausible deniability as to the user doing that action.  
    * Interpretations of DP
        * What are we getting if this is the privacy definition we use.  Useful for understanding the limitations.  Giving a more intuitive understanding of epsilon
        * Attacker has prior on user’s data, that they did convert for example.  DP guarantee bounds the posterior of suspicion after seeing the data from the api.  Applies to any mechanism to which DP is applied, even if they are single events, so long as you prove the sensitivity bound 
        * Read x axis as initial suspicion, up and down is new posterior, colors are epsilons. 
            * Need much higher epsilon if you already have a good prior. Looking at the data lets you finish getting to high confidence  
        * When we say Aggregation gives strong properties – it isn’t that single events doens’t give us aggregation. Just that it happens in a post-processing step. 
            * Aggregating after events of many users isn’t going to give you more information about individuals.  Gives tighter error bounds on the utility outcomes you care about. 
    * Ben Savage:  slide with graph – under the impression other higher the epsilon the higher the leakage,  hard to understand the bounds are getting bigger and bigger. Epsilon small seems to move it further.. 
    * Charlie, percent is 50% :50% is no idea the user did it.  Shoots in one direction or the other means have learned about the user.  [ ..] is not an interval in the notation.  Your probability goes to 25% or 75% if gave you a 0 or 1.
    * Brian:  Users are going to have a hard time making sense of potential privacy issues if not clear what data is being discussed, if they are not sure in what context collected and released.  Hard to make a comparison between aggregated data and events without knowing the data being discussed.   Aggregation of events could be about what individuals are doing online or ad an campaign.  Single or aggregated data seems less important than what the data is.
        * Charlie: fair, but want to disassociate inputs from privacy mechanisms in this deck – but what I’m thinking of is source event and you want to learn how many conversions resulted.   Also issue that platforms can’t really enforce what the events was, versus the api getting called when it is unrelated to something the user is experiences.  How we prevent learning about the user’s data is this post processing closer or DP.  bounds don’t get worse for user given post processing of event output
        * Brian: we are trying to build a system that provides information from one context to another context – our desire is for an understanding of ad usefulness but hard to prevent that being used for learning about a user’s trajectory.  If you have enough samples over time you’ll be able to make meaningful inferences about a user’s behavior.
        * Charlie: related to our discussion last time about leaking more information over time. What we can do is reduce the rate of the leakage.  Observing the user of time, years, you’ll be able to learn about the user.  In the short term the only meaningful way to look at the data is in aggregates. 
        * Brian: concern is that if we proceed with DP as sufficient protection when it is not, then we have a soft foundation for going forward w
        * Charlie: easy to say DP is the primary means, and not the auxiliary means.  We need to be comfortable with DP as a foundation and not regress from that.  It becomes the primary means we are relying on
    * Charlie: 
        * Aggregation post processing that doesn’t leak more information – from utility this is very helpful when you want flexibility of queries. You can issue many more queries after with different slices when privacy is already build it. Vs ARA or IPA where you need to craft individual queries that each consume some of your budget.  By asking the question on individual events we’ve paid the DP cost up front.  Often more up front but is more efficient if you’re doing to do many queries
        * Graph of different DP compositions 
            * At some point local DP is better than all the central compositions as the number of queries goes up
        * Also removes complexity of API.  let caller do the complexity of different aggregations. Can just give noisy data to caller of API. 
        * Another use case – label associated with impress; much easier to do 3rd party measurement  when you don’t need to standardize industry level aggregation keyss.  Some cases where we may be able to implement more efficient use cases by not giving individual sites their own budgets.  Open problem but interesting, even in case they are all colluding 
        * Finer point – optimization user case
            * Learning models that can predict if an impression will lead to conversion or not with high probability. 
            * We’d be in the setting of label DP – ad context is not privacy of where ad is show and maybe user if signed in. what is private is wether lead to a conversion, the “label”.  Lots of research in this area. TLDR: single event measurements are the best algorithms we know of for private learning – achieve state-of-the-art learning better than other DP learning methods.   Blue line doesn’t user other public information.  Data is images.  But we don’t have published yet. We are doing better than other DP approaches, even with small epsilons.  Research in Google and Meta in the setting of label DP.  want to continue to explore future innovations – expect better results in the future, but looks like event level are the best algorithms
    * Ben Savage: slide with flexible aggregation 
        * Agree with optimization is great for events
        * Criteo published on event level – event level not suitable for reporting use cases. Our conclusion too – poor privacy, utility tradeoff for utility.  What use case is this? Something I don’t get? 
        * Charlie: agree hard to support reporting with this.  Making the point this is a general approach that generalizes to other use cases like aggregation that require complicated processing outside the system. This is intuition why this works.  For reporting, we’d need to do more research
    * Ben: do you have another use case in mind for this than optimization?
        * Charlie:  if you have many parties doing budget splits about the same data maybe better to do event level and share the data.  Also true if you had some label DP for optimization that didn’t work on single events – but if we need to train 4 models maybe better to do events because would be more efficient than single events
    * Brian:  safe prenoise data vs not – two classes of safe event level and not safe aggregate – don’t want to mislead people
    * Charlie: would stay away from that framing – if we had aan aggregation mechanism that works on the data we’d like to say that these can be equivalently private – except that with aggregation you’re utility will go down with more queries.
    * Brian: concerned users won’t understand and be taken advantage of
    * Charlie: what part?
    * Brian: sounds like we’re saying some data okay to share because noise in preparation and others that not safe to share because noised in aggregation
    * Charlie: for the ones that do noise in aggregation there are protections in the security of the system that prevents it from being released. What we’re talking about there is the outputs.  It will be the systems job to aggregate the data.  If keys leak you’ll be able to construct the data, but otherwise the unaggregated unsafe data is ephemeral. 
    * Brian: sensitive data should be encrypted. Safe data doesn’t need that.  We should be clear of that in the designs 
    * Charlie: very common to have boundary of confidentiality and privacy outputs. Agree with that. 
    * Graham: is the point you’re making that if you intelligently choose the privacy mechanism that you can extract more utility at a give level of privacy?  Use case dependent, you may want to use local or central, but still get same level of privacy
    * Charlie: yes, exactly.  Not proposing this is the only output mode. Question is to ban or  not.  Agree there will be some use cases, e.g. reporting, where this doesn’t make sense and you’d do many aggregation queries.   We have a privacy bar — optimize within that to increase utility.  Don’t tie our hands 
    * Graham: what is challenging is how to define that bar and make comparisons.  Here DP and epsilon and delta – can you truely compare across these curves.  What about other privacy mechanism like information theoretic – is there a way to compare?
    * Charlie: once multiple privacy mechanisms can still have privacy utility curves, but harder as another dimension in the system.  Maybe can come up with some graphs if we fixe some things for comparing.  Any other constraints we add will make it hard to optimize for utility. Some of these other methods have nice properties and can be helpful to talk about in addition to DP
    * Charlie:
        * Aggregation hard to enforce 
        * A few flaws – k-anon style mitigations.  
            * Analyze cardinality of inputs to outputs.  Truncate or other mechanism to make more private buckets with fewer users. 
            * Remove certain campaigns from the output if they had fewer contributors than some limit.  Any row with less than 30, remove that campaign
            * Problems with this definition – doesn’t match with our security threat model – we don’t prevent injection of fake data that can be used to bring up a row to k or k+1 and it will be released.  Adversary putting in the data
            * Magical property of DP that it protects against this.  Not the case with k-anon techniques unless you can enforce strong verification of real inputs. Hard to establish that trust for clients. 
            * Even if you have an adversary that can’t generate fake events or prevent by making it expensive – k-anon doesn’t give prevention of targeting individuals if you can do flexible queries. 
            *  K-anon not robust under composition.  Hard to analyze it with many queries.  Privacy claims on k-anon often need to make assumptions on the input distributions. Unless you add noise, there can be major leakage to individual events. 
            * K-anon style preventions are weak. 
    * Ben Savage:
        * Technically correct.  Downplay potential benefit of making it not being economically feasible to do event targeting at scale.  Suppose a player is doing this tracking for 1B users with cookies, then would need 100x cost of the api do keep doing this. Probably means that whatever benefit they were getting is outweighed by the cost. Could do differencing by different queries, but also would have to do many queries to do this at scale. Would have to have many duplicate queries. Correct in the worse case scenario what you said, that this doesn’t give protections beyond the DP. but useful and valuable to evaluate system designs that make it difficult to do at scale. 
    * Charlie:  good point on scale. Next slide, but hard to judge if we don’t know what the cost is. We want the queries to be cheep.  Don’t want to claim economic non-viability because system is inefficient.  Strage incentive for the system. All trying to get at scale prevention.  Hard to evaluate if we’ve done a good enough job or not, if we make more efficient or introduce some interesting query.  Becomes more difficult if we set this as a goal. 
    * Bria: other side of k-ano – removing information from system; lots of value in that information. Low level information but useful. Limits to utility of k-anon. 
    * Charlie: there are approaches to k-anon that don’t remove data but coarsen instead. Not great to have loss in the api
    * Don: issue of budgets for queries.  Multiple independent queries by same adversary to identify overlapping groups of k users.  Users are concerned about [Texas SB8 private enforcement](https://en.wikipedia.org/wiki/Texas_Heartbeat_Act#Section_3) – where the payoff for identifying a user is high relative to most legitimate advertiser budgets.  Adversary might have a higher budget if they are well resourced, can do multiple queries to identify multiple groups of “k” users.  What do we get against them?
    * Charlie: hard without a specific case study. DP can make worse case claim in general. K-anon will always require some case by case study. Harder to say with k-anon if something impossible.  We can try and write down some of this but is an exercise to do. 
    * Don: what is the plan to do this? Other web users and stakeholder will be concerned about adversarial use cases, e.g. defense industry.  People concerned about adversaries. How to price out adversaries and not common users. 
    * Charlie: would first have to decide we don’t want event-level.  I’d like it. And in that case we’d don’t need to get into the details on these mitigations.  If we want to go there will need further analysis.  Premature to do there until we decide we don’t want event level
    * Charlie: another mitigation – max information gain. Goal for adversary is to maximise the useful information between x and y.  A different privacy definition that captures both noise and granularity.  Limites the number of distinct events you can get.  Is robust against composition.  Can be analyzed better than k-anon. Don’t have to make assumptions on the advertiser.  If we have an information gain bound we don’t have to worry about a $ budget mitigation.  This is an average notion – auxiliary information might let you learn more.  If you have DP, automatically induces an information gain bound.  You can make it stronger.  Information gain bound doesn’t necessarily bring DP.  weakly protects against measuring individual events.  More robust than k-anon to prevent scaled attacks.  If we want a at scale prevention of tracking, this is a good approach. 
    * Martin: aggregate measures of information not great at an individual level. DP gives you this and this is just supplementary.  Aggregate metrics don’t tell you how individual people are protected but DP does.  In aggregate we may only say x information on individual level but it could be that most people not contributing anything while a few contributing a lot
    * Charlie: agree. I think we all pretty much like DP.  single event is the intuitive effect of that being the only privacy mechanism.  If we are okay with that great, but if not we need to come up with something else. And what we may come up with not going to be great in all cases.  Agree with Martin that DP is the thing that protects individuals.  This if we want to prevent scaled attacks of targeting.  I’m not saying preventing that doesn't have privacy benefit
    * Martin: i’m not comfortable with event level people I don’t know how to explain it to people.   I understand the technical claim. 
    * Charlie: how to reconsite with mitigations
    * Martin: economic one helpful
    * Charlie: this one doesn’t need economics 
    * Martin: still does if you’re the person contribution the most
    * Charlie: agree not air tight but becomes easier to analyze separate of attackers $ budget
    * Ben: with $ in the other you lose just k-anon and not DP
    * Martin: concrete, with RR. make submission and 1 in 20 get flipped one.  From user’s perspective get some deniability but if prior is strong you get 95% confirmation of prior. Seems unsatisfactory from user perspective.  What we do here may be worse.  If we bound to information to .1 bits per user, it could be 5 bits from one user.  Don’t have concrete solution though. Passed 1am
    * Charlie: all of use could be comfortable with DP under certain parameters, epsilon = 0…, but that might be what it comes down to.  Some epsilons where it is okay and others where it is not.  Agree that if epsilon is hight enough event is pretty bad and we should bound the information somewhere else.  I think we can get useful data even with pretty tight data, epsilon 2, 3, 4 in our paper (see fair?).  Good outcomes if we can come to discussing how tight it should be with the existing framework we have. 
    * Joey: you mentioned a publication. For event level DP for advertiser, always concerned with lopsided labels – already so fewer conversions.  You’ll be overwhelmed with false positives. Happy to wait for paper
    * Charlie: 2023 paper uses ads dataset, where signal is weak.  Criteo and AppData(?) dataset. There is data.  We don’t have graph of comparison I showed for ads data specifically.  Please read the paper. Would like to publish more. 
    * Nick: sense of privacy. Plausible deniability and transparent queries. I think we make the mistake privacy is just the amount of information revealed more broadly. I’m working on describing the different privacy senses we care about. Individual decision making even with noise.  Adv doesn’t know this person but has enough information to target, not high confidence but can be used in individual way.  Bad for privacy not just because it revealed information but because creaps out the user. Users won’t be happy if that is the outcome of DP system. Should be concerned how individual data used
        * How are queries used.  Event level flexible for many queries.  Even though that might have same privacy claim could be hard for users to understand what queries are being made on their data. Not helped by the ability to share and query many times
    * Charlie
        * First one, we should bring to topic on optimization – does measurement lead to better targeting.  Is a question of whether we want optimization to be a use case or not. Wouldn’t be doing targeting but model training for inferences about general properties about people. Like something make like something else.  With DP with can bound the model outputs relative to individual user’s inputs. We can say it is only learning from the aggregates of many users. Separate from saying model training possible. Nick mauve you’re saying we don’t wan that use case
        * Nick: understand inferences will be used for targeting – won’t go away entirely.  But can design for individualized use or not. 
        * Charlie: but is the inference about user coming from aggregate or not – models are still aggregate process.  Maybe you’re concerned about use case where no aggregation but being used for targeting.  Not sure how to prevent but again the economic prevention that it wouldn’t work. Maybe people wouldn’t do it.  Understand 
        * Second point ; flexibility of queries 
            * Tough one. Post process is useful. System no longer cares how the data is used and it won’t leak more information 
            * If we try to go the other way and be concerned about how the data is actually used, feels appealing, but hard to enforce. Leads us to different solutions if a vague goal but if not a clear boundary it is hard to make decisions.  To what extent are we sacrificing usefully to achieve this goal but maybe we can’t measure if we achieve that goal event. Similar to k-anon situation. Maybe we forbit overlapping queries, slowly carve away useful features.  
    * Nick: enforcement is a difficult issue. Many jurisdictions agree but still think it is important what the information is that is released and think we should care about it too. 
    * Charlie: don’t think this is in conflict with formal event-level.  Could ask the user of the system to do queries in a transparent way.  Could implement that system more easily where the post processing is transparent but the DP is still event-level.  Is more a privacy specification. 
    * Nick: not saying totally incompatible with transparency – just saying that transparency isn’t a concern isn’t a benefit
    * Charlie: agree we can combine them
    * Ben: first about agenda. 
    * Aram: moving to thursday optimization 
    * Ben: let’s work through an example. RR, puts in a example where RR looks good.  But look at RR graph.  If random &lt; 2 … what epsilon is that if you pick random 50% of the time 
    * Charlie: that uses epsilon 1.1.  Picture is better. 
    * Charlie: prior of 50% is not best situation.  Port of 50% worst case. 
    * Ben: meta conversion rate is ~1%, lets say we use that. For every 100 ads 1 person buys.  This is the prior.  You’re paper on high performing label, if epsilon is 2 and this prior - what did this do to the posterior. 
    * Charlie: formula in slides. 
    * Ben: Prior .1%   epsilon is 2.   Jumps up?
    * Charlie: no not jumping high. Only jump high when get to high priories. We are protected in the case of good priors. 
        * Posterior update is .7% with your epsilon
        * Ben: cool that sounds good
        * Nicks’s example – conflating profiling with optimization. Nick talking about noisy user profile. Got a 1 would have .7% chance the person bought the thing. 
    * Charlie: database with 10 flipped and 1 real out of 1000,... better than 
    * Ben: thanks for correcting. My intuition was wrong. This is better than I thought. 
    * Charlie: thanks I’m sure many people also don’t understand. 
    * Ben: plausible deniability, start thinking about court rooms and reasonable double 99% confidence. What does it take to get to that?  In epsilon of 2 you’re not anywhere close to that. 
    * Charlie: epsilon of 6.8 and prior is 10% then posterior will increase to 99% if you see a 1. 
        * Problem with DP is we don’t want to fix an adversary with low priors. But worthwhile using to gude the epsilon for sensitive events. 
    * Ben: ads context you know everything before click. Post click page loads; did people wait long enough for page to load.  Then there is sensitive information about ad to cart, like 10%. Then there is buy which is like 1%.   Is there a post click conversion that is sensitive but high probability? 
    * Charlie: problem is this is a general web API and we need to think about some things beyond ads. For honest ads I agree.  Maybe there are mitigations against this.  Adversary wants to measure if you visited a fake website. Say 20% as still a high prior.  Overall point is right if we are concerned about ads then the fact that these things is rare is a benefit on privacy side and curse on the utility side.  Rare events means some better privacy
    * Graham: slide 10 with different DP compositions
        * Important to explain the magic of DP. All the datasets were individual at some point. The question is where you apply the privacy mechanism.  In certain situations where you want to use the data over and over, e.g. in ML, then local is a much better way to constrain a privacy leakage and get utility. But if you have a specific question and you just care about campaigns then you’re better off using a central method.  Main point is that in all you have a privacy budget, say 2, and then you can choose between the two.  In terms of leakage we should be unconstrained if we agree abide by a privacy epsilon that is reasonable.  Struggling with the debate there.  If you agree to the bound then who cares if you apply the aggregation before or after
    * Charlie: agree with you.   I’d like to get to us all agreeing that that.  But not sure we’ll get there today.  Different people may have different epsilons as which they need to look at additional preventions. At some point I’d like us to say it is strong enough and not require additional things
    * Graham:  to Ben’s example, none of these alow for retargeting if you choose a reasonable epsilon. Requires a high degree of confidence.  On the other hand all these approach lead to incremental learning over time even if done in a central way, e.g. i’m a runner, they all allow profile development, they just slow the process. All of them wouldn’t allow for instant retargeting
    * Charlie: generally agree.  Aram – will leave to you how we move toward consensus. 
    * Aram: we can follow up on Thursday 
    * Charlie: let’s keep an eye towards alignment. Seems we understand what the tradeoffs are. 
    * Ben: let’s wait till after the optimization talk tomorrow before getting to 
    * Aram: move TPACT to tomorrow. We’ll discuss Thursday. Also face-to-face coming. 
    * Aram: topic important to our final outcomes.  Think about how we can come to alignment on this so we can discuss on Friday. 
    * Aram: let’s also try and close out final PR on Thursday. 


## Day 2

Scribes: Paul deGrandis, Michael Kleber, _&lt;third volunteer could be you!>_


### Hellos, Intros, Google Doc, Call for Scribes

&lt;= 10m

[Policy Slides](https://github.com/patcg/meetings/blob/main/2023/03/21-telecon/W3C%20Read%20All%20About%20It!.pdf)


### Working Group Charter 

PR#59 [https://github.com/patcg/patwg-charter/pull/59](https://github.com/patcg/patwg-charter/pull/59) 

Aram: Note Nick Doty couldn’t make it today, we’ll progress without him despite the strong suggestions he mentioned;  Discussed this Tuesday, suggestions made on the thread from many members;  Queue open for discussion

Aram: Leaning towards Nick’s 1 and 2 (maybe 3)

Sean T: All we can do is specify what the protocol can do and not do (define the boundaries/guardrails).  I think what we’re getting at is tweaking the wording a bit and moving forward.  Less is more.

Ben S: I move we add Nick’s 1 and 2 and merge it

Brian: I think we identified what we want to incl and it’s good to go

Martin: I agree, we should take the words Nick used in 1 and 2 (not 3), make them look charter (matching in language) and move this forward.

[Aram live edits the charter in the issue to include new language]

 

Aram: Does this text look good to everyone [group gives thumbs up]

Call for objections?  Merged

Sean T: Asks Sam what the next step here, given we have resolved all outstanding formal objections

Sam: I believe we’re back into the process of getting this approved

And the crowd goes wild!

Aram: If you plan to object to the next version of the charter in some way, please also suggest text that would address your objection.  Would save us a lot of work parsing out what people want.


### [Private Conversion Optimisation](https://github.com/patcg/meetings/issues/117)

=> 45m

Ben (Meta): Talking about privacy-preserving ML and how it might work.



* Motivation: Ads selection.  You have a website visited by a bunch of people, and there are a bunch of ads.  It's a matching problem: you have to somehow decide which ad to show to which person.  One component is "Targeting" — advertiser lists some criteria, and particular people are not eligible to see some ads based on these targeting criteria.  But there might still be thousands of ads that are available to show to any particular person, and you need to make some choice.  So how do you choose the best mapping of ads to people [people to ads?]?
* For each configuration of people-seeing-ads, they lead to some eventual set of purchases.  So maybe you want to pick the matching that maximizes value creation.  But creation for whom?  Hierarchy of needs: foundation is _user value_.  Publisher value requires advertiser value so that advertisers keep spending, publishers and advertisers need user value so that it's worthwhile to spend.  But we don't have a good way to measure user value, so we use advertiser value as a proxy.  Ask advertrisers how much they are willing to pay for some event, and hopefully this is a lower-bound on user value — user's expected value > $spent, $spend > advertiser profit, and advertiser profit > $ advertiser is willing to pay for the conversion.  All of these inequalities are a little shaky, can't follow blindly, need guardrails, but we try to make it work.
* How to do this?  Loop over all ads and compute E(value) = E(conversion) * value(conversion), then pick ad with highest expected value.
* So need a function which returns an estimate of conversion likelihood.  Inputs to function: ad features, contextual features, and possibly user features.  Output of function: prediction of the likelihood that showing this ad will lead to a conversion.
* Constraints:
    * Just learn about _general trends_ in the data; do not memorize information about specific individuals
    * Not rubbish performance — should be better than just optimizing for clicks
    * single-digit epsilon budget
* General plan of how to do this:
    * Look at "thousands of rows of" historical data — features (this ad was shown in this context to a person with these attributes) and a label (either led to a conversion or didn't).
    * Find a function that does a not-terrible job at predicting the historical labels.  Define a "loss function" = some score of how far off this function's predictions are vs what actually happened in the past, hope it does well in the future.
    * Optimize loss function via gradient descent — make lots of local improvements in the parameters that define the prediction function until we get to what looks like an optimal point.
* How do we do this with privacy?  Here are four options:
    * 1. Release "noisy labels" at the event level: In some historical cases, give out the wrong answer to "did this ad lead to a conversion?"  This is "randomized response".
    * 2. Release "noisy labels" somehow capped at the _user_ level — so that we can provide a sensitivity bound at the user level, and even power users who generate lots of events get similar protection despite generating lots of training data
    * 3. Logistic regression which can be calculated in MPC
    * 4. DP-SGD in MPC — Differentially-private stochastic gradient descent.
* 1. Noisy labels, event-level:
    * Pick a value of epsilon, return random label with some probability
    * Pros: Absolute minimum inside MPC, so really cheap.  We know it works, epsilon 2 or 3 ish.  We could launch it today.  Yesterday Charlie showed graphs indicating decent performance.
    * Cons: Depends a lot of how we feel about private measurement of single events.  If we don't like noised single events on a philosophical, then this doesn't solve that — no aggregation guarantees coming from the mechanism.  Also does not have a user-level sensitivity bound (leading into idea 2 below), with the risk of disproportional impact on power users vs normal users.  Also there is a risk to model explainability: The system we build does not know how the training data is going to be used, so there are some kinds of promises to the user that we're not able to make.

Charlie: I don't think that for randomized response mechanism here we should have a _different_ privacy bar than for the overall system.  My point yesterday was that we should have the same guarantee for label-DP as for aggregate histograms.  User-level or event-level seem both workable, but there is nothing special about this data that lets me argue that event-level is fine vs user level.  What we chose in ARA was an attempt to provide a framework for privacy and then hit utility goals, and I don't think there is anything about these algorithms that must be event-level.

Ben: So optimization use case has the same answer as the aggregation use case?  Both user-level or both event-level?  IPA has an event-level sensitivity.  Does that mean that both ARA event-level and ARA aggregate do not have a user-level sensitivity bound, just an event-level?

Charlie: None of the systems provide a user-level bound, because budget is divided per advertiser.  We have some broader privacy scope if you take into account advertiser, publisher, ad tech.  We take that into account through rate limiting per privacy scope.  We didn't have the same privacy bar for event-level and aggregates, we could choose either route.  If we did lots of innovation on user-level and couldn't ship it and needed to fall back to event-level, we could make it work.  For now we're going to assume the same privacy units along either path, diverge only when necessary.

Ben: So since these two proposals both have different budgets per-site (whatever "site" means, maybe cross-product), you don't have a user-level bound.  But for a particular scope/site/whatever, you do have a cap implemented via a different mechanism, via a rate limit?

Charlie: Right, and that gives a composition bound, if you think about DP.  With event-level that's also trickier to think about since we bound conversions but noise impressions, so harder to calculate.  But there is an answer.

Ben: So there is a spectrum in between my #1 and #2, different ways to bootstrap from event-level to user-level.

Charlie: Right — and user level may be easier to get utility from if it's not implemented at the device level, central model may make it possible to make better decisions.

Brian May Q: What does "user" mean here in terms of data points?

Ben: In the ARA model (with on-device attribution), you get "this particular ad click #1234567, did it lead to a conversion? YES", but maybe that YES is a lie.

Brian: So by "user" here we mean "specific browser instance"?

Ben: That's my understanding of ARA

Brian: So no notion of user across UAs?

Ben: Right.  User might use multiple different browsers.

Brian: Let's try to be precise about language here.  There may be many users that use the same browser.

Charlie: In Chrome it's at the per-browser-profile level.

Ben: With IPA we do want to know the same person across a phone and a laptop browser, and that would indeed mean they share a privacy bound.  But we've walked that back for now, nothing cross-device for the moment.

Continuing the Ben presentation to options #2, #3 and #4 for how to do ML:



* 2. Noisy labels, user-(browser-)level.
    * Pros: Multiple ways to implement this, per discussion w/Charlie.  Only a bit more than the minimal amount in MPC.  Not quite as good as #1, but optimistic.
    * Cons: still noised version of single events.
* 3. Logistic regression in MPC: probability is just a simple linear combination of all the features, then put this through a logistic function so that we get values between 0 and 1.  Our task is to find the constant weights for each feature that minimizes the loss function, the loss function is concave, easy to optimize.
    * Pros: Easy to understand and explain — just learning about correlations.  Is the correlation between this feature and conversions positive/negative/zero?  Strong or weak?  Could build this with just a single dot product inside MPC
    * Cons: Super simple model, probably won't perform very well.  Won't compare to deep learning.  Unknown privacy-utility curve.
* 4. PD-SGD in MPC: Pick a random subset of training data, "randomly selected min-batch".  Compute gradient of loss function just with respect to the mini-batch.  Clip the gradient, so that it has a maximum magnitude.  Sum this over lots of mini-batches, add some random noise (proportional to the clipping value), update the model using noised sum, repeat until it converges.
    * Slide with table of three different options for which parts of this happen in MPC: Just aggregates (no mini-batches) vs all in MPC (with incremental releases after each update of model parameters) vs all in MPC (one single release of optimized model params).
    * Trade-off of total processing cost in MPC vs total privacy budget consumed.  Or at least we think so — no formal proof that only releasing the optimized model is actually less privacy leakage than releasing incremental releases.
    * Pros: Maybe can train a medium-sized neural network, pretty confident that the DP means it's not memorizing data about individuals.  Maybe decent utility for a given privacy budget, though Charlie's presentation yesterday points out that in practice we haven't really seen it.
    * Cons: Very hard in MPC, might not work at all, and no business continuity of ML training paradigm vs today

Mariana: Computing the gradient on-device, your column 1, is just Federated Learning.

Ben: I was thinking about the IPA model, where joining impression to conversion happens inside MPC, not on-device.

Mariana: Pre-compute each gradient update vs each model label?  With a small space of possible labels?

Ben: Right, conversion-or-not is only two possible labels, so this is OK.  With many labels, this will explode.

Ben: Here are the two big questions: (1) Do we want to support this use case?  (2) If yes, how do you feel about those four ideas?

Charlie: Strongly in favor of supporting this use case.  This is a P0 for Privacy Sandbox.  Which one do I like best?  My usual answer: Among those which meet the privacy bar, I want whichever gives the best utility.  Regarding noisy labels: Much more than just flipping labels, it's key that labels are private but features are not private.  Under DP-SGD the labels also are private.  Quality degrades as model size increases.  You can do other fancy things beyond just flipping labels — maybe something that's much better than just label flipping for these really spare ads models.  We think there is a big design space in the setting of noisy labels but is not limited to just that.

Brian May: It's hard to formulate responses here — Ben just covered a lot.  I think that your starting assumptions are biased towards the buy-side: should consider incentives of publishers also.  They are trying to optimize for yield = as much money for as many ads as possible, while advertisers are trying to optimize for as few ads for the least cost per ad per conversion, these are not the same.  I'm concerned about this group standardizing how inputs turn into outputs: a lot of what we do in ad tech is finding novel ways to compute based on a data set that everyone has access to, so if we're standardizing the space of what might happen, then we're standardizing the place that all value creation happens, which is very bad.  Need to leave a black box in the middle to the party that is trying to provide unique value.

Don Marti (noise and centralization risks [https://github.com/w3ctag/privacy-principles/issues/261](https://github.com/w3ctag/privacy-principles/issues/261) ): Trying to figure out more about the statistics of noise communication channels.  Would a large party with access to large amounts of noisy data be able to get more useful information than a smaller third party?  Tendency toward centralization is a risk.  If large parties can get more value from additional conversion data than small parties, then the privacy mechanism might drive centralization.  I think we have anecdotal evidence that users are less comfortable with large parties having an ability to make inferences about them.  Users are happier with more widely-spread information sharing.

&lt;scribe: just want to be sure I did not miss a "not" in there?  Don: Anecdotally less expression of concern about small vendors, lots of expressions of concern about large Internet companies with connections to or under the jurisdiction of foreign governments.>

Aram: Sounds like you're saying people like small exposure to many companies rather than large exposure to few companies.

Don: Yes. (In recent research, users have been more likely to express concerns about information sharing with a few large, well-known companies than about information sharing to smaller publishers and retailers)

Mariana: Just wanted to repeat / emphasize that Label-type guarantees are true only assuming features are public.  Parties that can receive output of mechanism has to be a party that knows the features in the clear.  Label-DP is one way to do this.  All other MPC approaches: If you have features known to one of the parties then you can simplify a lot of other mechanisms too.  Is this always the case in ML optimization?



* Ben response: Totally correct — I am assuming the setting of ads selection happening in a way that the party invoking the function is able to provide these arguments to the function — they know the ad, the context, and something about the user.  This is _not_ the case in a setting like FLEDGE, where you don't know both of these things on a server, only both known on the device.  In that case you perform ads selection on-device, or else it gets more complicated.
* Mariana: You're talking about prediction, I was asking about training.  Someone is recipient of the ML model.  With label-only type of guarantees, you are saying "Even if you get the whole model, it does not let you learn the labels of the training data"  But it does _not_ prevent the person who gets the model from learning something about the training features that went into it.
* Ben: In FLEDGE, you cannot collect training data in the clear, so it would be a problem — releasing the model, even if trained privately, might release data.  If there are features that we are OK with their use in models but not OK releasing it in the clear — that's the other example I can think of.  That is generic use case, where you are just a site that has some data and wants to show an ad.
* Mariana: So from your slide with three columns, if the party knows all the features in the clear, can compute gradiends.

Martin: There is possibly a scenario where feature privacy comes back: what if you collaboratively train models based on activity on different websites, and sites are not willing to share features.  But what I queued up for was: Ben claimed Logistic Regression was explainable.  To the extend that you're saying "We're just looking for correlation between X and what happened", it sounds good.  But what is X the feature space partition?  None of that is explainable to ordinary people or even engineers.  I would avoid making claims like that — I don't think any of this is explainable.  We shouldn't worry about that, we are already in an area where that is hopeless.



* Ben: So any stance on the big final questions?
* Martin: Not opposed to the conversion optimization use case.  Don't feel very happy about noisy labels on the event level — this seems very bad.  Some discussion about how to push that toward user level, which is a maybe.  I'm not interested in the how, I'm interested in the consequences for people.
* Charlie: You mean, given a privacy guarantee?
* Martin: I want to create a privacy guarantee box, and be as productive as possible within that box.  The idea that this might be individualized information still makes me nervous.

Paul deGrandis: There is nuance on all of these details.  Kevel’s “Core” product is a decision and measurement stack.  We isolate on first-party data, that's how we solve the privacy problem.  To answer the two questions: Yes, we should solve the conversion optimization problem.  Noisy labels are a good place to start, we have good data at Kevel that shows noisy labels work, and Federated Learning works.  I think logistic regression is pretty good as part of an ensemble, even if not by itself.  I disagree with Martin that it is explainable — the ensemble said "yes".  I feel like DP-SGD is a non-starter since I think the first three options work OK, so unless the privacy bar means that the first three options don't fly, very hard to justify going with 4.  Moving to LR in lots of different places, as part of an ensemble

Aram: Explanation — how explainable are things?  Advertisers and systems that work purely on buyer's behalf are fairly uninterested in explanations, they just want results.  Things successfully pitched to the buy-side indicate to me that they are not really looking at explanations even when given.  Need to be able to explain things to publishers, and to users, who will disable for their site or for their browser.  Need to be able to explain it to regulators: doesn't matter how perfect on privacy that we can make it, someone will challenge, and the person who needs to explain it will be Google or Facebook or some publisher who is caught on the front line.  Also: There are two marketplaces for digital ads right now: You, Ben, operate in a scale market — optimizing for more available impressions means more revenue, lift measurement means less impressions needed to fulfill a campaign and therefore more impressions overall to sell, this is how Meta can drive efficiency.  If you can get click-throughs then you get more impressions for more purchasing, via efficiency.  Meta is optimizing for scale of impressions.  Most other sites are more adversarial in relationships with buyers: they are employing techniques that push buyers to spend more per impression, and this model isn't Meta's but we still need to acknowledge it.

Ben: I expect that training prediction models is useful and important for both.

Aram: Yes, still important, but outcomes are different.

Charlie: Respond to Don's comment re. centralization and data scale.  Feels to me like we want to prevent companies of all size from tracking the user or invading privacy however we define it.  Doing something where big companies can't track users but small companies can feels weird to me — don't want it violated by anyone.

Don: I didn't want to put smaller attempting-to-track parties on a better footing than the larger ones.  Just concerned about centralization risks and how they overlap with privacy risks.  I don't want to rule out adding noise, but there might be some noise-adding math that balances out the centralization risks, by increasing noise added for parties that have more data.

Graham Mudd: Quick point: similarity between Aram's point and earlier from Brian — a centralized approach that works for everyone, that focuses on inputs, is more scalable than trying to ship an end-to-end solution.  It's harder but scales better, and we want to allow for competition in digital ads.  I don't have a strong opinion on user- vs event-level.  Question of what the budget is and how often it's refreshed will probably make a huge difference.  Event-level with stronger privacy def's may be better than user' level with weaker.  Either might be sufficiently private or not at all.

Michael Kleber: A few people have piled on Ben for one-sided view of how the ads marketplace works. I'll join the party. Feel like the discussion about knowing features “in the clear” was part of this same issue. A model where you assume ppl know the features in the clear makes sense for a small # of very large sites, which includes Google and Facebook among them. The display ads approach, in which you are trying to place ads on a large # of smaller sites, really at a deep level requires combining features from across multiple sites at the same time. In particular in our work FLEDGE / Protected Audience API we have found that it is absolutely essential to let both the publisher (where the ad will appear) and the advertiser (who chose this audience) contribute features to the prediction model. Models where features come from two different sites crosses this boundary where we need to think about ML training where we can’t assume combining two feature sets is OK to do in the clear.

Ben: Vote of interest in the latter techniques (DP-SGD-ish) for feature privacy and label privacy.

Michael: Large range of possible design space worth exploring. Ways to try to do training coming from two places and we don’t allow the mixing of the training data, might be OK to specialize for that. Options 3 and 4 already work, maybe 1 and 2 could be with tweaks. Very supportive of putting effort into that.

Ben, summarizing: Martin is not opposed to the use case, everyone else said they strongly support the use case.  If anyone is opposed to the use case, please speak up!

Brian May: I appreciate comments about multiple perspectives being brought to the discussion.  Important to me to support the whole ecosystem, and to be vigilant about case where someone's background colors their POV.  It's the entire ecosystem, we're all in this together.

Martin: I'm very aware of my biases!  I think there is a process of managing expectations: Nothing that we do here will be as good for the ads industry as having full data about everything that happens.  If the ads industry is expecting performance to be basically as good as before, then they are going to be disappointed.  That would be a terrible outcome: If people are angry that we didn't give them what they think we promised, even if we didn't really promise it, then bad state.  We are going to draw a box, and initially doing something inside that box will be bad compared to today — people have 20yrs experience in the world today, and it will take time to get back to that level of performance with these new constraints in place.

James Aylett: Expectation-setting is worth doing.  We do it inside omnicom, other people should do it too.  The future is going to be different, maybe not as good when we make the change, but it will keep getting better.  This doesn't really fit into the normal working of a GC or WG, but if we can encourage that sort of communication it would really help.

Aram: Chance for anyone to significantly object to Ben's position?

Brian: Support for the use case and providing inputs, but not for constraining how conversion optimization works.

Aram: Consensus: Support for the use case in this group.

Ben: Reasonably good consensus: Everyone but Martin liked noisy labels (opposed on event-level, wishy-washy on use label).  I am disappointed that John Wilander and Apple is not here; I pinged him on GitHub and I am disappointed that Apple did not show to state their position.  I want to know Apple's stance on "Should we support the conversion optimization use case at all?".  Also want to know Brave's position.

pa

~~ 10-min break until :05 ~~


### [Private measurement of single events](https://github.com/patcg/meetings/issues/112) (continue - aim towards alignment in the group)

Charlie:  Talked about Single Event Measurement in the last conversation using the term noisy label.  To reiterate the discussion we can analyze these approaches in the same way that we do aggregate approaches to private measurement. If you’re comfortable with a DP approach with a privacy unit / epsilon in an aggregate approach you should be for a single event approach.  If you’re uncomfortable with the single event approach, then my ask is that you provide a mitigation for preventing this.  Big concern I would have is that we’d spend a lot of time trying to prevent this approach and create a lot of collateral damage for use cases like measuring small slices.  An FYI, I put up [a calculator in Google sheets](https://docs.google.com/spreadsheets/d/1u5HsBiqCrhfq2ul4cwCmtaYV4ojoeAfWjE9Jm60wa9c/edit#gid=0) that is a version of the DP suspicion graph in the slides.  Feel free to copy it and use it so you can zero in on lower priors.  WE talked about how if the adversary has a low prior then typically to bump that prior meaningfully higher, you need a high epsilon.  Conversion rates are a good example, and you can use the calculator to play around with it.

Brian:  Can you clarify what you mean when you say we need to provide mitigeations.  On what?

Charlie:  If we want to prevent querying single events than we need to come up with other approaches.  Shared other examples of mitigations like k-anon.

Ben:  Two thoughts.  Thanks for calculator.  Screen sharing it.  Looking at this, it looks like if epsilon is 9 it is useless. 

Charlie:  Depends on the prior.  

Ben:  So based on the conversation yesterday, if in principle the whole system has a very low value of epsilon than this is pretty defensible. Can’t really learn and can update your priors accurately.  But worry with an epsilon that low then there will be no utility.  Also worry about the composition.  Think we need to analzye the whole system given all the properties – composability, epsilon, epoch, budget definition, etc.  In practice, what could a bad actor accomplish in the worst case.  Would love to see that kind of analysis.  Second comment, fully agree constituent we need to explain this to is likely a regulator so want to prepare us for that conversation.  I think we’re going to have to tell the worst case scenario.  I think we’ll also need to come up with better words.

Charlie:  Don’t think I can give you everything you’re looking for.  The setting in which we’re offering this is to be able to get rid of 3rd party cookies.  Different than the constraints we have in this group where we can tolerate much longer adoption curves and diminished utility.  We need to staunch the wound of 3rd party cookies. Working together we can very likely do better.  For the event level, the epsilons are 14. Originally no epsilon – we just limited info gain through coarsening.  Way we did it in ARA isn’t optimal and we’re slowly trying to tighten it up.  We now have an explainer out that provides for more flexibility that allows you to provide more specific settings and reduce the noise that RR adds.  Think we can dream bigger and provide something more private in this group.

Ben:  Martin earlier said we need to set expectations.  Are you trying to set our expectations that ARA will need to be unshipped in the future and be replaced with something more private in the future

Charlie:  Maybe.  Interested in exploring more efficient designs.  Do think we can support these use case in more private ways.

Marianna:  Are we trying to protect not being able to extract event level for any users.  Or are we trying to protect from doing this at scale?  I’m sure you can do extract info at a user level, but to do it at scale you probably need to kill all utility.

Brian:  Want to throw out my understanding and see if you all agree.  What we’re trying to do is share attributes that describe an event but do so in such a way that doesn’t allow you to identify an event with certainty. The two are at odds – allow certainty and guard against ii. Wondering if we should look at the attributes we’re making available so that it doesn’t matter whether they are truthful because they are so innocuous that we can share them truthfully.

Charlie:  When you say that sharing noisy events is at odds with goal.  The goal isn’t to make any decisions based on a single event it is to feed that event into a post processing approach.  In all case, they will be using events in aggregate.  This is one possible output – there are cases where an aggregate approach will be a better fit for the use case.  Hard to know what is innocuous.  The adversary is the one setting these events.  They have lots of random auxiliary information that could identify a user.  Even a timestamp can be used.  Would require very deep platform intrusion to only release innocuous information information.

Brian:  Totally agree.  Suspect it isn’t possible to traffic in safe attributes and curious if others agree.

Graham: To go back to the earlier point, maybe just using Ben’s comparison between targeting and optimization to sort of explain the difference here, is that helpful? The Event level approach would ever, or at least unlikely to be used to privately support retargeting. Because in order to do that, you would have to add so much noise that you would completely kill utility to use it for user level sort of ad selections. Where it’s ultimately used in an aggregate form something that’s event level could be really helpful. We have to pair the approach to privacy with the use case and that’s how you find utility. 

David: At least as designed today, there’s no protection on the input value.  Google Ads team requested the injection of private state (nee trust) tokens.  How can we distinguish between events that were changed for the purpose of injecting noise vs events that were changed by an adversary trying to mess up the data that an ad tech can collect?

Charlie:  This gets into an important point about protecting an adversary that is trying to inject fake events.  Hard to differentiate between these fake events and fake events injected by the platform.  Very difficult. Pushing more logic into the servers if you assume the servers helps. Even in IPA it’s hard for each party to verify the events imputed and trust the output of from the event.  In ARA, we only support the verification of the conversion event not the impression event. There is some research for how to protect these on-device noising mechanism but become much more complicated.  Will say this is orthogonal to single event measurement. More akin to local vs. central.  PCM wouldn’t be able to support the token based approach if they wanted to have a DP approach.

Aram:  Would like to talk more about process.  Important members haven’t been able to attend all meetings.  We don’t want to block progress.  Martin noted IETF approach that allows for aysnc responses.  Think it makes sense to establish a general explanation on the call.  The document editors can add these to the github.  Then mark it as ready for final consensus and then call it final later.

Charlie:  We’d come for consensus in the next meeting or in github?

 Martin:  We share what we've discussed in an issue, then start a timer.  If at the end of the next say two weeks than we merge the pull request if no objections have been raised.  There are parties that may have information that might change our direction, so we should give them time to share.

Sean:  We can put together a table that allows people to know what’s up for consensus

Aram:  [please document your proposed approach].  People have expressed concern that it’s not worth spending time on a PR if the use case won’t be considered.

Martin:  We should make the PR the document that memorializes the position.

Martin: My suggestion:



1. We discuss something at a meeting, and - if we agree at the meeting - then…
2. We record that conclusion in minutes and in the relevant issue (or open an issue if there isn’t one)
3. That issue remains open for (e.g.,) 2 weeks, after which the conclusion will be considered ratified.
4. Work on changes to a document can start in parallel to this process.  Proposals for changes can happen any time, but making the conclusion concrete is particularly helpful.  PRs cannot merge before the 2 week period ends, but - as long as the change is ready - merging them is the best way to memorialize the decision.

Charlie:  I think in this meeting we discussed the conversion optimization is a use case and weaker consensus on label based approach.  Is this something we want to use this process for?  I will take single event measurement, Ben can you take conversion optimization?

Ben:  Yes, I can write up something about the consensus call on desire to support the conversion optimization use-case. I am also happy to help with the writeup on “private measurement of single events”. Just to express my own thoughts about that topic: there are values of epsilon where single event based measurement in which epsilon value provides a reasonably private output.  And there are values where the output isn’t reasonable.  Very possible there is reasonable middle ground.

Brian:  Would be good to have a list of what’s outstanding and waiting for consensus.  Github labels could work if everyone has a query that can expose them with the level of urgency.

Aram:  I’ll look into a query that can do this.  I think this sounds good and we have an approach for use cases.  WE can talk requirements review in the next meeting.


### Future Meeting Planning

=> 15m


#### [Next Meeting](https://github.com/patcg/meetings/tree/main/2023/06/14-london)

F2F London


#### [TPAC Review](https://github.com/patcg/meetings/issues/116)

Sean:  Able to schedule next meeting far enough in advance. F2F in London at CLoudflare.  At this point we have 7 people who have signed up.  Should have plenty of room.  UK CMA people are planning to come.  We do need your info 48 hours in advance.  On TPAC, we are going to try to do a community meeting and ?.  We are going to try to get slots on Monday or Tuesday, hopefully not Wed.

Martin:  Let’s consider a join session at the privacy CG.  Tentatively agree that we want to get together and then we can figure out which group’s session. 

Aram:  DOn’t want to overlap with PING or Privacy CG.


#### [Times for July, October, and December Meetings](https://github.com/patcg/meetings/issues/89)

Sean:  Do have other meetings that are on the books. There’s a link for the times for july and october meetings.  Lots of meetings in europe, so need to juggle time zones.  So go in there an pick which time zones you prefer so we can lock down and get them in people’s calendars.  Then we’ll think about 2024.  Consider where you want to meet in person.  If you have a place where we can meet without NDA.  I do know lots of people at big companies and we can hit them up.  If anyone has any requests about meetings times/locations let me know.

Aram:  Think that’s everything we needed to talk about for meetings.

Joey:  How does TPAC work?  

Martin/Sam:  What is the extent to which non-members participate in WGs.  You can spectate at WGs, but you often attend but not participate.  This is at the discretion of the chairs.  

Sam: if you’re a member of this CG, you’ll be able to register for TPAC.  If you’re not a member of a particular working group, attendance as an observer is at the discretion of the chairs, and they’re generally pretty welcoming.

Aram:  TPAC website [has information about this and a list of chairs for folks to reach out to](https://www.w3.org/2023/09/TPAC/participation.html#groups) if they’d like.

Sean:  Idea is that you ideate in the CG and then move it over to the WG at some point. 

Martin:  I know others have used this process but I don’t know how they’ve managed the switch over to a WG.

Sean:  Alternatively, join the W3C!

Aram: Thanks everyone.  Please let Sean or me know if you have any question or concerns. 


## ***** QUEUE *****



1. 
2. 
3.  
4. 
5. **QUEUE OPEN**


### [Continue Baseline Requirements Review](https://github.com/patcg/meetings/issues/91)

Note from Aram - Let’s talk a little about process. 


## Participants Day 1



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Lisa Markou (Ford)
4. Jay Kishigami (W3C)
5. Brian May (Dstillery)
6. Martin Thomson (Mozilla)
7. Sam Weiler (W3C)
8. Paul deGrandis (Kevel)
9. David Dabbs (Epsilon)
10. Nick Doty (CDT)
11. Charlie Harrison (Google Chrome)
12. Andrew Pascoe (NextRoll)
13. Benjamin Case (Meta)
14. Ben Savage (Meta)
15. James Aylett (Omnicom / Annalect, first ~half)
16. Xiaoqian Wu (W3C)
17. Don Marti (Raptive) (Raptive is the new name for CafeMedia)
18. Joel Meyer (OpenX)
19. Joey Knightbrook (Snap)
20. Graham Mudd (Anonym)
21. Shivan Kaul Sahib (Brave)
22.  (Google)
23. Caleb Howard (Crain Communications)
24. Phillipp Schoppmann (Google)
25. Andrew Aikens (TripleLift)
26. Rotem Dar (eyeo)
27. Wendell Baker (Yahoo)
28. Ferdinand David (Intentsify)
29. Kyle Hogan (MIT)
30. Nicholas Longcroft (OwnYou)
31. Garrett Johnson ( Boston University) 
32. Vitalie Maldur (eyeo)
33. Alexandru Daicu (eyeo)
34. Christine Runnegar (PING co-chair, part of day)
35. Batiste Haller (Criteo)


## Participants Day 2



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Martin Thomson (Mozilla)
4. Brian May (Dstillery)
5. Ben Savage (Meta)
6. Andrew Aikens (TripleLift)
7. James Aylett (Omnicom / Annalect, first ~half)
8. Paul deGrandis (Kevel)
9. Michael Kleber (Google Chrome)
10. Benjamin Case (Meta)
11. Joey Knightbrook (Snap) 
12. Charlie Harrison (Google Chrome)
13. Wendell Baker (Yahoo)
14. Sam Weiler (W3C)
15. Xiaoqian Wu (W3C)
16. Vitalie Maldur (eyeo)
17. Don Marti (Raptive) (Raptive is the new name for CafeMedia)
18. Batiste Haller (Criteo) 
19. Graham Mudd (Anonym)
20. Mariana Raykova (Google)
21. Richa Jain (Meta)
22. Alexandre Nderagakura
23. Alexandru Daicu (eyeo)
24. Daniel Masny (Meta)
25. Lisa Markou (Ford)
26. Phillipp Schoppmann (Google) 
27. Kyle Hogan (MIT)
28. Garrett Johnson (Boston University) 
29. Nicholas Longcroft (OwnYou)
30. Tammy Greasby (Anonym)
31. David Dabbs (Epsilon)
32. Pasin Manurangsi (Google)
