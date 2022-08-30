# April 2022 Virtual Meeting

The Private Advertising Technology CG's will be meeting on April 5th and 7th for 3 hours each day.

## Schedule 

### Day 1 Start 

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
**| 22:**00 (10 PM) | 05 Tue | Tokyo         |
**| 23:**00 (11 PM) | 05 Tue | Sydney        |
**| 06:**00         | 05 Tue | Seattle       |
**| 09:**00         | 05 Tue | Boston        |
**| 14:**00 (02 PM) | 05 Tue | London        |
**| 15:**00 (03 PM) | 05 Tue | Brussels      |

### Day 2 Start 

| Time          | Day    | Location      |
| ------------- | ------ | ------------- |
**| 22:**00 (10 PM) | 07 Thu | Tokyo         |
**| 23:**00 (11 PM) | 07 Thu | Sydney        |
**| 06:**00         | 07 Thu | Seattle       |
**| 09:**00         | 07 Thu | Boston        |
**| 14:**00 (02 PM) | 07 Thu | London        |
**| 15:**00 (03 PM) | 07 Thu | Brussels      |

## Joining Information

~~[WebEx Link](https://mit.webex.com/mit/j.php?MTID=m6ba2258ea91917d9b56eb3e3865cda09)~~

WE HAVE MOVED TO ZOOM FOR DAY 2

[Zoom](https://mit.zoom.us/j/95356244879?pwd=NDBwZmxleTMwcHFpZG1MZW1tUXhVUT09)

[Minutes Doc](https://docs.google.com/document/d/1zsFNB-1tNUbSP6V2xpCDhiaPUN3B_lT_qn0OnzLvtYM/edit#heading=h.emacos7anbx5)


## Agenda

### Day 1 Agenda

**- <= 10m:** Intro, Google Doc, Call for Scribes
**- <= 35m: 25m Presentation on:** [Consider the Reach and Frequency Use Case for Ads Measurement](https://github.com/patcg/meetings/issues/12) by [@rmirisola](https://github.com/rmirisola) / 10m Q&A
**- == 5m:** Break
**- <= 1h 15m:** [Should PATCG be opinionated on which technologies are used to enable privacy?](https://github.com/patcg/meetings/issues/39)
  - 5m Introduction of Topic and Proposed Private Computation Goals by [@eriktaubeneck](https://github.com/eriktaubeneck) 
  - 5m Questions / Discussion on Proposed Goals 
  - 7m Introduction to TEEs by Andras Slemmer 
  - 7m Attacks on TEEs by Yuval Yarom
  - 11m Questions and Discussion on TEEs
  - 10m Introduction to MPC
  - 11m Question / Discussion on MPCs 
  - 19m Discussion on Next Steps for Consensus 
**- == 5m:** Break, free talk, etc...
**- ~ 40m:** [Reviewing](https://github.com/patcg/meetings/issues/7) Working Group [charter](https://github.com/patcg/patwg-charter/blob/main/charter.html), [PRs](https://github.com/patcg/patwg-charter/pulls) and [Issues](https://github.com/patcg/patwg-charter/issues). 
**- <= 10m:** Overflow for working group discussion OR Schedule next meeting

### Day 2 Agenda

**- <= 20m:** Opening Review / Q&A
**- == 30m:** 20m presenting [Collective Governance of Infrastructure proposal](https://github.com/patcg/meetings/issues/40) by [@darobin](https://github.com/darobin) / 10m Q&A
- == 5m break
**- == 15m:** Q&A on [Operational Experience with MPC](https://github.com/patcg/meetings/issues/44) by [@tgeoghegan](https://github.com/tgeoghegan)
**- <= 30m:** [Progress report on Private Measurement](https://github.com/patcg/meetings/issues/42)
**- == 30m:** [Update on Privacy Principles](https://github.com/patcg/meetings/issues/43) by [@darobin](https://github.com/darobin)
- == 5m break
**- <= 40m:** Review [Charter Changes and Calls for Consensus](https://github.com/patcg/patcg.github.io/pulls) with [@aramzs](https://github.com/AramZS) & [@seanturner](https://github.com/seanturner)
**- == 5m:** Schedule next meeting OR Charter discussion overflow. 

## Minutes

**https:**//docs.google.com/document/d/1zsFNB-1tNUbSP6V2xpCDhiaPUN3B_lT_qn0OnzLvtYM/edit?usp=sharing


## Day 1


### Administrivia

Agenda Bash


### Intro, Google Doc, Call for Scribes

**Sean:** Welcome, Code of Conduct, CLA. 

**Aram:** Please volunteer to scribe!


### &lt;= 35m: 25m Presentation on: [Consider the Reach and Frequency Use Case for Ads Measurement](https://github.com/patcg/meetings/issues/12) by [@rmirisola](https://github.com/rmirisola) / 10m Q&A



* **Raimundo Mirisola**: 
    * Two part presentation. Why Reach & Frequency is important to advertisers. Technical aspects and why it’s relevant to the PATCG.
* **Artie Bulgrin:**
    * Fundamentals as to why reach is important. Quote from Marc Prichard from P&G. How many people are we reaching, how often are we reaching them, how effective is it, how efficient is it?
    * Importance of reach:
        * Growing market share is the most important thing
        * Typical brand may lose half its customers
        * Growth comes from gaining more buyers
        * Law of double jeopardy: brands with less market share have fewer buyers and are less loyal. Sales are lower because they have fewer buyers who buy less often
        * Pereto Law: not 80/20, 60/20, meaning that only slightly more than half of brand sales come from 20% of customers
    * Marketing funnel
        * Suggests that a balanced approach, long term focus brings bigger effects
        * Marketing scientists recommend a 60 / 40 approach, top of funnel vs lower funnel
        * Nudging people along is important, never know when the next purchase will happen
    * Marketing science laws and truths
        * Long term brand advertisers by refreshing memory structures with emotional messaging
        * Short-term actiation uses rational messaging to nudge a customer
        * Mostly brand growth comes from including non-buyers, hard to get existing buyers to buy more
        * Long term + short term must coexist. Not an either or. Firms that spend too little on brand get too little on activation. Too little on activation don’t reach full potential.
* **Raimundo**:
    * What is R&F trying to solve? Counting unique people reached across different publishers and platforms. 
    * Counting unique people is not the same as counting unique devices / accounts.
    * Even if you solve this with a unified private ID solution, you still have to map to people.
    * Typical solution is to build a model from signals which allows you to understand how the number of unique people you are seeing from number of unique signals.
    * Requirement #1: Model needs to have access to private ad event level data that ideally includes cross site signals. Corrects for demographics, device, usage, etc. Need information to deduplicate people across different use cases.
        * Challenge: How do we deploy this model? Where do we run it? How does it preserve privacy?
        * Suggestion: Run the model on device. Sensitive data doesn’t leave device. Output is sent to some sort of secure aggregation. 
            * Need to keep models up to date. Can be resource hungry.
        * Suggestion 2: Deploy some parts of the model in the secure aggregation. Depending on the choice of privacy preserving tech, it can be harder or easier to run the model.
        * Spectrum of solutions.
        * Challenge seems relevant and similar to approaches discussed
    * Requirement #2: Even if you figure out how to solve the first challenge for one platform, you want to be able to measure the number of unique reach across platforms. It may be the case that solutions are different across platforms, if the outputs of different platforms are disparate, how do they get combined?
        * Some things we do know:
            * Using local differential privacy by adding noise on each platform, the noise grows somewhat exponentially, won’t scale to a large number of platforms.
        * Could have each platform pick their own solution, but then need some sort of private/secure cross platform aggregation.
        * Challenges:
            * Cross platform secure processing network trust model
            * Cross platform privacy budgeting
    * Summary and questions:
        * Simple R&F is important, unique cookies is not unique people
        * R&F needs to run models which has access to cross site data. Should the PATCG consider R&F when designing these solutions
        * Need this solutions to be interoperable across platforms. Local DP by platform doesn’t work. Should PATCG help with this problem?
        * WFA Cross Media Measurement initiative is working on a solution here based on MPC. Would this group be interested in learning about it?

**Questions**



* **Brian May**
    * Curious about how accurate these measurements need to be. Talking about user level accounting. Wondering if we can’t get 60-80% of the value by doing things on a statistical/probability basis?
* **Raimundo:**
    * This is what the models are attempting to do. They using the cross site data as input, but make estimations. WFA initiative is targeting for being within 10% of the correct answer 90% of the time.
* **Brian**
    * If I had estimates of individuals, could I measure this?
* **Raimundo**
    * Don’t need to know if a particular person saw an ad or not. Want to measure the audience behavior
* **Brian**
    * Seems like there are different classes of statistics . How many people have I touched, how many people across platforms.
* **Raimundo**
    * Not sure I’m fully following, but the models fail “gracefully” as it gets less data.
* **Brian**
    * Let me rephrase. If you know very little about the user, but that has information about the campaign, that’s useful right?
* **Raimundo**
    * Have done some research on this, can do some without impression specific data. But it doesn’t fully scale. For more accurate cross platform, you need more contextual data on the device, on the user, ect. When 3rd parties are deprecated, the quality will be deprecated. Looking to have privacy preserving tech in place.
* **Ben Savage**
    * Want to understand more about the use case. What the solution precisely needs to do. Meta offers tremendous metrics to marketers. Not convinced their all use full. To make this useful, how often does it need to run? How accurate does it need to be? +- 20% ok? What are the needs for demographics? What as a marketer would you do with this.
* **Raimundo**
    * Having break downs by demographics is useful. Having more frequent data helps optimize campaigns. When you measure large brand campaigns, age and gender in 5/10 year age bands are important. Use this for “cross media planning”. In general, the shape of the reach curve gets flatter (ie. less marginal reach) as you spend more on a platform. Depending on the campaign, you can make a hypothesis about the curve.
* **Ben**
    * Imagine we have a solution that’s cross platform, interoperable, but only could run once a week. Would that work?
* **Artie Bulgrin**
    * Wouldn’t be unacceptable. What we do know today is that marketers can’t plan for reach. For a campaign for deodorant, want to reach everyone who doesn’t stink. Right now, can plan for reach on Google or on Facebook, but I can’t do so for the internet in general. A weekly report would be far better than what they have today and is better than the past. Need to build up a dataset to plan for the future. Other thing this schema needs to do is to control excessive frequency. Excessive frequency can turn into media blindness. Right now, if we can do this on a weekly or monthly basis, right now most of this comes from model building.
* **Ben**
    * I think cross platform frequency control is very difficult. Is it OK to measure, but not control?
* **Artie**
    * Would be a question for marketers. Would need to understand why it’s harder.
* **Ben**
    * Measurement is one thing, showing ads is another.
* **Raimundo**
    * Measurement is a good step, can can help marketers experience.
* **Evgeny Skvortsov**
    * Getting measurement is first step in trying to get to capping.
* **Nick Doty** - is the problem the adding of noise for differential privacy? it seems more an issue of correlating identifiers between platforms/devices
    * Question about #2: Talk about Differential Privacy because it adds up. Is the problem that the noise ads up or that you can’t match up people across the different platforms?
* **Raimundo**
    * There are ways to create a differentially private set of people, and then you can produce DP unions of those sets. But because you are adding noise earlier in the stage, the noise compounds.
* **Nick**
    * Is the noise about the count or the people?
* **Raimundo**
    * It’s the count. Want to see the size of the union. If that noise is added for each platforms, it adds up very quickly.
* **Aram**
    * Encourage foks to follow up on the issue
* **John Douglas**
    * Advertisers want perfect information and aren’t going to get it. Always are going to bring their unique perspective. Question around what’s an acceptable solution for frequency capping, what types of data are available, etc. As a group we should focus on things that are much more limited in scope than something that is cross device. Media isn’t just planning for web. If we can be much more focused than a replacement for everything that 3rd party cookies do today, but instead do one thing, then I think we’ll be more successful and faster.
* **Mariana Raykova**
    * Wanted to highlight the two technical points, in the context of the last meeting, to make sure I got it right. Interoperability will need different platforms to agree on the security/privacy properties. They are exporting into some system which enforces that. 
    * The WFA solution is already having a solution to the problem to a large extent. Maybe this is too much for this group to bite off. WFA solution is a good stepping stone.
    * Need more access to signals on device. We need to rely on the browser providing those signals in some privacy preserving way.
* **Martin Thomson**
    * Starting to realize we may have different understanding of interoperability. May need a definition.
    * Asking about the status of the WFA - document is 18 months old. Is there any status on the current deployment, etc?
* **Raimundo**
    * Have developed a protocol to do this in MPC. We have a prototype, looking to deploy it this month. Over the next year will be running tests on that proof of concept. Paper you may have seen is the underlying MPC protocol. Can bring a more human readable document to this group.
* **Martin**
    * Paper I saw had a bunch of references to VIDs and SUMIDs without definitions. Anything else you can bring would be helpful.
* **Eric Rescoloa (EKR)**
    * Question that was asked, less about technology and more about interest. I think this is not something we should focus on. I think we should do *something* and this will get in the way.
    * With regards to this proposal, where are we at today? Is this a regression, or are you asking for more than today? Can this be addressed with sampling of people who have opted into more data sharing as opposed to whole population measurement.
* **Raimundo**
    * When we think about these standards, the argument is that there are a wide range of solutions. Hopefully we can come up with more generalized solutions.
* **EKR**
    * Understand why you want it. Curious what you can currently do.
* **Raimundo**
    * We have a prototype in the WFA solution. These tend to leverage 3rd party cookies. That functionality will go away, looking to preserve some of that. Looking for ways to get more access to the reach data in privacy preserving ways.
* **Andras Slemmer**
    * Address binary verifiability
    * Example of high-level side channel


### [Should PATCG be opinionated on which technologies are used to enable privacy?](https://github.com/patcg/meetings/issues/39)

[[Group slides](https://docs.google.com/presentation/d/1huChDQU_JsEk5TgcSqZXc7kRvlh2f4urqlVfY2WIjn4/edit?usp=sharing)]

[scribe: wseltzer]


#### 5m Introduction of Topic and Proposed Private Computation Goals by [@eriktaubeneck](https://github.com/eriktaubeneck)

[3d presentation, after audio issues resolved]

**Erik: “Private Advertising Technology”:** private advertising use case with secure/confidential computation. Not talking about use cases here, but focusing on secure/confidential computation as a tool. 

**Goals:**

**Client data secrecy:** User agent data (input data). We don’t want anyone to learn something they don’t have otherwise. Not cross-site.

Purpose limitation

Correctness, e.g. against malicious client

Technologies currently proposed, TEEs and MPC. 

Client data is encrypted, given to secure computation, revealed output is the only thing that can be learned. 


#### 5m Questions / Discussion on Proposed Goals


#### 7m Introduction to TEEs by Andras Slemmer

**Andras:** engineer from Decentriq. 

We use TEEs to orchestrate computations among mutually distrusting parties. Share results in access controlled manner, without giving access to raw input data. TEEs allow controlled access to code and data: confidentiality, integrity, freshness; attestation (proving you’re communicating with isolated code). HW vendor is the ultimate root of trust. When connecting to isolated code, you get signature from vendor. 

TCB recovery. (trusted computing base). Recovery process triggered when vuln found in hw or low-level sw, vendor invalidates certain keys used in attestation. Status code signed over by a vendor. Revalidate. Enables collaborative iterative hardening between researchers and vendor. 

Data at rest. Features needed to derive persistent keys. 

Programming/security model. Discussing Intel SGX and AMD SEV-SNP. 

Intel SGX, you load single-address-space single process. Application that hosts the enclave is treated as malicious, can’t make any system calls. Means you have to write everything from scratch. Newer approach based on virtual machines, put a kernel into the isolated environment, more usable but increased attack surface.

**Maturity table:** in my opinion, only Intel tech is mature. Extensive security research, many vulns found and addressed. Sw support is fairly good, need to write everything from scratch. Provided in the cloud by eg. Azure. Deployment and ecosystem still challenging. 

AMD SEV-SNP. Hardware mature, lots of work still to be done on sw side. Cloud support not yet available

NVIDIA new GPU with attestation capabilities. 

Performance.Because these techs use existing CPUs, performance hit is low. 1-2x slower. Memory limitationm lifted with icelake series. 

**Threat model:** initially, vague security guarantees. We can recreate threat model from reaction to vuln disclosures. 2019 plundervolt: changing voltage in sw to glitch CPU. Intel responded by issuing microcode fix, recovery process. VoltPillager, 2021, Intel said “not in threat model”. SO we see threat model is remote attacker who can get root privileges, not including physical attacks. These technologies don’t defend against attacker with physical takeover. 

TEEs are tradeoffs between security and perf/functionality/flexibility. So long as you can accept iterative hardening process, limitation to remote attackers. 


#### 7m Attacks on TEEs by Yuval Yarom

**Yuval:** University of Adelaide. Talking about attacks on SGX. 

**Model:** dev writes software, puts it on cloud server. What happens with user-produced info, how do we limit access? SGX enclave: attestation promises correct software, intel processor, isolation. 

**Where these promises can break:** Side channel attacks.  Program running affects microarchitectural state, as caching occurs, execution time improves. Side channel attacks reverse the process: monitor the execution time to learn microarch state, learn what previous programs have run. 

Sidechannel attacks known for 20 yrs, used to extract cryptographic keys. 

Untrusted operating system controls operation of enclave. It can single-step enclaves (run them one instruction at a time), observe all accessed memory addresses (though not what data was read/written). But since the branching depends on the data, can reveal information. In cryptography, answered by constant-time, but that’s unlikely to work with lots of data. Also, split-horizon attacks. OS can’t control what enclave does, but controls its interface to disk, network - i.e., what it sees. 

Another set of attacks, hw vulns. Some give read access to enclaves, get attestation keys - then attacker can attest to anything, run whatever sw they want.

Secure recovery isn’t easy. Once enclave is compromised, all its data is compromised. A period in which we have no access to the service. 

**Software issues:** issues of trust between sw dev and end-user. Attestation verifies you’re running expected sw, not the functionality of the sw. If user doesn’t trust sw dev, still needs to analyze the program. If you verify binary, hard to match between source and binary. Potential existence of vulns gives plausible deniability to insert backdoors. Run more securely on untrusted platforms, don’t protect against attacks from SW vendors. 


#### 11m Questions and Discussion on TEEs and Proposed Goals

**Ekr: A few notes:** these properties seem horrifying. The attacker has the device in their physical possession, and it’s not secure against them? How can it possibly work against well-funded attacker? 

**Andras:** if it’s possible for your use case that the attacker has physical access, 

**Ekr:** Not sure what the enclave is doing if it’s not protecting against untrusted environment. The data center is run by an adversary. Users wish their browsing info to be private, processed by people they don’t trust. I don’t understand how people think these systems would be deployed. 

**Brad:** one proposal, cloud host hosts systems with TEEs, browsers trust that the system is run, ad tech sends programs to analyse data. 

**EKR:** then you’re trusting the cloud host. What does TEE add?

**Andras:** trusting a party that doesn’t have incentive to mount attack. 

**EKR:** why not just use general purpose computing and promise not to look> 

**Andras:** protecting against remote attackers compromising the VM. 

**Aram:** let’s put this on hold and continue in issues: who owns the data center and has access to it. 

**BMay:** Our concern should be both those running data center and those who have influence over it, e.g. misusing location data to find people to deport. 

**Q:** seems resource intensive. Can you speak to the potential barriers to entry for advertisers? 

**Erik:** standardizing in group, with aim that there’s protocol, open source implementations, costs would then be the costs of running the code. 

**Stefan:** doesn’t require special hardware, already exists in Intel and AMD CPUs [Andras: But not in desktop CPUs] . 

**Bmay:** there are certain classes of problems ad tech can solve on their own, now. If we go to a model where everyone has to work with encrypted data, then they need to use third parties to process. 

**Andras:** that sounds like argument against MPC. 

**Aram:** to the issues-> what is the cost, and who is paying for it. 

**Bmay:** not just monetary cost, expertise. 

**Mariana: what I heard from these two talks:** SGX is the most mature, and we can break it in many ways. Do we have any hope we’ll be able to reason about TEEs in more secure way. In cryptography, well known hardness assumptions we can study. Don’t see anything similar here. Any hope for constructive argument? 

**Second question:** memory. If you don’t have trusted state, you can do memory rewinding attacks, compromise security of entire protocol. 

**Yuval:** you won’t get the level of guarantee you can get in cryptography. Hardware is too complex, vendor incentives wrong. Look at it as defense in depth. More security than privacy. I don't see it as a tool for generating trust. 

**Andras:** TEEs are practical tool, iterative, not proof. Security and stacks are complex. Iterative hardening to build security.  Re binding between code binary and source, need binary reproducibility. 

**Mariana:** Memory? 

**Andras:** SGX works with encrypted data in DRAM. In caches, unencrypted. 

**Yuval:** you cannot do replay protection

**Andras:** there are protocols that enable this that require distributed state 50+ nodes at the same time and you constantly need quorum.

**Mariana:** this is one way to implement persistent state. we cannot get around the need for this

**Andras:** in memory we have replay protection

**Mariana:** we need data on disk, for differential privacy budgets; if we can rewind, we can attack DP properties

**Andras:** The data that you persist can exist in two categories, state - which changes over time - the other is integrity data that you check and encrypt. If you provision some data and a hash. But for DP you need a counter and we only have built in counters in memory so you need to keep the CPU running and you can use this to protect the state. 

**Stefan:** You need to use counters in the hardware as well. 

**Andras:** the security properties are  weaker 

**Betul:** Attestation: for privacy, there is a unique signing key per CPU version Intel uses so that clients are not tracked. If that key leaks, it effects all versions. How hard is revocation of keys? How attacks mitigated: hardware level/software level?



* Privacy protections of intel? 
* When the CPU requires attestation it is one single key per model and creating complication. 
* Answer is on the chat
* They are ditching and designing a new protocol. 
* We talked about SGX which is great
* How about near original machine based proposals (???) 
* What are the major comparisons if you look at use cases, I know that the security / attack surface is larger. What is the status. 

**Andras**

* Not enough security research done on that 
* Broken until proven updated 
* Co processor there they found a vulnerability and even though AMD patched it they couldn’t prove it in attestations. AMD SEV that’s the one that’s useable where the version is transparent. There are attacks that specifically target the coprocessor and a glitching attack (to which there wasn’t an official response) physical attacks are not part of their threat model. Side channel attack published and mitigated 
* Nothing compared to SGX security research. 
* It lets you put in existing code though in a way that SGX cannot which is why it is exciting. 

**Nick:** Useful to have the properties Erik presented. Not sure that’s a complete list. I;m concerned how we can have confidence in the other properties. Not sure TEE as proposed can meet client data secrecy. What’s the intended way to show the user that their sensitive data is ok to send because secrecy will be provided? How will give user confidence in secrecy, purpose limitation? 

**Andras:** if you mean visual feedback, that’s where browser can play a role. Do something similar to TLS. Similar to browser lock, do a drop-down on TEEs to offer visual feedback. 

**Nick:** idea that the information will be provided back to client, what sw is run on remote server?

**Andras:** code hash, browser shouldn’t accept anything except completely ok. 

**Erik:** this is probably more a general question for browsers, user agents. In this group, we should be developing protocols that adhere to the principles. Then UAs can give visual cues. Give ability for UA to take action on behalf of user to guarantee these properties. “Purpose limitations” refers to not running arbitrary code, but specific protocols deployed in these systems. 

**Kleber:** TEEs as described here can plausibly be used as component of larger system. Posted link: [https://github.com/WICG/conversion-measurement-api/blob/main/AGGREGATION_SERVICE_TEE.md](https://github.com/WICG/conversion-measurement-api/blob/main/AGGREGATION_SERVICE_TEE.md) 

Basic idea is that encrypted reports for aggregation get sent to ad tech. Holder of the cryptographic key that is able to decrypt those reports is the one that talks to a piece of sw that runs in the TEE and assures it;s the right piece of sw. Another step in the middle where the person running the aggregation service is not the adtech, but the cloud host (e.g.IBM, Amazon), 3 parties: one holds keys, one has encrypted data, one provides the safe environment for processing. If you don’t trust Amazon not to run voltage attacks, this model won’t work. TEE is the way in which the cloud provider says this protects against many classes of threats, though not all.  It’s a component of a system, as is MPC. e.g. cryptographic key, how do you know it can’t be stolen. TEE is a part of a bigger picture, plausible component. 

**Aram:** break out concerns about sorts of attack in issues in [https://github.com/patcg/private-measurement](https://github.com/patcg/private-measurement) . 

[Useful note in chat from Mariana Raykova: [https://securecomputation.org/](https://securecomputation.org/) for anyone who wants more basic intro]


#### 10m Introduction to MPC

**Erik:** a light intro to MPC. A bunch of clients that hold some data. [diagram: MPC with 2 helpers] Assume the helpers won’t collude. Additive secret sharing. Individually, the values don’t reveal the input. 

[slide: XOR secret sharing]

Take individual input data value, split it up. 

Once we have secret shares, we can compute on them. [examples on slide] garbled circuits. 

**Threat models:** MPC can be implemented for various threat models. 

**Least protective:** semi-honest / honest-but-curious, holds only if all parties follow the protocol. 

**Covert:** may still expose client data, but detectable with probability p

M out of N malicious. Resilient against multiple malicious nodes. 

**Most robust:** N-1 malicious, you need to trust only one node. 

As you go down the list, can protect against bigger threats, more costly. 


#### 11m Question / Discussion on MPCs

**EKR:** What are you trusting in terms of endpoints? MPC ensures that a single defection can’t compromise the data. Contrast with the TEE threat model. If TEE actually promised that even someone with physical possession couldn’t break the TEE, then you would have a two-party system in which you were safe if either the TEE vendor or the TEE operator was not defecting. However, that’s not the current TEE guarantee.

**Raimundo:** can we think of TEE as semi-trusted model?

**Erik:** approximately 

**Mariana:** I don’t quite agree. Depends what guarantees we’re trying to make. Difference is are we distributing trust, or forced to trust *a* party? THat’s why I was trying to ask questions to quantify. 

**Erik:** in semi-honest case, you do need to trust all the parties. 

**Mariana:** case-by-case. Not all semi-honest protocols let a single defector get all the data. 

Ben Savage (can TEE be evolved to have similar trust requirements?): Very desirable property of MPC model, a single malicious party can’t compromise the input data. Whereas TEE has two single points of failure: HW vendor, someone with physical access to the machine. Is there a composite system we could buid out of multiple TEEs to creatively construct something with good performance and distributed trust? 

**Andras:** various papers proposing such a system for BFT consensus. My understanding that initial phase could be put in TEE. 

**Andrew Knox:** [paper reference](https://eprint.iacr.org/2020/1561), where if TEE is corrupted, you don’t get response. 

**Nick** (communicating to the user level of trust/whom trusted with mpc): similar to previous question. How do we provide user confidence? UA can encrypt data to multiple parties, assure no one else can get the data. Tell user, if you trust at least one of these parties, your data is secure. 

**Erik:** yes. 

**Bmay:** No matter how secure the compute stage is, we also have to validate that what comes out of the compute stage is privacy-preserving. 

**Erik:** yes. Entire separate discussion, what’s the privacy-preserving thing we want to do with these tools. 


#### Discussion on Next Steps for Consensus

**Erik:** it’s reasonable to say we’re opinionated, not just going to trust a clean room. Align on what techs we think satisfy the conditions we want. Next steps, maybe a group of folks who care about this work on an issue, bring to next meeting to try to reach consensus. 

**Aram:** makes sense. We’ve talked about lots of things to bring to issues, including threat model and responses. Bring further discussion to next meeting. Lots of learning still. 

Raimundo, suggest you bring your question (from the queue) to the private measurement issues. 

**Raimundo:** makes sense. 


### == 5m: Break, free talk, etc...

### ~ 40m: [Reviewing](https://github.com/patcg/meetings/issues/7) Working Group [charter](https://github.com/patcg/patwg-charter/blob/main/charter.html), [PRs](https://github.com/patcg/patwg-charter/pulls) and [Issues](https://github.com/patcg/patwg-charter/issues).

**Aram:** We have some issues, pull requests. Want to see how we can proceed. 

**Aram:** [Issue #9](https://github.com/patcg/patwg-charter/issues/9). Deosn’t make clear what stage to advance proposals towards. Proposal: evergreen. Variant on slide 8. Sean has a pull request. 

**Sean:** Yes. pull request follows this.

**Brian May:** Please describe the evergreen model.

**Sean:** Basic premise is you don’t have to go all the way to recommendation. Just keep the standard up to date. 

**Aram:** This is acceptable as far as I’m concerned. It’s a minor change. Call for consensus. 

**Jeffery Yasskin:** We should distinguish between CR and draft. “This feature is ready to implement” and “we think this is standardizable”. Living standard process is new - but I think the CR draft stage is intended as “please come implement this” status. 

**Sean:** I’m willing to take change requests. If you’ve got those words in your head - that’d be great. I did put something in about 2 interoperable implementations when we get to the CR stage.

**Aram:** Sounds like we agree in principle and maybe some wording changes. 

[PR #15](https://github.com/patcg/patwg-charter/pull/15)

**Aram:** Description of consensus. It’s a link. We will use the W3C process. Any objections? No objections. #shipit

[PR #14](https://github.com/patcg/patwg-charter/pull/14)

**Aram:** Community stakeholder feedback collection process. In addition to horizontal reviews, add a community group charter change. Basic changes intended to create a 4 week period for the community group to collect feedback from stakeholders who are not normally involved in working groups. Suggestions include a twitter account. Also have an opportunity for documents in the admin folder. 

**Martin:** My objection originally was that we were describing the process the CG would follow. When you start talking about opening issues, I don’t think we need that much detail. There is a wall of text here - the less the better.

**Aram:** When we get this to a slimmer stage, is this something we want in the Working Group charter? 

**Brian May:** How will we communicate with the wider community? Do we want a non-technical version of the proposal?

**Aram:** We can discuss this in the community group charter change. The W3C does have approaches to “explainers”. I assume any proposal that hits a reasonable level of maturity would have an explainer.

**Wendy:** Typically W3C groups establish coordination with other groups to get that feedback. Don’t need to specify too much detail about how their review happens. 

**Sean Turner:** We do have to time bound this. Asking some groups for input might entail waiting a LONG time. We need people to shepherd this feedback. 

**Aram:** Those who are interested in engaging particular parties - please help us collect that feedback.

**Wendell:** 4 weeks is the cadence of this meeting. It’s also the browser release cycle. For many of us a 4 week frame goes by in the blink of an eye. It may be that the 4 week number is worthy of some quibbling. 

**Aram:** I’m interested in the PR on hearing more about the time period. I’m hesitant to put it at more than 4 weeks. Will note that most W3C groups which do horizontal reviews don’t take longer than a month. I don’t want this period to be particularly long. And note that the candidate recommendation period is 3 months. 

**Sam Weiler:** This specificity is overkill for groups in the same problem space. I’d say we will notify the PAT-CG and cut out all the specificity. 

**Ekr:** If we will bother to say we will do something, the CG is the least relevant to ask for comment. Web-app-sec and PING, those have lower overlap. 

**Aram:** The idea is to let the CG orchestrate out-of-W3C feedback. 

**Ekr:** I thought the previous text was OK. I think it’s odd for the CG to orchestrate. If we will get external feedback fine, but why have the CG coordinate?

**Aram:** The original text described it in more detail. The CG has a greater level of access because anyone can join it. Private advertising technology has a big impact on a lot of stakeholders. I don’t want the working group to spend its time on that engagement.

**Ekr:** I don’t see how this works. If a non-technical person has concerns and they talk to the WG - how does that work? 

**Aram:** Is the WG going to be spent this way?

**Ekr:** One thing is notification. I’m not worried about that. Assimilating the feedback is hard. If anything the W3C does which has a big impact requires aggressively collecting feedback we will have to do a ton of active outreach.

**Aram:** I agree in principle. I think there is some role for the community group to engage with the community. I hear that even if this change is made - it’s not ready. We will continue to discuss on the PR.

Issue #13

Intended to be addressed by a PR

Issue #16

Not ready to discuss. This is new.

Issue #10

Blocked on a change to W3C processes.

Issue #8 (and others…)

…we have less than 10 minutes. James - can you speak to this briefly.

**James:** #16 is similar. It requires all parties to have access to the input data. #8 technical vs non-technical. If SWAN were to be advanced through the W3C… it seems ridiculous that a group called the “Private Advertising Technology” group couldn’t advance that. 

**Aram:** So the new issue #16 isn’t intended to close #8?

**James:** It has an impact on #8. It’s a sub-issue. Removing data, preventing competing solutions. 

**Aram:** 2 pieces, the engagement with non-technical stakeholders, and the issue of non-availability of raw input data. Can we close #8 and #5 (which seem similar) and keep open this issue #16? 

**James:** I would like the group to be broad enough to accommodate solutions that have non-technical components to them. 

Issue #7

How do we make sure that the working group charter involves work on non-browser things like TEEs / MPC / Bluetooth? This might be unclear. 

**Ekr:** I thought that the existing charter did contemplate things like MPC. If people think that this charter excludes MPC - that’s an oversight on my part. This seems more like it’s about something else. 

**Alex:** I wanted to note that I don’t speak for everyone here, but in experience, there is a mass of cross-functional staff behind the people’s faces that you see - because not everyone can show up. Making the statement that we are not including cross-functional stakeholders is incorrect. We are engaging with clients / legal / policy / advertisers large and small. We should dispel this inaccurate claim. 

**Aram:** I generally agree with this. James, I’ll give you a second to respond. #5, #7 and #8 are intended to address a single issue. 

**James:** Alex’s point about multi-functional people. That’s not my intention. It’s about the role those disciplines play. I’m reminded of a discussion with the TAG where I was told it’s not possible for a supplier to represent its customers. To EKR’s point, we need to represent multiple disciplines in the solutions we develop. [Note: added later - refer to [this comment on cross device](https://github.com/patcg/patwg-charter/issues/7#issuecomment-1088957780)] 

**Aram:** Is #5 / #7 / #8 all intended to address the same point?

**James:** I think we can make a pull request to address all of them. 

**Sean turner:** We shouldn’t be waiting on submitting a PR until its pre-accepted. PRs will get bashed - that’s how it goes. 

**Really useful note from chat here:** **&lt;jyasskin>** Note that "bashed" doesn't imply that it'll get strongly criticized. The IETF uses "bash" to refer to adjusting the agenda at the start of a meeting, so it includes even friendly amendments.

**Aram:** We have a bit more time set aside on Thursday to continue discussions about the charter. 

**Sean:** We put an extra day between the meetings for exactly this.

**Aram:** Thanks everyone for your participation. See you on Thursday. 

**Sean (added later):** I also use the term agenda bash to refer to requests to rearrange the agenda.


## Day 2

### Opening Review / Q&A

**Scribenick:** npd, schoppmp

[arranging scribes]

**Aram:** Run-through from Tuesday. Extensive notes plus presentations. We got an introduction to relevant technologies (MPC, TEE, etc.) including attack vectors and threat models. Need to explore more before we have consensus on a particular technology. Contribute on repo dedicated to measurement.

Working Group charter continued to be discussed, particularly on stakeholder input. Waiting for PRs for further discussion. PR is welcomed, best way to suggest or discuss charter changes.


###  [Collective Governance of Infrastructure proposal](https://github.com/patcg/meetings/issues/40) by [@darobin](https://github.com/darobin) / 10m Q&A

Pushed to next meeting.

### 5m break

### [Progress report on Private Measurement](https://github.com/patcg/meetings/issues/42)

**Aram:** not getting into MPC details, but we heard conversations about utility vs privacy, defaults. Can we make progress on these issues today? Tests. Is there anything else we would like to see about tests or the particular needs for tests?

**Betül:** has anyone changed their minds on tech based on earlier discussion?

**Brian:** useful to have a collective sense of the cost of various solutions. If collective resources need to be combined, we should know who will have to contribute what. Centralized solutions like MPC will rely on someone running the system.

**Aram:** where might costs be blocking for particular participants?

**Brian:** not just financial costs, but necessary expertise.

**Ben:** haven’t changed my mind, but clarifying to hear the threat model as about physical security. Could cloud providers have locked cages where the provider didn’t have access to the servers themselves without a physical key access from the separate party? Layered solution where you would need collusion between multiple cloud providers?

#6 high-risk contexts

**Don:** related proposal from Anti-Fraud CG; don’t want to get out of sync.

#3 utility vs privacy for attribution proposals

[switched from webex to zoom, *sigh*]

**Nick:** Different attribution proposals in the repository, some of them non-MPC, non-TEE (PCM, etc.). Do we want to discuss that here as a comparison?

**Aram:** got the impression that this is the venue for discussion.

**Kleber:** single Chrome JavaScript API produces different attribution reports, the small bit of cross-site (per npd) and the encrypted aggregation service report. Happy to discuss both of the output types if that’s of interest.

**Martin:** consider those APIs to be in scope, but not sufficiently private. The proposed event-level API has perfect fidelity with a high-entropy identifier to tie events to a source, and a little entropy coming back from the target/trigger. Believe this is unacceptable level of cross-site information, similar to the Private Click Measurement proposal from Apple.

**Kleber:** some structural protections in the API to introduce noise, but agree with description. Is intended to be a channel that joins information (with some amount of noise).

**Martin: differential privacy noise:** if lots of noise, then it’s not useful, and if little noise, then it’s privacy revealing.

**Ekr:** very useful to have presentations of different proposals of what these could or could not do. Would good to know the functionality and the performance properties of private click measurement/event-level attribution API. Google proposal has more information transfer, so could be a baseline of utility/performance. Would appreciate a presentation of these proposals, to evaluate whether MPC-style tech can get a similar job done.

**Kleber:** for the machine-learning use case of whether showing an ad will lead to a conversion was the primary use case for the event-level reporting api ("Attribution Reporting API with Event-Level Reports"?).

[https://github.com/WICG/conversion-measurement-api/blob/main/EVENT.md](https://github.com/WICG/conversion-measurement-api/blob/main/EVENT.md)

**Ekr:** pcm was low bandwidth enough that it probably doesn’t provide enough data to satisfy the machine learning use case.

**Kleber:** Yes, as I understand things, PCM also doesn’t handle ML use cases

**Aram:** [stub issue for further discussion](https://github.com/patcg/private-measurement/issues/11)

**Ben:** +1 for discussing this topic. Helpful for understanding our different definitions or thresholds for privacy. I understand attribution-with-event-level-reports providing X% confidence that this click led to this event. Randomness can be introduced both on sending an event, or altering the small id. That a specific individual took a specific action on another website, but with a certain amount of uncertainty. My opinion is that this is unlikely to reach consensus that this meets our privacy goals. Don’t understand how this could be operated in the EU without informed consent, because of sharing information about a particular individual.

**Brian:** Rather than trying to define what privacy is, we may do better to identify what facilitates violations of privacy. helpful if we could distill concerns to why a proposal is bad, so that we can use it to evaluate other proposals.

**Aram:** objection to the whole proposal, or just to the size of the data sent through?

**Martin:** difficult spectrum of privacy-utility. I suspect that the midpoint compromise is bad both for functionality and for user privacy.

**Robin:** don’t expect us to have a definition of privacy that will answer conclusively different bits of entropy/information, never that clear cut. But can have principles that allow us to compare solutions and discuss. There may be a good reason that a risk of learning X information in this particular context, we might not be comfortable, but if there were other properties, we might be. Information flows as a threat model. Won’t give a mechanical decision procedure of what is or isn’t private.

**Erik:** re Ben, even aggregate reporting gives the same probabilities of a particular user taking a particular action, maybe just a different probability. Aggregated API might not need to add nearly as much noise as an event level API, but no fundamental qualitative difference. Differential privacy describes the contribution that an individual provides, noise is proportional to the impact of the individual. Advantage of aggregated api is that the noise is proportional to the individual impact, not added to every individual.

**Martin:** most detailed documentation I can find is [the Android implementation](https://developer.android.com/design-for-safety/ads/attribution). Is that the right proposal to review? Definitely interested in seeing numbers about randomness.

**Kleber:** will provide a link to better Chrome documentation. Android has recently indicated their intention to provide a similar style of APIs, but are earlier stage and may not be exactly the same as Chrome. Interested in having alignment between Chrome and Android, but not definitive documentation.

**Mariana:** trying to quantify leakage of data that could be used against the user is hard, this is why differential privacy exists. Can think of event-level API as the same as the aggregated api, but just over a single user. Can set privacy [as defined in DP], but with different noise/functionality.


### Q&A on [Operational Experience with MPC](https://github.com/patcg/meetings/issues/44) by [@tgeoghegan](https://github.com/tgeoghegan)

**Tim:** Introduce system we claim operational experience on. Called ENPA (EN = exposure notification, PA = private analytics). Anonymously report how EN works to public health authorities (PHAs). Much simpler than the problems in PATCG (just sums of bit vectors). System is a collaboration between ISRG, Apple, Google, MITRE, National Cancer Institute in the US. 

**How it works:** Devices generate a measurement, split into two shares and generate a proof about the share range. Upload to an ingestion server, who sends the shares to each aggregator (ingestion can’t see anything). Two aggregators aggregate shares and send aggregates to a "portal server" operated by the MITRE Corporation. Tim will add a link to the [white paper](https://covid19-static.cdn-apple.com/applications/covid19/current/static/contact-tracing/pdf/ENPA_White_Paper.pdf).

**Betül:** Is it correct that the specific use case is working with short vectors only? How big are the bitvectors?

**Tim:** 1300-1400 bits

**Mariana:** Correct, order of thousands of bits.

**Betül:** How many buckets? What is the output to PHAs?

**Mariana:** Different metrics related to the use of EN, distribution of the scores deciding the exposes. Watch our talk at [RWC](https://rwc.iacr.org/).

**Betül:** Difference to Ads use cases?

**Tim:** ENPA built on Prio, key difference is that the input size is fixed. Proof size scales with the size of the input.

[Exposure Notification Privacy Preserving Analytics](https://covid19-static.cdn-apple.com/applications/covid19/current/static/contact-tracing/pdf/ENPA_White_Paper.pdf) (ENPA)

**Mariana:** No fundamental difference. Both are measuring things, system is oblivious to what exactly. Efficiency characteristics of Prio are that share size is linear in the size of the histograms being computed. Fundamentally these questions are the same. Difference to HH is the size of the histogram, and the resulting efficiency.

**Betül:** Not sure how representative of Ads use cases this is then.

**Brain May:** Things we have to deal at Adtechs is intentional misuse. What kind of mitigations are there in ENPA?

**Tim: Depends on threat model. Point of prio:** neither aggregator gets individual inputs. Both have to collude to deanonymize users. 

**Brian:** What about users distorting the inputs?

**Tim:** Key feature of prio is proof system, which allows checking the validity of inputs. Clients add proof that the vector contains 0 or 1. Other counter-abuse (rate limiting) needed. Ingestion servers, while not seeing inputs, can verify that the reports are coming from authentic devices.

**Mariana:** Both Google and Apple do device attestation. Clients prove that inputs are in allowable ranges.

**Martin:** Performance?

**Tim:** Handles millions of users in US & Mexico. Comparison to non-MPC system not available unfortunately.

**Martin:** Example numbers on number of machines needed per million users, etc… Aggregators on metal or in clouds?

**Tim:** Run in two separate clouds (AWS, GCP). Ingestion servers owned by mobile device vendors.

**Erik T.: 2 Questions. 1:** Saw divyup service, do you have any more details, API, availability, MPC beyond Prio & Poplar? 2: Are there mechanisms to add DP to the output?

**Tim: Divyup:** Service that ISRG is building. Built on PPM standard in IETF. Generalization of our learnings from Prio, allows execution of several privacy preserving measurement systems. Prio one of them, Poplar is planned. Could be used for Adtech use cases.

**Erik:** Who runs the other helper servers?

**Tim:** Working on deploying with a team at Cloudflare research, hopeful they would run other helpers. Regaring second question (DP): We don’t support server-side DP. DP gets added at the client, before shares are generated.

**Mariana:** DP by amplification through aggregation. Each client adds noise, much less than in local DP, but once added up this gives central DP.

**Erik:** So you only have to verify that there is a certain number of contributions.

**Nick:** Curious about the collusion threat. Any experience? How did you consider that threat, protect against it.

**Tim:** One aggregator is us, one run by NCI on AWS. Use the same implementation built by ISRG. Question is: Can we do an attack through supply chain? Other party has to check code. This makes it hard to build a system like that: Cannot just SSH into both servers for debugging, instead have to go through people at the other org and ask them to debug. But non-collusion is hard to prove. Compare to a single server: less likely something bad happens, need coordination between two parties. Comparison to putting keys into hardware: Two stages, first inject key into silicon, then establish a secure channel to the first stage. Need both stages to collude before someone can impersonate secure hardware. All about increasing the number of actors that have to collude.

**Ekr:** You could also add DP centrally at each helper. Maybe we should schedule some time to discuss collusion topic. 

**Aram:** Going to add stub issue to start that discussion.


### 5m break


### [Update on Privacy Principles](https://github.com/patcg/meetings/issues/43) by[@darobin](https://github.com/darobin)

**Robin:** Present progress on TAG and how we can use principles in PATCG. Not speaking on behalf of TAG.

 - **Comparison to nudity:** sometimes it’s okay, sometimes not. Rules have context. Privacy is the same, have to figure out which rules apply in which context. E.g. People don’t want their data to be shared vs. them sharing it themselves.

[Presentation Slides](https://github.com/patcg/meetings/blob/main/2022/04/05-telecon/PAT-privacy-principles-202204.pdf)

- Easier to think about privacy as a subset of data governance. Latter regulates flows about people or impact people. Rules again depend on the context and who you’re interacting with. We don’t always need it at a great level of detail, but thinking in terms of contextual rules is the simplest

- **In the real world:** People who think of governance have a very simplistic view: Hierarchy of UN -> Government -> Contract, that’s it. But in reality, governance is  all over the place. For example in forestry, no system dominates another, no hierarchy. NGOs work trans-nationally, local NGOs, municipal governments, etc. -> Overlap of multiple systems that apply at the same time. Important to be realistic about that. CS folks like a single system being responsible, but this will not be the case for PAT. What we can do is build the best rules for our context, governing in public, be transparent, etc., but this will still interplay with other systems.

- We also shouldn’t be afraid of hard discussion, and it will take time for proper rules to emerge. Initially when households started getting electricity. Stealing electricity was common and easy, and it was a debate for a century whether that was theft or not. Similar with data: was there anything that you could steal before that was like it? No. Data is a weird commodity, gets even weirder when looking from an economic standpoint.

- **Privacy principles:** Started with super-optimistic timeline (that didn’t hold), actively being written, pace is slow. Will soon come out as first official draft. Lots of research in there what the best privacy principles are that we can reuse.

- Not going into a lot of details, you can read these yourself, just highlighting a few.

- **First principle:** have to avoid asymmetry of power. People at the lower end cannot push back, people at higher end can make bad choices, not necessarily out of bad intentions. How this applies to privacy is that information is power -> concentrating it gives few actors a lot of power over many people.

- It’s also important that we respect individual autonomy. We need to take into account bounded rationality and avoid deceptive patterns. Consent can work for signing up for a newsletter, but not for offloading ensuring that privacy is respected to people.

- **Third high-level consideration:** Often-forgotten aspect of privacy is that it works well for collective governance. People find that you tend to end up educating everyone, which is not scalable. By moving to collective governance, you gain a lot. If people similar to you share information about themselves, that shares information about you. Should consider this in the context of Ads as well.

- How can we transform the high-level philosophy into principles? One avenue, which was followed for the past 20 years: All data available to any party present. Poor privacy, poor competition properties. But we’re not creating a system / rules from scratch: we’re looking for new rules, fixing the existing rules.

- **Moderately improved verison of current state:** People can opt out, “pinky promise”. But this is not having the effect we’d like to see.

- **Something still very much in scope:** Targeted advertising might get banned. Personally, I don’t think that’s the solution, but this is the likely future if we fail.

- Having looked at other proposals, we can propose some principles, and see where they will lead. No clear cut “follow this and you can forget about privacy problems”, but instead about having hard conversations, documenting findings. For example, “notice & choice is not sufficient” might be one of them. But we’re not going to have a broad theory of privacy in advertising.

**Ben:** Provocative question: You mentioned one principle about avoiding large concentration of information, and one about avoiding cross-context / cross-domain information. Now if we say Google owns the Play store, and Search, and Chrome with logged-in users, etc., then proposals like first-party sets would say “this is ok”. Is the distinction between first-party and third-party data important for TAG?

**Robin:** Not sure that this applies to ads use cases. But yes, if one company gathers data from many contexts, this is the same for privacy as if many companies were doing it. Chrome using data from Google Search is the same as selling the data. Or if my Whatsapp information is used for FB’s newsfeed, that’s a privacy violation because of data used across contexts. First-party sets: different domains -> different context. Only use case for FPS is security reasons. Regarding 1st/3rd party data: 3rd party is always a violation of privacy, 1st party sometimes yes, sometimes no. Difficulty deciding in general.

**Nick:** Purpose limitation is useful. Goal we have is ads-specific. Consequence of not having purpose limitation in the past. We need to try to enforce this limitation. Do you have any thoughts about to what extent? What are effective ways we can do it?

**Robin:** I said “to the extent possible” because this is the hardest problem we have. Data that is currently sent on its own is harmless. Only once it’s linked it’s a problem. So if you want to enforce purpose limitation, you have to break such data linking. Can’t have information that’s both useful and completely unlinkable. You can think of inferences from data as externalities in economic transactions, and what you can do is either limit or control them. Controlling is hard in our case, so we’re going for limiting as far as possible. E.g. IPA is purpose-limited for attribution, and you can’t use that data for anything else.

**Nick:** Getting the impression that we should be explicit about purposes (so they can potentially be enforced through additional non-technical means) because inference or re-use is always possible, but also try to enforce them.

**Robin:** stating the purpose allows regulators to step in if data is used for other purposes. If we build models using shared infrastructure, there should be purpose-limitations with that infrastructure. Weak in a sense if we don’t have enforcement, but can help as a “little extra thing” to protect people better.

**Alex** (is there a way to unblock ourselves from waiting on binary definitions of privacy?): Laws rarely tell you just what to do. Is there a way we can avoid not coming to a conclusion because there is no perfect solution? Is there best practice for not having the same questions again and again?

**Robin:** Nobody’s going to give you a clear line. We’re also not going to define privacy in a clear way. That’s why we should be principled rather than perfect. Going to get better after time: Going in circles, but slowly progress. Compare proposals using principles to practice this as a group, build culture around it.

**Brian:** How do we think about the dimensionality of data? Data is going to get stored in various piles, which will get merged over time. How do we manage transparency regarding who collects what data where, if it’s abused, etc.

**Robin:** Provenence in database design has been going for decades, hasn’t produced much. At this group, all we can do is prevent collection, and add purpose limitation. On a case-by-case basis, we can think about transparency and audit approaches as second line of defense. Transparency requirements for researchers in order to audit systems: What needs to be available, SLAs, … 

**Brian: Follow-up:** Concept of limiting collection implicitly biases towards those with greater reach. Impact on competitive landscape?

**Robin:** Disagree with purpose limitation giving a bias to those with greater reach. If there’s a specific case where data is being gated and creating a bias, we should take a look at it (e.g. Topics API). Hard to quantify effect without detailed reporting. In general though, purpose limitation limits also the power that reach gives you.

**Michael Kleber:** Agree with Robin that restricting availability of info in Topics was a hard question. We are interested in exactly the type of discussion that Robin described.  Purpose limitation should be a focus here. Heard you talk about how data collected on some person can be a privacy violation for someone else via inference, but I don’t know where to draw the boundary. Are opinions someone has about someone else a privacy violation? How do we get that into practice?

**Robin:** Can share a few papers on that topic. Not every case where you learn something about someone violates privacy. But we should be aware of it. We shouldn’t be maximalist in the sense that we forbid all kinds of inference. E.g. if we ban targeted advertising, companies with a lot of reach can target just based on context, but still very discriminatory. We should be aware of that but it will be case-by-case.

Ben (Inferences from data is *precisely* the purpose of ML. This is a potentially useful and positive thing - and an important ads use-case. Is this a case for bringing inference “under control” and not “preventing inference” at all? How do you think we can approach governance of ML models?): You talked about inference as this negative byproduct we want to eliminate. But this is the explicit purpose of ML, and that’s one of our use cases. Can you share some papers or thinking of how we can have a governance system for ML, where we can use ML to select ads in a way we don’t see as negative.

**Robin:** Externalities are not necessarily negative. Just whenever you have them, you need governance. Negative externalities are paid by someone else without governance, positive ones are captured. You are asking the right question, this is a major current research question. Have to think about worst-case outcomes, and protect against those.

**Next Topic:** Clarify Charter Scope for PAT-CG
### [Charter Changes and Calls for Consensus](https://github.com/patcg/patcg.github.io/pulls) with [@aramzs](https://github.com/AramZS) & [@seanturner](https://github.com/seanturner)

Issue #6: [https://github.com/patcg/patcg.github.io/pull/6](https://github.com/patcg/patcg.github.io/pull/6) 

**Nick:** I tried to address the concerns, unsure if they are resolved. I’ve responded to Martin’s comments.

**Aram:** Remaining point of contention is server-to-server without user facing component.

**Martin:** I realize I haven’t seen those changes. Was that removed?

**Nick:** It’s a separate paragraph now.

**Martin:** I suggested simply removed.

**Aram:** There is still a point of contention here?

**Martin:** I think so.

#### Issue #9, [https://github.com/patcg/patcg.github.io/pull/9](https://github.com/patcg/patcg.github.io/pull/9), #10  [https://github.com/patcg/patcg.github.io/pull/10](https://github.com/patcg/patcg.github.io/pull/10) 

**Sean:** It’s 9 or 10 or nothing.

**Aram:** Nick’s proposal for chair selection. At this time it looks like the group is leaning towards 10. I see objections. Is there any objections to merging in 9?

**Erik T:** One quick note, I agree with 9 in principle, but it says if there is no election in the last 12 months you can have an election. Might that be too long? What if a chair has to resign one month in?

**EKR:** What’s the point of this limit?

**Erik T:** To prevent DDOSing.

**EKR:** But you need 5 people… The idea that you have a chair that is malfeasant and is there for 11 months is ridiculous. 

**Aram:** I think that combination of things should prevent a malfeasant chair from entering. If one does enter because one has exited the group, the group then considers that chair malfeasant, at that time an election can be called.

**EKR:** This text says if one of you quits, and then we call an election, then we don’t like that… we can’t have an election at all. What’s the problem we are trying to solve?

**Erik t:** If we call for an election the chairs vacate.

**EKR:** If there is an egregious bug, let’s fix it.

**Aram:** That’s what’s happening. 

**Martin:** The nature of the bug is a DDOS attack. If we have 5 entities which persist in a denial of service attack, this group is doomed.

**Sean:** That’s the “do nothing” option. The option is either “do nothing”, or 9 or 10.

**EKR:** The only problem to be solved here is we have a chair who is bad, people want to pick a new chair… (too fast). I’m in favor of 10.

**Erik T:** As I understand it, the chair might not be bad, but someone wants to stall work. So you force the vote, which vacates the charis, and they cannot even be re-elected. That’s the bug. 

**Aram:** There is generally perceived to be a bug here. Neither 9 nor 10 is the correct resolution. 

**EKR:** This is the wrong form of analysis. We can’t close every possible way for people to stall work. If we don’t have reasonable norms, the whole thing will fall apart. I don’t want to look through this charter to find every way to prevent work.

**Aram:** It seems there is a way for a person to invite a number of organizations with whom they have an allegiance to sabotage the process. I think that’s a possibility.

**Brad:** I agree with EKR. 9 seems like an easy fix. EKR do you find the change in 9 to be objectionable.

**EKR:** 12 is too long. Make it 3. 

**Aram:** Anyone object to taking this change and making it 3 months?

**Erik:** I second that.

**Aram:** I’ll change to 3 months, then merge.

#### Issue #11: [https://github.com/patcg/patcg.github.io/pull/11](https://github.com/patcg/patcg.github.io/pull/11) 

 need more text to define deliverables. Making clear what the deliverables of this group are. 

**Sean:** This is truth in advertising, pointing out what we will do. It gets away from the idea that you need some super heavy-duty set of test cases.

**Aram:** I don’t see any objections on this pull request as stands? (silence…) I don’t hear any objections. Let’s merge.

Issue #15: [https://github.com/patcg/patcg.github.io/pull/15](https://github.com/patcg/patcg.github.io/pull/15) 

**Aram:** I see this was added 2 hours ago… I’m not prepared to discuss this… Is this about the “draft management process”? We will discuss this in #7.

**Ekr:** This is a much shorter #7.

Issue #14: Adding link to join [https://github.com/patcg/patcg.github.io/pull/14](https://github.com/patcg/patcg.github.io/pull/14) 

**Aram:** Anyone object to adding a link to the community page? Going once, going twice… OK!

Issue #12: [https://github.com/patcg/patcg.github.io/pull/12](https://github.com/patcg/patcg.github.io/pull/12) 

**Aram:** We want the community group to help the working group. The working group may send us requests to collect feedback from the community. Vague process. 4 weeks. Make a document. Any objections to this pull request being merged in? I see and hear no objections… merging.

Issue #7: [https://github.com/patcg/patcg.github.io/pull/7](https://github.com/patcg/patcg.github.io/pull/7)  and #15 [https://github.com/patcg/patcg.github.io/pull/15](https://github.com/patcg/patcg.github.io/pull/15) 

**Aram:** We had a long discussion here around this questions. I added additional changes. I see that there is a simplified version of this in #15. This has a mechanism to see if it’s in scope. This seems fine, I have no objections. I’ll note to the group that this is a way for us to discuss proposals within a different “Github organization” where individual authors can bring proposals to this group for discussion. Participants will have IP rights protections that the W3C provides. There is a moderation process whereby these can be determined out of scope. The group can also do stuff. Wendy says that’s a lot of overhead (another Github organization) but this is desirable to satisfy all of the requirements.

**Sean:** This is weight the chairs will carry.

**Aram:** I have no objections.

**EKR:** I with W3C would create a repo called “unofficial proposals”. People want to discuss things on repos. They have to go somewhere. This is somewhere.

**Sean:** We will slap the CLA. Is that going to help the Topics folks. Is this headed in the right direction? 

**Kleber:** This certainly meets our goals of having somewhere to discuss topics. If the group is happy we are happy.

**Chris Wilson:** I think we are OK with this as the solution. There is a sentence fragment and some oddities about work items that we don’t define here in the same way as the Privacy-CG does. You actually have to have this repo be owned by this CG because of the IPR assessment. It has to be related. Having a separate “Github organization” to deal with this should work.

**Wendel:** &lt;no sound>

**Aram:** We will come back to you once you fix your audio.

**Don:** Does the CLA actually apply if it is just an individual Github repo that’s moved to another organization? Is there some level of W3C involvement in order for CLA to apply here. It wouldn’t be a good idea to make this area if the CLA doesn’t apply to it.

**Aram:** Wendy - please correct me if I get this wrong. If we put this in our charter it applies. The W3C has a tool to make this work. The chairs will do that.

**Chris Wilson:** The IPR bot will work.

**Erik T:** There was some discussion about what it would take to remove something. I just want to make sure people are OK with it.

**Sean:** We will follow the process for consensus. If we don’t, kick us out.

**EKR:** As adoption is by Chair consensus. I don’t expect we will ever need to kick things out. 

**Aram:** Wendel, I still can’t hear you. I don’t see Wendel’s comment as an objection. Wendel - if you type in IRC if you are trying to lodge an objection to this process. No objection. With that in mind, I think everything looks good. I see the grammatical issues have been resolved. Any objections to merging #15? Going once, going twice, merging. Thank you everyone.

**Sean:** Thank you. That will help us move things along. 

**Aram:** There is still #5 - no PR against it. I hear the issue, I have responded to it here. It now requires a pull request for us to fully resolve it. Not sure if James is here. We are in the EU timezone. With that note, we have time remaining for the working group charter. Ben, you said there 


### WG Charter 

#### Issue #6 [https://github.com/patcg/patwg-charter/issues/6](https://github.com/patcg/patwg-charter/issues/6)

**Ben Savage:**- Near the bottom I proposed specific working and we can put it in the PR. My proposal: rather than a specific thing to have a minimum proposal instead we can establish some things for a minimum bar that would be productive. 

Proposals not do cross-site tracking & proposals not enable a site to recognize you again when you would not expect it to because you have cleared storage and like features. 

Some level of agreement with that direction.

**Sean:** Yes this approach makes sense. 

** Ben:** Yes this is good, cookies is just an example. I agree with Alex’s response here. We do need suggestions on how to somehow explain the idea of taking an intentional action to prevent the site from recognizing you it should not recognize you. 

**Alex:** I added a suggestion here. We are not recommending specific user controls but whatever we diesng needs to respect specific user controls. I tried to incorporate the spirit of what you are talkina bout here. ANd I called into question what you are trying to get to here with site vs cross-site. Instead I think you mean what happens on the same site is subject to user controls. 

**Ben:** Yes I don’t want ambiguous all-user controls. I think maybe storage is the right way?

**Someone:** I think we need to have a question where something is repeatedly taking the actions against the publisher's best interest.

**X:** We need to support the user taking a clear state 

**Ben:** We’re talking about new standards for new advertising technologies and I don’t think that’s what needs to prevent DDoS attacks. The proposals in this group shouldn’t have that function. 

**Brad Lassey:** It should likely be discussed on the Anti Fraud CGl. But we should not be enabling re-identification either. 

**Brian May:** Someone doing things that takes advantage of the publisher not knowing who they are to negatively impact the publisher is a problem. 

**Brad:** Yes I think that we do not want to enable abuse. 

**EKR:** There’s no way to prevent users from erasing all their data. Data that survives a state clear is what we want to avoid. Thinking of the Apple/Google thing that wants to be remembered over time but not tracked. 

**Brad:** We have general agreement but need a PR

**Aram:** I do think there is a situation beyond storage, Bluetooth being an example. 

**Ben:** Do you mean Bluetooth as a feature for fingerprinting? 

**Aram:** I mean more as something that might Identify the user or store or transmit data on the user. 

**Brad:** I think that’s trying to be accomplished with the proposed edits. 

**Aram:** I apologize for people who fell off the queue and for my bad scribing while talking. 

**Sean:** For our next meeting we need to target the week of May 23. Is everyone happy with one day in between to rest? Any conferences I don’t know about?

**Betül:** There is a conference May 23-26. [IEEE](https://www.ieee-security.org/TC/SP2022/) security.org 

**Chat:** The 23-25 of May is CPDP2022 - Computers, Privacy and Data Protection conference.

**Sean:** Expect the Doodle poll. I expect to have that doodle poll out tomorrow. I’m worried about summer vacations soon and people starting to disappear. 

**Aram:** We will shift the timezones again.

**Sean:** Sorry europeans - we are back to super late for you again. It’s not great for everyone but it’s kind of OK.

**Sean:** Thanks to scribes, presenters, everyone in a weird timezone.

**Aram:** Please continue to participate on the working group charter. 

**Sean:** Final point I’d like to make on the WG charter, I’d like to be done talking about that before the next meeting. I think that’s a reasonable timeframe. Not a lot of “falling-on-sword” issues left.

**Aram:** Thanks everyone! Looking forward to hearing from you on Github.

### Schedule next meeting OR Charter discussion overflow.


## Participants Day 1



1. Sean Turner (sn3rd)
2. Aram Zucker-Scharff (The Washington Post)
3. Brian May (dstillery)
4. Mariana Raykova (Google)
5. Brad Lassey (Google Chrome)
6. Andrew Pascoe (NextRoll)
7. Valentino Volonghi (NextRoll)
8. Mihaela Ion (Google)
9. Chris Wood (Cloudflare)
10. Wendy Seltzer (W3C)
11. James Rosewell (51Degrees - 1st Hour Only & Last 20 mins)
12. Kris Chapman (Salesforce)
13. Michael Kleber (Google Chrome)
14. Joel Pfeiffer (MSFT)
15. James Aylett (Annalect / OMG - R&F topic only)
16. Robin Berjon (The New York Times)
17. Alex Turner (Google Chrome)
18. Jonasz Pamuła (RTB House)
19. Erik Anderson (Microsoft Edge)
20. Simon Harris (DPG Media)
21. Alexandru Daicu (Eyeo)
22. Martin Thomson (Mozilla)
23. Eric Rescorla (Mozilla)
24. Tim Holmes-Mitra (Glimpse Protocol)
25. Christy Harris (Future of Privacy Forum)
26. Abhinav Sinha (PubMatic)
27. Graham Mudd (Anonym)
28. Ratko Vidakovic (AdProfs)
29. Alex Cone (IAB Tech Lab)
30. Don Marti (CafeMedia)
31. Heng Tang (LinkedIn)
32. Alexandre Nderagakura (IAB Europe)
33. Alasdair Macdonald (Glimpse Protocol)
34. Daniel Smedley (Booking.com)
35. Brandon Maslen (Microsoft Edge)
36. Marçal Serrate (Hybrid Theory)
37. Nick Doty (Center for Democracy & Technology)
38. Alexandru Mihai (Eyeo)
39. Erik Taubeneck (Meta)
40. Russell Stringham (Adobe)
41. Sam Weiler (W3C/MIT)
42. Braedon Vickers
43. Jukka Ranta (Comscore)
44. Michal Bryc (Twitter)
45. Evgeny Skvortsov (Google)
46. Andrew Knox (Decentriq)
47. Brad Smallwood (Anonym)
48. Andras Slemmer (Decentriq)
49. Richa Jain (Meta)
50. Ben Savage (Meta)
51. Narayanan N (Huawei)
52. David Dabbs (Epsilon)
53. Lukasz Wlodarczyk (RTB House)
54. Dinesh Kandhari (PubMatic)
55. Davis Gilton (Microsoft)
56. Betül Durak (Microsoft Research)
57. Cornelius Witt (eyeo)
58. Sam Finegan (Glimpse)
59. Paweł Wiejacha (RTB House)
60. John Douglas (WeTransfer)
61. Achim Schlosser (European netID Foundation)
62. Bosko Milekic (Optable)
63. Moshe Lehrer (Neustar)
64. Mateusz Ruminski (RTB House)
65. Leif Högberg (eyeo)
66. Aditya Desai (Amazon)
67. Amol Deshpande (WireWheel)
68. Tamara Yaeger (IPONWEB)
69. Wendell Baker (Yahoo)
70. Harneet Sidhana (Microsoft Edge)
71. Paul deGrandis (Kevel)
72. Juan Alvarado (Demandbase)
73. Sean Bedford (Meta)
74. Akshaya Mani (Optable)
75. Przemyslaw Iwanczak (RTB House)	
76. Tara Whalen (Cloudflare)
77. Alberto Roman (Acuratio)Grant 
78. Nelson Vitalie Maldur (Eyeo)
79. Phillipp Schoppmann (Google)
80. Grant Nelson (TripleLift)
81. Lisa Markou (Ford)
82. Daniel Masny (Meta)
83. James Hartig (Admiral)
84. Pedro Alvarado(Resonate)
85. Matt Liu (The Washington Post)

## Participants Day 2


1. Sean Turner (sn3rd)
2. Kris Chapman (Salesforce)
3. Aram Zucker-Scharff (The Washington Post)
4. Tara Whalen (Cloudflare)
5. Michal Bryc (Twitter)
6. Wendy Seltzer (W3C)
7. Ben Savage (Meta)
8. Chris Wood (Cloudflare)
9. Ratko Vidakovic (AdProfs)
10. Martin Thomson (Mozilla)
11. Erik Anderson (Microsoft Edge)
12. Erik Taubeneck (Meta)
13. Brad Smallwood (Anonym)
14. Braedon Vickers
15. Tamara Yaeger (IPONWEB)
16. Don Marti (CafeMedia)
17. Brian May (dstillery)
18. Michael Kleber (Google Chrome)
19. Brad Lassey (Google Chrome)
20. Phillipp Schoppmann (Google)
21. Marçal Serrate (Hybrid Theory)
22. David Dabbs (Epsilon)
23. Jukka Ranta (Comscore)
24. Wendell Baker (Yahoo)
25. Alexandru Daicu (Eyeo)
26. Paul deGrandis (Kevel)
27. Nick Doty (CDT)
28. Vitalie Maldur (Eyeo)
29. Graham Mudd (Anonym)
30. Sam Finegan (Glimpse Protocol)
31. James Aylett (Annalect / OMG)
32. Andrew Pascoe (NextRoll)
33. Valentino Volonghi (NextRoll)
34. Lisa Markou (Ford)
35. Daniel Smedley (Booking.com)
36. Alex Turner (Google Chrome)
37. Simon Harris (DPG Media)
38. Robin Berjon (The New York Times)
39. Joel Pfeiffer (MSFT)
40. Jonasz Pamuła (RTB House)
41. Richa Jain (Meta)
42. Heng Tang(LinkedIn)
43. Robert Kubis (Google Chrome)
44. Mariana Raykova (Google)
45. Eric Rescorla (Mozilla)
46. Matthew Liu (The Washington Post)
47. Davis Gilton (Microsoft)
48. Alexandre Nderagakura (IAB Europe)
49. Jeffrey Yasskin (Google Chrome)
50. John Douglas (WeTransfer)
51. Juan Alvarado (Demandbase)
52. Akshaya Mani (Optable)
53. Tim Geoghegan (ISRG)
54. Tim Holmes-Mitra (Glimpse)
55. Amol Deshpande (WireWheel)
56. Daniel Frenkel (Meta)
57. Betül Durak (Microsoft Research)
58. Alex Cone (IAB Tech Lab)
59. Alasdair Macdonald (Glimpse)
60. Moshe Lehrer (Neustar)
61. Aditya Desai (Amazon)
62. Dinesh Kandhari (PubMatic)
63. John Delaney (Google Chrome)
64. Kacper Polewiak (RTB House)
65. Sam Weiler (W3C/MIT)
66. Harneet Sidhana (Microsoft Edge)
67. Russell Stringham (Adobe)
68. Sergey Tumakha (Microsoft Ads)
69. Pedro Alvarado(Resonate)
70. Chris Wilson (
71. Abhinav Sinha(PubMatic)
