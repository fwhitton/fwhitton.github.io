---
Title: "Paradoxes Part II: Ravens"
Date: 2026-01-14
---

Just as the last paradox was an excuse to talk about proof by induction, this is an excuse to talk about some basic logic. Let's lay some foundations so that we're all swimming in the same pool. We're going to be playing with statements which I'm going to define loosely as something which makes sense to assign a truth value to. "I am the president" is a statement (a False one in fact) but "France" isn't really a statement, perhaps there has to be a verb involved. Then one relationship that a pair of statements can have is the 'implication' relation, or more succinctly the word 'if'. Fact: all thumbs are fingers. This sounds like a statement that can't be decomposed but it's actually an implication: "if something is a thumb, then it is a finger". Notice that this isn't symmetric; "if something is a finger, it isn't necessarily a thumb". We would say here that A implies B but B does not imply A. We can define an equivalence relation on the set of statements by saying that A and B are equivalent if A implies B and B implies A. I hope that seems sensible. The implication is the perfect way of describing (and in fact the definition of) subset relationships. In this case thumbs are a subset of fingers. 

There's a subtletly here: an equivalence of statements is itself a statement. This is very different to the familiar case where we have numbers, say 2 and "the positive square root of 4" and our equivalence relation declares them to be equal. "A implies B" is itself another statement and we can build things like (A implies (B implies C))

For every statement A, we can define it's complement or negation: NOT A. It's a fact of logic (The law of the excluded middle) that precisely 1 of A and NOT A are true. How does this play with implication? Quickly we realise that we can't just wack NOTs on things and keep the implications: "if something is not a thumb then it is not a finger" can't be true, what about index fingers. But if we reverse the direction of the implication then we get a true statement: "If something is not a finger then it is not a thumb". And it turns out this is equivalent to the original statement! (This can be checked more thoroughly using a truth table). This statement is called the *contrapositive* of the first one. I'll emphasise that these statements are equivalent: they encode the exact same information. If they were numbers, they would be equal (and just different ways of writing the same number).

Let's start talking about ravens. All ravens are black. More precisely "something is a raven implies it is black". Then the contrapositive statement is "if something is not black, then it can't be a raven". Now we'll consider a specific instance a statement to be evidence for the general statement: if I'm trying to decide whether all ravens are black, the observation of a black raven certainly provides evidence. But here's the paradox: evidence for the contrapositive should also provide evidence for the statement. As it's commonly phrased:
"The observation of a green apple provides evidence for the fact that all ravens are black"

Which can be seen as I find something not black and check that it is not a raven, thus being evidence for the contrapositive. But since the contrapositive is logically identical to the first statement, it must be evidence for the first statement.

I haven't classified paradoxes but the quoted statement seems nonsensical but is logically coherent. In fact the Bayesian framework seems to rectify this. Since most things are not ravens and most things are not black, the evidence provided is miniscule, but non-zero.



