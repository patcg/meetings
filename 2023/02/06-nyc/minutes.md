# Private Advertising Technology Community Group Minutes - 2023-02 Meeting

## Agenda

- Day 1
  - \<= 20m: Hellos, Intros, Physical space ground rules, Google Doc, Call for Scribes
  - == 20m:[Review baseline requirements for Private Measurement from participants](https://github.com/patcg/meetings/issues/91)
  - == 30m:[Remove "draft" label from Threat Model document](https://github.com/patcg/meetings/issues/93)
  - == 45m:[Review the PRs on PATWG charter ready for consensus calls](https://github.com/patcg/patwg-charter/pulls?q=is%3Apr+is%3Aopen+label%3Acall-for-consensus)
  - == 15m: Process Discussion[on Privacy Principles](https://github.com/patcg/meetings/issues/101)
  - == 45m: Lunch Break
  - \<= 1h:[Review PRs on PATWG charter that may not be ready for consensus calls](https://github.com/patcg/patwg-charter/pulls?q=is%3Apr+is%3Aopen+label%3Acomment-response+-label%3Acall-for-consensus).
  - ~15m: Updates on PATCG organization, schedule, next meetings
  - Industry updates around privacy features and trials
    - \<= 45m:[Updates and lessons from the Attribution Reporting API Origin Trial](https://github.com/patcg/meetings/issues/95)
    - == 15m break
    - \<= 30m:[Use cases and principles for Attribution/Measurement proposals](https://github.com/patcg/meetings/issues/96)
    - =\> 30m:[Update on the status of Topics API + Q&A](https://github.com/patcg/meetings/issues/92)
  - == 5m: Day 1 wrap up.
  -

- Day 2
  - == 5m: Intro, Recap Q&A, Call for Scribes
  - =\> 1h 25m:[IPA Status Update](https://github.com/patcg/meetings/issues/70) led by[@eriktaubeneck](https://github.com/eriktaubeneck)
  - \<= 1h 25m:[Further MVP Discussion](https://github.com/patcg/meetings/issues/56) and Setting up MVP Survey led by[@aramzs](https://github.com/aramzs) (and hopefully others)
    - Intro / Overview
    - \<= 30m: Absolutely Required
    - \<= 25m: Nice to have / Advanced Capabilities
    - \<= 30m: Survey Design
  - == 5m: Closing

## Day 1

## \<= 10m: Intro, Google Doc, Call for Scribes

## \<= 1h Threat Model: remove "draft" label

On the subject of the _Threat Model Document_ entitled [Security Considerations](https://github.com/patcg/docs-and-reports/tree/main/threat-model).

Erik: This is a pull request: [Threat Model Update](https://github.com/patcg/meetings/issues/93). I've updated this to remove the "draft" status. It still says its a living document, a working threat model. Not all issues resolved. It's what we are currently considering. Any objections to that change? Not saying this cannot be changed, but saying we're roughly on the same page with regards to where the document stands. Probably the most obvious piece still missing is some description of the "secure hardware" component. If anyone wants to volunteer to open a PR for that section it would be appreciated.

Aram: Opening queue. Any concerns? Or volunteers?

Martin: Will point out this is an opportunity for people to review and object. We discussed bringing it here to induce people to expend the effort to review, and raise issues if it doesn't agree with what they say. If people don't agree with it, but haven't raised issues that's not great. One option is to give everyone a chance to review - and merge it at the end of that.

Erik: I support that. No need to merge today.

Nick: I have no objections with the "living document". The document is entitled "security", but is it covering "privacy" as well? We have a separate agenda item to talk about privacy considerations. I've opened some issues about that. I wouldn't want it to be implied that this covers everything the group cares about regarding privacy.

Charlie: From a process perspective, what's the formal distinction between a "draft" and a "living document"? Are we signaling this is "up to date" with the general consensus of the participants? Any other formal significance?

Erik: That's my intention. Don't have a working group - but as Martin said, we want everyone to review this and see if they agree or disagree.

Aram: Under the W3C, the "living document" is a document available to use in our process, but is expected to be continuously updated through a formal process.

Martin: I don't think we publish this as an output of the group, but more to document a threat model and how we deal with that. To respond to Nick, I think the privacy questions are more nuanced and difficult than the security ones. I think we maintain this as a security document and avoid getting into the tricky privacy ones - which will require a lot more work. This is a pretty pragmatic document, here are the actors / capabilities / etc. The privacy document will always be far behind in terms of maturity.

Erik: +1. I think it's sensible to have 2 documents.

Aram: I think the main intent of this change is it's a document we will be referring to more formally.

Erik: Yes, and I'm happy to change wording to reflect that. Anyone willing to take a stab at the hardware piece.

Maryana: What are we looking for? Analysis?

Kyle: I can volunteer.

Erik: There is a section in there discussing multiparty computation. It's only a paragraph. Looking for something similar to that. We sort of reference these two modes of security, but the actual description for what that might look like is just a TODO.

Aram: Any objections to this threat model should be done in the next 2 weeks. If there are none, we merge this and start using it for our work.

Maryana: Just to clarify, we are not providing an assessment right?

Aram: Just describing the technology and the threats.

Erik: What capabilities would the actors have under those paradigms. No assessment of if that is acceptable or not.

Sean: You can modify a living document by just opening a PR. We don't even have to wait for the next meeting. We can have discussions on the PRs.

Aram: We can use the meetings for consensus calls based on the discussions on.

## == 20m:[Review baseline requirements for Private Measurement from participants](https://github.com/patcg/meetings/issues/91)

Aram: We came up with questions. It's a poll. I want to put in the Google doc. People can sit here and take it. Before we move to that I want to ask a question. As it stands, the survey asks for your organizational affiliation. That will be visible only to me. I'll make a chart that does not emit that organizational affiliation. It's useful for we the chairs to facilitate conversations between strongly opinionated folks. Are people OK with that being a required question? I can switch it off of required mode. I don't hear any objections. If for whatever reason you aren't comfortable - put your organizational affiliation in as "null".

[https://forms.gle/MSo9gTqX3SeuxWuc6](https://forms.gle/MSo9gTqX3SeuxWuc6)

Charlie: two things. One, I was drafting up text responses. I think it was useful to be able to say something about my answer, like \*why\* I thought a particular way. I think it would be useful to explain \*why\*. I'm also happy having my comments being public and associated with my name. I get not everyone will be. The form doesn't support that right now.

Aram: Put it on the agenda. If you want to remain anonymous - reach out to me or the "chairs" email, and I'll put it into the thread. Those you can give to me after this meeting.

Luke: I had a question on the first slide. "Is an API sufficient"... what's the alternative?

Charlie: I think the key part is a "private computation configuration", which means "servers".

Martin: I think it's "necessary" but not sufficient.

Charlie: If you're \*strongly opposed\* to using any kind of trusted server configuration - we want to know that.

Aram: While all of the points on this scale are important - we are looking for strong objections and what's important.

Luke: I think if the word was "necessary". "Sufficient" makes me confused… I'm sorry…. I'm being pedantic.

Erik: I think the intention is "is it acceptable".

Luke: I think regardless of what you do, you need some configuration that goes through an API to specify things.

Aram: I think we are assuming an API of some sort will be involved. This is more about does that API go through some kind of "private computation configuration".

Charlie: This used to say "trusted server". I think it's more like "off device… are you OK with it…"

Erik: We went back and forth on that - because nobody wants just one big trusted server.

Aram: I've updated the question wording in the poll.

Brian: With respect to Charlie's question about explaining our reasoning, do we have a number or place?

Aram: Put it in the thread in issue #91. Otherwise I worry we will have 5 issues about a single topic.

## == 45m:[Review the PRs on PATWG charter ready for consensus calls](https://github.com/patcg/patwg-charter/pulls?q=is%3Apr+is%3Aopen+label%3Acall-for-consensus)

Scribe: Charlie Harrison

- Aram: We are first going through the call-for-consensus issues, they will be the easiest to go through.
- Number 28: technical measures scope front and center
  - [https://github.com/patcg/patwg-charter/pull/28](https://github.com/patcg/patwg-charter/pull/28)
  - Make it clear we are a technical working group
  - Not creating documents of law, etc. Just engineering
  - Everyone OK with "predominantly" technical means
  - Erik T: Don't want to preclude policy for privacy
  - Consensus, merging
- Number 43: Mozilla FO resolution
  - [https://github.com/patcg/patwg-charter/pull/43](https://github.com/patcg/patwg-charter/pull/43)
  - Martin: Sam is no longer with W3C
  - Aram: This changes
    - Adds current chairs of the CG
    - Adds chairs to the WG
    - Rep from the W3C, whose position is in motion, will be figured out in the W3C
    - Modifies a testing plan, with a test suite
    - Additional clarity of the specification stages, with respect to passing tests
  - Consensus, merging
- Number 52: Grammatical precision in Normative Specifications
  - [https://github.com/patcg/patwg-charter/pull/52](https://github.com/patcg/patwg-charter/pull/52)
  - Aram: Grammar change, it's basically punctuation
  - Martin: commas, surely?
  - Aram: Complex lists should use semicolons!
  - Consensus, merging
- Number 53: Make design teams work clearly under IPR
  - [https://github.com/patcg/patwg-charter/pull/53](https://github.com/patcg/patwg-charter/pull/53)
  - Aram: Makes it clear that design teams are subject to IPR. There are a few comments.
  - Applying Martin's suggestion
  - Nick Doty: Was the first sentence intentional? IPR policy does not state that.
  - Aram: the intent is to make clear that the design teams work under w3c rules, that particular line is not required
  - Michael Kleber: Is the point that we want to avoid information being considered by design teams which cannot be made part of public record?
  - Aram: We want to make sure that the groups operate in the open.
  - Kleber: Is there some specific behavior not ok?
  - Aram: Rules under which all operations of the working groups are clear. No anomalous operational constraints. Generally these things are public, IPR commitments apply. Any objections?
  - Consensus, merging
- Number 54: Location of term definitions
  - [https://github.com/patcg/patwg-charter/pull/54](https://github.com/patcg/patwg-charter/pull/54)
  - Aram: Significant opposition to this change. Objections to closing out?
  - Erik: Is it standard to include this in WG charters? Is there are reason this is specifically called out.
  - Aram: Don't think it is particularly standard, but not sure if it's never happened before. Some questions about scope, how the w3c discussions would run. Constrained by the rules of the W3C. Idea was to synthesize concerns about specificity of scope.
  - Erik: but this isn't about the rules, just about terminology
  - Phillippe: This document hasn't been vetted by the whole W3C membership. There are ways to address it (AC reviews). Right now you are referencing a document on github.io, would prefer that you are referencing a document with a date that doesn't get changed, otherwise a change is effectively a change to the charter itself.
  - Aram: Referring to it for privacy terminology. We have a privacy document we are authoring within this group that might establish some of these terms, perhaps differently. Other thing discussed, what is the definition of privacy? Would establish a definition as established in the TAG document. When we last discussed, definition of privacy, we talked about a relative issue, privacy is a thing that we want to accomplish through this work. Not necessarily a strongly defined term in the traditional sense. This would define it.
  - Martin: You can put these things in charters, binds to whatever we wrote down. We can push the discussion to the WG. The reason to put it in the charter up front, everyone goes in understanding the terms. For definitional things like this it's probably not necessary, it's useful for this to remain open for discussion, especially since definitions are heavily contested.
  - Aram: If we reach consensus to remove, that's what we're agreeing on
  - Brian May: Spirit of this comment is that there should be some stable, versioned definitions people should refer to. Stable and referable. We should make sure we're referring to a versioned definition. We should require there be something defining the terminology in cases where the terminology is important and and subject to different interpretations.
  - Nick: there are links to terminology elsewhere in the doc, but if we want to remove all references to a non-dated draft, we should change those too. We should change the earlier paragraph to stay consistent.
  - Aram: Not directly related to this PR, we can file another PR to change the links to be dated.
  - Philippe: Added a link in the slack chat. Charter is always a balancing act, too many or two few constraints
  - Erik: Do we set ourselves up to future problems if TAG does get the document vetted.
  - Philippe: We'll have problems whether its in our charter or not
  - Erik: what I want to avoid is that if we come up with our own document in the WG that differs from what the TAG has, would we have to resolve this?
  - Philippe: We are supposed to work in sync with the TAG, we expect a review from TAG. If out of sync, we could be on the wrong path. It is "built-in", whether you specify in our charter or not.
  - Alex: when do you want to have this battle?
  - Aram: we may end up coming back to this. Enough objection to the text of the PR, that this group could find consensus to drop. Consensus call to close this PR without merging.
  - Consensus, closing

I find myself unable to make a PR for the links, can someone do one for me (Martin):

enabling

of \<a href="https://www.w3.org/TR/2022/DNOTE-privacy-principles-20221214/#dfn-cross-site-recognition"\>cross-site\</a\>

or \<a href="https://www.w3.org/TR/2022/DNOTE-privacy-principles-20221214/#dfn-cross-context-recognition"\>cross-context\</a\>

recognition of users or

enabling \<a href="https://www.w3.org/TR/2022/DNOTE-privacy-principles-20221214/#dfn-same-site-recognition"\>same-site

recognition\</a\> of users across the clearing of state.

## == 15m: Process Discussion[on Privacy Principles](https://github.com/patcg/meetings/issues/101)

- Nick: this group decided to take on this work item. Interest in an editorial group. Actual writing hasn't been done yet. Suggest that we change the editors and find some volunteers to flesh out the document.
- Aram: spoke with Robin, technically not a member of this group anyways, so it's appropriate to change editors. Nick are you volunteering to lead the group?
- Nick: yes, but it shouldn't be just me
- Aram: express our privacy principles through the proposals we make, recording them into this document.
- Aram: Proposals would crystalize privacy principles, recorded more abstractly. It is a historical note, not necessarily how the document will proceed. Nick feel free to comment if you have an opinion
- Nick: Some of both. When we have some work in some proposals, what privacy guarantees we're trying to provide, they should be abstracted and recorded here. Can also go the other way (e.g. Martin's suggestion about entropy).
- Mariana: this has to be a companion document to the threat model, in sync with it. In discussion w/ threat model document, we said privacy will be complicated and punted. Is this doc tasked w/ figuring this out?
- Nick: Not sure we "punted", but yes this is the appropriate place for this document.
- Aram: Groups of editors should coordinate and talk w/ each other.
- Aram: volunteers?
- **Brian May: Interested in participating** , but don't have formal privacy/policy background. We were going to try to put together something (principles) without stating exactly what privacy is
- **Michael Kleber volunteered**
- **Graham Mudd volunteered**
- Aram: we've got our first few volunteers, moving forward with this document. Might have more time tomorrow discussing this doc. If we can slot it in we will
- That's it for the first half of our day today. 45 mins on the agenda. Try to get here promptly at 12:45

## == 45m: Lunch Break

## \<= 45m:[Review PRs on PATWG charter that may not be ready for consensus calls](https://github.com/patcg/patwg-charter/pulls?q=is%3Apr+is%3Aopen+label%3Acomment-response+-label%3Acall-for-consensus).

Scribe: Graham Mudd

- Aram: May not be able to resolve these. Some of these PRs are directly contradictory. Goal is to discuss not close. Hope to push toward additional responses.
- Aram: Starting with #45. Background: This isn't necessarily my position. Objector was concerned with user agent being able to do privileged processing that others wouldn't be able to. For example, if we came up with a privacy proposal that stopped people from using window.screen from using it for fingerprinting. If, for example, FLEDGE used window.screen as a targeting variable, but others wouldn't be able to access it because it was deemed a privacy concern. That's rough example. Queue open.
- Ben: Strongly disagree. Doesn't think it makes sense to object to this. This is the nature of the world. Browsers have access to lots of sensitive information – that's the way it will always be. Move to close without merging. The PR asks us to stipulate that browsers disclose any information they have available to them that could be used for advertising.
- Nick: Agree in substance. But there is also a statement that user agent is not a data processor as defined in GDPR. If we clarified that user agent doesn't have a particularly stipulated role in GDPR, I'd be fine with.
- Martin: +1 we should close. The role of the user agent is special. It acts on the behalf of the user. To eliminate the distinction between the user agent and other entities destroys the value of having that agent.
- Alex: +1 to all the above comments.
- Aram: Reasonable agreement to close the PR. Do we have consensus to have a vote?
- Erik: Looking at the diff, it looks like it's just adding the line about the role of user agent.
- Martin: I don't think we need to put anything into the charter that stipulates the role of the user agent. There's enough material in the canon.
- Aram: I think it would be helpful to define this because it will help us with future objections. I think we should establish another PR that establishes the role of the user agent, it will significantly reduce the noise surrounding further objections.
- Martin: I'm happy to put something together.
- Aram: That would be great.
- Consensus to have a vote close.
- Consensus to close this issue without merging closed.
- Brian: Whoever filed this PR may not be comfortable speaking up.
- Aram: Yes, but htat's the nature of this process. With that noted, moved to close this objection.
- Aram: On to #46. Goal is to establish that the working group should make clear what it is trying to accomplish at what cost to utility/privacy.
- Charlie: Two things in this PR. 1) Statement about privacy/utility tradeoff 2) what we're trading off is data about the user for utility. #2 is not clear and could use more refinement before being merged.
- Nick: Similar feeling. Transparency into privacy/utility is good. Not clear change on line 272, it's much more complicated – not clear that there's a linear relationship between privacy and the amount of user data shared.
- Aram: Let's make a note to separate out these two issues – 272 and 278.
- Erik: Agree 272 isn't particularly helpful because these changes take place in the context of broader issues (for example, deprecation of cookies). On 278, we don't have a definition of utility. We have a group focused on privacy.
- Aram: In terms of defining utility, would the work that Ben is doing defining business group's use cases be a good starting point for defining utility?
- Erik: Not sure. Challenge is that a use case has many potential definitions of utility. Much more challenging than measuring privacy (episilon).
- Aram: Think we should move on. Not sure we are looking for a quantification of utility.
- Erik: May want to say 'functionality' instead of 'utility' since utility is typically quantified.
- Charlie: I do think we want a measure of utility. May need to be use case specific. Do think the business group should consider this as a work item.
- Erik: Don't disagree. But that means if we're going to refer to utility we should have a way to quantify it.
- Aram: I think we'll probably need both. I think the intent of the objection was focused on functionality. We should ask the business group for this. They are changing chairs so we probably need to author a request to them. Erik, if you have a version of the functionality focused language, we could evaluate that.
- Erik: Might be as easy as swapping in 'functionality' for utility in 278.
- Ben: This group isn't the group that's focused on removing fingerprinting or stopping cross site tracking. The objection implies that we are making a tradeoff. This group is really focused on adding something new – not restricting access to anything. Would be fine with sharing views on how a new approach compares to a historical approach.
- Brian: Think we should focus on 'information' not 'data.' Think we should be careful not to constrain anti-fraud approaches.
- Erik: +1 to information instead of data
- Aram: We'll split the issues as discussed. Next up 47. Lot of discussion here. Generally moving toward closing. The goal is to secure the role of non-browser entities in the ability transactions that enable to privacy. Running low on time. Queue quickly.
- Erik: Move to close. Will constrain browser vendors in ways that are unprecedented.
- Nick: Don't think we need this but do think we should make a note that we don't hard code the entities. Maybe we don't need to change the charter but we should document.
- Kleber: There are many places where the browser has an opinion about entities outside the browser. Browsers pick and choose certificate authorities, for example.
- Aram: Closed consensus on closing without merging. 47 closed without merging.
- Aram: 48. Charter should be more specific about what rules it follows. Encode something that is an extension of the anti-competitive guidance that makes it extremely clear.
- Brian: Think we should get rid of this. It's unnecessary and encumbers an already difficult process.
- Charlie: Motion for consensus to close.
- Nick: Might be helpful to make clear that design teams don't make decisions, they bring proposals to the working group.
- Aram: Hear a motion to close this without merging. No objections. Closed this PR without merging.
- Aram: 49.
- Martin: Think we need to address Tess's comment. Think we need specific wording suggestion to consider.
- Aram: In general, if folks have objections to charter language should propose replacement language.
- Nick: think this was a problem earlier too. Some of the proposals we've evaluated include entities outside of the user agents (like helper parties) – does the scope include these?
- Aram: I think the scope would include these entities.
- Charlie: More context on the underlying issue here?
- Aram: Think the idea is just that it was overly complex language, not that it was overly constraining.
- Martin: Think this is a difficult problem, so language from Tess would really help.
- Michael: For some of these objections to the scope of the group it might be helpful to make a clear statement about what should be in-scope to ensure there aren't any statements that preclude things we want to work on. For example, in the scope of conversion measurement work we're doing, if we believe that conversions that occur in apps (and not the browser) should be include in scope, let's make that clear.
- Aram: Do you think we should have a conversation here or put together a proposal? I think the privacy principles group should develop a document that clarifies scope of the working group.
- Aram: 50, which is in direct conflict with 49. This restricts the scope in the other direction. Think our decision to have the privacy principles group work on a scope document addresses this issue as well.
- Nick: Concerned about adding a new concept 'browser like user agents.' Can someone explain why?
- Aram: This is direct language and I can't speculate as to why.
- Philippe: I think the intent here may be to exclude applications or other types of agents?
- Charlie: Really don't think we should merge this unless we have a better understanding of 'browser like user agents'. This is probably an attempt to take mobile applications out of scope, which is counter to what we've discussed in the past.
- Brian: Suggest we get some specificity on what is meant by browser-like, what features.
- Aram: Will attempt to get more clarity on the language.
- Aram: 51. Another scope change. Goal seems to be to formalize something that is assumed to be part of the standard W3C process. Goal is to clarify that the group will produce open and standard protocols.
- Erik: You said 'provide' the PR says 'use'
- Aram: Intent isn't to say we can only use existing protocols.
- Erik: One can definitely read this to constrain the technologies we can utilize vs. produce.
- Charlie: Agree that there is ambiguity and may also constrain downstream non-open use cases, which we shouldn't attempt to constrain.
- Aram: Clearly the text can be improved.
- Martin: Agree that this can be improved and I'm happy to work on it.
- Aram: Ok, we'll focus on improving the language. May be redundant, but will help us resolve these formal objections.

## \<=15m: Updates on PATCG organization, schedule, next meetings

Sean: Now we're going to attempt to set the next few meetings. Question: Do we want to do one more additional in person meeting in addition to TPAC in Spain. Earliest it could probably be is in June so that we can give people enough time. Helpful if we can at least get agreement for the virtual meetings in March and May.

No objections. Locked in those dates.

Sean: Pushed to get consensus to do the June meeting in person. Location: Would probably be in Europe, but could possibly be in APAC. Proposed meeting dates:

Meeting timing: [https://github.com/patcg/meetings/issues/89](https://github.com/patcg/meetings/issues/89)

Nick: Yeah, it's a ton of work to do these in person. I think there are requirements for planning in these in advance are specific to WGs. The people that are worried about this should push us to create a WG. Not great to just continue indefinitely as a Community Group that just closely mimics what a WG would be doing.

Sean: Requirements: Somewhere in Europe, no NDA requirements, audio requirements

Ben: Move to consider Asia.

Kleber: Second that.

Sean: If asia, maybe a longer meeting.

Aram: Maybe consider combining with other CG/WG.

Erik: If we're considering f2f, can we not start on a Monday.

Ben: Real world crypto is March 27-29 in Tokyo. IETF is also around same time/place.

## Industry updates around privacy features and trials

## \<= 45m:[Updates and lessons from the Attribution Reporting API Origin Trial](https://github.com/patcg/meetings/issues/95)

[https://docs.google.com/presentation/d/1i8aa7DyLmmJKLVjzGXUpiY1vVbkOCkpr80vLnSNO3wE/edit?usp=sharing](https://docs.google.com/presentation/d/1i8aa7DyLmmJKLVjzGXUpiY1vVbkOCkpr80vLnSNO3wE/edit?usp=sharing)

Charlie Harrison (Google Chrome): Currently running an Origin Trial where we enable the ARA with real users with real Chrome devices. Wanted to give an update on how that's going, and lessons learned. Hopefully that's useful to any API this group puts out.

ARA is used on 0.4% of all page views in Chrome. [Via](https://chromestatus.com/metrics/feature/timeline/popularity/3365)[via](https://github.com/WICG/attribution-reporting-api/blob/main/ara-tester-list.md). This is a lot of web pages, getting pretty good coverage. In our repo, we have a table of active testers with those who've shared publicly that they are testing. This is only a subset, some testers are private.

In terms of scale, ARA has been in OT for quite a long time, and we've been making tweeks to it. In the last quarter or two, we're introduced a number of new features:

1. Debug reports, some are reliant on 3rd party cookies being enabled
2. Supported open issue where ads point to multiple destinations, i.e. user can convert on many different sites
3. Flexible attribution windows
4. Other minor features

Other's coming soon:

1. Integration with Android's Privacy Sandbox to support attribution across web and app, delegated to the OS
2. Proposed an integration with some of the crypto stuff in private state tokens, can have a signature that this was produced from a trigger that you verified
3. Better FLEDGE integration
4. Multi-cloud support

That's where we're at on the OT.

Now want to move to some lessons, tried to keep these pretty generic.

1. Report delays. We have two types of reports.
  1. Event-level: fine grained about the source and coarse grain about the trigger. Here the delay can be up to 30 days, as we are trying to disassociate these.
  2. Aggregate: Here the delay is up to an hour. Here the events are already disassociate by the aggregation.
  3. Have heard that the delays for event-level are too long.
  4. In practice as the browser, can only send reports when the browser is up and running. We aren't sending in the background, at least for now. This means we have ideal delays vs real delays, often longer than ideal. Need complicated retry logic, so you don't see loss. This decreases utility as the delays are longer, and increases complexity on the client.
  5. In practice, the extra delay scales with how long the ideal delays are. The longer the ideal delay, the more likely the browser isn't still open. For aggregatable reports, it's not as bad, but not entirely gone.
  6. Takeaways for delays:
    1. hurts utilities.
    2. Expect longer effective delays
    3. Some privacy risks (presence / IP tracking.) Could leak that your IP address changed.
    4. Almost impossible to eliminate with on-device attribution. Might need to send events unconditionally. For event level, may be impossible without a server side configuration.
2. It's really important and we've been focusing on. Somewhat of a problem with on-device. The algorithm for attribution is complex, and growing. The logic in the client is complicated, and the failures are opaque. Vast majority of failures leak cross site information, so we can't leak this. Makes the API really difficult to debug.
  1. We've added debug reports temporarily, and most require 3rd party cookies. 4 error cases for source registration, and 17 for attribution triggering. Immediate reports when attribution succeeds and 3rd party cookies exist.
  2. Building and launching a simulator.
  3. Note: Debugging tools links:
    1. Debug reports spec: [https://wicg.github.io/attribution-reporting-api/#attribution-debug-data](https://wicg.github.io/attribution-reporting-api/#attribution-debug-data)
    2. Noise Lab: [https://developer.chrome.com/docs/privacy-sandbox/summary-reports/design-decisions/](https://developer.chrome.com/docs/privacy-sandbox/summary-reports/design-decisions/)
    3. External simulation library: [https://github.com/privacysandbox/measurement-simulation](https://github.com/privacysandbox/measurement-simulation) (Web support coming)
    4. Chromium-specific simulation tool: [https://source.chromium.org/chromium/chromium/src/+/main:tools/attribution\_reporting/simulator\_main.cc](https://source.chromium.org/chromium/chromium/src/+/main:tools/attribution_reporting/simulator_main.cc)
  4. Takeaways: We should invest in as much tooling as possible. More work is needed on long term debugging strategies. We've invested in an easy way out, but want something that's sustainable even after 3rd party cookies are no longer available. We don't have it now, but are thinking about it. Any proposal will need a debugging story.
3. Aggregation function. Right now we expose a function for computing a fixed and noisy histogram. When you query the system, you list out the key space where you want to compute over. This is the simplest thing we could have done to support differential privacy. Other asks/feedback:
  1. Key discovery (e.g. exponential / non-enumerable key space.)
    1. For example, in FLEDGE, you may not know all the sites, and cannot enumerate them all.
  2. Distinct counting, Might want to say 10 users even if 1 user contributed 100 times.
  3. ML model training. Won't get into details now.
  4. Flexible privacy budgeting, e.g., daily budgets + a weekly roll up.
4. Takeaways: Should be built to accommodate a diversity of algorithms, to support a diversity of private measurement use cases.

Aram: Trigger attestation convo with anti-fraud group?)

Charlie: Chatted on the side.

Aram: Would be useful.

What are the critical use cases for event-level? Is this on the record anywhere?

Charlie: Not yet, opened an issue. Responses may come through privately or publicly. Will get to a slide later on explicit parameterization.

Aram: Did you consider debugging delegation to address privacy considerations? Some people delegate debugging to a service.

Charlie: Like a trusted service? Potentially in the realm of the sustainable long term evolution of this. There is a tradeoff of the privacy of the whole system. We'll need to treat these debug outputs like real outputs, should not elevate them as a different type of output. Would want them to be similar to a private computation system.

Brian: Can you talk about other debugging approaches?

Charlie: Beyond what Aram mentioned, are thinking about aggregate debugging reports. May not solve all the issues, but it's privacy positive and provides utility. In addition, having more simulations tools that can integrate directly with ad tech stacks. For example, we have a header validator in javascript. I don't think I have any silver bullet, and it might not exist.

Brian: Have you talked about sending a signal that "this is broken" but without details?

Charlie: Hiding information like that is on the table. Goes hand in hand with aggregates. Also investigating other teams adding adjacent reports. There was an issue on permissions / permission policy system. Asking that team to do error reporting.

Nick: Debugging conversation is useful. If I were trying to implement this, in my test setup can I turn on something in my browser to send clear text so I can see if it's working on my machine.

Charlie: Lots easier to support, and do have a Chrome flag. Doesn't evade the 3PC check, but it could. In general, the thing that's going to be difficult is scaled testing. Local testing will be easier and we can more or less solve it (at least for ARA.) The question I'm still grappling with is how much that will cover if we don't have scaled testing and debugging. Even potentially an enterprise setting where you wanted to test against all your employees. Could allow you to reduce the privacy settings because you could do that already with other means.

Ben: Thanks for sharing. Talking about reach and distinct counts. Realized that fell out of IPA for the user level capping. Do you have some user level capping for DP that could be leveraged?

Charlie: Challenge with ARA is that we do privacy budget accounting on device. I think we could probably come up with changes to limit that contribution to 1, the challenge is when we're doing accounting on the client, it's hard to support multiple use cases. User are contributing different amounts, and it's hard to make two queries across two sets of data, for example one for total value and one for total reach.

Ben: Earlier question about shorter delays. In general what we've found at FB, when training an ML model, the more recent the data, the better the model. Making data pipelines go faster can get wins. The event level seems primarily to support ML, and that would suffer from delays.

Charlie: Beyond just freshness, knowing the time between the events is useful (but this is explicitly trying to remove that.) It's also a problem for reporting. Aggregatable reports is more fine tuned, but you could support reporting dashboards with event level reports, and waiting 30 days for that is pretty difficult.

Joey Knightbrook: Key discovery problem. Is that a fundamental problem?

Charlie: We started with fixed histograms as an MVP. Thought we could support a majority of use cases from this. Some recent issues that lead us to consider prioritizing it more. It's also much easier to deploy if you don't have to keep track of keys. Probably a win, even if the utility is slightly lower.

Joey: So it's not a fundamental law.

Charlie: No I don't think any of these have hit that (except perhaps ML training.)

Luke: Debugging and having predictable outcomes. With the exposure notifications, we had some expected fixed distributions to know the right thing is coming out.

Charlie: So you inject some expected data.

Luke: It's a random number generated on the device.

Charlie: And you found bugs with that?

Luke: Yes

On key discovery, does it have to be done on conversion data. Can you just do it on the advertising data, since you already know that?

Charlie: Maybe I don't fully understand the suggestion. Also support keys coming from the conversion reports. In addition, with FLEDGE, some pieces of the key may not be immediately readable on the impression side. Can also use our API to do this by querying a lot of keys, but you increase the chance of false positives.

Charlie: Event level parameters:

1. Clicks: 3 bits of metadata, 3 reporting windows, and 3 attribution: 2925 output states.
2. Views: 1 bit of metadata, 1 reporting window, 1 attribution: 3 output states
3. Takeaways:
  1. If you don't use the full output space, you may be "paying" for utility that you aren't using
  2. Some advances in ML training techniques with label DP can take advantage of flexibility of having a prior on the features.

[Not sure where this is intended to go] Tweaks based on the number of output states and randomized reporting algorithm

Permissions: Initially we wanted some opt in. Also had a goal of making this adoptable. Murphy's law in ad tech "if you can think of it, it exists in ad tech deployments". Permissions policy is pretty fragile, and it requires boiling the ocean. We currently don't think we'll be able to ship, and instead will default to opt-out. Need to balance privacy, utility, and adoptability.

User data deletion:

1. With attribution on device, users can delete pending sources.
2. With delayed reporting, users can delete pending reports.
3. Double edge sword
  1. Probably don't want to send debug reports. Maybe can do this in aggregate.

Summary slide, won't go through it. More feedback needed on parameters like epsilon. Conclusion: we have some useful learnings. Continuing to ship improvements.

Aram: A great deal of data loss exists in the current world of measurement and the system has persisted, I'm not sure it should be a priority.

Alex C: The time delay has a bigger impact on debugging than previous loss.

Charlie: One thing different in ARA is that you can see an ad, delete 20 days later. Also user deletion in Chrome is overly conservative. It can cascade, and delays exasperate this.

Brian: Any sense of how it will scale?

Charlie: Do you mean the aggregation service?

Brian: All the pluses and minuses.

Charlie: We don't have evidence that things won't completely fall over. This should be fairly linear. Wouldn't expect the ratio of deleted reports to increase as we increase scale. Deploying to less sophisticated callers might struggle with the configuration. Default might be on the more difficult side.

## == 15m break

## \<= 30m:[Use cases and principles for Attribution/Measurement proposals](https://github.com/patcg/meetings/issues/96)

Discussing: [https://github.com/patcg/proposals/issues/14](https://github.com/patcg/proposals/issues/14)

Thomas: Want to talk about what use cases measurement should address. The survey talked about "how", but "what".

- Billing - publishers need to be able to bill for placements. Either CPM/CPA. Requires a good level of accuracy.
- Reporting - need to include common dimensions (list in issue), common metrics (KPIs). Needs to be flexible, so that dimensions and KPIs can be chosen. Needs to be reporting on brand safety performance after the fact. A/B testing.
- Legal req., optimization, piloting,
- Incident detection - compromise of accounts and other problems need to caught in near realtime
-

We wanted to reflect on what use cases we think attribution measurement should reflect - we wanted to survey what had worked and what things we think should be used.

Martin: (regarding legal requirements, how is this not a function of the bidding/placement process?)

Thomas: This is not currently how the system operates. Fenced frames and FLEDGE introduce this problem.

Michael: Need to think about this any time a decision about what ad to show happens in the browser.

Graham: Sometimes you need to attribute conversions to publishers.

Thomas: Advertisers pay ad tech on performance.

Michael: Payments based on conversion exist.

Aram: Publishers can discount ads based on conversions.

Luke: I was confused about tying brick and mortar sales to the web.

Thomas: Yes, there are some mechanisms for doing that. Loyalty cards, etc…

Luke: identifiers?

(many): yep, the world is full of identifiers, and there are widespread methods for tying offline purchases to online interactions.

Nick: Compliance is not trivial at all. We should enable compliance with relevant privacy laws. The current situation does not seem to do that. Consent in particular, but not exclusively.

Thomas: Examples here in France, there are lots of other laws we might need to consider.

Brian: Did you look at which of these require user data as opposed to those that don't need user data? Example: billing.

Ben(?): CPA Billing though?

Thomas: Not much needs to be user-specific, but it does need data from users to operate in most cases.

Erik: we should avoid attempts to comply with ALL laws. Some laws are in conflict. We should avoid laws that require individual identification.

Michael: as a browser, we want to ship an API that people can use. If it's impossible to comply with some law while you use an API, then some folks won't be able to use it.

\<rathole entered, then curtailed by Aram\> \<well done, chair\>

## =\> 30m:[Update on the status of Topics API + Q&A](https://github.com/patcg/meetings/issues/92)

Josh: A way to address interest based advertising. The user wants the site to make money, the site wants to make money. Interest based advertising . We started with FLOC in an origin trial, which grouped users into cohorts with 16-bit identifiers, which could be used as signals to some ML model. We got a lot of feedback from that experiment. It was hard to understand, there was no transparency. It added fingerprinting, more than we were comfortable with. The set of topics was unknown. The Topics API came from reacting to all that feedback. UX gives control over what topics are shared. The amount of entropy per user is in the order of 1.5-2 bits per week, would take many weeks to reidentify people across sites. Lots of sites using the OT. Criteo has expressed utility concerns, e.g.that the topics are less relevant or too high level. We intend to address this over time. The taxonomy can be improved. We've heard that utility and privacy could be improved. We've heard disagreement over doing worst-case vs. average-case privacy analysis. We feel like if the average user takes many weeks to track, that is a huge financial disincentive to track users en masse. We've heard the concern that even with human-curated topics, sensitive topics could be inferred. On the utility side, ad techs say that this is not as good as 3p cookies for inference. Opt-out remains as a control. Some feedback is of course from people who seemed to generally dislike personalized advertising. The API is not going to progress through the standards process without significant changes. Chrome is still testing the API, we hope to roll it out. We think its privacy is strong relative to 3p. Some ideas are out there.

Kyle: Is your analysis for the 10 week number public?

Josh: See the repo. One paper at [https://github.com/patcg-individual-drafts/topics/blob/main/topics\_analysis.pdf](https://github.com/patcg-individual-drafts/topics/blob/main/topics_analysis.pdf), a second one forthcoming

Nick: It might be worth trying to see if there is a solution that is good for both utility and privacy. It might be worth finding things more opt-in or if the spec is less specific about the selection mechanism. Some data might be released by any mechanism and people might be comfortable with that. It might be good if this didn't depend on browsing history, but the users might be able to opt in.

Josh: opting in to topics might be a worse fingerprinting risk

Michael: any API needs to think about both privacy and utility. The idea that users suggesting their own topics has come up a lot, since we have been discussing this area since 2019. We've heard from ads people that they get nearly zero utility from users' self-selected topics.

Graham: How did you reach that conclusion?

Michael: Not my conclusion, passing along what we have heard. Direct that question to the ads people. Self-volunteered information doesn't help is what we've heard.

Nick: if there is data to this point, I would like to see it, or maybe it's worth testing

Aram: If you believe users do not want personalized ads generally self-volunteered data is a very strong signal. But if you believe users do want personalized ads, then there is a perceived value seen from buyers that users would want to misrepresent themselves. Buy side says that self-selected topics can mislead the buyer, which goes to deeper questions about what all of us think about user preferences about personalized advertising

Ben Savage: Ad topic hints tried this. Uses ads that are shown to train something like this. Users might be able to say things about the ads they see and use that. For instance, ranking ads as irrelevant.

Josh: When the user clicks on an ad, what information can be get from that? But people don't click on ads that much. Not a lot of useful data there.

Ben: People could provide information on ads they don't click on.

Josh: The ad choices stuff, for instance. People don't click that.

Ben: you would provide different UX if you wanted more feedback. Collecting data about a person runs afoul of people's conception of privacy. Whereas a direct choice might not.

Josh: We want it to have utility, so everyone gets privacy. Very little chance of that if it required action.

Brian: Asking users about preferences, we found that users will set preferences and forget about them. They are lopsided and neglect what they are spending money on. Have you any plans for a UI?

Josh: There is a developer page and settings. The internals page has all the info, but that is not part of the UX plan.

Brian: I would like to know what my browser is saying about me.

Josh: We have that. We have a display for topics and have an opt-out.

Michael: Look at it in your copy of Chrome. You can check what data Chrome has inferred for browsers that have Topics turned on in the trial, right now 5% of people, and you can opt in to turn it on if you weren't randomly selected.

Aram: Inferring information about user interests carries unique risks that none of the other proposals have as extensively. Particularly as they relate to algorithmic redlining. Increased vulnerability for users, either intentionally or inadvertently through automated systems. Housing, discounts, etc… It doesn't seem that there is a clear step to address that issue.

Josh: The amount of data is very limited. The chance of being redlining based on this is small. And saying "redlining" you're describing something that is already illegal. All APIs leak cross site data, but Topics makes it up front.

Aram: Two things: 1. We have seen a lot of proof that policy (in regards to algorithmic redlining) is not sufficient. This is unique, but the agent that creates the data today are companies that push it to the browser, not the browser. Those entities are subject to regulation. 2. It is not clear what is being used to redline. Computer science education or video games being advertised exclusively to men disadvantages women, for instance. Not illegal, but still creating societal problems.

Graham: I land closer to Josh on this. We need to come to grips with the fact that targeted advertising will have bad outcomes, but instead make an effort to reduce the harms. Algorithms are inherent biasing. The point of legislation is to control the bad effect. That form of argumentation \<I give up\>

Michael: Information is limited to what foo.com saw you visit last week. Lots of information can be inferred from that, but topics provides much less information. Topics doesn't create new, different, or more extensive information. By design it takes information that already exists and compresses it down to an extremely small amount of information, which we take great pains to limit the way it can be used in these negative ways. That doesn't mean we have zero bad outcomes.

Aram: Does Topics emit less than browsers where, unlike Chrome, third party cookies are blocked?

Michael: To answer that, you need to look at what tracking is happening using things that are not cookies. These techniques are in use.

Brian: Shouldn't compare measurement which reports events and topics which reports inferences based on events. There is a lot of good in interest-based advertising, but I think that having this done by the browser represents something of a conflict of interest.

Josh: If every ad tech got their own topic, then they get a very good identifier. I don't know how to get there.

Brian: How can we get away from a single entity making these inferences.

Josh: An external actor could be responsible for making these inferences \<sorry, this answer made no sense\>

Michael: The taxonomy and the on-device model that performs inferences is something where we needed to ship a thing in Chrome now to run the trial, but we would be interested in having these come from "the ad tech industry at large" in the future. What is important for privacy is some limit on the size of the taxonomy and the sensitivity of points in it, and that the model be the same for everyone. If you have ideas, please let's hear about it.

Martin: I don't know where to start. We've heard a lot of things that are troubling. Starting from the notions of aggregate privacy. Effectively, I'm just giving up. I've heard some interesting arguments, but I don't think anything has changed my opinions here. It's a difficult thing to rationalize from a privacy perspective. I did want to call out Micheal's call out that information foo.com sees informs the Topic. Some people have 3PC and some don't, I heard "we can't fix the tracking problem so why bother". The mechanism that says "we're only going to release information to foo.com if there was activity on that site" has problems that were pointed out. The thing we're trying to accomplish is setting the wrong baseline.

Michael: On the specific subject on which sites see which information, let's acknowledge that's a tradeoff, and we made the opposite tradeoff in the original FLoC design. I'm not sure which is better. Topics is trying to split the baby and make tradeoffs in a bunch of places. I'm not sure we've made the right one in many of them. In the long run, Mozilla has made it clear this is not something they'd support. Chrome's goal is to find an interest based API that is supported by all browsers. We've been through the era of browsers diverging and websites having tags "best viewed in Netscape Navigator". We don't want an end state where browsers diverge.

Martin: You realize we're in that state now.

Michael: Absolutely. When we have the Topics API available in 2023 while gearing up to remove 3PC in 2024, we hope the feedback will be useful in informing a discussion around whatever API does get cross browser support, even though we are not all in the same place right now.

Alex: TAG walking away from interest based advertising would be a mistake. Not only do we lose the interop potential, but an influential body loses the ability to influence its design. You may not like Topics in its current form. That's understandable. But we should try to come up with something. Advertisers are going to try and show ads based on interests and will come up with other ways that are less well lit. I implore the group to step up to the plate and stay involved in work to support interest based advertising in a well lit way that would lend itself to more transparency and more control than the work-arounds we're already seeing in much of industry.

Aram: As a point of order, while Topics is in our drafts area, it's not currently the work of this group or currently scheduled to be part of this group, but we're also not intending on kicking them out of the patcg-individual-drafts space. We're interested in hearing reports on, but we are not developing currently for or by the CG.

Martin: There may be some people outright rejecting the concept of interest based advertising, and others rejecting the implementation. We aren't opposed to the concept, but we have a gap between what is currently possible and the privacy properties we are trying to attain.

Michael: I 100% agree with you. Within Privacy Sandbox, there is also a second very different API, FLEDGE, that is also looking at use case of ad selection. If there were no timing or difficulty constraints, we may not be pushing on all at these at the same time. Given the time frame we are aiming to remove 3PC from Chrome and the ad tech ecosystem that needs to make changes, we felt it necessary to have an API that could be used now and that wasn't as complicated as FLEDGE. W3C tends to look towards something happening in the long run. Something slower may expand to cover everything, or Topics may get incorporated into FLEDGE. All of these seem possible, even if not in the "before Chrome removes 3PC next year" timeline.

## == 5m: Day 1 wrap up.

## Day 2

## \<= 20m: Hellos, Intros, Physical space ground rules, Google Doc, Call for Scribes

W3C Read All About It \<- W3C Policy and Procedures reviewed

Since we're in Meta's spaces, don't wander. We can get you an escort for the bathroom!

## == 20m: Review and discuss[survey](https://github.com/patcg/meetings/issues/91) results.

[PATCG - 91 - Results](https://docs.google.com/document/d/1bydwuN0_K2anOZV41xNJn1Kt0vt9WPOkf56ESnmQ5_A/edit?usp=sharing)

Aram Zucker-Scharff: Google doc has all the questions in a histogram. Going through major interests and concerns. You can get the data as a CSV. Do you your own analysis. The proper way to examine is to combine 4,5 and 1,2 (strong interests and strong objections, respectively). We can see the strongest concerns are around in-browser computation. Strongest interests are can measure view, clicks, third parties can invoke the API. We have time to discuss and talk about the results. Any thoughts?

Erik Taubeneck: anything specific you want to talk about as chair.

Aram Zucker-Scharff: I think this represents some useful drivers for what we can do. It seems like there are some concerns about (acknowledging total responses are 24) "The API requires requires in-browser as the primary site of operations to compute the output" is rejected conceptually.

Ben Savage: This is similar to a discussion from an earlier meeting. Last time Apple wasn't with us. Put Luke W on the spot. Are there concerns?

Luke Winstrom: I don't think there is a fundamental objection to where joins happen. But whatever we do we should try to minimize the data that is leaving the device and is the minimum amount for the use case. Time series cannot leak because that data does not exist any more. If you are trying to create a measurement that joins data. If there is a specific task useful for browsing that requires the data to remain on a server for a longer time that makes sense. My preference is to minimize everywhere that data is transmitted the best we can so there is less risk.

Wendell B: Reacting generally to the survey. Amplifying some of Yahoo's views. One of the things we want to figure out is how to sell this stuff. Came up yesterday with Criteo. The market for this stuff is not the person you think it is. It's the advertiser. If they can't figure out how to purchase this stuff and run campaigns against it they aren't going to play. The plea is to scope things down as far as possible to show it can work. There's no story or narrative for how you use this stuff. Best example is the COVID tracing. And that is really expensive. Numbers coming from public talks. Count the number of FTEs to set this stuff and run it. Picking one, measuring and views would be great. Then we have to go convince another party to work with us. All this private stuff requires at least two parties.

Mariana Raykova: The conclusion that this is astronomically expensive isn't actually backed up.

Aram Zucker-Scharff: Clarify what you mean by not expensive.

Luke Winstrom: the startup costs to come up with this design in a very short period of time were expensive and it was mostly volunteer work. Second version has been much easier to do.

Aram Zucker-Scharff: Clarify Wendell

Wendell Baker: I'm here because I feel like it could be cheap enough to run. We're still on the first version though and haven't made it work. Yahoo doesn't have scores of people running capex/opex behind this. We want to get something basic that works.

Aram Zucker-Scharff: The scale of the company matters in the view of the costs.

Nick Doty: Curious about concern about pre-registration with the browser and just want to get a little more on what is meant. Is the concern you have to work out a deal with the browser? Differing user configurations? What is the concern.

Charlie Harrison: Personal concern (though ambiguous about who is pre-registering). IPA for example has delegation of measurement and a pre-commitment to helper network. That sounds like pre-registration. You have to put a file somewhere for the browser to read. There could also be a type that has a developer going straight to browser (ex. FPS github). Adoption costs are problematic. If you need parties to take actions the harder it is for the ecosystem to adopt. Chrome has tried to make it so publishers and advertisers don't have to do anything and ad tech can set things up for their customers. IPA has advertisers and publishers making choices. There are way more publishers and advertisers than ad tech companies and thus makes the ask harder. I don't think pre-registration is bad. But we should be aware of these issues.

Aram Zucker-Scharff: Agree the concern over pre-registration is the work required for participants. Publishers are going to be the least capable for any pre-registration process. The vast majority of them are smaller. Ad tech has less of an issue. Advertisers are not as much of a problem as with publishers but more than ad tech.

Wendell Baker: I like the idea of getting clearer on pre-registrations. [A/V difficulties…]

Erik Taubeneck: I agree with Charlie. It's a tradeoff we're going to have to work through. We probably can't avoid it entirely.

Charlie Harrison: Responding to Aram's confusion around in-browser objection. Guessing a lot of people in the room think that this means we could only support on-device. The constraints with local only mechanisms are typically use see much less utility for the same level of privacy. We are making it harder to achieve utility goals if we restrict ourselves to on-device only.

Luke Winstrom: agree with Charlie. It should be a trusted process that isn't exclusively browser. But how that happens has to be very carefully considered.

Aram Zucker-Scharff: part of the issue that causes this is that among some participants in this process there is a decreasing level of trust in browser vendors.

Ben Savage: I interpreted the pre-registration question differently. I hadn't thought about it as pre-registration with a browser. I thought about it as a pre-registration with a helper. There should be no way to use pre-registration to be exclusionary.

Brian May: Primary concern with browser processing is stability. People in ad tech are paying for data that might be lost. It gets harder to make the case to advertisers that they should pay if we can't guarantee that what we are promising will actually happen. Users clearing data is also a concern.

Luke Winstrom: responding to question on expense of COVID tracing. It takes 1 engineer about 10 minutes to implement new metrics. Level of effort has gotten much lower. 1 phone call with Google. Incremental costs to expanding things are very low.

Wendell Baker: Preregistration. I had interpreted this as permission from the browser. You request a key and browser says no. Or the browser just decides to take away the feature. There is a history of this. Example: Trust Tokens. Yahoo built to it and now things seem stalled. Continuity for people outside of an original dev team takes longer than you expect. Going and building a business on something that isn't sure to stick around is a large business risk.

Aram Zucker-Scharff: Additionally to build on that. There is an invisible implementation cost. Almost everyone in the ad tech landscape is going to be doing all sorts of other operations on the tools we build (data pipelines etc). Cost concerns are generally about more than just integrating with the tools. It's about retooling processing after integrating with the tools.

Martin Thomson: Reiterate something that comes up in the back channel: User control vs other entities in the system exerting controls over other entities. Businesses don't want the browser to be the gatekeeper that preregistration might imply. Mozilla doesn't think about standing in the way of developers building to any new API. But users should get control over the situation. It would be completely unacceptable to Mozilla if that is not the case.

Michael Kleber: Responding to Wendell and Trust Tokens. Sounded like that was about the Trust Token origin trial? [note added later: that OT has now ended actually.] Origin trial does require registration. Chrome isn't super selective about the process, but there is pre-registration. Has nothing to do with how things work after Origin Trial is over and APIs become generally available.

Aram Zucker-Scharff: Closing queue. Does the editorial group feel like this survey provides the right inputs to the next steps in the process?

Charlie Harrison: I feel a bit concerned that it appears we all tended to have different views of the questions. This makes it hard to proceed. Perhaps a solution for this would be to talk directly to those with the strong objections to pull apart their understanding and answers.

Erik Taubeneck: I didn't view this data as making decisions for us. It is a conversation started. In that way the survey was successful. Editors are happy to talk to strong objectors.

Martin Thomson: I'm not as concerned as Charlie. Some things are very clearly indicative around certain directions. Including areas where it's clear we don't have to spend a lot of time worrying about. Some of these things can also be deferred to later in the process (ex. pre-registration). I think it was helpful to get this data. For instance, we're going to measure views. It's no longer a question. The objections are where we need to have more conversations. Even if there are just a few objections, we need to find out why. Some may be based on principles.

Aram Zucker-Scharff: Is there anyone else who wants to take the poll. DM me on W3C PATCG slack if you do want to take the poll. You can also email Aram your responses and he will add to the CSV. On that we are done with this discussion for now.

## =\> 30m:[Update on IPA implementation effort](https://github.com/patcg/meetings/issues/94)

Erik Taubeneck: Please jump in with questions. A recap of last presentation from August. We have some data from a prototype. That gave us some estimated cost numbers for 1M events. Framed as % of a media campaign. We've been trying to implement IPA from scratch in Rust. We're trying to build something that is prod ready, but also something that allows us to do complexity and security analysis. Previous prototype was a bit more academic. You can check out the code at (LINK INSERT). The old version for testing is also in there.

Alex Koshelev: Brief overview of what we've done so far. Single party helper network with 3 nodes. Implemented both malicious and semi-honest. Semi-honest is the benchmark to see how much penalty you incur. Have helper and report collector. RC is the one who submits the events. Coordinator gets assigned. After inputs are submitted we perform computation. RC then consumes the results when they are read. TLS for securing. Slides show architecture. It includes IPA protocol. That is based on core primitives. Control plane coordinates. Large network infrastructure layer that among other things insures order. Code is written using green threads in Rust.

Ben Savage: Last time I presented the benchmarks and let the group know we weren't expecting getting a lot better. But somehow we got to 32-45x better on cost. Most of the costs were from communication and sort. Have spent a lot of time on optimizing sort. Richa was instrumental. Paper on Radix Sort. Start sort by least significant bit and then work your way up on more significant bits. This allows us to not have to worry about sort on timestamp. Helpers sort by match key. All of the rows from a single person will be consecutive and in time order. Will need about 40 bits of match key to represent everyone in the world. Doesn't scale linearly. We're scaling nicely. We have not be able to benchmark how much less computation there is. Done our best, but acknowledge it's not perfect. See table in presentation for stage-by-stage comparison. More efficient in MP-SPDZ than in Rust. There's more low hanging fruit for optimization. Sort is now down to 42% of cost (down from ~90ish).

Martin Thomson: Note that this is based on relatively small inputs. Later when we scale there are going to be more areas for optimization.

Ben Savage: Using stock Amazon egress. Cost is really starting to look plausible. A large advertiser with 100MM events. Would cost around $250.

Richa Jain: exploring real tests in future: real ads, advertisers, publishers and measurement companies. Looking for help to coordinate. Won't use match key. Will use IDs that already exist (like Android MAID). We want to demonstrate it is viable to run and affordable. Plus want to compare real life to the earlier tests. Excited to learn from Charlie's experience taking ARA to market (ex. debugging). Want to assess potential for match key collisions. Still early. We are looking for help and interest in participating. You can reach out to Richa or anyone else on the team.

Ben Savage: Started having preliminary conversations with people interested. I don't have permission to share names. But there is in principle agreement from at least 2 potential helper party testers. Publishers, advertisers, ad tech companies and measurement companies are all welcome.

Jay Kishigami: I think these results are great. You have good efficiencies in sort. Is it mainly based on the language or the algorithm. Which is the main factor? We don't know what MP-SPDZ was doing. It compiles to something that was difficult to see what was happening. It could be the language, but it could also be the algo. [https://eprint.iacr.org/2019/695.pdf](https://eprint.iacr.org/2019/695.pdf)

Benjamin Case: The difference on the algo side is multibit. 50-60% improvement in communication and MPC speeds. We aren't trading one cost for another. We're able to work on the optimal size field.

Ben Savage: We are working on a 4-byte field, improving on MP-SPDZ.

Aram Zucker-Scharff: from Slack - can you explain the difference between malicious and semi-honest models.

Ben Savage: in semi-honest, all of the parties are expected to stick to the protocols. If one of the parties is malicious it can learn more than it should. In malicious, even if one of the 3 parties attacks, information doesn't leak. 2 of the 3 need to collude to leak.

Erik Taubeneck: We can configure the approach to be 1 out of 3 or 2 out of 3 being malicious, but there are significant gains with "honest majority". Generally there aren't 3 malicious actors. Goal is to make the weakest assumption.

Charlie Harrison: Thanks for the presentation. Awesome! 2 questions: The first is about the test with real businesses. What layer is being tested. Is there a browser simulator?

Erik Taubeneck: Going to use an Android ID and pretend it is secret shared.

Charlie Harrison: What's the activity data.

Erik Taubeneck: regular campaign data you would collect.

Ben Savage: Running a campaign on Meta property (or others). Going to run on Android because Android provides everyone with a MAID. The MAID gets three way secret shared. This allows us to run the protocol and simulate costs, work on noise, send results back and allow advertisers to compare with normal results. We've found several companies excited to run helper parties.

Charlie Harrison: Second question: Performance improvements? What is the scale at which this was tested?

Erik Taubeneck: Not high.

Charlie Harrison: In IPA this is called calibration. Going across all advertisers the scale can multiple quickly. I want to see what happens with 5 orders of magnitude more data flowing through IPA. Perhaps next presentation can focus on this. If we can cross that line and show this can scale, that would be a great accomplishment for IPA.

Ben Savage: Totally agree. Started scratch prototype 5 months ago. Alex is working really hard. Scaling up to 1BN is non trivial. Working on it. Give us some time.

Martin Thomson: Most of the work has been about the algorithm writing being ergonomic. This has caused throughput issues.

Erik Taubeneck: The upper number cited was 200 BN events. No reason not to go higher. If you do the back of the envelope math is 10TB.

Charlie Harrison: Not convinced we can do off-device without MPC.

Erik Taubeneck: We have to figure out horizontal scaling regardless. That's the limiter at the moment. Both MPC and TEE face this threshold. We need multiple machines coordinating on secret data.

Charlie Harrison: Agree, we don't have a TEE solution either.

Erik Taubeneck: Reiterate that we have to figure out horizontal scaling. Does this finish in an amount of time that is reasonable and at a reasonable cost.

Martin Thomson: We get a lot of value for a lot of people before we have to worry about horizontal scaling. Could run this for moderately sized campaigns without running into the threshold.

Charlie Harrison: There is value in supporting the middle tier. For Google to be committed though it has to work for everyone. Love the results though. Horizontal scaling remains important to hash out.

Erik Taubeneck: There may be ways to break queries up where we don't have to worry about horizontal scaling.

Brian May: Has anyone done calculations to "run ad tech."

Charlie Harrison: There's a github issue from Google Ads. Suggests single queries. Asked for 100BN impressions and 100BN conversions in 1 query. My previous assumption was that impressions would be bigger than conversions. (https://github.com/patcg/private-measurement/issues/21)

Ben Savage: I think these queries can be sliced up. Facebook today does measurement for all the advertisers. This is not how IPA is designed. In IPA each advertiser is running its own queries. 10 MM advertisers on FB. You can slide into different batches. Might slice on web vs mobile, geo, etc… Mariana has also had some ideas on this topic.

Aram Zucker-Scharff: If you are continuing to look for volunteers, it would be great to create an artifact with more details on expectations of participants.

Nick Doty: Can you say more about match key collisions. What's the harm and why do you expect?

Erik Taubeneck: When a match key doesn't exist, you need to generate a random value because you don't want to leak that a match key doesn't exist. The less entropy in the match key the more chance there is for collision. Randoms and reals could collide and create false positive attribution results. You can fix it by using more bits, but then you suffer on sort. So we're looking for the right balance.

Martin Thomson: also based on how much tolerance querying parties have for this issue.

Ben Savage: There is no re-identification problem. Just query accuracy.

Benjamin Case: We have a mitigation for the collision issue. User agent could be a fallback match key provider. Will put out doc on pros and cons.

Luke Winstrom: opening question as a github issue

## =\> 30m:[Scaling Up Reporting with Option for Off-Device Attribution](https://github.com/patcg/meetings/issues/97)

[logistical reminders: sign in to participants list!]

Mariana: ideas related to previous discussions. 1) can we extend IPA like designs with MPC that only reveal the output of the computation? Relax some security/privacy notions but buy some more scalability.

2) architecture that can support both on-device and off-device attribution

IPA summary: only a private aggregate histogram as the output of the computation. Requires doing a sorting of the reports. Good that the new result shows that the sort can be done in linear rather than n log n time. Handling billions of views and conversions weekly.

Trying to come up with a 2-party protocol that computes a private histogram over very large, sparse domains. Where the domain size is much much larger than the number of reports. Additional information than just the histogram: some differentially private counts. A differentially private partitioning algorithm: everything with the same match ID will be in the same group.

If done completely within MPC, algorithm is super-linear. This algorithm is linear with the number of contributions. Start with encrypted reports, insert a number of dummy records (tricky to determine exactly how many), shuffle all records, evaluate a distributed pseudorandom function on the ID, partition based on these pseudorandom values, with dummy records proving that we can provide differential privacy. Can aggregate, using homomorphic encryption, and then a mechanism to get back to the real IDs for values above a certain threshold.

Erik T: how many dummy records?

Mariana: smaller

Adria G : (log (1 / delta )) / epsilon

Martin: Does it matter how many partitions you are trying to partition to?

Mariana: It depends on the log of the domain types.

Adria G: (In the MPC setting) You'd look at the aggregated histogram with non-zero entries

Mariana: It is the actual buckets you are aggregating over

Mariana: inputs are impression or conversion-type reports, which contains an encrypted match id and encrypted data (either about impression or conversion). Distributed anonymous partition protocol layer: guarantees that every record with the same match id will be in the same group. Granularity of match ID could be configured, like the IPA proposal or even with a much higher scale. Go from billions of records to millions of groups. Groups include both real and dummy records (which will have zero contribution to aggregations).

With more manageable groups, we can invoke whatever attribution protocol. Can run attribution algorithms in parallel. Obviously parallelizable to each group.

Think of output as attributed reports, similar to what ARA handles. Can merge or aggregate them. The number of reports will still be much much smaller than …

If histograms are a smaller size, could be manageable with an MPC.

Could step up the scalability. What are we revealing? The sizes of the groups is additional information, but still differentially private, and we could configure the groups to include a minimum number (like millions of users).

Adria: paper has detail on number of bytes.

Martin: great stuff about how to scale. Fundamental problems with this sort of design. Still need to read the paper, but couldn't see how you couldn't link something, given that all the contributions from the same user end up in the same bucket when it comes to adversarial use. If all of the items end up in the same bucket, you learn that they are the same user.

Mariana: have to configure the sensitivity.

Martin: yes, but sensitivity will typically be outside the control of the system.

Ben: have been evaluating similar ideas, very interested. Just from latency, parallel would be very helpful in speeding it up. In the worst case analysis of an adversary sending in malicious records. If a consumer does learn something, could configure the protocol to punish them in terms of later data. The report collector that gets a very unusual distribution, that collector couldn't run more reports later.

Mariana: auditing mechanisms that could detect violations of the sensitivity.

Ben: preventing the attacker from repeatedly doing something.

Charlie: when composing the DP histogram in off-device attribution setting, can be less sparse by putting the aggregation key up front.

Charlie: Challenge with sensitivity of attributed records, IPA lets records be generated from everywhere. No entity can limit how many reports go out with a given match key. Would be easier if there weren't interoperability and matching across devices, could bound the sensitivity just on a single client.

Erik: not just the cross-device component, also about the ability to remove time delays.

Charlie: partitioning unattributed reports

Ben:

Charlie: could at least bound the sensitivity of a user's contributions

Erik:

[scribe is missing the cross talk about this attack]

Mariana: hybrid architectures that combine on-device and off-device attribution and different sizes of domains.

Because output is in the form of attributed reports, can potentially merge attributed reports from different systems together. If you have off-device attribution, can constrain yourself to smaller domains. Or maybe there is a way to map from sparse domain to a smaller denser domain. We have a way to process unattributed reports and generate attributed reports. And once all systems are processing attributed reports, we can use strong MPC techniques to aggregate attributed reports and produce private histograms.

Possible to merge systems that have off-device and on-device attribution.

Ben: (Queue: you lose "late binding" - as attributed conversions cannot participate in multiple queries, with different parameters e.g. user contribution cap, a different set of source reports) like the attempt, but seems constraining. IPA provides ability to run multiple different queries on the same conversion data. Might first run a query on views and later run a query on views and clicks. Don't have to decide up front what the query is going to be. Sensitivity (how much a single user can contribute to the report) is a query parameter. Maybe you could cap

Mariana: won't have the full flexibility, but trying to see if there's a path if some participants refuse off-device attribution.

Luke: by creating late binding feature for advertisers, not communicating to the people who are giving the data what they are contributing to. If you required pre-statement of the queries, then the user would have more transparency about what is being done with their data and what the end results might be.

Adria: public verifiability properties of what the underlying protocol is.

Luke: It is useful to be able to run multiple queries over the same set of events in order to do some discovery mechanism. But that means you're potentially doing something unclear to the end user.

Erik: queries would be constrained by a differential privacy budget, can't indefinitely run queries.

Luke: but once you're beyond a frozen query, there's a communication problem.

Erik: the queries we aim to support are the same as other proposals.

Luke: if your proposal is to be able to run a small fixed set of queries, then running all those queries on the device is equivalent.

Ben: but would be more complex/expensive to run on the device. An alternative way to do transparency would be for the helper nodes would be to publish publicly all the queries that were done. Users can see the list of queries that were run on your data. (Cite Dan Boneh.)

Erik: agree that we need to communicate clearly, but that applies to all APIs/proposals.

Luke: agree, but wanted everyone to hear the concern about after-the-fact analysis.

Charlie: ARA works via sensitivity budgeting on the device. Running multiple queries requires sending multiple reports. You can optimize the budgeting if you impose certain constraints on sensitivity. Clever optimizations possible under certain circumstances with forced constraints. On-device budgeting where different use cases have different constraints, harder to push that to the device. Satisfying all of these use cases exclusively on device becomes much more difficult to support.

Kleber: don't believe the query transparency proposal addresses Luke's concerns about data usage. Query transparency is blind to the filtering that is done before the query is done.

Erik: for a certain set of functionality, that's on or off device. Is there a fundamental difference in the transparency available to the user?

Luke: if you provide the same functionality… Limit data to what is necessary. Sending a reduced set of data is preferable to sending lots of data and trusting a lot of engineering security on the server side. If the math is perfect the guarantees are the same, but I don't trust that the engineering will be perfect.

[lunch break until top of the hour]

## ~~\<= 20m: Additional updates, questions, trial results related to 'Industry updates around privacy features and trials'~~

## == 45m: Lunch break

## =\> 30m: Open Feedback on private measurement, current tests, and the existing[document](https://github.com/patcg/docs-and-reports/tree/main/design-dimensions). We would especially like ad industry participants who do not usually speak up at PATCG events to take this time to ask questions and give feedback. Come to Aram after this if you'd like to further add your survey response to the set previously discussed.

Aram: What is the wider user interface / experience vision in the browser for users, as well as for businesses who use these APIs, e.g., publishers who want to see their own stats. Do we envision new systems they have to go into, browser vendors they need to work with, working with existing systems. Generally we've been pretty far from this, but curious if people had thoughts on this.

Other use cases. Still have a lot of time on measurement. But what else we want to take on next.

Charlie H: Point out 2 potential next steps. Topics that Josh presented, or more generally the interest-based advertising use case. The other is similar to attribution, but auxiliary measurement that's not directly related to measurement. There's an existing repo called "private attribution api" that supports other things like reach measurement. If our output does not include that, we may need to look at these.

Nick: Appreciate the prompting on UX, I think it's important to think about the user experience and privacy beyond just the statistical properties. Status quo is terrible, and we should be able to make it better. You're constantly surveilled, and also harassed with prompts that you cant opt out of. There should be some transparency, see who the parties that they are trusting, etc. May be able to see what measurements are being done on users. Users should be able to express general preferences about wanting to engage in measurements or not.

Michael K: I'd love pointers to other places where standards get into the UX domains. I came into this with the expectation that standards didn't get into this and if we want to tackle that, I'd like to do some more reading.

Aram: Agree this isn't usually the work of standards orgs, but is important for browser vendors to think about it more publicly. Organizations without the same technical resources often ask "what is this going to look like". From Nick's perspective, there's useful work on privacy UX that might inform how we design the system in ways that aren't interacting with the UX.

Nick: Agreed that we aren't going to standardize a UI. If you wanted transparency, you may make certain design decisions. If a user grants permission, you need to know what it means.

Martin: There's often an interplay between what happens in the standards and in the implementation. Setting expectations in the spec is useful. You can carve out a place for that to happen. There's some exploratory work on how we can communicate this with GPC. While we're not going to be specifying what the UX does, there is a need to understand what the UX does. Push and pull.

[written, not voiced, Wendell] For example [Standards and Technical Requirements for Age-Appropriate Design](https://ico.org.uk/media/for-organisations/documents/2620427/accs-3-2021-technical-requirements-aadc.pdf), and Accessibility law refers to WCAG . Also, the [California codes](https://californiaaadc.com/).

Don M: Agree with Nick. UX helps shape how the standards can be designed. If there is an expectation that the browser will maximize opt-in to cross site tracking, that limits what can be done in the standard. If the browser is going to design the UX to accurately represent the user's preference, the number of options on what can be done in the underlying standard goes up.

Brian: Want to point to the "lock icon" when my browser is in HTTPS mode, and similar UI hints about my current context. We'd do well to consider if we should provide that type of context. Maybe not a lot of detail, but high level sense.

Kiran: Wondering if there is any work done on TEE. Didn't talk about it earlier.

Charlie: We use TEEs for the backend for the Aggregate ARA.

Kiran: How do we see the ad tech server, the bidding and the ad serving. Trying to visualize how that could work.

Aram: There are outstanding proposals, but for now we've been focused on Measurement. FLEDGE/Turtledove, Parakeet, Topics.

Kiran: I mean off browser.

Aram: Back end or off browser devices.

Michael: The Chrome proposal called FLEDGE has most of the computation happening on the browser. The Microsoft proposal called PARAKEET is optimized for moving computation off the browser, and into some appropriately protected server side component. There is some work in Privacy Sandbox, called "Bidding and Auction Server" (https://github.com/privacysandbox/fledge-docs/blob/main/bidding\_auction\_services\_api.md), that is more similar to the Parakeet approach, and also a limited version of that is already built into the FLEDGE world today with the key/value server using User-Defined Functions. Note that there are differences of opinion about how important, valuable, or desirable it is to move things off device.

Aram: There is a separate meeting for that proposal.

Michael: Every other week call, details in FLEDGE issue 88 ([https://github.com/WICG/turtledove/issues/88](https://github.com/WICG/turtledove/issues/88)). Currently under the WICG. This 1 hour every two weeks is just about FLEDGE. (Sometimes there is also a PARAKEET meeting, but not recently.)

Aram: It's an ad hoc meeting.

Gun: (how can we fix the data when receiving IPA or ARA reporting? Or should we just assume that such data changes are inevitable in the future?) Working at AB180 building an MMP. Heard that with IPA, you'd apply DP every time. How can we fix this, or is it inevitable.

Charlie: I can give it a shot. A few different ways to think about this. As an MMP or measurement provider, you're providing a dashboard to advertisers, and these are recording noisy data already. Some users are deleting cookies, some things get lost. The noise that we add to these aggregates, if you're doing large groups, it shouldn't be too much more. It may not change the advertiser decisioning. That may not be true in all settings. You may have to coarsen the data or show confidence data, we'll need to work together. This is about the utility we discussed yesterday. Difficult for us to understand. Specific things that break under specific scenarios. With this much error suddenly become unusable, etc, these types of examples would be useful, so that we can understand these tradeoffs. These are discussions I'd want to bubble up and discuss here.

Brian: Just going to add what Charlie said. Data is messy in ad tech. Here we are adding noise consciously, and we can make some reasonable assumptions about the impact. Other cases

Erik: One way we've thought about this is that you should only rerun queries when you have new data — it's not that the underlying results should change, it's that you've added new data. Running the same query over and over is generally not useful, just using more privacy budget on the same query. Data shouldn't shift underneath you, just overlapping data sets that grow over time.

Charlie: There may be ways we can provide consistency. If you have break outs that you expect to add up. With these types of contraints, you may be able to make them consistent. Always a game of providing privacy and the advertiser expectations, and product level of what you'd want in your dashboards.

Alex: Discrepancy is a constant for digital advertising. It would be great, and it's true people may want this, but it's not what they're getting today. Some of these systems could even help.

Brian: I've been assuming what we're building here for measurement will have a privacy preserving output that will be imported and used for your own analysis. That's your starting point. The problem arises not in people running different queries, but when two different people run queries and get different results.

## \<= 30m:[Advance private measurement work](https://github.com/patcg/meetings/issues/99)

1. **private computation configuration vs on-device/in-browser**
  1. **Aggregation**
  2. **data join**
  3. **private computation configurations**

Erik: this is from before we ran the poll, just a course categorization of what we had. I'm happy to start on any of these, on device, etc… What the implications are for cross-device and how this works for 3rd parties, etc… Maybe we can skip preregistration since we've talked about that more than once. Are there any of these that we should start.

Charlie: This is maybe calling out something said earlier today. One of the open design decision - is local only privacy mechanism something we want to align on. Can we cross this out perhaps once and for all, at least for now. Let's see if we can find a tentative consensus that some kind of private server is fine and this is what we need to get this work done. Apple has been a hold out on this and PCM is very opinionated on-device but it feels like we're moving in the direction of we're cool with servers. Does anyone want to challenge me on this?

Luke: PCM exists with an information theoretic approach and we don't have a problem with that. I know Martin has pointed out a lot of security holes in it. It is there, a thing. Creates privacy as something that is easy to think about and prob not as useful as some of the other proposals. We think that something like an MPC approach where a server creates aggregation through multiple parties is something we are interested in and a way to expand the functionality for these types of things. We think there are two approaches and we are not fundamentally opposed to either of these approaches.

Erik: Can we make a motion that a server architecture may exist for our approach in doc editors.

Luke: I am ok with that.

Charlie: Some people were against this in the poll.

Luke: I'm one of those people because the problem was the word sufficient. I think you cannot just do it this way. A conversation between what the user is using and what is happening on the server that the advertiser is using and an agreement that they have to protect users privacy is required. It is required but not sufficient.

Brian: On item number 6 - do we need to be more specific about what we mean about these kinds of things?

Erik: This was meant to be a conversation starter. We should continue to refine what these things mean.

Brian: Lets do a prioritized list? What is most important and what is least important?

Martin: Let's do one on a time for this.

Nick: I think there are a sort of easy to think about idea or simpler design - advantages for implementation, adoption, privacy. There are privacy advantages beyond guaranteeing certain protections, for transparency, something users will understand and protect beyond throwing up their hands and giving up control. There could be advantages for simpler things even with less rich functionality that are easy to explain.

Mariana: Simpler? What do we mean by this? When we talk about cryptographic techniques we can illustrate the protocols but it is harder to do so with hardware. We have to be clear.

Nick: I am being a little imprecise when I saw simpler. This is homework for us to explain how and why there are advantages. The advantage of transparency is end-users understanding the capabilities. If they don't understand the capabilities users might go like it is one more system we know nothing about among the others.

Mariana: The question about explainability depends on the technology that enables the capability.

Nick: Yeah, that's why I'm not saying you can't do these technologies

Martin: The nature of these technologies needs to be better understood. But I'm not sure we're yet at the point where we can understand what we're doing ourselves effectively yet, at least not well enough that we can communicate it effectively to others. We can look at the envelope of what is possible and explain what that is.

These things will be a lot more complicated but they will bubble up to others. Defining that box and how it works and what the capabilities we are dealing with look like is going to be a challenge for us but we need to do it.

Martin: There is a multistage system we have where user agents are releasing data to be used in this system and the nature of the data that is released is critical to limiting what comes after and explaining just what information is released will be critical for people. The outputs of what are building also have to be explainable to people.

What utility they provide for advertisers and what privacy properties they have we need to be able to explain. Once the information leaves their control they need to understand they need to trust how the system operates to give it their data and we need to be able to explain it. We have a good story we could come up with but it is hard, it needs to be small and well polished and we haven't polished it yet.

Ben: We have approx consensus we are saying the same thing, we need to view the system holistically, what privacy protections does the entire system find. We seem to be saying: THe entire system seems like it could be conclusive of server side components. It matters to us to be able to communicate to the end user clearly what it can do and what privacy provides

Luke: There needs to be more that we also need to explain. Not just that we promise this is safe and we have math. It is a hard thing to turn it into something consumable but it needs to be available.

Martin: I'm uncomfortable with talking about match keys leaving their machine because that is user identifying data so we need to be clear about what happens after it leaves their machine because that's very important.

Ben: I'm working with a design firm to try to explain MPC. It's hard but I think we can do it.

Erik: Nick correct me if this is not your intention, but is it a lot more important to explain to the users what is the total output of the system, what does it do. Not just how does it work. It is much more important to them to be able to rationalize what does the system do and how does it treat my data instead of the cryptographic formula. Similar to how we communicate an encryption, most people can't explain the technical thing, but they can explain how their data is secured between the browser and the server.

Martin: A sort of folklore builds around these things that approximates how this happens but we are lacking that folklore here.

Erik: That complexity is offloaded onto the browser vendor by the users . They trust the browser when it says your messages are private or your credit card can't be sniffed from network traffic, they trust those claims without going into the math. What does the system allow for, that is what we have to explain to users because they are going to push their implementation trust to the software

Luke: I don't know if I agree - how is the encryption done and what does it do and how does it work, this is stuff available to people without exact math and implementation. We do not have a story like this, Martin is correct. It is challenging to bring this together and be able to say 'this is what is happening' in a way that is graspable not to say 'this is what the end result is' and trust us to get it right.

Martin: Some people will grab the folklore version and be ok and trust someone I trust understands it. But we will also be talking to engineers with a mild understanding and they need a clear story. There are multiple levels of communication and we need clarity at each of the levels of detail.

Erik: My main point is I don't see it as a failure of the group if most of the population doesn't understand MPC but uses MPC. It doesn't mean we shouldn't = and browser vendors are incentivized to show that trust to users and people want to be explained to – but I dpon't think we should set the bar that everyone understands encryption.

Brian: The user levels are very important. Unlike TLS we're asking users to buy into this story we are telling them and trust the things we say are what we are, this won't just be users but representatives of users that will understand privacy better and translate stories to users that they are going to depend on.

Data containment vs utility - is there a version that degrades a dependency on servers?

Erik: TLS, explain diff

Brian: When my dad gets on the computer he trust that it does what he needs to do and the browser does what it needs to do but when it comes to advertising we are saying we want the users to agree to be measured on the conscious level and it is part of how the browser works.

Erik: I don't think I fully agree with that. Most of what we've talked about is default on. Similar to TLS this is accomplishing the privacy goals we wish to have. There ought to be mechanisms to turn this off, though, which is not similar to TLS, but in my head there will be lots of people who include my dad as well, who will never think about this thing beyond the fact that I work on this and we need to serve those3 people as well.

Brian: We're coming at this differently - advertising is struggling with a reputation issue and we need to provide a critical story to experts.

Aram: I think to Brian's point, there is a different information structure for this conversation than for TLS. The conversation for TLS, the lock, etc, was mostly a conversation between browsers and developers. Most users still don't think about the lock. The difference in the conversation now, because they've lost trust in the system, they've delegated to experts who can talk about this in public. There will be people who talk about this in public in ways that wasn't' the case before. There are new people, and we'll need more complex communication. I don't think this is a bad change, but it makes it more complicated. We should be heading for a higher level of communication.

Michael: Respond to a few different things. TO Luke's point earlier - we need to explain things to users' questions - the fact that there are lots of popularized explanations of something like public key encryption - that is 100% true and a great success story but those only scratch the surface of how browsers protect people's information. Public encryption is an enormously valuable primitive and once you learn that it is possible it is not unreasonable to impaging there are things that you could do with this to protect privacy and MPC is a similar primitive where it is a thing that can open people's eyes to the idea that your individual data is protected but you can learn things in aggregate and that is a good goal that we can hope this archives and we can hope that MPC is a new and useful primitive. Teaching people one idea is the best you can hope for. Two is a miracle. But it is still the case that users are going to delegate to the browser the responsibility for thinking about this. The change from the old story of the lock icon to a current version where not everyone is trusted in the same way. But that is completely the opposite of what has happened for browsers and lock icons. Once upon the time the way browsers worked was to expose the information to the user of the browser where we once exposed to the users the way to make a decision and that was a disaster. Over the last 10 painful years we have learned that the browser needs to do the right thing by default. This is enormously better than exposing things to the user and hoping they make a decision. That is why the lock is much less prominent now and the browser instead leaps in front of you when something is wrong. The exact UI of how to communicate that to the users. We shouldn't be figuring that out in this room . This should go to the actual designers who figured out the better current way of protecting users' security.

Nick: I think there's a lot to talk about. One smaller point - the challenge of the analogy with things like TLS is that we sort of have a different background like this reputation problem - users have come to believe that they don't have control that they are being surveilled that they have lost control that their data is working against them it isn't just about this capability - people believe they are being abused and you have to provide them confidence that they are not and I think this is a different situation than the lock icon and has to be approached differently. It isn't just about what is true, it is about a willingness to participate.

Ben: Luke can you clarify your goals as I want to make you happy - what would success look like - deeper levels? People can start at an analogy and then more people are going to need something in the middle and then some people are going to go all the way?

Luke: Yes, I think you have described a particular type of success. MPC isn't primitive, it is a whole field. So some particulars work in one way or another. When we talk about these things we have multiple different types of MPCs and MPC operations. You will have to have a reasonable analogy, a better more technical thing that fills in the holes and a very good pure technician implementation of what has been implemented. That would make me excited, I don't know any of these things. Then you'd have to have a discussion of - do these make people comfortable with this product.

Ben: After many attempts I have found what things work and what things don't work. Maybe I can market test. One metaphor that works really well - modular addition is hard to explain - it's like a combination lock digits 0-9. You spin it around and it wraps around. Secret sharing - bike lock - you take your combination lock that has a secret code, then you lock your bike with this thing and then you spin the lock so it isn't in the same place. Why is this secure? People grasp those four numbers are random noise that says nothing about how the lock is set. You'd need to know how many clicks to turn the dials. Imagine a post it note with random numbers, 5 6 9 7, you'd give that to someone and they didn't know what it is. They also need the lock to know how many times to spin it. Then they can, with these two things, understand how to unlock the lock.

Luke: I got to explain this to some people and I was surprised by how many were frustrated by modular arithmetic and I had to come up with similar analogies and I agree those are effective for associative and commutative addition processes. On the other hand how do I describe sharing a unique identifier across mult parties that do a join on it and have an aggregate we add noise to, that's a separate analogy and I don't know how to explain it and I would be glad to bring it to other people.

Erik: Key takeaway we need to target specific decision makers instead of all users?

Luke: all; end users will eventually look to someone they can find to say it is trustable. If it is, I looked at the code. I know someone who looked at the code or I heard from someone I trust.

Brian: Comes down to trusting the browser you use.

Charlie: Meta discussion - what level of stuff do we need - but these conversations need to drive towards progress towards the designs. We want to get the level of detail here so we have actionable items to take back and be able to explain particular pieces that we want to be able to take back to users with a solve. Synthesize discomfort with design elements so we have actionable tasks. If there is going to be a red line for us if we don't believe this will ever be explainable and that is a problem we need to determine that so we can constrain the design properly. Luke can jot these properties down to show what you feel needs a better example of how we would describe it to a particular audience(s).

Luke: What do the users of the browsers expect us to do with this information? Is this an appropriate use of this data? Would I expect my browser to do this or would I be uncomfortable with it? This is something we should be able to answer for users

Charlie: would they feel regret for having participated once they find out that they have participated in this particular activity or tracking system? A lot of users' stories are like this.

Martin: We don't want people to feel betrayed. That would be awful.

Brian: I think the best we can do re:story is that this is the thing that does the stuff for the users and be as clear as possible. It is good to discuss, but ultimately this group is not who is telling users the story, others will take what we do and tell the story. Is there a possibility that we could have a model that works on or off device depending on what the user is comfortable with? Richer details only available for people who are comfortable with it

Erik: Yeah, I think it should just be a thing users can turn on and off.

Brian: If Apple wants to do it one way and they want to only do it on device we could figure out a way they could participate in the current effort.

Erik: That's what Mariana presented earlier. But it seems like Luke has not ruled out MPC.

Luke: We understand how it works. We understand the value. We have done a lot with local dp and realized it is hard to do anything particularly useful about it. Having a way to distribute trust to these things is appealing but we really feel like we owe it to anyone using our products that we can stand behind the story we tell and never lose their trust. That's the most important thing for us. That is why I say: We need explanations.

Brian: Multiple constituencies here. End users are one. We need to serve them but we also need to serve others in the ad tech ecosystem.

1. privacy definition (differential privacy / information theoretic / k-anonymity)

Erik T: There are 3 approaches that are under consideration. The simplest is The Information theoretic. What PCM uses. There are a small number of buckets. Probably the simplest to explain, but also has some issues. K-anon is another mechanism where you need a certain threshold before the bucket and you need more values than distinct buckets. Finally there is differential privacy and the main claim there is that by adding some random noise you are unable to identify and particular contribution. Diff privacy has a thing called epsilon there is also a delta that I won't get into because I may not explain it correctly, but the basic idea is that as epsilon goes up the as far as I know there is no golden value of epsilon that is the correct one, browser vendors would need to take an estimate of what they deem appropriate. Census bureau has one, it is probably not the only one. That is basically the context for this. Where we want to get to is some sort of understanding is any of these preferred to others? Do we need multiple in particular? Oftentimes we see DP and k-anonymity combined.

Charlie: For terminology sake, let's differentiate between the privacy mechanism and the privacy definition. There could be many different mechanisms that satisfy a criteria. When we discuss these definitions, we should not be shoe-horned into one mechanism. I have a couple things that I want to say, the first is about multiple privacy definitions composing them. This is something that has guided our design discussions for ARA, we are now with ARA at a place where we did not feel with DP that we could always provide an epsilon value that fully protected everything that we wanted. SO we have an information theoretic that acts as backstop. From a DP point of view you do not need to limit the coarseness or fine-grained piece ??

We also wanted DP as it provides much stronger worst-case guarantees.

If there is fundamentally a definition we all agree on, but choose different places to place the knob, it may be good to have a fall back definition we can all agree on that protects a different thing. A corollary to that is, you can imagine having different kinds of DP protection. DP can protect not just the sum total of a users contributions to a measurement system, but also narrower slices. For example, you could only catch this one attribution report or something. One attribution report - I can only learn so much about it. I want to encourage us to learn about multiple different privacy grains, multiple constraints we want to protect against to give us different choices on where we are setting privacy levers

If one browser does not believe they can provide enough utility

As we are thinking about composing these multiple systems, having multiple points of protection gives us backstops if one point fails. If this thing fails, at least we are protecting this thing.

Graham Mudd: So, I guess the high level is that I agree with Charlie's point that it feels very likely that to strike the right balance of privacy and utility and combination of tools will be required. How do you communicate a level of privacy when you are using more than one of these tools together. The assertion is - wouldn't it be wonderful if there were some empirical measure of privacy across these tools that would show how they work in combination. I don't think that exists - which is why people think DP is so attractive. I wonder if trying to come up with that measure of empirical privacy that could be applied to more than one technique so we could explain to a user – you don't need to understand one specific technique

Joey Knightbrook:I understand k-anonymity and DP very well. INformation theoretic - can you explain that a bit more? Where can I learn about the information theoretic of privacy?

Erik: The basic idea is that there in this specific example, at the time that a click happens you have every limited entropy that you can assign to that. And then if a conversion happens, you have 4 bits or 86 something like that that denote the value and then there is a time delay to try to disconnect that conversion from the real conversion and then that gets sent to the server and the idea is that since that is a constrained enough space, that in aggregate you wont learn things about individuals, or a small number of individuals.

Luke: It is trying to dis-incentivize tracking because it becomes so expensive to track.

Joey: so narrowing the information space on the impression and conversion

Charlie: You can show that noise reduces the total number of entropy, the maximum amount of information. This is just another way to measure the amount of information

Erik: On its own it is simply the pigeonhole principle.

Luke: Designed to be explainable and implementable and without a server

Martin: Reduce this to the total amount of information over a fixed period of time. And that is the way to think about it. For something like PCM, this is a total # of bits over an entire population. IN this case, the caller gets to splice that information, that space, and attribute each slice to groups of people. It is a useful concept, but i don't think it has the same rigor or strength in various areas, as Charlie has explained.

Charlie: it can boil down to one number, "bits of information gained", per \<scope\>

Martin: My sense is very similar to Charlie's on this one. DP has some very strong advantages in its ability to protect individuals from being isolated from groups, however, the explainability of DP suffers really badly and there are some advantages to having some notion of minimal set size when it comes to? There are at least a number of people who are in the set and you can defend that and explain that and talk to people about that. I have landed close to where Charlie is - we apply DP and we look at other ways we have narrowed the information release and ?? and that gives people much easier things to reason about.

Joey: If we can explain MPC, why not also try to explain DP

Martin: Explaining the privacy model we are using is going to be more valuable than trying to explain MPC. there will be audiences for each I am sure.

Michael: Start a YOuTube channel and see who gets more views.

Sean: We (technically AWS/Wire did these videos) were able to do this with MLS. There is a woman who explains complicated math (Ratchet Trees):

- DoubleRatchet:[https://www.youtube.com/watch?v=7uEeE3TUqmU](https://www.youtube.com/watch?v=7uEeE3TUqmU)
- MLS:[https://www.youtube.com/watch?v=FESp2LHd42U](https://www.youtube.com/watch?v=FESp2LHd42U)

Ben: A few thoughts about DP. I think it is pretty complicated. ON the one hand, I really like the way that it allows us to tell people "you're not in this results. It is an aggregate result that cannot be linked to you" I think that non-linkability is key to the system. This gives us aggregate results. K-anon does not give us this guarantee. People are not used to having random noise added to their measurement and they are not going to like it and it is going to make it hard for them to understand. I love DP and I hate it at the same time. I think it's really going to come down to if we can find a value of epsilon that works for everyone. If we come up with something that is really private, but not useful, then we fail. If we come up with something that is more useful but doesn't have that non-linkability - we fail. I keep being asked what this group will lean towards in regards to epsilon. I would like us to get to a number of epsilons. What do people need? Then we can start to do some analysis.

Graham: We need a process discussion on how we get there. What would a productive approach be?

Martin: I don't think we can have that discussion just yet. I want to see where these decisions need to be made in the protocols. We need DP here, those are the decisions that have direct impact on these outcomes. Most proposals have said, there is a variable there, there is a variable there. I would like to have that conversation on what the variable needs to be assigned to. People are coming up with numbers. That's why we want to run the IPA test so we can get an understanding of where that needs to be. Beat down drag out discussion on ? I would like to build a bit more understanding on the other aspects of the problems and more about each other before we have to fight because it is going to be a fight i am afraid.

Erik T: I am not saying anything new, if you have ever tried to explain DP to anybody it makes MPC looks easy. I have one analogy from The Office with the scale, the next step is "so what". So if our overall goal is that we need to explain this system then we are going to have to tackle that question. To the process question - it may be worth making some more precise general statements about what we want out of these systems. Ben made one about people are unlinkable, i think a good place to start in terms of process. To the point that marin was making around what those values are, there are a lot of different components to that. As charlie was saying, it may not be just one. The scope question. I am going to guess, these statements that we want ot make are fairly holistic about what we want to learn about people and so the scope will matter a lot. If for example some of these end up having a scope that repeats a bucket in a lot of different places and allows a lot of different parties to learn about you, and less parties to learn about you, we need to learn more about what the epsilon is. Ill stop there.

Luke: (k-anonymity comments) - I just wanted to make, Charlie, I think the comments on "pick what works best", I like the practicality there. Some sort of randomness, a lot of the discussion i have been involved in adversarial models and if we have something with k-anonymity then there is a very clear incentive to put exactly 50 marks in that bin and measure they one they dont know. All of the discussions we have there is benefit to the DP, there is benefit in putting in random noise that nobody can know. It is a very nice feature of that. But i am not going to go die on a hill because it is nice to have that kind of guarantee around it.

Kyle:: the basic guarantee at least k people have this exact information about them, so you cannot learn about individuals in this group. In most cases you cannot guarantee that. It is more important that it is true than explainable. I don't think we have that guarantee anymore [insert paper into this] [[Insert talk into this](https://www.usenix.org/conference/usenixsecurity22/presentation/cohen)].

Erik: Differencing attacks?

Kyle: schemes that meet these requirements are re-identifiable, you can recover features about these roles. Read [the paper](https://www.usenix.org/system/files/sec22fall_cohen.pdf). There is a talk that is a little bit clearer.

Kiran: I am leading an effort in India to test about user consent to the measure the acceptability of this and a particular epsilon between advertisers and agencies and understand the effect this is going to have on the epsilon factor, happy to have people jump in and take a look at this project. Starting this in a couple of months. Putting together the acceptability factor of running a user interface and using a TEE or clean room for this purpose.

Charlie H: (utility bar, BYOε ARA OT test, specific adversarial settings) - From the earlier discussion about how do we pick an epsilon, I will point out the strategy we are going for ARA, at least for aggregatable reports. We are letting the epsilon value be flexible and sending whatever value they want, up to a maximum cap, and providing feedback. That is along the lines of what people have been sending before as part of the OT. This is going to be an input in our conversation when we decide what epsilon we want to support. It is going to be about use cases and utility bars. At a certain level of epsilon a certain level of slicing will not be supported, how will you handle that in your measurement? Getting to that level will be really great to set an epsilon. Even if you have an epsilon bar ?? . those types of abr will be great to help us

The last point I wanted to make about k-anonymity and other privacy definitions. I want to point out that our setting, the setting that we are in for this private measurement work, is a lot different than how a lot of these mechanisms are often deployed, in partially trusted environments. Census bureau, Facebook, what kind of data is being collected is fixed. Who is collecting the data and deploying the privacy mechanisms is often the same entity, a lot of these adversarial designs can be avoided there. Unfortunately we are in a setting where the bad guys are creating the inputs into the system. And that is really different. Often you can look at some of these definitions - in our company we do k-anon and that's fine, we have to have the security mindset that the people getting info from these systems may have full control over the inputs. That is a way different setting. It should make us feel we need stronger definitions and protections in multiple different ways.

Wendell: (how to make a business proposal on tradeoffs for privacy and $$$ survivability) - The time has probably passed. What techniques to deploy and on what timescale. Many of you work for very big companies that have disciplines on these things and have read or participated in writing these. What is the time, how soon can your team get it and deploy it and what can your team recover on that before it peters out. I think the work wants to approach this from this perspective ?? we are looking right now towards measurement in a PCM kind of setting since that seems explainable and achievable given the team we have and advertisers will pay for that. Build a business proposal for building a product, there are a couple that are public, and take a look at that.

Brian May: Couple thoughts 1. It is very hard to define a privacy definition that covers all of these use cases and it may be more productive to define a use case and then privacy definition for that. For views, there is lots of data, for clicks relatively little so for views there is more potential to add meaningful noise without having too big an impact on results.

The other thing I want to mention whenever I think about data and privacy is that data hangs around forever on the internet. If this data hangs around forever, eventually someone will find uses for it that we probably didn't think of and wouldn't condone. Is there a way to define a life to the data that is meaningful?

Luke Winstrom: How to think about whether a particular value of epsilon is appropriate for the analyses that need to be done. And I think we should convert this to be there use cases that can be supported based on the privacy definition. Those of us that build ad tech tools that put out advertisements and measure should build a useful interface for them so that they get "hey that's not a good idea - you shouldn't do that". This framing makes me much more comfortable.

Ben: I think if we do start adding DP random noise to measurement results some things that are possible today will not be in the future. Some things are not going to be possible anymore. Maybe you can no longer run daily queries, but weekly queries. I want all of the breakdowns available all the time, and they wont be available to you anymore. And you have to choose what is valuable to you.

Luke: Don't do that [the confidence intervals]. It is a terrible plan. It didn't work. Its b

Ben: even if we do all that, i am still skeptical we will even be able to do anything useful because DP is hard, you have to add a lot of noise if you want to provide really robust privacy protections just with DP you could get in a situation where just doing some basic breakdowns you already can't do it. This is my biggest concern.

Charlie: I want to piggyback on what Ben said. I feel like if you feel Luke that we can set a privacy bar and we just say we have to fit all the use cases into that, that would be a really great output from you because that is something really concrete we can say this is a hard line for Apple, this is what we think the utility we can get out of Apple users.

Luke: I can't do that today.

Charlie: Right, you said think really hard about the prior on my adversary what i want to protect against. If anyone in this group can produce a privacy bar they would never feel comfortable going above. There is going to be a privacy/utility trade off providing a well-lit path for ad tech and advertisers will stop cover tracking and all these other bad things, having a hard line we don't want to leak over X epsilon for a user may mean the whole system is so useless that everyone just goes and does covert tracking. We may end up setting some of these privacy parameters to values that are not ideal or perfect - we may have to use multiple methods such that the system is used, useful, and stops some of the bad incentives.

Luke: Belief in "defense in depth" "You must satisfy epsilon of 2 over one month for each user" - i will not say that. To make a call on you, what do you think the best you could do on a given epsilon for utility might be? Really I am pushing on the idea that we will have to make the same data available to every advertiser that is currently available in this system since it is so easy to calculate. Is all of this actually useful? If you have one count in a bin is that useful or is that statistical noise you should not be analyzing anyways? The ad tech people in this group may want to think about this as ?

Charlie: probably we don't want to just recreate the status quo with window dressing. This is why I am pushing for some of these - utility bars and looking to folks who spend time building dashboards for advertisers to tell us if there are requirements. This approach from first principles coming up with an epsilon without taking into account the utility side has real problems, at least from the chrome side, of protecting privacy in this holistic way.

Luke: We need conversations from both ends. Probably very difficult to have a per user epsilon in any of these systems, you don't know what is leaking. More attractive to do event-level epsilons. We all want to do the best for those people using our products. Some people are more sensitive to the needs of advertisers than I would ever be. If we need to condense it, here is what would be useful. If we condense it to "this" we would have no utility ever. If you gave me that, I would never ever ship this product.

Ben: for me, one particular bar, we at Meta care a lot about small businesses. If you look at our long-tail, our vast majority are small advertisers who spend small budgets, The bar for me is that they can measure at all. If you spend $10 you may only have 3 conversions, if we cannot let those advertisers see anything at all then that is a failure.

Luke: in that system you dont need this conversion data.

Charlie: Incrementality measurement!

Erik: I am hearing and want to make a formal call for soft consensus from the editors. DP should be part of the privacy definition, maybe not the entire definition, but almost certainly part of it. Are there any objections to me asking for consensus on that? Any concerns with that assumption? Is that a reasonable place to work forward from?

Luke: if you can put a # that is guaranteed given this . I do this, i sample from this

Aram: Unless there is something else you want to add, we should close out.

Thank you. Lots of good progress. Thank you to scribes and hosts.

We have a list of dates. One is going to get updated. July has been moved forward. Locked down the next two meetings. We will discuss whether we will meet in June.

1. if DP:

privacy budget management

  1. privacy budget scope (epoch, domain, etc.)
1. cross device
2. limits on multiple 3rd parties
3. what can be measured? (clicks, views, opportunities, events within an ad, conversions)
4. time delays
5. preregistration / configuration overhead
