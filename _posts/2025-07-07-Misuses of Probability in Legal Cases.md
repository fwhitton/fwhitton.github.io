---
title: "Misuses of Probability in Legal Cases"
date: 2025-07-07
image: /assets/images/OJ.png
---
# O.J. Simpson
In 1995 O.J. Simpson was acquitted of the murder of his ex-wife Nicole Brown and her friend Ronald Goldman. During the trial, it was accepted that Simpson had been violent towards Brown when they were married. The defence argued that only 1 in 2500 women who experience spousal abuse are murdered by their partner and so the probability Simpson murdered Brown was low. However, this is a gross misuse of conditional probability.

For concreteness, imagine 100,000 women who are victims of domestic violence. Before Brown was killed, it is true that the probability she would be killed by Simpson was 40/100,000 = 1/2500. However the Bayesian framework tells us that once we learn of her murder, we must update our probability: no longer is she one of 100,000 victims of domestic abuse but she is now one of the 45 women who are victims of domestic abuse and have been murdered. Of those 45 women, 40 are killed by their partner and so the correct probability is 40/45, not the proposed 40/100,000. 

<img src = "/assets/images/OJ.png" alt="probabilities" width = 200>

# Sally Clark

Sally Clark, a British solicitor, was accused in 1998 of murdering both her children at 11 weeks and 8 weeks old respectively. The prosecution asserted that the probability of 2 children suffering from Sudden Infant Death Syndrome (SIDS) was 1 in 73 million, a figure they found by taking the underlying population rate and squaring it. The tacit assumption here was that the events were independent. As all A level students know, and many of us intuitively understand, if two events are independent then the probability of them both occurring is the product of their individual probabilities. In this case this was a baseless assumption given there is a genetic predisposition to SIDS.

Clark was convicted but the ruling was later overturned when it was revealed that the prosecution forensic pathologist had withheld exculpatory evidence. The case caused hundreds of similar cases to be re-examined and as a result two other women had their convictions overturned.

