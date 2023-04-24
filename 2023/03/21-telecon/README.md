# March 21 & 23 2023 Virtual Meeting

The Private Advertising Technology Community Group's meeting will be meeting two days for 3 hours at the same time both days.

## Schedule

### Day 1 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 18:00 (06 PM) | 21 Tue | Sydney        |
| 16:00 (04 PM) | 21 Tue | Tokyo         |
| 08:00 (08 AM) | 21 Tue | Brussels      |
| 07:00 (07 AM) | 21 Tue | London        |
| 03:00 (03 AM) | 21 Tue | Boston        |
| 00:00 (12 AM) | 21 Tue | Seattle       |


### Day 2 Start

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
| 18:00 (06 PM) | 23 Thu | Sydney        |
| 16:00 (04 PM) | 23 Thu | Tokyo         |
| 08:00 (08 AM) | 23 Thu | Brussels      |
| 07:00 (07 AM) | 23 Thu | London        |
| 03:00 (03 AM) | 23 Thu | Boston        |
| 00:00 (12 AM) | 23 Thu | Seattle       |


## Joining Information

[Zoom](https://mit.zoom.us/j/95356244879?pwd=NDBwZmxleTMwcHFpZG1MZW1tUXhVUT09)

[Slack](https://www.w3.org/slack-w3ccommunity-invite)\
Our group is called “private-advertising-technology-cg”



## Agenda

### Day 1

- [Review WG Charter PRs](https://github.com/patcg/meetings/issues/108)
- [Review Ad Hoc groups](https://github.com/patcg/meetings/issues/107)

### Day 2

- [Review Privacy Principles progress](https://github.com/patcg/meetings/issues/110)
- [Continue Baseline Requirements Review](https://github.com/patcg/meetings/issues/91)

## Read All about It!

[Slides to Read All About It!](https://github.com/patcg/meetings/blob/main/2023/03/21-telecon/W3C%20Read%20All%20About%20It!.pdf)

## GDoc Minutes

https://docs.google.com/document/d/1fZTAG6j-LKk991aaQx_cPoqK9h5m4W8pwq46oQD4WEo/edit#

### Scribes

Willing Victims (Tuesday): Erik & Charlie

Willing Victims (Thursday): Michael

## Agenda

* Day 1
    * [Review WG Charter PRs](https://github.com/patcg/meetings/issues/108)
    * [Review Ad Hoc groups](https://github.com/patcg/meetings/issues/107)
* Day 2
    * [Review Privacy Principles Progress](https://github.com/patcg/meetings/issues/110)
    * [Continue Baseline Requirements Review](https://github.com/patcg/meetings/issues/91)

### W3C Read All About It!

[Policy Slides](https://github.com/patcg/meetings/blob/main/2023/03/21-telecon/W3C%20Read%20All%20About%20It!.pdf) 


## Day 1


### [Review WG Charter PRs](https://github.com/patcg/meetings/issues/108)

Current Scribe: Charlie Harrison



* Aram: Going to go through open PRs on the WG charter. Goal to conclude these and submit the charter again
* Update Privacy Principles:
    * [https://github.com/patcg/patwg-charter/pull/57](https://github.com/patcg/patwg-charter/pull/57)
    * Straightforward, we needed to link to a date-controlled link. Thanks to Martin who corrected the anchors. I don’t think there are any objections, just link fixes.
    * Call for consensus, let’s do it!
    * Merged!
* Any proposed feature should increase the protection of data about a…
    * [https://github.com/patcg/patwg-charter/pull/58](https://github.com/patcg/patwg-charter/pull/58)
    * Aram:
        * Coming from feedback in the formal objections, there needs to be clarity about tradeoffs in proposals. This is now split into two different changes. The first one is #58. Any proposed feature should increase the protection of data about a user.
        * Some changes in this PR that generated this sentence. Previous discussion seems to indicate this change is not desired.
    * Martin: This one is really hard. If you baseline the way the web is today, diff people experience the web differently, increased protection of user data is not going to be possible. Some things we do here might reduce protection. I don’t really see that we can put this in a charter and stand by it.
    * Brian: This is fraught with problems, what all these words actually mean. Not well defined. Should get rid of the sentence
    * Charlie: Agree w/ Martin
    * Erik T: Agree w/ folks before me, going to suggest that if we wanted anything like this, it could involve formal analysis about what privacy properties a proposal has. Might be simpler to let it be.
    * Aram: Next issue will discuss formal analysis
    * Shivan: Wondering if we all agree that proposals in this WG will expose more user data than not. Should we have that in the charter? If not, should we?
    * Erik T: The question that Martin opened with is “relative to what?”. Relative to 0, yes there will be some data coming out of the system. It’s not currently necessarily 0. What we’re trying to do is take something less formal and make it formal.
    * Aram: We should deal with this in the specifications themselves, vs. restricting us unnecessarily in the charter.
    * Brian: Putting anything in the charter about what happens with data, what’s going to be exposed. I don’t think we need to say that because APIs use data and if we get into kinds of data and POVs on that data, not a lot of objectivity on a subset of data. We don’t need to put the argument about what data is exposed in the charter, can be on a proposal by proposal basis.
    * Aram: Queue over, general agreement to close the PR without merging. Call for consensus. No objections.
* Proposals should clearly state business factors and user risks
    * [https://github.com/patcg/patwg-charter/pull/59](https://github.com/patcg/patwg-charter/pull/59)
    * Aram:
        * Not sure if we’re ready to merge or dismiss this one.
        * This text came out of feedback from the formal objections on the origin charter. Theme we saw was that we needed to require a statement of risk and how we will balance risk.
        * Idea of this paragraph which we synthesized from the feedback was to move that responsibility to the individual proposals that come through.
        * I imagined this would be similar to the statement PING requests, potentially with a little more detail with why the decisions are made, not just the privacy risks.
        * I saw some feedback from Nick, noted in the last session, these are synthesized from formal objections, not the opinions of either of the chairs.
        * With that noted, opening the queue.
    * Ben Savage: I wonder if we could just shorten this PR to be more or less equivalent to the title of this issue. The text currently is wordy. Why not just say proposals should state what business factors they want to make possible and the associated user risk.
    * Nick Doty: There is a section already talking about privacy implications for each specification. [Line 278](https://github.com/patcg/patwg-charter/blob/4f0d970bb4983d5e46c795de7da91e6e524c1f60/charter.html#L278), default language in most charters. It could perhaps be improved. But I’m not sure if the objectors were asking for something in addition to the privacy implications. I think the privacy implication piece is there already. If we want to talk about the use-cases, groups often document use-cases and I would be fine with that. Don’t know if it needs to be in the charter but not opposed.
    * Aram: What differs from the standard PING language is that this will also address what specific business factors/use-cases were the reasoning behind risks that were opened for privacy. We are looking to improve the state of privacy from the current state, but that will still be less private in theory than the future state without our participation. In the future, everything is partitioned, 3p cookies gone away, etc. We are intending to introduce proposals that introduce new data about the user. If we are doing so, this is what we are stating, why we are opening up these vectors that could decrease privacy (somewhat), in exchange for these things we want or need to do.
    * Nick: I don’t know if we want to talk about “in theory” in our specifications, and I am not following the proposals that things are going to decrease privacy vs. some theoretical state.
    * Aram: Private measurement as an example. It is looking at a more private version of what is used for 3P cookies. We have a bunch of use-case goals. Proposal as it stands as opposed to the current state is that privacy is increased, because 3P cookies exist on at least some browsers. If 3P cookies go away, none of the measurement proposal use-cases would work without the proposals. That’s the “most private state”. We are using privacy properties to make not worse privacy but proposals that endeavor to accomplish business goals that require more data than that most private state of post-3P. (scribe couldn’t follow the rest)
    * Brian May: Getting a sense of what this PR is trying to communicate. Any kind of risk to the user will be difficult to do in a comprehensive way. Not sure if it’s something we should mandate. People working on the proposals can figure if the user risks are acceptable. When I read “business factors” I read what the impact to business will be. I can imagine people could get confused about that. Maybe the language should be changed.
    * Aram: Open to language changes
    * Erik T: Most private version of the web is the one that doesn’t exist. Any feature has to trade off what it enables vs. privacy properties. What’s unique about the things we’re working on it’s a second order effect, supporting use-case that typically supports ad-supported web sites, so people don’t have to pay. Unlike e.g. some CSS feature that benefits users first hand, where we can say this tradeoff is worth it. I think that’s what this change is trying to get at. Do other working groups have similar statements in their charters about evaluating the utility of APIs relative to privacy risks, or is that just the role of TAG/PING, etc. Does dropping this change anything we do?
    * Aram: difficult question. There are standard requirements for W3C. PING assessments, TAG assessments, etc. Beyond that, it’s probably different WG-to-WG.
    * Sam W: Not immediately
    * Martin T: Not 100% on something like this in the charter. Reason to put something in is to constrain the working group, so it doesn’t go off the rails. This is difficult because the rails we’re looking for are “don’t make privacy much much work” and “don’t produce useless features that justify taking away 3P cookies”. [I put a different framing](https://github.com/patcg/patwg-charter/pull/59#discussion_r1142973007) in the text but not sure it’s something that we want to see. Would rather talk about the tradeoff between functionality, but I’d be just as happy without this text in.
        * Proposed: 
        * > Many of the specifications that this group is expected to produce will have a special need to balance privacy risks with the interests of businesses that rely on advertising. Specifications produced by the group shall contain clear justification for any use of private information or any privacy risks that are introduced.
    * Michael Kleber: I disagree w/ Martin in that I think there is a good reason to have something along these lines in the charter. To respond to previous discussion, about what other groups say, there is a common line in W3 group parlance, where people say “this group does not address ways in which trade offs…”. E.g. [PING says](https://www.w3.org/2019/09/privacy-ig-charter.html) tradeoffs of privacy vs. other goals is against the PING guidelines. The thing we’re trying to express in the charter is that this group _is_ involved in discussing the tradeoffs between privacy and business use-cases. Saying this group’s domain explicitly includes discussing these tradeoffs makes it clear we are embracing. Don’t have particular opinions about the language. Saying this group embraces this tension is appropriate.
        * [Nick: PING’s charter doesn’t appear to say that, but it might be common for groups like PING to only talk about one topic, and not always address the possible trade-offs on other topics. Sam: +1]
    * Mark N: If I were reading a charter and came across this text, I would be confused. First sentence is confusing, does the output show up in minutes, a document, etc? Not specific enough. Second statement is more concerning to me. Word “proposals” here, does that mean that if I submit a proposal here, this is raising the bar? This could be a filtering function, but it could be weaponized to suppress contributions. Should think very carefully about the dynamics of when this will be used. Charters are weapons chairs can wield for success. Do we want this to be specific to _outputs_ rather than _proposals_? Bearing on reality for this in proposals might be slight. Make this apply to output not the input.
    * Aram: Very useful
    * Sam: I’m also confused when I look at this, what scale it applies to. Do we need 3 paragraphs for every 1 paragraph, or is this more macro scale. If this is in the micro scale, as a document editor this would be terrible. If macro scale, it covers 80% of what we’d consider in a privacy considerations section anyway. It’s basically asking for the same thing. I don’t think we need this.
    * Aram: Is there some additional 20% that we could write to cover the additional concerns here?
    * Sam: Not convinced we need to. Extra 20% would involve articulating business factors. Not sure we need to explicitly call this out. Don’t think it needs to be in the charter.
    * Aram: I don’t think you’re misunderstanding, just not sure the formal objectors would agree w/ you, but I’m trying to represent as a proxy.
    * Brian: Agree w/ Sam, these things should be worked out in the proposals. These proposals will have a long lifetime and we’ll figure these things out later. Trying to figure it out upfront will be too hard and might kill off good proposals. Privacy principles we’re working on should guide the work the WG is doing. Rather than have each proposal re-litigate, we should adhere to the privacy principles when developing our proposals
    * Ben S: My understanding of the formal objections is less about degrading privacy and more about degrading business practices in the name of privacy. I liked Mark’s suggestion to constraint this to the group’s recommendations. “Recommendations of this working group will attempt to lay out what the considerations were, balances / tradeoffs” etc. I think that’s fair.
    * Aram: Do you think that the framing that Martin has produced here meets that? Also curious about Mark / Sam’s opinions on this comment
    * Mark: Happy with it
    * Ben: Eliminate part about “special needs”.
    * Martin T: Can you type a proposal? I typed this up in real time while we were discussing
    * Sam: Don’t really have feedback. Y’all will do something competent here. I’m in favor of keeping charters simpler, but this is fine.
    * Martin T: Yes we will balance these things, to Kleber’s point its probably worth saying so. Less concerned about constraining the shape of the output, but this signals our intentions about the outputs. This will help the membership if they are voting on the charter. Group has committed to considering those factors. These sentences are useful in some way.
    * Aram: Is “specifications” the right word?
    * Martin T: You can’t say recommendations until we’re done. I think “specifications” is fine.
    * Erik T: Agree, Michael’s comments were convincing. Does this fit better in the scope? If we’re not looking to constrain work items, might be better to put in the scope section, without adding requirements to specifications.
    * Aram: Endpoint is that there is specific output we want in the specifications.
    * Erik T: That’s my question, do we really need this in the output? From Michael mostly its a signal of what we’ll talk about. Martin also not keen on constraining output. Just trying to keep this simpler for us.
    * Sean: Putting myself in the shoes of the formal objector, signaling that we’ll do this might be worth putting it in. For specific comments like this I think we can put in this suggestion.
    * Aram: Sounds like we are moving towards “seems like we want this but might need edits”. Closing queue with the expectation that there will be another round of edits. Maybe we can revisit Thursday.
    * Brian: Mentioned a few times that formal objectors views are represented by proxy. If the objectors are not coming to the meeting, we should not… (scribe lost this)
    * Erik T: But then the charter won’t pass
    * Brian: Can anyone just kill a charter and then walk away?
    * Sam: Trying to push for a world where charter objections are resolved in a public process. If people aren’t (?) advocating their positions, they might find their objections being called as being in the rough.
    * Brian: Not totally against this language, but it might complicate people developing these proposals. There are people on the side of privacy and on business, and not a lot of people in between that.
    * Nick: Happy to work offline on wordsmithing. Did want to say that I think it’s valuable to describe the considerations about use-cases and privacy. Saying we want to balance this human rights issue with this business issue. I’m opposed to that way of thinking, you don’t need to hurt users a certain amount to help businesses. Their interests can be aligned. I would prefer to talk about considering use-cases and privacy implications.
    * Aram: Idea is to make the consideration a clear part of the requirements for specifications
    * Ben Savage: I provided some suggested text. Glad Nick said his concern. Does imply there will be some tradeoff. As much as I want an “everyone wins” solution, we will have tradeoffs. How to set the differential privacy epsilon? At some point we need to set this. Inaccurate to say there is no tradeoff.
    * Mark: The word “shall” and “expected” in these suggested texts are concerning to me. If we word these to be more aspirational, “the group aspires” is less weaponizable. Problem here is that the interpretation of these goals is subjective, and the charter can’t contain enough information to align people’s perceptions of the goals.
    * Brian: People will come up with novel interpretations as time goes by
    * Aram: We have some suggested edits and tripping points we want to avoid. Making a note in this one, we need additional reworking but may result in a change we want to add.
* An alternative approach for scoping
    * [https://github.com/patcg/patwg-charter/pull/56](https://github.com/patcg/patwg-charter/pull/56)
    * Aram: Context for this: there were 3 different proposals around reframing top level scope. Two were in direct opposition. After discussion in last session, idea was to resolve. Martin has synthesized them here. Seeing general agreement here.
    * Martin: Talked to a number of people about this, addresses the core concerns that Tess has w/out compromising the thing we value.
    * Aram: Would like to see us decide on this PR this evening. Queue is open.
    * Nick D: Thanks Martin for doing this, it does a good job at handling the complex set of constraints. I think it’s an improvement on the explainability of how we’re handling the server-side specification / impl. +1 to merging
    * Ben S: Merge it
    * Brian: Merge it
    * Aram: Consensus call, objections? Hear no objections, ready to go. Merging.
* Clarify scope of group w/using open processes
    * [https://github.com/patcg/patwg-charter/pull/51](https://github.com/patcg/patwg-charter/pull/51)
    * Aram: some changes here and discussion. This has been open and discussed, incorporates feedback from members. Does it need additional work?
    * Nick D: Seems like there will be a merge conflict w/ the previous PR. I would suggest we just talk about open and standardized part. Don’t mind the open and standardized protocols, it’s a little redundant.
    * Aram: Ignoring line 157 change. Some merge conflicts
    * Charlie: is this change a no-op? Do we need it if a no-op?
    * Sean: This is a no-op. We don’t need to say this.
    * Aram: Reason we came to this change was that ppl were concerned about this. Whether we feel that restating here is necessary or not.
    * Ben: Prefer to close w/out merging. In the part I recall many conversations where James where any API we propose could be fully implemented by a non-browser operator, all inputs to make that possible. Github issues where this is discussed at length. Would the “open” word get weaponized. Doesn’t meet a certain definition of open.
    * Aram: Sounds like we’re moving in favor of closing w/out merging
    * Charlie: Support closing without merging
    * Brian: Also support closing w/out merging. We should say we follow W3C guidelines 
    * Sean: We do say this
    * Aram: Consensus call to close this PR without merging it. Any objections? Hearing no objections, consensus to close w/out merging. Let’s do that.
* Addressing #35 - making explicit that proposals should detail the data they intend to use and return
    * [https://github.com/patcg/patwg-charter/pull/36](https://github.com/patcg/patwg-charter/pull/36)
    * Aram: Does anyone want to pick up this PR? At this point it’s basically abandoned. Would prefer to set this up for a consensus call for next time. This change adds anticipated data inputs / outputs. Similar to “stuff we would already do in the course of writing a spec”.
    * Erik T: This feels overly specific to the private measurement work. Some other specification might not have inputs/outputs in the same way, seems too specific.
    * Aram: Any other feedback?
    * Sean: “All known” phrasing could be weaponized
    * Aram: that’s already in there
    * Nick: Wonder if people who proposed this would want this to be part of PR 59 ([https://github.com/patcg/patwg-charter/pull/59](https://github.com/patcg/patwg-charter/pull/59)).
    * Brian: Suspect i was the original advocate for this change. I am willing to let go of it for the sake of finishing the charter. Why I wanted this was you can’t really talk about the privacy invasion/analysis without seeing the data, but this doesn’t have to happen in the charter
    * Martin: Just an observation, this could rule IPA out. We don’t have a way of constraining the inputs to the system.
    * Aram: Anyone else want to queue up on this PR? Going to note that there will be a call for consensus in the next meeting
* Deweaponize ‘all known’
    * [https://github.com/patcg/patwg-charter/pull/60](https://github.com/patcg/patwg-charter/pull/60)
    * Aram: Any objections with putting on the call for consens for next time?
    * Nick: Some problems with this, but can discuss later
    * Aram: Mark as call for consensus, give people time to respond between now and next month
* Aram: This leaves us with two we will be calling for consensus next month, and one that needs additional reworking on the PR, and then probably call it for consensus.
    * Will note #18 remains blocked. James is not here to discuss. It is left open as an artifact.
    * Continue to keep this open for record keeping purposes
* Charlie: Why can’t we close?
* Aram: Open request to the author to reframe this PR into more digestible components. Author has not responded. Until they do, we don’t need to respond.
* Sean: At some point we will have to call it and move on.
* Erik T: to clarify on timing, we will have to close these remaining issues and call for consensus at the next meeting before we resubmit.
* Aram: Will make a note here that we do want to close this. We want to resolve the last remaining issues here. Unless something else comes between now and next month, we would submit it.
* Erik T: Just trying to get this submitted
* Sean: Are there any more comments coming? Any advanced intel? Are people generally happy with what they are seeing?
* Erik T: seems like it’s moving in the right direction to me
* Aram: Chairs are available via slack / email. You can reach out if you prefer to discuss privately. 
* Sam: Can also file an issue or PR in this repo without filing a formal objection.
* Aram: Would be great if you submit suggested text. Would be great if you could include suggested text with formal objections too. Closes current business around WG charter. Returning 40 mins after the hour.
* Erik T: Maybe we can keep going if the next topic will be quick (so those in bad time zones can go to sleep).
* Aram: Maybe there are progress reports
* Erik: Does anyone have something to talk about
* Aram: Alex is not here to do an extensive report


### [Review Ad Hoc group](https://github.com/patcg/meetings/issues/107)



* Aram: Ad Hoc groups are increasing. Working in the individual draft space, with the thought that they may end up in this group.
* Aram: IPA
* Erik: [Bi-weekly meeting](https://github.com/patcg-individual-drafts/ipa/issues/47). People can add topics, will discuss protocol work.
* Ben: Our first meeting will talk about the client interface.
* Aram: [Private Aggregation](https://github.com/patcg-individual-drafts/private-aggregation-api/issues/19). [Shared storage ](https://groups.google.com/u/1/a/chromium.org/g/shared-storage-api-announcements)and [FLEDGE](https://groups.google.com/a/chromium.org/g/fledge-api-announce/) have mailing lists.
* Charlie: The scope of the first meeting is discussing using the proposal to satisfy the reach measurement use case. [Minutes](https://github.com/patcg-individual-drafts/private-aggregation-api/blob/main/meetings/2023-02-15/minutes.md) posted on the repo.
* Aram: [Topics](https://github.com/patcg-individual-drafts/topics/issues/115). 
* Michael: Talked about Topics in the last PATCG F2F. Holding ~monthly calls to work out outstanding issues. There’s a Google doc linked with agenda in upcoming calls. Ongoing discussions of taxonomy, epoch length, improve privacy with filtering. 
* Nick: Not in individual drafts, but at the last meeting we discussed privacy principles. Got folks together and opened a PR and issue list of topics to cover. Not sure if we’ll make that a recurring meeting.
* Aram: Should we add that to the queue for Thursday.
* Nick: Could discuss Thursday, but would also be further along in a month.
* Aram: Let’s add a short report for Thursday.
* Nick: Could we use the W3C calendar for the ad hoc groups?
* Aram: adhoc vs sub meeting. I think we could.
* Sean: I can add it, or put it in an issue.
* Aram: First PATCG to end early

Meeting closed after 1 hour and 45 minutes.

## Day 2

Scribes: Michael Kleber & Nick Doty

### Read All About It!

Slide, as usual.  If you contribute, be sure you are bound by the Contributor License Agreement.


### [Short report on Privacy Principles](https://github.com/patcg/meetings/issues/110)

Nick Doty:



* Rough notes from volunteer group working on editing a PAT Principles document: [https://github.com/npdoty/patcg-docs/blob/summary-202303/principles/summary_202303.md](https://github.com/npdoty/patcg-docs/blob/summary-202303/principles/summary_202303.md)
* Principles to be used for the proposals that will come through the group, separate from the threat model.  We've meet in the last week or two, pulled together some sources and a list of areas we want to cover.
* Current list of areas includes: consent, control, profiling, distress & intrusion, relevance, reporting and context, transparency, security, trust model, explainability / comprehensibility, competition, inferences, identifiers, accountability.  Not exhaustive.
* There is also ongoing work in the TAG draft about privacy principles, some of that is more directly relevant to our work.  We're pulling those into this doc so that we can chew on them also.  We expect to elaborate in some areas on the TAG note, but we don't plan to address every topic for the whole web of course.
* We've also pulled together a list of resources — assorted documents that might be useful, previous related work.
* Please point out things that are still missing, things we should be talking about but are not yet.  Just got access to the repository, so we will start working on this in PRs
* Aram Z-S: Question for kleber: You published your privacy model — is this still the most up-to-date?
* Michael K: we/Chrome has not published a new version of this.  the original document (listed here) partly fed into the TAG document that is ongoing and should influence this discussion we are having in this group.  I don’t know if Chrome has plans to add to this; the point of the list was philosophical motivation behind privacy sandbox proposals that Chome has been working on. our work has moved on to specific proposals rather than refining underlying principles
* Martin: It's hard to see from here whether the intent is a broad work, or whether this group plans to focus on the delta between the broad goals and what we're going to push on in the advertising work specifically.  The places where there are differences includes the cross-side flow of information in measurement, how we rationalize the flow of information that we decide to enable — places where our group has things uniquely to add.  All the things about transparency and consent have established principles, and yes maybe we need to talk about them and come to some agreement.  But the document that we're producing may not need to add anything new.
* Nick: That is important guidance — we don't want to recreate everything, that's a very large topic, not helpful for us to try.  Maybe even more specifically, could be helpful for us to focus on the most active proposals, or interest-based targeting since that also has some specific proposals upcoming.  We might be able to focus on principles we're already using, or trying to use, for specific proposals.  I would welcome hypothetical initial principles that we are using, to get us started.
* Martin: We are using most of the principles you've listed.  The things that are most uniquely specific to the work we're doing are e.g. continuous release of information over time to websites, and the release of information to websites that needs to happen.  We want a narrow release of information, we don't want to rely on consent as a major factor — that is, we have already reached a conclusion about a principle that is unique to our context, and that's where we ought to concentrate mode.
* Nick: The "continuous release" concept, or the DP concept, if we can describe it as a principle, would be good.  That would be unique to us, we're not seeing that in every other web API.
* Ben Savage: Let's talk about the hardest part: Minimization.  The TAG doc you quoted says "user agents should share data only when it either is needed to satisfy a user's immediate goals or aligns with the user's wishes and interests."  If you asked the average user whether they want something like the private measurement API, everyone would say "no".  We need to have some story about how this is aligned with the user's "wishes and interests".  We need to tell some story about why our work is aligned with that principle.  Maybe it's that people want to use the web for free, or for discounted content, so we need some sustainable way to fund it.  Or maybe it's that people want to see more relevant instead of less relevant ads, and measurement helps with that goal.  I think our principles document needs to address this head-on.
* Nick: That is why people who have worked on the task force included that "or aligns with the user's wishes and interests" clause.  Users aren't going to say "I really wanted those CSS files to load".  Likewise in telemetry, websites need it to work well, and users want their websites to work.  Might fit under the next section about solicitation of preferences also — "I want to contribute data so that websites work well".  Maybe can also solicit general preferences about wanting some kinds of content.
* Brian: We do need to explain our principles.  If we need some cross-site information to be provided to advertisers, maybe that should be in a separate doc, rather than trying to work it into the principles doc.
* Shivan: I don't think we should be talking about trade-off between privacy and X in the principles doc, also because UAs have different opinions.  Should be in a different document.
* Martin: I disagree with Shivan — maybe we should talk about it over a drink when we're in the same place.  It's useful for us to identify on the principles that we intend to apply, and many of them are already written down.  The value of this community is that we can talk about how they apply to us.  But the real value is in saying: Because we have these special needs, the following principles are going to apply to the ways in which we release additional information to websites.  We're providing APIs that are not directly relevant to users, the information we provide is going to be some loss — some additional flow of information.  We should justify and explain why we are doing what we're doing, and what value that has for users.  That's going to have to involve why we made the choices we did, we're approaching the problem in the following way, DP / information theoretic / etc.
* Shivan: This document should concern itself with the proposals being discussed in this group.  The people woking on the doc should come back and present it regularly, so it's tied to the work being done.  I was thinking of making it more relevant by talking about the mechanisms.  I don't think this doc should be talking about whether advertising is needed, or whether users should be compensated.  The technical mechanisms definitely belong.
* Martin: I can agree with that. We can probably make that work.
* Charlie: My biggest concern with avoiding discussing trade-offs is that it will be really easy to write a doc where the surface reading would reject most of what our group is working on.  That would be flawed: we need a doc somewhere that makes the case for the work we're doing in broad strokes, even if we're not agreeing with where the trade-off line should be, we should have a case that it's not at the extreme end.  If thinking of second-order effects is contrary to putting the user first in the priority of constituencies, then needs careful thinking and explaining about why we are doing anything at all.  We should be making the general argument that the line is somewhere that it not at an extreme.
* Aram: There is already extensive documentation on general privacy principles.  I think establishing the baseline is the first step, but the purpose of this document is less "privacy principles" and more "how we as a group are going to deal with this", what trade-offs we are going to make and why.  For the direction we want this document to go, what we need is an understanding of what this group is interested in, what makes the web healthy, what users would be satisfied with, how that interacts with privacy in some way.  We do need to articulate trade-offs in some way. Maybe not all trade-offs. This a document of our principles, there are a number of documents we can start off from, but what we are thinking about when trade-offs come up or why we make the choices we do.
* Brian: I think it's important for us and for the larger community to decide and articulate what the contract between advertising, the internet, and the users of the internet is, so people have some framing for what we're describing.  We are approaching a set of relationships that are rather novel compared to the general perspective on the web that the w3c has put forward.  They are very reasonable and reality-based positions we're taking, and not well articulated anywhere.  The reality is that a lot of the web depends on advertising and it had some position of authority in a lot of the way things move on the web, and we need to acknowledge that.  I originally suggested that we make explicit how it fits into the hierarchy of constituencies.
* James Aylett: I think this is largely compatible with what people are saying: Principles documents should include the principle, and we're going to compromise on them to achieve utility and balance.  I think that's going to be specific to each proposal and system that we build.  I thought about instead of trade-offs, let's discuss risks and what we're doing to mitigate them, to claw back some of the (potential) loss of privacy that is inevitable in moving data around.  The principles doc should be saying "these are what are important, and we're going to have to trade them off, we're not going to hit all of them perfectly."
* Martin: &lt;sign of general agreement noted>
* Aram: We should note reasons why we might make trade-offs.  A lot of work has been done on privacy principles, and a lot of work about use cases, but not much has been done on how these meet and trade off.  We do need to note that these are what we're considering when we encounter them in proposals.
* Shivan: I agree with that.  My gut reaction is opposed to text around "advertising is really important to the web" — I would be opposed to that, it's fine to say what we want to achieve, but justifying a loss of privacy for some principle that we absolutely need advertising because it's more equitable? I don't think it belongs in this document.
* Aram: Let's take that to the PRs and discussions we'll have there, this is not the context to argue over this particular point.
* Nick: This has been an interesting discussion.  Partly we're speaking in the abstract because we haven't come to you with any principles to evaluate yet — all we have is some bullet points, so talking in the abstract is inevitable.  Regarding trade-offs: They are inevitable in engineering, but that's not what's going on here, a trade-off in release of data or entropy is not the same thing as a trade-off in user autonomy or in human rights.  We don't need to say that we are trading off fundamental user protections.
* Brian: I'm curious about how people think we should employ the principles document — how would that come into play in what we're doing in this group?
* Aram: Let's not answer that now, depends on what form the document takes
* Brian: But how I would approach creating the doc is dependent on how it will be used!
* Aram: It's an articulation of why we make the decisions in proposals that we do, but not an articulation of those decisions.  I want to avoid talking about the specific content of the doc here — let's not go down the road of things that might be a PR.
* Ben (advertising principle: providing a “well-lit path” that realizes some critical advertising functionality. Providing this somewhat mitigates the demand for tracking through other means, and makes it possible for UAs to more effectively police other types of tracking): I liked what Shivan said.  I want to talk about what we want to achieve, what our goals are.  Our goals are to mitigate covert tracking.  We believe that platform-based measurement APIs can provide a means to avoiding the route of covert tracking.  If you make it so that it's not necessary to do covert tracking and advertising is still possible, then it's possible to take new routes to combat covert tracking.
* Martin: The benefit of talking in the abstract like we're doing now is real but is limited — you never get anything done if you spend too much time in the abstract.  I think we need to make things concrete as soon as possible.  Ben just indicated in that direction.  We do have some concrete conclusions in our discussions so far — capturing those is valuable.  As we discover these, it's worth documenting and capturing them, driven by the work we are doing rather than some abstract ideas.
* Charlie: Meta-point: What belongs in this doc vs e.g. the TAG document or elsewhere: I would prefer that we have a strong editorial eye towards whether something we're writing here belongs, and avoid writing principles that don't apply to any existing proposals actively discussed in PATCG or the individual drafts.  Let's save those up if we need them.  We don't need to rehash things that are not clearly relevant to work we're doing.  Also, if there is another document that we can base the structure on, like the TAG document, it might be interesting to have a "diff" view, where we point out the ways in which we refine or alter one of the TAG principles.  Coming up with a template for how we think about what belongs in this doc maybe should be documented in the doc itself.
* Brian: Agree with Charlie: if we diverge from TAG then we need to explain why.  E.g. TAG has a principle against providing users with unsolicited data — that is what advertising is all about, we should make the case for why.
* Aram: Closing the queue.  I think this has run its course.  I suggest that PRs on this documents are the way to move this doc in the direction of something this group can come to consensus on.  Anything people want to make sure gets covered?  If not, let's move on.  I encourage comments and PRs and prioritization for how the work should progress — concrete PRs with actual text are better than directional suggestions.
* Nick: That was more than the amount of time I expected we would spend on this.  Agree with Aram, we will take any concrete feedback, and issues/PRs are welcome.


### [Continue Baseline Requirements Review](https://github.com/patcg/meetings/issues/91)

See the following background: 



* [https://github.com/patcg/docs-and-reports/blob/main/design-dimensions/Dimensions-with-General-Agreement.md](https://github.com/patcg/docs-and-reports/blob/main/design-dimensions/Dimensions-with-General-Agreement.md) 
* [https://github.com/patcg/docs-and-reports/tree/main/design-dimensions](https://github.com/patcg/docs-and-reports/tree/main/design-dimensions) 
* [https://chart-builder-patcg.glitch.me/](https://chart-builder-patcg.glitch.me/) 
* [https://docs.google.com/document/d/1bydwuN0_K2anOZV41xNJn1Kt0vt9WPOkf56ESnmQ5_A/edit?usp=sharing](https://docs.google.com/document/d/1bydwuN0_K2anOZV41xNJn1Kt0vt9WPOkf56ESnmQ5_A/edit?usp=sharing) 
* [https://github.com/patcg/meetings/issues/99](https://github.com/patcg/meetings/issues/99) 
* Charlie: In our last face-to-face we were going through some controversial things that came up in the survey — can we continue going through the hot items?  E.g. cross-device was a hot topic we didn't get to yet.  I think there was a GitHub issue where you synthesized something — [https://github.com/patcg/meetings/issues/99](https://github.com/patcg/meetings/issues/99) — I think that list was based off of the survey thought not 100% sure.  We discussed numbers 1 and 2 on this, touched a little on 3 and not the others.
1. private computation configuration vs on-device/in-browser \
a. Aggregation \
b. data join \
c. private computation configurations
2. privacy mechanism (differential privacy / information theoretic / k-anonymity)
3. if DP: \
a. privacy budget management \
b. privacy budget scope (epoch, domain, etc.)
4. cross device
5. limits on multiple 3rd parties
6. what can be measured? (clicks, views, opportunities, events within an ad, conversions)
7. time delays
8. preregistration / configuration overhead
* Aram: Looking back at minutes from last time, lots of discussion on privacy mechanisms 2, but not past that.
* Charlie: 
    * A lot of the private measurement proposals have some notion of leaking information about users, and this cuts across all the different tprivacy definitions — you can think about entropy loss, or epsilon loss in DP, this is a meta-parameter across these proposals.  Privacy budget describes how much information is being lost, across some budget scope.  The strongest notion would be "information about one person across all time".  More practically, most proposals in this space start divvying out more budget over time — so adding a time epoch into the privacy budget scope, so we will allow this amount of user information to leak over 7 days, or something like that.  This shows up in some form in basically every proposal — it's not feasible to define an API that doesn't operate in this spigot mode — wouldn't make sense to launch an API that started working but slowed down and stopped after a month and was only available to new users!
    * Other things that go into the privacy budget scope: Top-level site.  Proposals have the property that if you've been on a few sites that do some ad measurement thing, that should not degrade the functionality of the API on a new site that you go to.  This is often just practical: Hard to design a system that is reliable and consistent that advertisers and the ecosystem can trust if it's easy for "your budget" to be consumed by websites that you have no relationship with.
    * This brings us to a common theme: the privacy - security trade-off.  If we think of the budget as a shared resource, shared by parties that don't truste each other, then it's really easy for us to produce an API where some actors can deny access to others, by some eating all of a budget before someone else gets a change to do so — denial of service attack that can rob your competitors of revenue.
    * In ARA, but not IPA, the specific ad tech shows up in the budget scope, in an attempt to mitigate this DOS attack.  Any one proposal can mix-and-match a bunch of scopes, make constraints at different levels.  In ARA we have a top-level scope, and also separately a limit on the number of reporting sites as a total cap.  Budget across lots of different scopes — if we end up in a situation where different vendors need to set knobs in different places, might be hard to get alignment in some scopes, but would be better if we could get alignment in broad scopes at least.  Could end up in a situation where we might have very broad limits in high-elvel scopes that we need to tighten up in more narrow ones.
* Brian: The information that is budgeted, is there a good definition of that?
* Charlie: That was point #2 in the different privacy discussions list!  For DP, Entropy, and K-anonymity, the budget concept really only makes sense for the first two.  The budget only makes sense if you have some notion of "composition" — when you release data once and then later release data a second time, there's no way for K-anon to consider the result, while DP and Entropy / information-gain / information theoretic definition, there are formal definitions of what that sort of addition looks like.  In DP this is often the parameter epsilon, in information-gain metric this is usually bits of information.
* Brian: If we have a privacy budget that says you can only emit 200 bytes of data and those describe the last 10 sites that you were on, then constraining that number of bytes does not constrain how much you're tracked.  I assume this somehow constraints things in different dimensions?
* Charlie: Let me rephrase: If we're just talking about epsilon or bits, what is the scope of information that we're considering?  If I load cnn.com right now, it's going to load megabytes of data, issue a thousand network requests — but that's not all relevant or under consideration for the budget, so what are we actually measuring?
* Brian: More like: If you try to control information leakage by metering data, then if the data released as an identifier, just 64 bits, that's not much data but it's a huge leakage.
* Charlie: That resonates.  This is what makes our job hard.
* Brian: If I've got a privacy budget with the number of bits, if those bits are not providing much information about the specifics of this report but could be used in another context to provide a lot more information, how do we account for that?
* Charlie: Right, goes to what is linkable to a report.  In ARA we have a high-entropy identifier, because of the linkage that we add to the report, the thing we're most worried about is that we've already given away a user identifier on one site, and we're most worried about giving out an identifier on a second site.  In something focused on aggregate reports like IPA, there's only risk if you leak a user identifier on one site and another site simultaneously.  So what you need to worry about leaking is different in the two contexts.
* Brian: If I have a campaign and I target that campaign at a specific user, and I get a list of all the publishers that saw that user, then I got information about one user.  There's no way for ARA to know that.  So privacy budget, the only way to prevent that information leak is to not allow the data to be provided.
* Charlie: Your hypothetical already involves the user's privacy being leaked — you're assuming that you had some targeting criterion that you can use across sites, so you're assuming an attacker that already had succeeded at tracking across sites.
* Brian: That's what everyone wants with first-party data and email addresses.
* Charlie: If a user's privacy has already been completely violated, then there's not too much that our APIs can provide.  We should think about how we want our APIs to work in the event that a full or partial violation has already happened: "you might have X information about the user but we're only adding Y more."  This is difficult — this is why an analysis often fixes an attacker or an attacker's capabilities.  One useful thing is that the DP guarantee models a worst-case attacker who knows a lot about the underlying dataset, and can bound the adversary's update in terms of its knowledge even in the face of some prior probability distribution of knowledge.  So DP assumes a worst-case threat model, and can sidestep some attacker modeling.
* Brian: My concern is that a privacy budget is about data bits leaked, and information is about data in context, and you can't really know the context.  I do want to ask about the part where you can't have a continuous budget because at some point you run out.  Are there any natural boundaries?  Instead of "every 7 days" could you do something like "per campaign"?
* Charlie: In platform APIs, need some boundary that the platform can enforce.  Platform knows what time it is, knows what's the top-level site you're visiting or that is receiving an HTTP request.  I am interested in ways where we can let the platform have control over more narrow things, could be useful.  But the budget scope needs to be something that the platform has a way to understand, rather than something an adversary can lie about.
* Brian: So only things local to the browser?
* Charlie: You can be creative, maybe could pre-declare something so that the browser can trust it so that it's truthful or consistent across users
* Brian: Time windows might be what's available to us but not what's useful.
* Nick what do we mean/how do we ensure it’s a budget for a single specific person. Budget for a user or for the entity doing queries?: Are we talking about budget for user, or for the person doing queries?
* Charlie: We sometimes use the term interchangeably.  Budget is trying to measure how much user data is leaking, keyed to a specific scope.  When we talk about budgeting from the querier POV, we talk about "you have this much budget for this scope left, and you can't learn more about that user in that scope."  Comes up when you want to support multiple queries over the same data — could query data over last week once, and I leak X bits per user on average, or epsilon DP budget.  But if I do double the noise and do the query twice, get the same budget usage.  Querier's budget is the way they eat that amount of user privacy budget loss.
* Nick: So it's how much budget for any particular user could be revealed.  Are we going to have the definition of an individual user?
* Charlie: That shows up — in some ways it's the thing that you are trying to protect.  For something like ARA, if we got rid of all scoping options, a user would be a device; controls how much a user contributes to those aggregates.  As we add user, we're protecting the user across these different scopes.  User is the base level of the privacy scopes, which in IPA is the match key and in ARA is the browser instance / the browser profile that is the stand-in for the user.  There is some user proxy definitions going on in all these proposals.  So ARA can't bound across all of a user's devices, IPA can try
* Martin: IPA can't do that either — we don't have that luxury because match key providers might not make that information available to the API.  There's a nice way of thinking about this: For a user, the scope is the bucket that they are throwing their information into, and for ad techs it's the bucket they are drawing information out of.  If I'm a person interacting with multiple sites across multiple buckets, I'm contributing to all these buckets over time, and report collectors users can draw from all of them.  The DOS risk that Charlie mentioned is that if a bucket is too small, someone else might draw everything out of the bucket you want to use. &lt;scribe missed some stuff here, sorry>
* Martin: The firm guarantees that we'd like to provide on scope were per-site and per-time.  The cross-device thing means we need to add devices into the mix, which is annoying.  We were also thinking about policy controls to help improve bounds — eg. for a large company that has multiple sites and can induce people to link their identities across sites, maybe budgets should be pooled if identity is, so as a matter of principle and policy, the system will collapse budgets across multiple sites to avoid someone making an end-run around budgeting.  
* Charlie: There are things beyond policy controls: the First Party Sets proposal…
* Martin: I knew you were going to say that.  It's terrible, let's not go there.
* Charlie: We would like some more structure rather than just defining our own policy, so that if we have some other invention somewhere else, we could piggy-back on it.
* Martin: Also if we're doing TEEs or helper party networks that cost something, the fac that someone needs to produce more payment instruments helps tighten up also.
* Aram: Let's try to wrap this up and take a break.  We've discussed before the idea that IP Blindness might help, might mean you can have more privacy budget elsewhere?
* Martin: Privacy budgets in this context basically assumes you don't have any other cross-site correlators to re-identify people.  The unsaid assumption is that people don't look at IP addresses, but this is the grand lie that people tell ourselves.  A lot of these protections don't work if people use fingerprinting or IP to re-identify people.
* Charlie: This relates to what I was saying before to Brian about the context in which the data is being leaked.  The relative cross-site data in ARA comes with useful context — IP address is a similar thing to think about.
* Aram: There is a lot of ongoing work to keep the IP address from being a problem.  There's a lot of work making participants in the ad tech landscape not share IP addresses for legal concerns and reasons.  If we can assume it's not being shared, or if we could use that in budgeting, they might end up satisfied somehow.  There may be legal as well as technical remedies here.  Changes in GDPR, California Virginia Colorado privacy rules about using the IP address, etc.  Things that are pushing participants on publisher and ad side to strip IP addresses out of consideration for legal protection reasons.
* Martin: Some of these IP protection mechanisms will be important for the system we're building.  We should keep using these systems there, like OHTTP in FLEDGE.  But we can't assume they're being used for general web browsing.
* Aram: Legal interpretations are more extensive than that — we're looking at mechanisms to ensure that nobody gets IP addresses on our page, not just the top-level sites.
* Ben: I want to know what the goal of this discussion is.  We talked at length, ranged around a bunch of topics — privacy budgets, IP blindness — but not closer to consensus on anything.  I would like for us to have some goal and drive to consensus on that.
* Aram: People are asking for clarity when our survey saw lack of consensus, so when we have shared understanding, we get to a place where we can use that for further discussions and proposal-building.

– [scribe change]



* Aram: getting specific tradeoffs, let’s talk through and get consensus on those specific tradeoffs.
* Charlie:We have a specific tradeoff between security and privacy in adding narrower scopes to address the security issue of people taking budget from others. We may not be able to get consensus on exactly the right scope. Narrower scope than just user/time is something we are okay considering. Tradeoffs exist and we are choosing a point on this spectrum. Think we should agree to some budget re-setting. Not feasible for us to build something useful that will turn off the spigot.
    * Comfortable with user/device/time dimension, we may leak up to an infinite amount of information on a user over infinite time. 
* Martin: cap on the rate of information leaked per time period. For some apis, may be able to use visits to a website rather than time.  The denominator might change to be something other than time, but it might approximate to time.
* Ben: Agree. Don’t know of a feasible mechanism more than a rate over time. Internal to Meta, there are ways to have lifetime limits, but that only works with data deletion, and I don’t know how to enforce data deletion on the Web. APIs shouldn’t continually leak more and more information to sites over time if you don’t ever visit the site again.
* Brian: natural time-bound in advertising, windows after which the information won’t have meaning in the advertising context. Should have expiry times. When reporting to an advertiser, if they don’t use it within a certain time, then it’s deleted.
* Charlie: Not sure formally how to do that; platform can’t be aware/confident that some data was deleted by the advertiser. Summary reports that are released are permanent privacy loss with no way to undo.
* Nick: I would be comfortable with scoping to site/query/etc if there were some external policy or accountability to know that people aren't colluding to go beyond the stated budget.  Can we use other accountability mechanisms to avoid just making our budgeting work irrelevant?
* Charlie: Please elaborate!
* Nick: Will do
* Kleber: Ben you mentioned limited/non-ongoing provision of information to sites that people don’t visit any more.  Good principle, even if we release information over time.  In IPA, is there a limit on validity for match keys?  Because match key providers might be able to continuously siphon information.
* Ben: when generating an encrypted match key, you will bind it to the epoch, so it can’t be used outside of that time.  Helpers will need to know and can reject bad / validate it. Requesters have to supply the Epoch That has a bound.  A malicious MKP has an attack that it can mount that is very much in that direction that is deeply concerning to us.
* Charlie: binding to epoch is only on getting the match key, not on setting the match key? 
* Ben: Yes.  setMatchKey gives the person who sets the match key some ability to break these bounds.
* Michael: This problem is more serious than that, or at least it seems to be.  In IPA, if you are talking about the ability to do cross-browser joins, the malicious party can make up a browser and pretend that you are using that browser, so they can get a match key.  The restriction on only giving information to sites that people go to can be circumvented by pretending.
* Ben: preview of issue… Ben Case was doing a formalism, and discovered this. If you setMatchKey and then some legitimate site requests an event from a legitimate visit.  You can generate synthetic events from sock-puppet sites.  Those sites get distinct budgets, which can all measure that legitimate event, circumventing the limit on the privacy budget.  We haven’t come up with any good ideas.  No way of attesting that events are genuine.  Maybe we don’t have setMatchKey and only have same-device attribution.  We’re still thinking about it.  Charlie suggested that maybe only “trusted” parties can set a match key.  We don’t love that because it is only as good as the trustworthiness of the match key provider.
* Michael: I might have a distinct threat, but I will need to think about it.
* [Detailed discussion of a particular issue and threat on IPA that we should just take offline.]
* Aram: not desirable for marketers/sellers to enroll a user as a potential match forever. Even a month is probably more than is useful.
* Aram: Let’s aim for a call for rough consensus.
* Brian: monitoring privacy budget consumed by various actors in order to see whether someone is acting inappropriately to gain more than appropriate information? Controls around the systems to prevent abuse.
* Charlie: Possible, to be considered later.
* Ben: support call for consensus on APIs that can’t enforce deletion and therefore have continual release over time, and the APIs constrain the rate, and constrain the release to parties that the user has interacted with.
* Charlie: for a private measurement system, we accept that as users browse the web over time, data will be released about that user over time with a narrow, configurable rate limit over time/interaction.
* Ben: proportional to time, correlated with the number of sites that you visit (linear not quadratic or some other proportion),
* Brian: +1 to proposal. The more you use the web, more privacy/data is leaking. So your only option is to use the web less.
* Charlie: Should still have control mechanisms, like turning off the measurement capability. Not that there is no hope or that you have to accept it.
* Martin: In using the Web, some amount of information is released to sites, visiting pages and mouse movements. Measurement features should be much less revealing.
* Brian: I just gave a headline, but putting it into context like that helps.
* Aram: consensus call on ‘for a private measurement system, we accept that as users browse the web over time, data will be released about that user over time with a narrow, configurable rate limit over time/interaction.’
* Shivan: Is there a formal statement on github that we are reviewing?
* Martin: Formalism will depend on the particular implementation, whether it’s DP/information-theoretic. But currently discussing it is a little more abstract.
* Shivan: Spectrum that user agents could work under.
* Martin: Different browsers may implement the proposals with different values or qualifications.

    Consensus call on this “feature”: \



    For a private measurement system, we accept that as users browse the web over time, data will be released about that user over time with a narrow, configurable rate limit over time/interaction

* Brian: Someone can write it up in more detail.
* Aram: rough consensus on this as a feature. No objections, rough consensus.

Aram: different pieces of privacy budget may be picked up in future.


### Meeting Planning


#### Review next meeting

Aram/Sean: See [https://github.com/patcg/meetings/tree/main/2023/05/02-telecon](https://github.com/patcg/meetings/tree/main/2023/05/02-telecon)

Scheduled meeting for May 2nd/4th; details in the repo. Agenda should be planned further in advance and get more attendance.


#### June Meeting -> F2F

Sean: In late stages of arranging a meeting location, potentially in London. Hope to close the deal within the next week. Trying to confirm in order to get 8 weeks of lead time.

Aram: please propose agenda items early/often, so that we can plan out agendas in more detail and further in advance.


## Participants Day 1



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Jay Kishigami (W3C)
4. Brian May (dstillery)
5. Erik Taubeneck (Meta)
6. Shivan Kaul Sahib (Brave)
7. Michael Kleber (Google Chrome)
8. Ben Savage (Meta)
9. Nick Doty (CDT)
10. Martin Thomson (Mozilla)
11. Sam Weiler (W3C)
12. Charlie Harrison (Google Chrome)
13. Nicholas Longcroft (OwnYou)
14. Mark Nottingham (Cloudflare)
15. James Aylett (Omnicom / Annalect)
16. Richa Jain (Meta)
17. Thomas Prieur (Criteo)
18. Xiaoqian Wu (W3C)


## Participants Day 2



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Brian May (dstillery)
4. Jay Kishigami (W3C)
5. Nick Doty (CDT)
6. Shivan Sahib (Brave)
7. Martin Thomson (Mozilla)
8. Michael Kleber (Google Chrome)
9. Laura Book (Snap)
10. Charlie Harrison (Google Chrome)
11. Ben Savage (Meta)
12. Sam Weiler (W3C)
13. James Aylett (Omnicom / Annalect)
14. Severin Ferrand (Google)
15. Thomas Prieur(Criteo) 
16. Nicholas Longcroft (OwnYou)
17. Przemyslaw Iwanczak (RTB House SA)
18. Achim Schlosser (European netID Foundation)
19. Joey Knightbrook (Snap)
