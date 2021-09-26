
# Introduction

Human activity has rapidly reshaped the face of Earth's surface, leaving
fragments of patchy habitat. Although there is no shortage of debate as to the
effects of fragmentation _per se_ on biodiversity and ecosystem function [@cite
], it is generally accepted that the combination of habitat and ensuing
subdivision produce negative outcomes for ecosystem function and services
[@resasco review].

In order to mitigate the consequences of landscape change on ecosystems,
developing landscape _corridors_ has seen much attention in the last several
decades. Bit more evidence for corridors here. But still, the spatter of
fragments in a landscape, where should ecologists choose to use their limit
resources to build a corridor?

Here we propose to answer that question by proposing an algorithm to estimate
the landscape modification that results in optimizing a specific ecosystem
process (in this paper maximizing the time until extinction of a metapopulation,
although the algorithm and associated software can be generally applied to any
process-based model with a quantifiable target state).

Although algorithms have been proposed for this [@peterman etc], they are
focused on finding the where the paths of least existance for a given species is
given data on that species dispersal.


# An algorithm for optimizing corridor placement

Start with some definitions and notation.

The set of possible landscape modifications, $\mathbb{M}$.

The transition probability function, $q$, which gives the probability
of moving from one modification $i \in \mathbb{M}$ to a new proposed state $j \in \mathbb{M}$, as a function of a chains temperature.

Here we define $q(i,j)$ using a logistic function,

$$q(i,j) = \frac{1}{1 + e^{\alpha (s(j) - s(i))}}$$





# Simulation of data for testing the algorithm

## Simulation of occupancy dynamics

## Simulation of landscapes


# Results


***MTE versus epoch fig***: shows the chains move toward higher extinction times over time, i.e. it works.

***Some type of performance fig vs. raster size and budget figure***

# Discussion
