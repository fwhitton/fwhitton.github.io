---
Title: "A Probability Problem That Uses No Probability: Part 3"
Date: 2025-01-07
---


Now it's time to address the title of this trilogy: how can we solve a probability problem without using probability? We translated our original problem into one about area and took our answer to the area problem to be the same as the answer to the probability, but how can we justify this? There clearly is a relationship between the two, as we'll see in the next example, but that if that relationship isn't a perfect correspondence then our solution rests of shaky ground. 

Let's start with an example: suppose $A$ and $B$ are two events, perhaps some overlap.  Concretely, maybe I roll a die and $A$ is the event that I roll an even number and $B$ is the event I roll a number greater than $3$. Then the event $A$ OR $B$ is that I roll one of $\{2,4,5,6\}$ and the event $A$ AND $B$ is that I roll $\{4,6\}$. To clarify the terminology, the individual numbers I could roll are *outcomes* (of which there are 6) and some combination of those outcomes is an *event* (of which there are $2^6 = 64$). We can express this conveniently in a Venn diagram:

<img src="/assets/images/dice.png" alt="Venn Diagram" width=350>

Here $A$ OR $B$ is everything inside both circles and $A$ AND $B$ is everything in the intersection (overlap). What if we wanted to find the probability of the event $A$ OR $B$, denoted $P(A$ OR $B)$? Then it's certainly not $P(A) + P(B)$ since both $P(A)$ and $P(B)$ are equal to a half and $P(A$ OR $B)$ isn't $1$. The issue is that by adding up all the outcomes in $A$ and in $B$, we've counted everything in the intersection twice: once when counting the outcomes in $A$ and once when counting the outcomes in $B$. To account for this we need to subtract off the probability of the intersection, giving us the formula $P(A$ OR $B)$ = $P(A) + P(B) - P(A$ AND $B)$, which we can verify since $1/2 + 1/2 - 1/3 = 2/3$, the result we would expect from counting. While the formula is correct, this is a proof by picture. A more precise proof if you're curious:

$$
P(A\cup B) = P(A\sqcup (B \setminus A)) = P(A) + P(B\setminus (A\cap B)) = P(A) + P(B) - P(A\cap B)
$$

But there's an equivalent statement about area: the area covered by the two circles is the sum of both of them minus their intersection. This isn't a coincidence: in fact probabilities and areas are distinguished mainly by the fact that the probability of "everything" is 1 and the area of "everything" is infinity. Both of them are ways of measuring the size of a set (either of a set of outcomes in the sample space or a set of points in Euclidean space) and hence we call them measures. In general a measure is something that assigns a number to a set and obeys 3 rules:

1. It must be greater than or equal to zero for all sets
2. It must be zero only for the set containing nothing
3. If I have a (possibly countably infinite) collection of things which don't overlap, then the measure of the collection is the sum of measures of the individual things.

And both of these make perfect sense for both probabilities and areas (and lengths and volumes and other dimensional analogues). And this is a common theme as one progresses in maths. We take a concept familiar to us and examine which features are desirable and which are superfluous. We might find 3 or 4 conditions that an object satisfies and ask what else satisfies these conditions. And thus we can extend the notion of length to a norm, the notion of symmetry to a group action and the notion of size to a measure.
