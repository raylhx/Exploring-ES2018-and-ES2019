3. The TC39 process for ECMAScript features

3.1. Who designs ECMAScript?
3.2. How is ECMAScript designed?
3.2.1. Problem: ECMAScript 2015 (ES6) was too large a release
3.2.2. Solution: the TC39 process
3.3. A word on ECMAScript versions
3.4. FAQ: TC39 process
3.4.1. How is [my favorite proposed feature] doing?
3.4.2. Is there an official list of ECMAScript features?
3.5. Further reading

This chapter explains the so-called TC39 process, which governs how ECMAScript features are designed, starting with ECMAScript 2016 (ES7).

3. ECMAScript特性的TC39流程  
3.1. 谁设计了ECMAScript
3.2. 如何设计ECMAScript
3.2.1 问题：ECMAScript2015（ES6）版本太大了
3.2.2 解决办法：TC39流程
3.3. 谈谈ECMAScript版本
3.4 FAQ: TC39流程
3.4.1. [我最喜欢的拟议功能]做得如何？// todo
3.4.2. 是否有ECMAScript特性的官方列表
3.5. 深入阅读

3.1. Who designs ECMAScript?
Answer: TC39 (Technical Committee 39).

TC39 is the committee that evolves JavaScript. Its members are companies (among others, all major browser vendors). TC39 meets regularly, its meetings are attended by delegates that members send and by invited experts. Minutes of the meetings are available online and give you a good idea of how TC39 works.

Occasionally (even in this book), you’ll see the term TC39 member referring to a human. Then it means: a delegate sent by a TC39 member company.

It is interesting to note that TC39 operates by consensus: Decisions require that a large majority agrees and nobody disagrees strongly enough to veto. For many members, agreements lead to real obligations (they’ll have to implement features etc.).

3.2. How is ECMAScript designed?
3.2.1. Problem: ECMAScript 2015 (ES6) was too large a release
The most recent release of ECMAScript, ES6, is large and was standardized almost 6 years after ES5 (December 2009 vs. June 2015). There are two main problems with so much time passing between releases:

Features that are ready sooner than the release have to wait until the release is finished.
Features that take long are under pressure to be wrapped up, because postponing them until the next release would mean a long wait. Such features may also delay a release.
Therefore, starting with ECMAScript 2016 (ES7), releases will happen more frequently and be much smaller as a consequence. There will be one release per year and it will contain all features that are finished by a yearly deadline.

3.2.2. Solution: the TC39 process
Each proposal for an ECMAScript feature goes through the following maturity stages, starting with stage 0. The progression from one stage to the next one must be approved by TC39.

3.2.2.1. Stage 0: strawman
What is it? A free-form way of submitting ideas for evolving ECMAScript. Submissions must come either from a TC39 member or a non-member who has registered as a TC39 contributor.

What’s required? The document must be reviewed at a TC39 meeting (source) and is then added to the page with stage 0 proposals.

3.2.2.2. Stage 1: proposal
What is it? A formal proposal for the feature.

What’s required? A so-called champion must be identified who is responsible for the proposal. Either the champion or a co-champion must be a member of TC39 (source). The problem solved by the proposal must be described in prose. The solution must be described via examples, an API and a discussion of semantics and algorithms. Lastly, potential obstacles for the proposal must be identified, such as interactions with other features and implementation challenges. Implementation-wise, polyfills and demos are needed.

What’s next? By accepting a proposal for stage 1, TC39 declares its willingness to examine, discuss and contribute to the proposal. Going forward, major changes to the proposal are expected.

3.2.2.3. Stage 2: draft
What is it? A first version of what will be in the specification. At this point, an eventual inclusion of the feature in the standard is likely.

What’s required? The proposal must now additionally have a formal description of the syntax and semantics of the feature (using the formal language of the ECMAScript specification). The description should be as complete as possible, but can contain todos and placeholders. Two experimental implementations of the feature are needed, but one of them can be in a transpiler such as Babel.

What’s next? Only incremental changes are expected from now on.

3.2.2.4. Stage 3: candidate
What is it? The proposal is mostly finished and now needs feedback from implementations and users to progress further.

What’s required? The spec text must be complete. Designated reviewers (appointed by TC39, not by the champion) and the ECMAScript spec editor must sign off on the spec text. There must be at least two spec-compliant implementations (which don’t have to be enabled by default).

What’s next? Henceforth, changes should only be made in response to critical issues raised by the implementations and their use.

3.2.2.5. Stage 4: finished
What is it? The proposal is ready to be included in the standard.

What’s required? The following things are needed before a proposal can reach this stage:

Test 262 acceptance tests (roughly, unit tests for the language feature, written in JavaScript).
Two spec-compliant shipping implementations that pass the tests.
Significant practical experience with the implementations.
The ECMAScript spec editor must sign off on the spec text.
What’s next? The proposal will be included in the ECMAScript specification as soon as possible. When the spec goes through its yearly ratification as a standard, the proposal is ratified as part of it.

3.3. A word on ECMAScript versions
Note that since the TC39 process was instituted, the importance of ECMAScript versions has much decreased. What really matters now is what stage a proposed feature is in: Once it has reached stage 4, it can be used safely. But even then, you still have to check if your engines of choice support it.

3.4. FAQ: TC39 process
3.4.1. How is [my favorite proposed feature] doing?
If you are wondering what stages various proposed features are in, consult the readme of the ECMA-262 GitHub repository.

3.4.2. Is there an official list of ECMAScript features?
Yes, the TC39 repo lists finished proposals and mentions in which ECMAScript versions they are introduced.

3.5. Further reading
The following were important sources of this chapter:

The TC39 process document
Information on the ES6 design process: section “How ECMAScript 6 was designed” in “Exploring ES6”