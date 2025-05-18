# MSDS459-Week-7.-Individual-Assignment-3

Part 2 - Week 7 - Knowledge Graphs

For week 7, chapters 8 and 9 of the textbook Knowledge Graphs by Kejriwal et al., 2021 were assigned. Chapter 7 covers instance matching or what may be referred to as de-duplication.  This process is necessary in a knowledge graph to provide clarity both in the volume of objects as well as the precise relationships between them.  Due to the sheer volume of data common in such systems, a two-step approach is often followed.  These two steps are blocking and similarity (Kejriwal et al., 2021).

Blocking is the process of gathering similar mentions into groups prior to processing.  This lessens the quadratic complexity and therefore server cost of instance matching.  Three of the more influential blocking methods are traditional blocking, sorted neighborhood, and canopies.  In traditional blocking, all mentions with a matching key are gathered into overlapping blocks.  Sorted neighborhood orders keys and creates blocks via a sliding window that does not change in size.  The final method canopies does not rely on keys but rather gathers mentions that are within a certain preset distance range of each other within the knowledge graph (Kejriwal et al., 2021).

In the similarity step, pairs identified in blocking are assigned scores that indicate the probability that both refer to the same entity.  Typically, all pairs with a resulting score over a given threshold or the pairs with the highest scores will be assumed to be a match.  Typically, machine learning methodologies for classification are utilized to produce these scores.  Approaches such as random forest, multilayer perceptron, and support vector machine have been found to perform this task well.  Neural networks have also been proposed with some limited success seen with Siamese networks (Kejriwal et al., 2021).

Chapter 9 of the text covers statistical relational learning frameworks.  Statistical relational learning is concerned with combining uncertainty and probability modeling with relational dependency modeling.  According to the text, there are four necessary pieces for a successful statistical relational learning framework.  First, the framework must combine both probabilistic graphical models and first order logic.  Second, it must allow for issues typical to statistical relational learning such as link prediction and collective classification.  Third, the framework should allow for ways to use and represent domain knowledge.  Finally, it should permit the use of techniques from multiple disciplines including statistical learning, probabilistic inference, and inductive logic programming (Kejriwal et al., 2021).

Two frameworks that provide for many of these requirements are Markov Logic Networks and Probabilistic Soft Logic.  With Markov Logic Networks, it is assumed that variables that are random are also binary.  However, in Probabilistic Soft Logic random variables are considered continuous. 

References

Kejriwal, Mayank, Craig A. Knoblock, and Pedro Szekely. Knowledge graphs: Fundamentals, techniques, and applications. Cambridge, MA: The MIT Press, 2021.
