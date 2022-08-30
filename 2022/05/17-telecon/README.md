# May 2022 Virtual Meeting

The Private Advertising Technology Community Group's meeting will be meeting two days for 3 hours at the same time both days.

## Schedule 

### Day 1 Start 

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 07:00         | 18 Wed | Tokyo         |
| 08:00         | 18 Wed | Sydney        |
| 15:00 (03 PM) | 17 Tue | Seattle       |
| 18:00 (06 PM) | 17 Tue | Boston        |
| 23:00 (11 PM) | 17 Tue | London        |
| 24:00 (12 PM) | 17 Tue | Brussels      |

### Day 2 Start 

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 07:00         | 20 Fri | Tokyo         |
| 08:00         | 20 Fri | Sydney        |
| 15:00 (03 PM) | 19 Thu | Seattle       |
| 18:00 (06 PM) | 19 Thu | Boston        |
| 23:00 (11 PM) | 19 Thu | London        |
| 24:00 (12 PM) | 19 Thu | Brussels      |


## Joining Information

[Zoom](https://mit.zoom.us/j/95356244879?pwd=NDBwZmxleTMwcHFpZG1MZW1tUXhVUT09)

## Agenda

### Day 1 Agenda

**- <= 10m:** Intro, Google Doc, Call for Scribes
**- <= 30m:** [Community Group Charter Changes](https://github.com/patcg/meetings/issues/36) led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)
**- <= 45m:** [Working Group Charter Changes](https://github.com/patcg/meetings/issues/52) led by [@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)
**- == 5m:** Break
**- == 30m:** [Brand and Ad Safety - "Keeping good ads off bad sites"](https://github.com/patcg/meetings/issues/49) led by [@dmarti](https://github.com/dmarti)
**- == 1h:** [Deep dive on measurement use cases and requirements](https://github.com/patcg/meetings/issues/51) led by [@csharrison](https://github.com/csharrison)
### Day 2 Agenda 

**- == 10m:** Intro, Recap Q&A, Call for Scribes
**- == 30m:** [Privacy Principles for Web Advertising Features](https://github.com/patcg/meetings/issues/18) led by [@darobin](https://github.com/darobin)
**- == 30m:** [Collective Governance of Infrastructure](https://github.com/patcg/meetings/issues/40) led by [@darobin](https://github.com/darobin)
**- == 5m:** Break 
**- <= 55m:** [Aggregate Measurement Threat Model](https://github.com/patcg/meetings/issues/50) led by [@eriktaubeneck](https://github.com/eriktaubeneck)
**- == 5m:** Break
**- <= 40m:** Overflow for [Measurement Use Cases deep dive](https://github.com/patcg/meetings/issues/51) and open discussion on measurement topics. 
**- == 5m:** [TPAC F2F coordination](https://github.com/patcg/meetings/issues/53) 

# Minutes

[Meeting Link](https://docs.google.com/document/d/197tQGt2K9mI5zESsTtjoQdg5kt0yZziFKobHRn_zysA/edit)

## Scribes

**Willing (Tuesday):** martin thomson, sam

**Willing (Thursday):** wendy,, [Charlie Harrison](https://github.com/csharrison) (Collective Governance of Infrastructure), Erik (other than Threat model)

## Day 1

### Intro, Google Doc, Call for Scribes

[Read All About It!](https://docs.google.com/presentation/d/1uahuT9ugb79YDEmpcYz3R4ymjCQg1G3S1JfhVpYVFrM/edit?usp=sharing) W3C Policies and Process

**Call for scribes:** [https://github.com/patcg/meetings/issues/54](https://github.com/patcg/meetings/issues/54) 

**Sean:** links to process, process, process

**Aram:** please sign in


### [Community Group Charter Changes](https://github.com/patcg/meetings/issues/36) led by[@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)

**Aram:** introduction to charter.

[https://github.com/patcg/patcg.github.io/pull/6](https://github.com/patcg/patcg.github.io/pull/6) 

**Aram:** unsure about the status after the back and forth

**Eric Rescorla (ekr):** having trouble reading this, in particular provide user privacy with a strong technical basis.  what is the intended meaning of these changes?

**Aram:** the intent is clarification of scope, if that is not the case we have a problem.  Nick D?

(Nick Doty is on vacation)

**Aram:** generally the idea is that the focus is clear

**Ekr:** the substantive change seems to be to add mobile apps to the description, but it doesn’t seem to clarify things for me

**Aram:** noted

**Eli Grey:** I would like to support these changes.  Keeping server-to-server out of scope really helps with the core use cases.  I like that it is scoped to user agents and what users engage with directly.

**Michael Kleber:** The use of user agents to mean something more than user agents meaning browsers, is that something that appears in other W3C documents.  Is this a novel use of the term here?

**Paul deGrandis:** the lack of clarity on server-to-server is not clear to me, some consistency when we talk about server-to-server functionality as it ties in to user facing features.

**Aram:** I am not aware of user agent being used to refer to things other than browsers in W3C, but this is not uncommon in other contexts.  user agents can be crawlers, embedded browsers, and other things.  I  am not sure that the way we say this is clear.  Maybe we can say things that consume the web and interact with users.

**Eli:** Developers have an understanding of user agent, it is also a term that existed before the web.  “Software that you own and represents your interest”.  Say you have a smart assistant, that is also a user agent.  The usage in standards is where this is confused.

**Hober:** Apple just joined PATCG!!!!!!!!!!!!!

**Hober:** It is important for a charter to be crystal clear about the scope of the work.  It helps with people who are looking to join the group.  I heard that this text doesn’t seem to clarify much.  Selfishly, joining the group took a lot of effort and is based on the text.  I don’t want to have to ask lawyers to read the text again.  There doesn’t seem to be a huge increase in clarity here.

**Sean Turner:** Generally in these cases, people suggest text and people rally for or against it.  Maybe they suggest changes.  I’m going to suggest that we close this because there is no movement to support this.  

**Aram:** We don’t seem to have consensus.

**Brian May:** let it stew for some time.

**Aram/Sean:** we can close it.  It’s always OK to come back to it.

**Brian:** I was suggesting closing it.

**Resolution:** Closing PR #6.

Reminder that we created an individual area for proposals.  Related change: [https://github.com/patcg/patcg.github.io/pull/15/files](https://github.com/patcg/patcg.github.io/pull/15/files)

**Erik Taubeneck:** I asked for one of these for IPA.  Hasn’t happened yet.

**Aram:** anyone else who has submitted something that I might have missed?


### [Working Group Charter Changes](https://github.com/patcg/meetings/issues/52) led by[@aramzs](https://github.com/aramzs) & [@seanturner](https://github.com/seanturner)

[https://github.com/patcg/patwg-charter/pull/21](https://github.com/patcg/patwg-charter/pull/21)

**Aram:** any objections to this change … 

**Resolution:** OK, let’s merge it.

[https://github.com/patcg/patwg-charter/pull/14](https://github.com/patcg/patwg-charter/pull/14)

**Aram:** intent to merge in changes to CG charter about collecting CG feedback on work in the working group

(merges suggestion)

**Aram:** responsibility for the WG to collect feedback from the community; will ask the CG for input; CG can do the outreach (not in this change)

**Wendell Baker:** going to +1 Tess “get on with it” (her words). solicitation requires an understanding on what the gatekeeping function is.  will we wait for input.

**Aram:** 4 weeks; in the change

**… Resolution:** consensus on this change

[https://github.com/patcg/patwg-charter/pull/20](https://github.com/patcg/patwg-charter/pull/20)

**Aram:** some comments from Ben about this one.

**Ben Savage:** Brad (Lassey) has a PR that is out for this one and I left a comment recommending a change.  Not sure if Brad updated the PR at the end.

**Aram:** it looks like it has been updated.

**Ben:** Not sure if my recommendation has been taken

**Brad…:** (silence, not present?)

**Aram:** pinging Brad.

**Eli:** wondering why we are redefining privacy and not assuming the broadest definition and listing those things that are not included.  Don’t say these are the things we expect to be private as opposed to exclusions

**Ben:** I don’t think that what you just said is a definition of privacy.  It is more than just that.  This is a pretty broad stroke definition that talks about appropriate processing. Using tracking as a specific example is intended, but broader than that.  Maybe we can include a specific example of things that are not private.  This just allows us to strike down things that don’t fit these very broad things easily.

**Eli:** the list is not big enough, there might be more things we can add

**Brian:** I would prefer not to identify specific things in the charter but instead reference something specific; we will spend a lot of time on debating whether something is covered by the charter

**Ben:** I disagree. I don’t want to waste time on proposals that would enable cross-site tracking.  We won’t reach consensus on those.  We need a trivial fast way to strike down those proposals.  Definitely need something in the charter to do that.

**Brian:** have a document that lists those things we don’t want to allow.  That can include these items.  The charter should be able to encompass all privacy violations and it is the wrong place to specify specific ones.

**Aram:** I think that Ben’s proposal covers that issue.

**Ekr:** We are burning valuable time discussing things that aren’t important.  Propose that we limit the time on this topic.  I am fine with this text and endorse landing, but I will also stop debating if we decide not to.

**Aram:** closing the queue

**Sean Bedford:** in agreement with this. if we are covering mobile OS in addition to web, then we need to include apps when we talk about sites

**Kris Chapman:** OK with this change, however knocking out cross-site tracking is not defined because of things like first party sets.  Cross-channel and cross-device is not clearly in or out.  I would be a little more broad.

**Aram:** having cross-channel might be important, not concerned about getting this in the charter because that is what we will do anyway

**Wendy Seltzer:** the place this has in the W3C process, the charter scopes the work the group might do and that is important to lawyers as well as participants as it scopes the patent commitments that people make; next steps for the charter are to send it to the W3 membership where the AC votes on it.  they too might have comments on scope or other aspects of the charter, which might need to be resolved before it is final. you can have multiple different working groups focussed on different issues or you can have lots of specs in the same WG. goal is to find a comfortable scope that allows progress to be made

**Aram:** some changes made here, but there are still objections; are these charters reviewed by groups like PING?

**Wendy:** there is charter review and then review of the specs as they move toward REC, so PING is very much involved in spec review (FPWD and other transitions)

**Aram:** would s/site/context work for Kris

**Kris:** better, yes.  let it be more of a process rather than relying on it being built into the charter.  that change softens it some

**Sean T:** Does this make the charter unacceptable to new participants?

**Aram: confirming that cross-context is OK (Kris:** yep)

**Resolution:** take Ben’s changes with “cross-context” in place of “cross-site”

[https://github.com/patcg/patwg-charter/pull/17/files](https://github.com/patcg/patwg-charter/pull/17/files)

**Sean:** I suggested this last time and Jeffrey Yasskin has some suggestions.  I think we agreed to this last time, but this is now including details.  Intent is to use the new Living Standard process.

**Aram:** Objections?

**Resolution:** Accepted

[https://github.com/patcg/patwg-charter/pull/18/files](https://github.com/patcg/patwg-charter/pull/18/files)

**Aram:** Not ready for this group.  We’ve asked that this be split or made more consumable for our process.  James (Rosewell) has commented.  Lots of words.  Read it.  Discouraging work on this PR until it is in a more complete state.  Opening the floor to comments on this, not looking for +1/-1.  Any changes that you might like to see out of this?

**Aram:** #18 (or was it #20… it was #20) will be the final blocker, but we are close to taking this to the W3C.

**Erik:** Are we done?

**Sean:** Close

**Aram:** Most of James’ comments are probably best addressed in AC review

Any final comments?

Closing the session for a break.


### == 5m: Break


### [Brand and Ad Safety - "Keeping good ads off bad sites"](https://github.com/patcg/meetings/issues/49) led by [@dmarti](https://github.com/dmarti)

**Don:** To fill everyone in, there [is a new version of ADS.TXT standard from IAB TL](https://iabtechlab.com/wp-content/uploads/2022/04/Ads.txt-1.1-Implementation-Guide.pdf). Let me talk about why this matters. In the time that the ad forum discussion has been happening at W3C, there has been a discussion at IAB space to handle high profile questions about how good ads get on bad sites. There is a standard, there is a link in the agenda item, ADS.TXT standard where a site can say what intermediaries they use to sell on their site. Similarly there is SELLERS.JSON for intermediaries to specify who they work with. Third parties can then look at this and verify. In certain cases, you can identify where an advertisement ends up on a site where they would not advertise. The complementary problem is “how does a bad ad show up on a good site.” As long as good as are leaking out onto bad sites, that creates space for the bad ads. Addressing one helps the other.

The reason I added this as an agenda item was a discussion around Topics API, when the browser takes on the role of placing an ad on a site, should the browser be taking on the role to validate these things that an intermediary typically would.

**Charlie Harrison:** thanks for bringing this. I think this is useful for us to solve. Part of me wonders if this is not a more generic problem of: there exists third party content that belongs/doesn’t belong in certain contexts. There need to be generic mechanisms to make sure they have the security tools in place to prevent ending up on sites they don’t expect. To what extent does this need to be an ad specific API vs a generic API.

**Don:** We have a reputation network that’s built out between ADS.TXT and SELLER.JSON files in practice. When I’m buying some ad-supported content for my user (spending the user’s attention and computing resources), can I use that reputation network that’s already there?

**Charlie:** I think that makes sense to me. How can we take advantage of the existing network that IAB has built. A middlelayer translation from ADS.TXT to the more generic solution could work. This may be a two layered thing we want to do. This group could do ADS.TXT translation, but this doesn’t feel like an ads specific problem in general.

**Don:** If you want to generalize, there are probably other reputation files that could be used. The situation now is that we’re dealing with the advertising use case, and relationships among domains there are already encoded in ADS.TXT/SELLERS.JSON. These files are essentially nodes on a reputation graph, and matching entries are edges. This could be a good first use case for the reputation in the browser you’re talking about.

**Brian May:** I wholeheartedly agree with keeping the ads ecosystem clean and honest, but I think we go to far if we expect the user agent to be a part of that. I think “what is a good ad” should be from the ad ecosystem, and not something the user should need to worry about. Maybe this middleware is something that could help, but getting the browser involved in this could be a huge burden on users.

**Alex Cone:** Two comments. 1. I think it’s really difficult to define good and bad, and having a browser do that is weird. I realize we were spending a bunch of time on charter, but I think this is why. This feels like a stretch for a Private Advertising Technology CG. This is all going to take a long time, and if we go off things that require gymnastics to connect to privacy we’ll never get anywhere.

**Michael Kleber:** Agree with Brian. To be clear, speaking from the browser side, our job is to create a platform that enables the ecosystem (advertisers, intermediaries, etc) to use whatever sort of system exists to accomplish their goals. I fully support a system to do reputation checking, but I’m hesitant to say the browser itself should do that. Looking back at [Issue 61](https://github.com/patcg-individual-drafts/topics/issues/61), one of the examples is the need for the site where the ads API would be used is to be in the ADS.TXT matching up to the SELLERS.JSON. It’s clear to me that this is a best practice across all “good sites.” I remember a time when some boring sites claim to be NYT, and understood why that’s important, but I don’t understand the need for a lower reputation site. As a browser, I shouldn’t be evaluating if there is sufficient adoption of a standard to use the web platform. Second, looking at the details that a browser may do, there are somethings the ADS.TXT standard where the browser should explicitly not follow the standard, and shouldn’t follow that part of the standard that you don’t like. In exactly the same way, the browser shouldn’t be picking and choosing, or be a guardian of this.

**Don:** There are a variety of types of reputation. You call out that not everyone follows everything within the standard (some intermediaries enforce additional checks or do not use optional or controversial features). Some intermediaries that participate in RTB  have high standards, and some have lower standards, and each intermediary needs to take on their own policy. When the browser takes on the role of participating in the flow, they need to set a policy.

**Michael:** I don’t think that’s the case. In the existing proposed APIs, the browser is a place where certain things play out, but isn’t taking any agency away from the parties that act in that. It’s not the browser's place to usurp those parties' decisions.

**Kris:** Use case for ADS.TXT. Two publisher networks. Not just for which are authorized sellers, but creating personalized ADS.TXT to deal with abusive users, who might do bad things to the advertiser. It’s not done widely, but it is one to potentially keep in mind.  (Example from IRC: a personalized ads.txt was given to a user after they clicked through an ad selling masks to leave abusive comments to the advertiser and started harassing other users there.)

**Eli:** Michael and Don covered most of my point. If the browser audits these, you could game the system by attacking the auditors. It will always be detectable who is auditing who. Current IAB standards mostly serve as an enumeration of sites, not a validation of specific behavior. Not solvable without a different paradigm.

**Erik:** if all parties can still participate and verify, that seems reasonable; but if changes such as fenced-frames make that impossible, we might want to consider new middleware as Charlie suggests

**Don:** Express my appreciation to everyone for participating in this discussion, and would like to hear more about the middleware idea from Charlie, perhaps at a future meeting. Want to see how we can make this shift towards in-browser advertising work without taking a step backward in which ads show up on which sites.


### == 1h: [Deep dive on measurement use cases and requirements](https://github.com/patcg/meetings/issues/51) led by [@csharrison](https://github.com/csharrison)

**Charlie Harrison:**

 &lt;Slide presentation titled "Attribution Measurement Use Cases">

**Table of contents:**



* Reporting
* Incrementality
* Optimization
* Third-party reporting
* Cross-environment attribution
* (maybe tomorrow if we run out of time:) optimization challenges & call to action

Main goal is to get everyone on the same page for how attribution measurement is used today — these are all important to some people — so we should probably be thinking about the use cases while we develop solutions.

**Charlie, next side:**

**Reporting: Advertiser insights**.  How much "value" did my advertisements "lead to"?

"value" is defined by the advertiser; could be very heterogeneous, different advertisers have a wide range of definitions.  Could be "purchase" or "site visit" or "sign up for mailing list" or "add item to cart" or more.

"lead to" is also ambiguous.  Ideal would be to capture causation, but really this is more direction about correlation most of the time, and there are complex attempts to do inference on top of that.  Could use basic ways to attribute credit, e.g. "last click" or "last view", but could be a whole ML model whose job is to decide what ad really should get credit.  Lots of complexity hiding here.

Most advertisers are small.  Conversion counting is very important; conversions themselves are rare events.  Hard to aggregate with noise when the things you're aggregating over are single-digit sized.

Large advertisers want to drill down into their data, slice and dice in lots of ways.  They want to build dashboards that let them study counts.

**Aram Z-S:** Can you share slides?

**Charlie:** Maybe later, will take a little work, I'll get back to you.

**Brian May:** Proposals so far have all been last touch.  Is that good enough to start, or do we need something richer even for an MVP?

**Charlie:** +1 to the question!  I personally (as a not-advertiser person) believe that there are attribution models that are way more useful than last-touch, but would be prohibitively complex to implement.  E.g. Data-Driven Attribution, looking at the full database of all events for every user.  Leaving aside the too-complex-to-consider category, do the remaining options beyond Last Touch offer enough benefit?  (Simple things like "first touch" or "linear", “quadratic” places where we can apply a simple algorithm to a record of the user’s behavior ?)  My personal opinion is that those other models are not that much more useful.

**Brian:** Last-touch alone triggers incentive problems, though.

**Ben Savage:** Let me point out that my IPA proposal aims to support different attribution models.  May be that only some things can be supported by MPC.  Structurally it is important to us to let the advertiser have their own methodology, rather than PATCG forcing everyone into one.  Last touch over-credits search ads — when you see a bunch of ads for something, you search for it on Google, click on the ad, and get all the credit.  That's not realistic.  The real goal is incrementality: run randomized controlled trials to actually measure lift for real, then pick the attribution heuristic that is aligned with the result of your A/B trial, and use that the rest of the time.

**Aram:** Would be great to know how many entities are using something other than last touch.  I agree that last touch is not particularly accurate, but that has never stopped people from using something before.  Google Floodlight makes it clear that it works that way, advertisers use it anyway.  How many advertisers would make use of it if something more sophisticated were out there?

**Charlie:** Generally agree that incrementality is the gold standard for causality.  There are some channels that have trouble with incrementality studies — hard to get volume to achieve statistical significance.  Unless you're running a platform that shows 5 ads to a user every few seconds, because they are scrolling through some kind of feed, may not be possible to run that kind of A/B.

**Alex Cone:** "Advertisers" is pretty rough classification here: lots of advertisers spend money pretty indirectly.  The value that people are looking for may not be the end value of a campaign.  May want to spend all your budget well, prove you spent all the money and got some decent outcome, then get more budget.  The people making the decisions may be very far from the folks who are the source of the money.  Regarding last-touch, large +1 to Ben: Companies like Walmart might *like* to be able to do is very far from what the industry makes it possible for people to move forward with, just because there are so many parties who need to agree with sort of currency for measurement to make it happen.  Let's not skew to last-touch just because everyone is "good with it today" — they are probably not, even if they use it in practice.  Don't build the system to the past, it would hurt adoption.

**Charlie:** Would be really useful to have an understanding of what is the preferred alternative (and the "is it doable?" part especially).  Adoption feels like a double-edged sword: it feels like we want to change as few moving pieces as possible in order to get people on board.  If it was hard to get attribution models changed before, then the odds of people changing attribution models and moving to a private system at the same time seems even harder!

**Alex:** If it's going to take a while, and we build something that is pretty constrained, then I fear that everyone will just run to email matching DMPs parading as “cleanrooms”, do all their analytics there, and we get a race to the bottom. Lots of folks turning to solutions that are not as private as it claims on the box. If we take 2.5yrs to build something that can only do one thing, we run a big risk nobody will use it, they will have moved on particularly if it is building to the way things were in the past that no one really liked anyway.  If you build something that is more useful, people will adopt, smart money and large budgets first.  Standards are a long game; if it has bad incentives and only does the thing that's wrong but easy, we're sabotaging our options

**CHarlie:** What is the better thing?

**Alex:** Some sort of multi-touch that allows for querying in a way that makes sense for the campaign you've just run.  Don't close the door on incrementality.  Would be great to get more folks besides just me to speak to this — advertisers, agencies, people who pull the levers.

**Charlie:** We could branch this out into a new Issue

**Aram:** Would be great to bring buy-side and agency people into this group.  It's not too soon now to bring in someone for the next meeting.

**Alex:** James from Annalect (Omnicom Media Group) is here tonight in the middle of the night from London.

**Erik Taubneck:** We are inherently changing the system, even if we keep it last-touch: we're doing something across multiple ad networks here, since it's implemented in the browser, so it is not just re-creating the world we have today.  Today you have to deal with double-counting; here you would only get the last out of everything.  That means we're dramatically changing no matter what.

**Charlie:** The Chrome ARA does mimic the existing world: Attribution is scoped to the party issuing the event, so it does have that same double-counting property, exactly so that malicious parties cannot steal credit.  The platform _could_ do cross-channel attribution, but it has pretty serious risks.

**Erik:** Ah OK.  There are other proposals where all source events are mixed together.  Preferably the advertiser would have control over whether they pool events or not.

**Wendell Baker:** There is no definitive model that everyone will be happy with.  It's like asking "name the best data structure" — it's all about "best for what?"  I worry more strongly that we land on "one ring to rule them all", and then losers band together and say "this will not stand".  Picking a single algorithm is not going to go down well, with companies that sell this service.  I've been on IAB committees where that was the end result of years of deliberation.  It's great to do this learning, but trying to standardize on any one of these may not be fruitful.  The browser has asserted that tracking will stop, that is very defensible; that means we can derive that attribution needs to happen, but within some large set of ways.  Need customizability for those who sell these services.

**John Wilander:** (Yay we Apple are here!) COmmenting on what Alex said about circumvention if we don't do a good job: it doesn't make sense for us to assume that circumvention won't be challenged by the browsers.  We must assume that we are going to prevent regular cross-site tracking.  I think that's what Wendell said at the end also.

**Charlie, next slide:**

**Incrementality / Lift**

We want to do the actual causal experiment — not just whether there was an ad engagement that looks for correlation, but actually run an A/B experiment to ablate the ad campaign, not show the ads in the A branch, look at lift relative to the ads-shown baseline B branch.  There are two complicated things here: (1) Do we need the ability to measure things that are not in front of the user?  I.e. in the A branch, we would need to measure the trigger event by looking at the times where we chose not to show the ad and otherwise would have!  And (2) Not all channels are equally amenable to this kind of cross-channel ablation coordination.

**Erik:** This is not a panacea: running this experiment requires scale, not everyone has it.  This doesn't get away from the conversation above about figuring out attribution.

**Ben:** I think this is an absolutely important use case, one of the most important.  This does imply that for some group who never even saw the ad, we are measuring the total number of conversions.  This is reasonable, just like any other fully aggregated count is reasonable.  We should be equally OK with that whether or not they saw an ad or saw a blank rectangle.  As for malicious parties who attempt to steal credit through various means: Lift is the antidote.  Bad apps that listen for a signal about when an app is installed and try to sneak in an ad right beforehand — that would get zero lift, no matter how clever they are about cheating other metrics.  I'm not sure how to deal with ablation across lots of different channels, I'd like to kick that down the road, because it's hard.

**Charlie:** I hear what you say, but as Erik said, lift is not a panacea — we can't use this as an excuse for not solving security or abuse issues.  We need to serve advertisers who can't run A/B also.

**Ben:** Agreed, just saying that it is really valuable to design a system where advertisers should expect lift is a reasonable thing to ask for.  Google Search Ads doesn't do randomized controlled trials, and this system should be the kind of thing that pressures them to do so.

**Charlie:** Agreed, this is an important use case, useful to get feedback from other browser vendors and whether anyone sees risks here.  If we remove any sort of constraint about this measurement being related to viewing or clicking on an ad, then it is more easily open for abuse.  Need to think about it.


**Martin Thomson**: Say more about security issues? 


**Charlie:** If you have the platform doing cross-channel attribution, with the current constraints we're working under, we wanted this to be adoptable by advertisers and publishers without them needing to lift a finger.  That meant relying on existing third-party relationships on publisher and advertiser sites: things that require millions of publishers or advertisers to do things really hurts adoption chances.  That precludes something where advertisers need to jump through lots of hoops to certify 3p's again — but now that opens the door to malicious 3p's trying to steal credit, like claiming every link is an ad click or every page is lots of ad views.  How do you trust the system?  We could come up with something clever that requires the advertiser telling us exactly what they want, but doing so hurts adoptability.  That tension is why we chose the model that we did in Chrome.  Even if you do trust Google + Facebook + Foo Advertising Company separately, there is still a chance that one of the platforms could get deceived by another in some undetectable way.

**Martin:** I've opened a question on the repo asking about this, I would love more info about this.  Not sure whether you've invented things that make this a harder problem than it needs to be.  

**Charlie:** There is a whole discussion about the priorities of this group  — do we want to build something that gets used, or something that is pure?  I legitimately don't know the right place on the spectrum where we want to land.

**Erik:** In Lift there is an implicit assumption that we have an inclusion of view-through impressions.  There is no contrapositive to a click.

**Charlie:** Definitely meant to cover both clicks and views.  Clicks would only be a fraction of what attribution measurement is used for.

**Ben:** For IPA, the race-to-the-bottom problem, we designed it so that the advertiser is in possession of all of the impression and conversion records.  And you can filter out chunks of those source events — i.e. you can take ad vendor Foo, run the query with all the impressions without theirs, run with theirs, and compare the two.  If all you see is a change in the mix shift, but no change in unattributed conversions, then you've learned something.

**Charlie:** Yup, you have really placed the advertiser in the driver's seat.  I fear that if there are more levels of indirection, e.g. you buy through two different agencies, this might not work — do we need to force them to do everything in-house?

**Ben:** Need to assume the advertiser, or their proxy or delegate, has their interest aligned with the true outcome.

**Charlie:** Definitely — but advertisers now may trust too many proxies, whose interests are mis-aligned with each other.  If we get to a world where any advertiser just trusts a single proxy, then the problems mostly go away.  But if they have many, you may be in trouble again.

**Aram:** Advertisers will definitely delegate to a proxy, and they also delegate to too many proxies, and this causes bad incentives.  Investigations into agency claw-back corruption make that clear.  It would be great if we could clean that up as a result of this.  One outcome that would be very useful is for results to be so consistent that even if they delegate to multiple agencies the results would be the same.

**Charlie:** Let's table this and discuss it in a Threat Models discussion.

**Charlie, next side:**

**Optimization**

**Caveat:** Not an ML engineer!  But I'll try.

What are you trying to accomplish with your ad campaign?  What is value?  Sometimes it is a binary — did they create an account or not?  Sometimes it's real-valued — how much money did they spend?  Sometimes it's a count — how many times did they play the game?

These goals can be modeled as traditional machine learning tasks — binary classification, linear regression, Poisson regression, etc.

How is it done today?  With Machine Learning!  Organize important input (serving-side data about the ad and ad showing opportunity) into "features" — contextual, ad-specific, or user features.  Put these into a big feature vector, label with an outcome: did they make a purchase?  did they sign up?.  Join the features to the conversion using cookies or ADID, train an ML model.  Could be logistic regression; more recently taken over by Deep Neural Networks (DNNs).  Key question of how we can support this use case.

**Erik:** Thanks for the overview.  One part you glossed over is where you use that to allocate the budget: that is often done by the ad network.  Then that propensity is used to adjust the bid.  So there is a need to have that information come to play in the auction.  Also, need those features at the time when you're training the model and when you are using (predicting with) the model.  Without cross-context tracking vectors, that changes the distribution of who has access to what features can be used on both sides.  And finally, sometimes people think of optimization as "campaign optimization" — should I spend my $1000 on ad campaign A/B/C?  Let's be clear that we're talking about "conversion optimization", where you're using it for bidding adjustments — make the best bid for any given time and any given user.

**Charlie:** Not all signals may be available in the future — e.g. using a 3p cookie to get demographics for the user, might not be known on all sites int he future.  Also some info might be known only on a server not in the browser.  Right now I'm making a simplifying assumption that most features are available in the contextual information that we know at ad serving time.

**Paul deGrandis:** Sometimes this turns into a multi-objective optimization problem.  Might not just be optimizing for clicks, maybe for revenue at the same time.  This complicates things.  DNNs are indeed a trend here, but simpler methods (random forests, boosted trees, regression, Shapley models/SHAP/LIME) are coming back, for explainability reasons.  Also coming up is Federated Learning: sharing data across multiple parties, esp if you're in Chrome and doing the auction in the browser, or in a multi-party relationship.

**Charlie:** Also relevant for the MPC case, which is in a sense very low resolution federated learning with only two parties.  Overall, multiple decisions, and how can we optimize for all of them?

**Eric Rescorla:** If we stipulate that these are things that people want to do, the question is how we can do them with appropriate privacy properties.  If you locally DP everything, then you get bad performance.  If you FL things then you have to push a lot of the structure of the model to the device.  We really don't know how to do this.

**CHarlie:** I have some slides!  But they will agree that we don't know how to do it.

**ekr:** One thing if we can do logistic regression, another thing if the client needs to know the structure of the model.

**Charlie:** Let's go through the queue and get back to this?

**ekr:** What I'm trying to get to is, is this problem ripe for us to work on?  Can we work on aggregate measurement first, and come back to this later?  We're not trying fix the problem today, we're trying to figure out what lines of attack to work on.

**Charlie:** Even if this is out of scope for V1, let's not pick an architecture that makes this really frickin' difficult in the future.

**Brian May:** A lot of this can be done using contextual and 1p-data channels.  Do your models lose significant value if you don’t have cross-context data?

**Charlie:** That feedback would be very valuable.

**Paul:** Kevel only deals with first-party data.  You can be removed from the data and still train the models.  You still need FL (or some other privacy-preserving technique) to share data/context that you haven't been able to see.  We don't use any cross-context stuff on the models that we train.  Also Amazon has switched to only using first-party data across their own channels, no non-Amazon properties involved.

**Mariana Raykova:** Since I heard Federated Learning sometimes: recall that FL requires sending the models to the device.  Are we OK with that?  From the proprietariness point of view?  And are the features all known to a single party, or are they known to multiple parties who can't share them?

**Charlie:** There are certainly some features that are agnostic to publisher, like time of day.

**Erik:** Sometimes model architecture is proprietary, but that probably isn't a show-stopper if that [a proprietary feature set] is not possible.

**John Wilander:** When we look at this and think about privacy preserving things, we are not just interested in something that you can define as technically private based on aggregation or some amount of data, but also looking at outcomes.  The more we recreate things that happened with 3p cookie data, the more we're moving away from privacy.  This whole line of pursuit is using AI to change people's behavior.  This is a dangerous path.

**Charlie:** There is a spectrum of creepiness of learning tasks.  There is "I've tracked you, John, and I really know what you want to buy" and there's "our models tell us to sell the flowers a week before mother's day".  There is benign and there is harmful learning.  Ideally we would craft out solution so there is not a lot of harm.

**Brian:** What do you mean by outcome, John?

**John:** Getting to privacy means we are not trying to create a drop-in replacement for everything we could do using 3p cookies.  The web needs to change.  People need to perceive it as more private.  The outcome needs to change.  People need to feel like it's not creepy, like they are not being manipulated, all these things that we are talking about.

**Andrew Pascoe:** Data Science team focused on algorithmic bidding.  We break data down into three categories: contextual data (what is the page about, how big is the ad slot?), ad features (historical performance), and user data.  I understand John's point about creepiness, but user data does span a lot of things: includes "they have been very engaged on the advertiser's site" or "they added these particular items to their cart", or "number of times they have seen this ad already" or "how long has it been since they've been to the site?".  Maybe useful for this conversation.  I wouldn't say that a lot of the performance comes from the context alone — it's important, but only works in combination with user features like time since site visit.  I don't think that it's creepy to determine the price of an ad.  Generally speaking, what we would be looking for: fine to execute some training code to generate a model in some kind of private server, where we don't have access to the data.  If we want to have all these different modeling capabilities.  Should be sufficient to represent features and outcomes as a matrix.  But data scientists do frequently look at the data going into the model, to be sure the model training is doing what they expect!  Maybe we could get away with looking at synthetic data based off real data, to see if we can tell the value of adding a new feature — maybe we don't need access to raw real data — but this is an important part of the process.

**Charlie:** Synthetic data might well be useful.

**Eli:** There was a question about what you get if you don't have any cross-contextual signals.  There was a Google study from 2019 that said 52% loss on average.

**Charlie:** That's a good topic.  User features do seem to be important.  I think it would be good to rewrite this categorization of features into what would or would not be available.  This 52% was used to justify some of the targeting signals features, like the FLoC or Topics API — we took this signal that used to be done with cookies or ADIDs and distilled it into something on the more private side.  We should think about what things might be available as user features even post-cookies.

**Jonasz:** I was going to describe our signals, but let me just build on what Andrew said: important for our models to build on contextual + user behavior on advertiser site + previous exposure of this ad to this user.  These are super important areas.  We need to optimize or train with respect to all three feature groups.

**Aram:** I'm glad we have another 45min dedicated to this tomorrow.  This is a good core conversation to have more of.  I personally won't be able to make it to the next session, but I look forward to reading up on the notes.  Charlie for last words?

**Charlie:** Not much else left to say about the use case.  A few slides of more challenges on ML learning that I've been pondering, or whether we should continue the use case discussion.

**Aram:** Too late to go to another slide.

**Charlie:** This is a hard problem.  Telegraphing my conclusion: I don't even know how to solve this *classically*, not even in an MPC or TEE environment.  It's an important enough use case that we should dedicate research time to it, solicit help in the group and in other groups in the W3C, to solve this problem in the long term.

**Aram:** Happy to solicit contributions from other groups.  See you here (same time, same Google Doc) on Thursday.


## Day 2


### == 10m: Intro, Recap Q&A, Call for Scribes

[Read All About It!](https://docs.google.com/presentation/d/1uahuT9ugb79YDEmpcYz3R4ymjCQg1G3S1JfhVpYVFrM/edit?usp=sharing)  W3C Policies and Process\

**Sean:** Martin’s PR regarding cross/site, cross/context. [PR 23](https://github.com/patcg/patwg-charter/pull/23). 

Any objections? Hearing none, merging.


### [Privacy Principles for Web Advertising Features](https://github.com/patcg/meetings/issues/18) led by [@darobin](https://github.com/darobin)

**Scribe:** Erik Taubeneck

**Robin Berjon:** Aim to go quickly through the privacy principles. Don’t have a lot of slides for an hour. Happy to shorten if there isn’t significant discussion. 

Return to Garuda after covering privacy principles.  TAG has been working on privacy principles to ground work happening elsewhere. Task force has agreed to publish a first public working draft. Not final, but enough to engage with. Encourage folks to look at the source document. Now would be a great time to pay specific attention to this document, goal is for TAG to enforce this in reviews.

**Sean:** Calling out that you’d like to have people look at this.

**Robin:** There are changes to this on the agenda.

Two things worth noting. THis doc is in TAG, best place for feedback is in TAG. This doc is meant to apply to all of the web. There are some specific advertising. Encourages people to be cautious around consent, respect people’s autonomy. Can specialize that document in our context. There are cases where this group by want to poke some very specific holes, that’s what building these purpose constraint APIs are, will call them out, and say why they respect people. I believe our doc will be short (I hope.) 

The way we approach privacy is the state of information flows, and power over those flows. IT’s our job to rectify these asymmetries of power. People come first. Start from the idea that privacy is contextual, contextual integrity is used. Privacy is collective. Shouldn't have it managed just by people. Groups can make decisions and can be affected.

Questions? Interest in reviewing this doc?


### [Collective Governance of Infrastructure](https://github.com/patcg/meetings/issues/40) led by [@darobin](https://github.com/darobin)

**Scribe:** Charlie Harrison

**Robin Berjon:** Discussing GARUDA and governance. Context to explain. We can’t be sharing data to random third parties on the internet. We need to be developing for a bunch of reasons (priv principles). User agents need to be good at data protection. Core mission.

This has implications in terms of architecture. Can’t follow today’s practice of giving data to services. Studies show this. Enforcement is easier if there is less craziness. Stop “race to the bottom” for publishers. Not great for an industry trying to produce trustworthy content.

How we get a trustworthy supply chain. Current system is predicated on the fact that pubs should be subsidizing clickbait farms, we can’t accept this.

Can we do things on the client? There are a few things we can’t do purely client-side. Aggregation is more difficult to do on client. Architectural concerns about too much ad-tech functionality in the browser. Browsers have to be maintained at a high level of quality, indefinitely. Browsers compete on user experience. Infra supporting ad-tech is not rewarding for browsers to work on (esp for browser vendors that dont own an ad network / ad revenue). The more complexity in the browser, more trouble we are inviting for bitrot, low qual impl. Worry about excess complexity there.

**EKR:** Are we jumping in? Not sure on the right hand corner is our problem (good shouldn’t subsidise the bad). Not our problem. Not disagreeing. Not the appropriate topic for standardization.

**Robin:** the reason the point is there, it is often said if you don’t send data to third parties, you “destroy open web”. This is a concern for standardization. Little evidence that “long tail” sites will be harmed by more privacy preserving environment. ALl points go in the same direction, need better privacy in the browser.

**EKR:** This is not an empirical claim, it is a moral claim. Reason not to have data sent to third parties is not this.

**Robin:** This is not the basis of our work. The opposite is being used to criticize our work.

**EKR:** You made the empirical claim this was irrelevant

**Robin:** No, I said there was no evidence that the opposite claim was true, no reason to believe one or the other. Let’s move on though, if you agree with the 5 other reasons, I don’t think you should be concerned about the 6th.

**EKR:** The conclusion of the preso should be “don't send data to third parties”, not about these claims.

**Robin:** If you can’t do something on the server, and not on the client, where do you do it. Landed on “Trusted server”. Lots of proposals that use a trusted server. This shows that there is an interest in the idea of trusted servers doing things. Not familiar with the details of every single one, but they say things like “if the server is trusted, it’s ok” but not why the server should be trusted.

There is clearly lots of discussions around trusted servers. Should figure out how they work. Sweeping under the rug. We’re looking for infrastructure. What are the issues with infrastructure? Standards themselves are infra. This is a step beyond. Provides actual live services. Needs a few things

* Money. Provision is always a key problem. Everyone thinks someone else should pay. End up with 60% of bridges are structurally damaged in the US. Universal problem
* Neutral. Subtle point, but important. Any infra will embody values, but need to be careful about the infra shaping users. At scale, leads to negative effects, lose positive externalities. Should be as “dumb” as possible.
* Capture-resistant. Don’t want 1 party to have excessive power. Much more active defense needed. Can be technically centralized but collectively governed.
* Commons. Lots of lit supporting the “commons”. Open access system, that provides guarantees of sustainability / trust.

**EKR:** tragedy of the commons?

**Robin:** that is a cliche, lit is definitive against this

**EKR:** this is a debatable point. This is not definitive. We should note this is contested

**Robin:** OK to note contested, but does it impact downstream decisions?

**EKR:** Yes it does

**ErikT:** When we were discussing IPA, idea is the browsers would have some set of trusted pairs of servers, and the ultimate end user of the API would buy that service from one of those pairs. Pairs are not unlimited, manufacturer needs to trust them not to collude, but probably not one pair as a public service. Optionality / market.

**EKR:** this is what I’d assumed as well, not my take home from this slide.

**Robin:** These are not contradictory. There are commons options that include pay-for-service. e.g. toll roads. Doesn’t prevent commons management that governs the road. Commons can govern markets.

Erik’s point of markets and separate entities can also be organized as a commons.

**Erik T:** Did not make the point to object, just give context for how we are thinking about it.

**EKR:** table until we see what commons means in this context.

**Robin:** Who can you trust? Enter GARUDA. Put together an institution to govern. Not a competitor to any other system that can make guarantees of trust. Meant to complement. Can work with other systems to make guarantees those systems are unable to make.

Entity can shepherd standards, drive consensus, takes stakeholders directly into account, manage OSS infra.

Power structure is balanced, multiple constituencies, each representing their own part of the market. They each have a third of the board seats. Set this up such that

User agents, speak for the people (need to make sure that’s true). Area of discussion

Publishers. Sell-side

Buyers, putting money into it

Does not include ad-tech intermediaries are already working for at least two of these groups, don’t need to be represented. Have concerns that 4 constituencies will lead to deadlock / alliances that could derail the system. Meant to balance power.

Balance is implemented through a number of features / approaches.

1. Values framing org. How you succeed in resolving debates

2. Threshold eligibility. Don’t want every blog out there to add an extra vote. Don’t want orgs to break up to flood things.

3. One company one vote.

**Brian May:** How are regulators and users going to be represented here?  One step removed via user agents? 

**Robin:** People are represented by the user agent. The way we implement this is open for discussion. We can build a regulatory framework. Aligned with what most user agent frameworks describe, can extend beyond browsers. How to make browser work in the person’s fiduciary interest is TBD. None of this can be illegal, by nature. If regulators want to intervene, they have access to their own legal framework.

If we do put this together, might be useful to support a small policy function so it can be explained to regulators, so we get a smooth worldwide privacy ecosystem. Down the line concern.

4. Only one board seat across constituencies, you have to choose.

5. All work in public

6. High impact decisions need supermajority (any constituency can veto). Prevent alliances.

7. Participants need to register. Need “KYC” (?)

Features exist that support this form of governance.

Funding is an issue. There is money in advertising. This might be a good source of funding for ad systems. Don’t want to overthink how fund this. What type of infra impacts funding (IPA vs. PARAKEET). Multiple ways of doing this. We have options.

**EKR:** Misunderstood. I thought you were talking about CABF (Certificate Authority Browser Forum, https://cabforum.org/). You seem to be thinking of a monolithic entity. A single system funded by this mechanism

**Robin:** Yes that’s correct.

**EKR:** Institution?

**Robin:** Set of rules with a legal entity / governance.

**EKR:** Is CABF? 

**Robin:** I suspect it is of some kind, not familiar? \
**EKR:** IETF?

**Robin:** Yes.

**EKR:** IETF requires a tiny amount of money. Running these services are expensive. I can understand collective governance. You seem to be assuming this is actually funding the services.

**Robin:** What I’m presenting is a toolbox for dealing with these issues, not prescribing a specific arrangement of tools, way to support this. If we need trusted servers, we need some governance, going to need to agree how to fund them. Lots of options for funding, setting rules, directly funding, etc. All options on the table. What I’m presenting is possibility. Explaining the toolbox is important. These are the decisions we need to make. Funding is possible and we have options, exact modality of funding will vary depending on what we support and decisions we make on what is appropriate.

Principles come into tension. “Wide open market” vs. “centralized thing”. Not sure if either extreme is the best.

**EKR:** Thank you

**Michael Kleber:** I’ve been heavily involved in proposals with trusted servers. I think I agree with EKR in that, Robin you’re bringing two things together where there might be benefit in pulling apart. A lot of the discussions about TEE vs. MPC e.g. have focused on “how can a browser be confident that a server is doing what they are supposed to do”. Each proposal has different mechanism.

Separate from that, “what is the OK things that the trusted servers ought to be able to do”. Huge benefit of GARUDA that we don’t have any other discussions to address is how do we make the decision of “what are the acceptable uses”. Collective governance model coming to a unified answer seems like an outstanding idea.

Q of “how do we turn that decision into what is OK into servers that do it” could involve the model described here. Same organization. Or could involve lots of other technology / organization (TEE, MPC), how a browser trusts this thing, has desired properties.

Description of the agg service proposal in Chrome’s Attribution Reporting API has 4 different parties, someone writing code, someone else verifying build, someone else doing cloud infra, someone else using the server and paying for it. [https://github.com/WICG/conversion-measurement-api/blob/main/AGGREGATION_SERVICE_TEE.md](https://github.com/WICG/conversion-measurement-api/blob/main/AGGREGATION_SERVICE_TEE.md) Sidesteps some of the funding issues. Really important to pull these things apart.

It would be great to answer what is OK to do.

**Martin T:** Going to disagree with Michael on this one. We have a giant box with inputs / outputs. Want to trust it isn’t leaking anything. Part of the job here is defining inputs / outputs. Governance pieces here are closing the gap between theoretical definition and operationalizing (writing of code, audits, etc.). That’s where governance falls to me.

What the system should do is not the business of a body like that (though it may be). There is a decision making process “what are the goals of the system” we are sort of having here. Talked about differential privacy, what is the epsilon? That’s a policy that’s critical. Don’t know where that decision will be made. Suggest that it happen here rather than somewhere else (if it happens at all, e.g. if ppl decide for themselves). Gov structure closes the gap between the thing we design and its operation. Funding pieces, systems we need so we can trust the services in how they operate. Input/output not in scope.

**Robin:** I think I almost agree with both of you. Sounds impossible :) At the conceptual level separating “what is done” with “how it is operationalized”, something for me to think about. Who decides the “what”, I think there’s a discussion about staying in standards or shifting. Possible it could be a bit of both. Not crazy for browser stuff to be in PATWG. Things that are standardizing operational aspects in the other org. Where we put dividing line isn’t important, though we have to decide.

On the other piece, the “what” vs. “operation” is important to distinguish. Can’t separate them though. can’t decide on “what” unless we know the operation. Everything depends on what we can audit, enforce, etc. These are coupled in both directions. Hard to split, institutionally.

One side says “We do TEE system”, but operational side says “not possible”. how to reconcile? The two questions are intricated somehow. Doesn’t mean everything needs to be monolithically controlled. Whole bunch of options. Don’t think we can splinter these two though.

**Brian May:** Risk of complicating things more than they need to be, there are 3 constituencies.

1. What we want the system to do

2. What the system are allowed to do

3. People who run the system

**Robin:** 3 constituencies I have are ones that debate what we want and what we can do. All direct the operational arm.

**Brian:** constituencies is the wrong word. There is tension between the people in the system.

**Robin:** whole thing revolves around tension.

*Next steps:*

this is a toolbox, things we should be thinking about. No next step unless there is a system to govern. If we have confidence that yes, some of those things are things we’re going to do (ed: trusted server), plenty of discussions we will have. We should get started. Otherwise I’m not going to be pushing this until there is something that needs it.

**EKR:** “We” is doing a lot of work here. I don’t think W3C is a good group, even though it may end up being some of the same ppl. 

**Robin:** Which group?

**EKR:** It will involve lawyers . As michael was alluding to, many things this hypothetical group will do are non technical. Legal ramifications. If Mozilla would be part of this group, not me or MT. It would be ppl we send to CABF. I agree we need something like this, not sure what there is for us to do.

**Robin:** Precedent to convening lawyers in standards groups. The important thing is to have basic consensus structure to get this thing off the ground. Wouldn’t do it in PATCG with PATCG ppl. Could be a splinter group. Don’t care how it is organized.

**Brian May:** You mentioned picking an impl to work on. That raised in my mind how to do that, given we have at least 2 flavors of attribution servers that want aggregators, and helper servers that want impl.

**Robin:** Don’t want to decide for myself, group discussion. Let’s say we know as a group that we are looking at attribution, all remaining require a similar server arrangement. THen we know we will need this, let’s get it running. If we still have 27 things that need some server, can’t move on that reasonably. Decision to be made as soon as we know we need one of these. No sooner.

**Wendy:** Thanks Robin, modular architecture. Useful to think about governance of this thing and systems where this thing is needed and in which group it could be specified further. W3C as successful and unsuccessful attempts at the untechnical. Doesn’t mean we should throw out the attempts.

**Robin:** Didn’t mean to imply either way W3C or not. Could imagine where we convene ppl with W3C mechanisms. It’s what we have and is convenience, splinter it off once it is off the ground.

**Michael Kleber:** Robin said there is no need to do this sooner than when this group needs action. An example of a place where this body could be useful is “FLEDGE” proposal that we are experimenting with ads ecosystem. It does involve a server. Server is specified as a Key-Value server. Browser sends keys, server does lookup with value associated with key. Used for on-device bidding. Simple API for what server is supposed to do. Privacy properties: as long as server does not keep request logs (or cannot log, e.g. priv info retrieval), then it succeeds at not leaking information.

However, there is a policy question. How is it acceptable for how server produces values. What info can server use? In the design for FLEDGE, every key has to be independent from other keys. When you place a person into an interest group, bidding involved in choosing how much to bid, is based only one interest group, not all IGs the user is in.

That means that ad targeting in the FLEDGE model is based on what a person did on ONE website, not something based on a web-wide browser profile on many different sites. Policy decision. Following the “MT principle” of “let’s do the simplest thing that is most likely to launch and agreeable to most parties off the bat”. Kick down the road the question about ML / cross site data. Can’t answer right now these additional capabilities. Don’t know what the boundaries should be in a moral sense. This is a question about what shows up your screen, even if nobody learns anything about you. This group might be the wrong group. I’m surely not the right person. We need a group with multiple constituencies, closer to a group that can answer this.

**Sean:** summarize. Everyone should review privacy principles in TAG. Do think those principles will inform our work. Second part: discussion will continue. Still need to figure out more, get everyone on the same page. Ability to keep talking, use github issues / PRs.


### == 5m: Break


### [Aggregate Measurement Threat Model](https://github.com/patcg/meetings/issues/50) led by [@eriktaubeneck](https://github.com/eriktaubeneck)

**Scribe:** Wendy Seltzer

**Erik:** separate discussion from use case.

**Goals and anti-goals:** We can’t get all the way to threat model or debate all the specific tradeoffs/implementaitons/parameters.

**Goal:** get some editors, bring a draft to the next session to prompt well-defined conversations. 

Where should this draft live, CG or WG? 

**Sean:** the WG won’t be around for a while yet, so start here. We can always move it if needed

**Wendy:** thumbs-up.

**Erik:** Outline. Aggregate measurement scope. Actors. Actor capabilities. Security goals. Privacy goals. 

**Scope:** [diagram] 

**Actors:** [slide] We probably want to consider leakage from malware, corrupted software. Can it corrupt the results of the aggregator? 

**Charlie Harrison:** One more potential actor. In TEE, we’ve described “Coordinator”, someone other than operator or tenant, who verifies the code that runs in the TEE.

**Erik:** thanks, want to get other actors we want to consider

**JohnW:** do you consider fraudulent users among “users”? 

**Erik:** Yes, we want to consider users potentially acting fraudulently. Users and bots pretending to be users. 

**JohnW:** users real and malicious

**Brian:** Agree, breaking that out would be helpful

**EKR:** TEE vendor is a relevant actor; they could make fake TEEs. 

**Erik:** TEE vendor, potentially CA. 

**Mariana Raykova:** re whether users can be malicious actors. Are we scoping with respect to privacy, or correctness of computation? 

**Erik:** think we should discuss that a few slides ahead, with security goals. Thanks. Would you add a different actor? 

**Mariana:** How we think about the user and the potentially malicious actors. 

**Erik:** Slide, Actor Considerations. The assets that actors can have, the secrets that should remain private or could enable attack. Capabilities, attacks. Collusion capabilities. Collusion risk. Some discussions assume that source and trigger are likely to collude. Also risks depending on setting. Think explicitly about which parties we assume will (or might) collude, where we trust that parties won’t collude. 

**JohnW:** We typically talk about 3 Cs: Curious actors, Compromised (e.g. hacked), and Compelled actions (e.g. compelled by law enforcement). Would governments be an actor here? 

**Erik:** If we want to take compelled action in-scope, we want to consider the capabilities of the government actor too. 

**EliG:** Also think about client-side tools that might intercept ads, delay attribution reports. The tool the company I work for makes, we quarantine ads and replay them later & will likely integrate with these future APIs. 

**Erik:** I’d put that in user-agent, but should we call out separately?

**EliG:** useful call out if there’s different API surface, like client-side site-level. Extensions and content-level code could apply restrictions. 

**Erik:** thanks, good to have in the notes.  

**CharlieH:** Do you have any thoughts on how to scope capabilities? My concern with formal threat model is we get into situation where a bad site is using a plethora of other web plat features including ours, and they’d get almost as much as using ours. How do we scope to look only at the “diff”- between the target web and what we have today? 

**Erik:** I’ve been referencing the [ threat model on the PPM spec](https://www.ietf.org/archive/id/draft-ietf-ppm-dap-00.html#name-threat-model). That’s a good place to start. I welcome input. 

**Charlie:** Let’s try, even as we recognize it will be challenging. 

**BenS:** I tried to write this down and hit the same problem. Strawman proposal: write down an idealized model of a browser, super stripped-down, that goes to idealized privacy model for the web. Consider that idealized browser with and without this thing. 

**Charlie:** how should this work relate to target threat model in PING? 

**Ben:** could be. A world where there is no cross-site recognition, etc. and then add one new feature. 

**Mariana:** We may end up defining some nice ideal functionality, then to meet utility requirements, find ourselves challenged to analyze output. Spend more effort to compare with existing model. 

**EKR:** Agree it will be difficult to scope out privacy implications of new things. I’m less sensitive to “the web is already terrible,” because that leads to doing nothing. I start from perspective, if the browsers did all the anti-tracking stuff in the works, then add this,  how much worse is it? 

**Brian:** How much concern should we have for integrity of overall platform? As we focus on threats to privacy, also consider threats to validity of impressions, other attacks on ecosystem? 

**Erik:** A bit of that on next slide, back to Mariana’s mention of correctness of result. 

**Charlie:** we’ve already thought about this in context of target privacy threat model. We might need to scope down adversary’s capabilities to get to possible. Suggest we review [Target Privacy Threat Model](https://w3cping.github.io/privacy-threat-model/) to see if we want to start there? Or tighter scope. 

**Erik:** I’d like to get some volunteer editors. That seems like reasonable place to start. 

**Mariana:** maybe bare minimum is to say whatever we compute here cannot be used to recover 3d-party cookie behavior. It’s not obvious to me that we won’t end up back there. Don’t think that’s trivial. 

**Erik:** Slide: Security Goals. Broken out from privacy goals. Security: we should only be able to learn what we say we’ll learn. Some references. 

**Charlie:** there might be value in describing some security goals as spectrum, rather than binary. E.g. this might be possible, but mitigated by lack of incentive. 

**Erik:** don’t feel strongly. 

**Brian:** we need to work iteratively, once we have more to discuss. 

**Martin:** Agree with Brian, it’s abstract until we have more concrete detail in building a system. Understanding the things we need to talk about, as an issue on the threat model, until we have something concrete. Don’t need to make this perfect before moving on. 

**Erik:** My hypothesis is that we’ll get 90% without much controversy, then need to find and argue about the remaining 10%

**Brian:** if we get anything wrong, plenty of people will point it out to us

**Erik:** Slide: privacy goals. Some will come from Privacy Principles doc Robin presented. Diffs will include some terms relating to measurement, parameters. 

**Martin:** I’m not sure this is the space we want to talk about specific privacy goals. Economic incentives, and also worst-case scenarios. How a system works when twisted against the interests of those participating, not just when participants behave honestly. 

**Erik:** once we have a use case, there’s probably more threat modeling that needs to be done. 

**Martin:** task some people to start the work, add to this slide

**Charlie:** You describe some properties of a system. We should mention specific threats we want to block, what properties would help neutralize these attacks. E.g. for economically motivated threats, where it’s useful to have a profile, explain how privacy e.g. k-anonymity prevents that. 

- **Re privacy grain, we should discuss later:** over infinite time, infinite data leaks; we need to discuss that. Probably a separate doc. 

**Mariana:** privacy grain probably relates to adversaries, scope. Which definition is relevant ties to the adversary model, e.g. worst-case adversary, DP. Think about parameters, what does epsilon value mean, more concretely. 

**Erik:** when dealing with infinities, concerned about how fast it grows. 

**Charlie:** want us to be clear that we’re talking about rates of leakage, nothing in absolute. 

**Erik:** So, who wants to volunteer? 2 docs or sections: privacy goals and threat model

**Mariana:** I’m not convinced security and privacy goals are separable

**Charlie:** think we can start with the building blocks in one doc

**Brian:** I’d recommend we think about them separately

**Erik:** Volunteers can choose how they work!

**SPT:** Contact Erik if you want to volunteer. 

**Erik:** or add yourself to the open issue that heads this agenda item. 

[some volunteering in irc: MT, Charlie, Erik]

### == 5m: Break [return at :06]

### Overflow for[Measurement Use Cases deep dive](https://github.com/patcg/meetings/issues/51) and open discussion on measurement topics.

**Scribe:** Ben Savage

Sensitivity of the system scales with the max contribution per user. Hugely important for private ML. 

**Criteo PPML challenge:** 

* 190 total features
* 190 total buckets that one user’s contribution was added to.
* Histogram with 190 total buckets.

One winning solution implemented logistic regression where they used the aggregates + the labeled panel.

They bounded the sensitivity of the user by the L2 norm. That leads to noise that gives you differential privacy guarantee of ??

If you bounded by L1 sensitivity, the effective noise would have had a STD of 243. Almost 15x more noise. This is because the L2 sensitivity takes advantage of the structure better. You limit the contribution of the user. If you have a less structured sensitivity, you’d need to add a lot more noise.

Being able to manage the sensitivity leads to much less noise.

With gradient updates on a huge ML model with tons of parameters, if you add noise to provide a differential privacy guarantee, the noise scales with the sensitivity of the gradients. The noise could grow out of control. In a lot of the ads ML gradients there are sparse features. Maybe if we have a sophisticated system that allows us to place constraints on the contributions we are adding we can add less noise.

If you have conversion values (label). Sensitivity issue still holds. You have to add noise proportional to the largest possible contribution. 

This is a really important consideration.

Turns out delay is also very important for training tasks. Recent reports are much better at predicting the current reports than past reports. 

Recency is really important. A lot of proposals introduce delay. Sometimes delay is imposed on the API itself. Too much delay can destroy the training utility. 

**Erik Taubeneck:** Agree with this point. This was a design consideration with IPA, although this only addresses one type of delay (the automatically added one).

**Charlie Harrison:** I agree. An aggregate system where you just have to wait for enough reports is a good approach. If we want this to be private that’s the minimum thing we need to tolerate. 

**Tim Geoghegan:** What order of magnitude of delay is a problem? Your example of months… How about hours? 

**Charlie Harrison:** Gut feeling is that a delay on the order of 1-day is where we should be trying to hold the line. More than that is not awesome. If it’s much longer than that (week / month) you get into these cases where it’s obviously different. 

**Tim G:** This has an impact on the report collector. Tradeoff on fine-grained vs. delay. This is a knob vs. something to solve.

**Charlie Harrison:** Totally agree. Systems which allow the user to make a choice are better.

**Joel Pfeiffer:** What is in real-time? Are the features in real-time? Or is the model trained on real-time? If you trained on 30-days of data… Varies. How you featurize matters.

**Charlie Harrison:** This slide is about the recency of the data you can use to train. Realtime features are also there.

**Joel Pfeiffer:** You can think of models like a calibration layer and you can accept a longer delay. Features should be more immediate. You have a query with conversions. You want that to be recent. You want to keep counts. That model’s label might be 30 days out into the future. 

**Paul deGrandis:** It’s typical to do this training up to 24 hours prior, then factor in recently thereafter. The other sneaky trick is that last year on the same date matches today modulo some shift. If you know the shift from yesterday you can apply that. In cases where a model is stale we can utilize this old data. 

**Charlie Harrison:** Maybe we have tricks to mitigate reporting delay. 

**Andrew Pascoe:** I kind of agree about taking 1-day as the limit where we want to be. Paul and Joel both said accurate things. But the thing is, we constantly have new advertisers and campaigns coming onto the system. Incorporating them into the data-set and into our models. It’s OK to talk to a client and say: “We will start running you campaign and it’ll take a day to learn…” Another thing about reporting delay is making sure the campaigns are spending correctly. A misconfiguration can blow through a budget quickly, or maybe you aren’t spending at all. Now we need to wait another day to see if it works… Might be worth separating out the categories of use…

**Charlie Harrison:** Near-realtime for budgeting / pacing is important. We build the event-level API specifically to support the ML use-case and it fails due to delay. 

**Brian May:** Budgeting and pacing can be done in realtime. No delay required. As for modeling I’ve found that what you’re trying to model for can have a significant impact on how much delay matters. 

**Mariana Raykova:** What about if we throw in the privacy requirements? If we add DP to your spending? If reported in a timely fashion are we OK?

**Andrew Pascoe:** Our spend numbers will have some noise and we’ve set client expectations. The noise isn’t so bad for contributions to JUST a spend bucket. Even the smallest campaigns will have thousands of impressions. 

**Charlie Harrison:** Are you talking about an aggregate measurement of spend at ad serving time? It’s a different use-case. It’s not clear sometimes when we talk about spend… is it CPA? 

**Ben:** Why is spend and pacing in consideration? This isn’t third party information. Each time you show the ad, you get billed. Except in FLEDGE. If we’re worried about real-time budgeting and pacing, that’s not a problem.

**Charlie:** Let’s scope this out of our conversation because we are not talking about FLEDGE right now. 

**Andrew Pascoe:** The reason I’m bringing up privacy mechanisms with spend, is because I can track users with bids. 

**Michael Kleber:** Yes, this is something we need to worry about with FLEDGE, but out of scope for now.

**Charlie Harrison:** Another consideration is negative examples. In general when we are doing supervised learning we need to know which examples did NOT lead to a conversion. Criteo competition is a different example. In general if we want to support a lot of different architectures we need to know negative examples. What information needs to flow to these systems? MaskedLARK built on something similar. You also needed to send all the impressions that did NOT lead to a conversion. 

**Call to action:** there is a big gap in between DP-ML research and our current setting. Most techniques protect the features and the label and do not take advantage of the structure (only the label is private). I believe this would be hugely beneficial to the noise we need to add to the system. 

Most research focuses on dense-features. DP works a lot better there. Everything blows up with sparse features. The 3rd is that it works on the multi-classification problem, but actually the predictions that are useful for ads are binary classifications / count. Generalized regression model. These are typically not studied in the literature. Delay: has not been studied at all. It would be great to have more public ads data. I think we can really improve on the existing literature if we take advantage of the structure of this problem. There are many important questions we need to answer.

Even if we aren’t training in MPC and it’s all on the server, there’s a lot of problems to solve.

**Erik Taubeneck:** I just wanted to call out that John made this point 2 days ago that while this is a form of aggregate measurement we need to consider the argument that this is a different use-case. We will likely have disagreement over the validity of this usecase. We have less consensus than we do on measurement.

**Charlie Harrison:** I pretty much agree with you. I don’t think a v1 needs to support both reporting and optimization. Let’s not paint ourselves into a corner. I think this is a long-term effort. Let’s not choose an architecture that prevents us from doing stuff.

**Erik Taubeneck:** I don’t disagree. If the contention is “this wouldn’t work for optimization” that’s not a blocker but it’s a consideration.

**Charlie Harrison:** I’m not sure I agree.

**Ben Savage:** If were looking at an architecture that could support optimization theoretically, I’d argue IPA does that. You could add feature vectors to the source events. Instead of SUM you run _train model_. But, harping on what Erik started and John said, I’d really like the group to agree on starting on a use case. I think we made progress on msmt because we have agreement on that output. 

I’d love for us to come to some consensus on the ML use case. To kick that into gear, I have a couple ideas. If the tech exists to do this privately, it may not be enough. We may need some of Robin’s governance for transparency. What features are OK? Are there things that can’t be features? Are there correlations you shouldn't be able to learn? Is there a level of contextual integrity? Returning to John’s statement about not recreating everything from before, maybe we need guardrails, and maybe they are policy not technical. To the question of hiding the feature vector: I’m not sure. Is it OK for helper servers to see a feature vector in the clear? I don’t know the answer. I’d like to hear if others are concerned.

**Charlie:** That’s a lot of things. I think it’s important to separate out the security and privacy goals. Maybe we do want to hide the feature vectors. While yes, maybe we can move forward on reporting, I don’t want to give up on critical use cases, and we should try to work on those. Would like to work with you on those.

**Martin Thompson:** I didn’t read that Criteo paper until yesterday. It gave me a far more positive sense. There is a piece of work in this space that’s giving results. When you can work with aggregates you can produce something. Until we do have an idea of what we want here, I don’t know if the shape of the thing we build for measurement should be constrained. I’ve heard enough from people here that this ML thing is critical to their business. There will be a strong incentive to go build this ML thing. I’m not concerned on that front. If what we build is a great base for ML cool! If not, that’s OK.

**Charlie Harrison:** I think there is potentially a problem there if it means a big ecosystem push if everyone has to re-tag all their sites. It’s not free and we should be mindful of the migration costs. If there is a crossroads, we should go into that knowing the costs.

**Martin:** We don’t build this one thing, and then we build this next one. I don’t think the timeframes are such that we complete one before we learn more about the other. It’s a pipe dream that we might complete something in the next year. We will learn things on this multi-year effort. I’m not concerned.

**ekr:** This is the very definition of the best being the enemy of the good. We have just enough energy to get moving on some kind of measurement thing. If we try to think if it can also be used for optimization we will not go anywhere. Scope down the use-case for aggregate measurement, table the discussion about optimization. Frankly this is a research effort right now.

**Don:** Thanks for the helpful pointers to different areas in the literature. I have some background reading to do. What I’m wondering is how end-users will get to the level of mathematical education required to be able to consent to this. 

**Charlie Harrison:** There is precedent for deployed private-ML systems. There are existing non-private ML systems that users consent to. It’s a good question. Consent is a little orthogonal to what the platform is providing. It’s a question for people deploying specific technologies. It’s not an insurmountable problem.

**Mariana:** Scoping down the effort and is optimization in or out. If we scope it down to just measurement do we want to scope it down to just on-device? The 3 browsers are all doing privacy-preserving aggregation. Are we scoping down and ruling out use-cases.

**Charlie Harrison:** We don’t have time to debate that. File an issue.

<&lt;shows slide comparing ARA vs IPA>> 

IPA can support more use-cases at the expense of complexity. ARA does pretty well but the big gap is cross-device and privacy-efficiency things like the sensitivity management from earlier. 

**Sean:** TPAC 2022 in Vancouver. Will we meet? I think yes? We need to put a request in by the end of the month.

**Wendy:** Hybrid meetings available. 

### [TPAC F2F coordination](https://github.com/patcg/meetings/issues/53)

Next TPAC 2022 will be a hybrid meeting with the main in-person hub in Vancouver, Canada: 

TPAC 2022 

Hybrid Meeting 

12-16 September 2022 

**Main in-person hub:** 

Sheraton Vancouver Wall Centre 

1000 Burrard Street 

Vancouver 

Canada 

British Columbia V6Z 2R9

Hybrid mode involves a plan to build a dynamic meeting to bring more cross participation and new opportunities for work between groups.

Need input on whether we are going to meet by **31 May 2022.**


## Participants Day 1



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Sean Bedford (Meta)
4. Sam Weiler (W3C/MIT)
5. Shivan Kaul Sahib (Brave)
6. James Aylett (Annalect/OMG)
7. Andrew Pascoe (NextRoll)
8. Brian May (dstillery)
9. Tara Whalen (Cloudflare)
10. Pedro Alvarado (Resonate)
11. Paul deGrandis (Kevel)
12. Martin Thomson (Mozilla)
13. Eric A. Bruce (NY Times)
14. Chris Wood (Cloudflare)
15. David Dabbs (Epsilon)
16. Joel Pfeiffer (Microsoft)
17. Anuvrat Singh (Amazon)
18. Andrew Aikens (TripleLift)
19. Kris Chapman (Salesforce)
20. Charlie Harrison (Google Chrome)
21. Christine Runnegar (PING, co-chair) part of meeting
22. Eli Grey (Transcend)
23. Wendell Baker (Yahoo)
24. Wendy Seltzer (W3C)
25. Alex Cone (IAB Tech Lab)
26. Michael Kleber (Google Chrome)
27. Heng Tang (LinkedIn)
28. Don Marti (CafeMedia)
29. Aditya Desai (Amazon)
30. Erik Taubeneck (Meta)
31. George London (Upwave)
32. Davis Gilton (Microsoft)
33. Garrett Johnson (Boston U) 
34. Eric Rescorla (MozillA)
35. Betül Durak (Microsoft)
36. Alex Turner (Google Chrome)
37. Braedon Vickers
38. David Hong (IAS)
39. Ray Kim (IAS)
40. Nan Lin(Google Chrome)
41. Ben Savage (Meta)
42. Jonasz Pamuła (RTB House)
43. Stephen Somerville (Anteriad)
44. Daniel Masny (Meta)
45. Theresa O’Connor (Apple, Privacy CG, TAG)
46. Mariana Raykova (Google)
47. Dan Boneh (Stanford)
48. Phillipp Schoppmann (Google)
49. Luke Winstrom (Apple)
50. Richa Jain (Meta)
51. Brad Rodriguez (Magnite)
52. Rachit Sharma (IAB Tech Lab)
53. Matt Wilson (NextRoll)
54. Siddharth Sharma (Microsoft)
55. Erik Anderson (Microsoft)
56. Akshaya Mani (Optable)
57. Tamara Yaeger (Iponweb)
58. John Wilander (Apple WebKit)
59. Benjamin Case (Meta)


## Participants Day 2



1. Sean Turner (sn3rd)
2. Ben Savage (Meta)
3. Robin Berjon (The New York Times)
4. Pedro Alvarado (Resonate)
5. Paul deGrandis (Kevel)
6. Martin Thomson (Mozilla)
7. James Aylett (Annalect / OMG)
8. Graham Mudd (Anonym)
9. Braedon Vickers
10. Tara Whalen (Cloudflare)
11. Michael Kleber (Google Chrome)
12. John Wilander (Apple WebKit)
13. Sean Bedford (Meta)
14. Chris Wood (Cloudflare)
15. Tim Geoghegan (ISRG)
16. Don Marti (CafeMedia)
17. Davis Gilton (Microsoft)
18. Andrew Pascoe (NextRoll)
19. Wendy Seltzer (W3C)
20. Heng Tang(LinkedIn)
21. Joel Pfeiffer (Microsoft)
22. Theresa O’Connor (Apple, Privacy CG, TAG)
23. Eli Grey (Transcend)
24. Anuvrat Singh (Amazon)
25. Wendell Baker (Yahoo)
26. Benjamin Dick (IAB Tech Lab)
27. Alex Cone (IAB Tech Lab)
28. Brian May (dstillery)
29. Erik Taubeneck (Meta)
30. Alex Turner (Google Chrome)
31. Luke Winstrom (Apple)
32. Eric Rescorla (Mozilla)
33. David Dabbs (Epsilon)
34. Daniel Masny (Meta)
35. Benjamin Case (Meta)
36. Charlie Harrison (Google Chrome)
37. Lisa Markou (ford)
38. Mariana Raykova (Google)
39. Ratko Vidakovic (AdProfs)
40. Andrew Aikens (TripleLift)
41. George London (Upwave)
42. Phillipp Schoppman (Google)
43. Sam Weiler (W3C/MIT)
44. Siddharth Sharma (Microsoft)
45. Przemyslaw Iwanczak (RTB House)
46. Erik Anderson (Microsoft Edge)
47. Richa Jain (Meta)
48. Betül Durak (Microsoft)
49. Christine Runnegar (PING co-chair), part meeting
50. Moshe Lehrer (Neustar)
