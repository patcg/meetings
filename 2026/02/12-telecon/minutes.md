# Private Advertising Technology Community Group Minutes \- 2026-02 Meeting

## Scribes

* Pierre Tholoniat

## Agenda

* \<= 15m: Hellos, Intros, Policies, Google Doc, Call for Scribes, Action Item Review
* Proposed sub-group on optimization query evaluation: [Issue 244](https://github.com/patcg/meetings/issues/244)
* \<= TBD
* Action Item Review

## \<= 15m: Hellos, Intros, [Policies](https://github.com/patcg/meetings/blob/main/W3C%20Read%20All%20About%20It!.pdf), [Google Doc](https://docs.google.com/document/d/1l5upphNTLcrvzHbXyiI5842QZh0WHyO0wrLSwSNBQ30/edit?usp=sharing), Action Item Review

## \=15m: Proposed sub-group on optimization query evaluation: Issue 244

* Ben: Roxana and Columbia group spent some time on optimization queries, would like to widen collaboration.
  * Subgroups happened in the past: biweekly for IPA, also privacy measures
  * Goal for proposed subgroup: evaluate optimization methods
	* Both in level 1 and potential level 2 → guide level 2 features
	* Compare tradeoffs and approaches
  * Proposed logistics: biweekly, slack channel, open to all PATCG participants, minutes, reporting to PATCG (e.g. every 2 months, or at least at every f2f meeting).
  * Facilitators: Ben and Roxana.
  * Example items:
	* Expand evaluation previously presented at PATCG (in Nov?) with proper accounting. Previous evaluation didn’t consider on-device budgeting.
	* Evaluate Learning with Label Proportions (bins, noise, late binding, etc)
	* Evaluate WALR, which gave good results according to Criteo folks under certain regimes.
* Roxana:
  * It’s important to support ML, but our work so far has been focused on simple measurement queries. So there is academic interest in more complex queries.
  * Also focus on whether small advertisers would be disadvantaged, especially since DP works better on big data.
  * Roxana’s students are working on building the evaluation. They are starting with LLP, and evaluate on their own implementation of the spec, called PDSLib ([github.com/columbia/pdslib](http://github.com/columbia/pdslib)).
  * Envision making the evaluation infra public on Github so others can expand or try different datasets (Roxana et al are starting with Criteo dataset) or methods (like WALR).
  * Will report back once they have results on some optimization queries and hope to get more continuous feedback and engagement from others at PATCG.
* Ben: would like to receive ideas from others that are interested in optimization, e.g. Google.
* Aram: lots of interest from different people about this type of work.
  * Logistics: fine to put minutes in the existing PATCG repo, just add subgroup name as meeting type.
* Michael Kleber: Charlie Harrison can’t join today’s meeting but interested in joining the subgroup
* Aram: we hope Criteo will be able to join. Some parties might be reluctant to share the structure of their optimization workloads, but ideally we can find general structure.  Aram might be interested to drop in occasionally.
* Michael Kleber: in terms of scope, it’s important to take into account the fact that some browsers will keep third-party cookies, while others don’t. So an important use-case is where the browser holds some event-level data, and wants to combine it with aggregate data. This is a change compared to what we expected say 2 years ago.
* Pierre: interested in staying involved.
* Aram: we are broadly in favor of this subgroup, process is in place. Looking forward to hearing from the subgroup\!

## \=10m: Action items discussion

Roxana will follow up on explainer for epsilon by next meeting.
Aram: considering whether existing W3 guidance (https://www.w3.org/TR/differential-privacy-guidance/) is enough.
Ben and Martin: probably won’t use this.
Michael and Tara: that doc is intended for potential non-expert privacy reviewer, but might not explain the privacy properties we care about in our implementation

IAB no longer have organized  privacy sandbox review group. But reaching out to them about best people to give feedback.

Vinod will have presentation about fraud in the CG meeting next month.

## Action Items

- [ ] **Roxana**: Need an explainer for epsilon and privacy unit.
	  - [ ] This information should go into the area of the spec at [https://w3c.github.io/attribution/\#dp](https://w3c.github.io/attribution/#dp)
			- [ ] What are the answers to the questions presented in the document below are a good place to start.
	  - [ ] Please review\!
	  - [ ] Also privacy working group has a basic explainer, maybe between these too it will be sufficient explanation for any needs \- [https://www.w3.org/TR/differential-privacy-guidance/](https://www.w3.org/TR/differential-privacy-guidance/) \- at this time we do not want to use this doc.
- [ ] **Aram**: Reach out to some Auditors for feedback on the spec and the last touch process specifically. (Will prob need help from James Aylett here)
	  - [ ] Make sure to check in for Feb.
- [ ] **Brian** (lead), **Aram** (support): Approach IAB Tech Lab for feedback on auditing API
- [ ] **Vinod**: Write up a threat model for fraud.

## Attendees

1. Aram Zucker-Scharff (The Washington Post)
2. Roxana Geambasu (Columbia U and part-time Google, here in Columbia faculty capacity)
3. Michael Kleber (Google Chrome)
4. Alex Turner (Google Chrome)
5. Pierre Tholoniat (Google)
6. Tara Whalen (W3C)
7. Ehsan Toreini (Samsung)
8. Benjamin Case (Meta)
