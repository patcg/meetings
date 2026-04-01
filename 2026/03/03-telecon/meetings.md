

# Private Advertising Technology Community Group Minutes \- 2026-03 Meeting

***We agreed to record this session\!***

## Scribes

*

## Agenda

* \<= 15m: Hellos, Intros, Policies, Google Doc, Call for Scribes, Action Item Review
* \=\> 60m: Importance of Invalid Traffic (IVT) filtration and current approaches \#[237](https://github.com/patcg/meetings/issues/237) \- @donivatamazondotcom
* \<= 60m: Discussing Threat Models and Write Ups of Them \#[238](https://github.com/patcg/meetings/issues/238) \- @donivatamazondotcom
* Action Item Review

## \<= 15m: Hellos, Intros, [Policies](https://github.com/patcg/meetings/blob/main/W3C%20Read%20All%20About%20It!.pdf), [Google Doc](https://docs.google.com/document/d/1l5upphNTLcrvzHbXyiI5842QZh0WHyO0wrLSwSNBQ30/edit?usp=sharing), Action Item Review

## \=\> 60m: Importance of Invalid Traffic (IVT) filtration and current approaches \#[237](https://github.com/patcg/meetings/issues/237) \- @donivatamazondotcom

*

IVT is Measurement Integrity Slide:

MT: Is there any correlation between premium properties and better ability to detect IVT?
VP: It kind of depends. While they might have higher fidelity signals but it’s not clear they use them.
Aram: I would say that from the premium property perspective, to book more valuable advertising you need to use many IVT \- double verify and IS. Not sure it does a great job, but they do have more work to try to block.
VP: Wouldn’t take that as a truism.

Every Industry Participant is Affected Slide:

Michael: You mentioned low quality content (Made For Advertising sides).  How does that relate to IVT categories?
VP: I can’t really answer that because the boundaries are intentionally fuzzy.  MFA sites seek to stay just within policy while doing stuff that is probably outside of what the advertiser wants.  AD to content ratios are too high, it will look fishy, but it is hard to pinpoint because of the tactics they employ, because they try to avoid getting caught by IVT filters.  While enforcement does take place, there isn’t a clear demarcation.

MRC only mandated transparency

MT: Any requirements about technique for getting accreditation.
VP: Technique does not need to be disclosed, but they need to show MRC accreditor that it met the bar.
VP: MRC published guidelines (e.g., identify risk areas). Has biz identified risks? Has biz implemented controls? Accreditor then evaluates whether the risk areas are addressed.
MT: This is a custom process that gets accredited.
VP: There’s a lot of overlap in controls.
Aram: The MRC has guidelines that they require participants self-attest to.
VP: self-attestation and quality of detection. To the later there is no universal measurement quality \- it’s about whether the process laid out in the guidelines.  Self-attestation doesn’t support MRC.
Aram: Correct TAG does self-certification.
Aram: What the MRC does provide is a way for the market to decide on quality.

Users pay the price of broken IV detection

Aram: Status quo is not great right now. A Billions in fraud. Lots of CPM collapse. Significant opportunity to improve the status quo.
VP: I would take Billions with a grain of salt. Estimates are way more opportunistic than they need to be. Thinks publishers needs to do more work.
Aram:  This goes to the very problem \- we don’t have a good estimate. They range from 2% to 98%. Agree publisher side is the best place to handle this.

We should make sure to share this information around.

VIDEO available \- [https://www.dropbox.com/scl/fi/35x14jvni5b1f81y4ud78/ICT-W3C-Presentation.mp4?rlkey=asuv73putk8pgfmioem6loccs\&st=tozetncz\&dl=0](https://www.dropbox.com/scl/fi/35x14jvni5b1f81y4ud78/ICT-W3C-Presentation.mp4?rlkey=asuv73putk8pgfmioem6loccs&st=tozetncz&dl=0)

## \<= 60m: Discussing Threat Models and Write Ups of Them \#[238](https://github.com/patcg/meetings/issues/238) \- @donivatamazondotcom

This will be a follow up artifact.
Vinod: Noted that the W3C model and the RFCs are different.
MT: They come at it from a very different perspective. You are the expert so do it how need to do it. Some of the W3C is very expansive and maybe over the top.
Vinod: Definitely benefit it looking at each stake holder. The intent might be intentionally bad or unintentionally bad.

Aram: I do like the idea of surfacing the tools as we go forward. Most valuable places are 1\) pre-bid \- better trustworthy process before ad is out is super beneficial\! 2\) on ad impressions shown\!

## Action Items

- [ ] **Roxana**: Need an explainer for epsilon and privacy unit.
	  - [ ] This information should be found in [https://w3c.github.io/attribution/\#dp](https://w3c.github.io/attribution/#dp)
	  - [ ] Please review\!
	  - [ ] Also privacy working group has a basic explainer, maybe between these too it will be sufficient explanation for any needs \- [https://docs.google.com/document/d/1pE3p6TVsERPln00PLXj6j9rTdoG3PmiNHhv3NtXDtEU/edit?tab=t.0\#heading=h.3kkvhdgpiso9](https://docs.google.com/document/d/1pE3p6TVsERPln00PLXj6j9rTdoG3PmiNHhv3NtXDtEU/edit?tab=t.0#heading=h.3kkvhdgpiso9)
- [ ] **Aram**: Reach out to some Auditors for feedback on the spec and the last touch process specifically. (Will prob need help from James here)
- [ ] **Brian** (lead), **Aram** (support): Approach IAB Tech Lab for feedback on auditing API
- [x] ~~**Vinod**: Write up a threat model for fraud.~~


## Participants

1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Michael Kleber (Google Chrome)
4. Martin Thomson (Mozilla)
5. Vinod Panicker (Amazon Ads)
6.
7.
