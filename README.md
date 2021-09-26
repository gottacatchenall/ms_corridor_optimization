
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

Define the set of possible landscape modifications, $\mathfrak{M}$,
in optimization language called the _search-space_.
Introduce uncountability argument of this space.

Because we cannot test every possible modification in $\mathfrak{M}$, we
use simulated annealing, a method for estimating the global optimum of functions
with NP search-spaces.


## Proposing landscape modifications

This is really important. We propose (no pun intended) several algorithms for
generating landscape modifications. Some of the details here might have to go
in a supplement/appendix.

### Graph-based

Consider only modifications that consist of connecting nodes.

#### The two stage approach

Stage-one: accept a new topology of connected nodes with probability in proportion
to chain temperature (see next section).

Stage-two: modify way that the connection for a given topological structure is
chosen. Because we are working in a 2D raster, all distances between points are
Manhattan distances, and any link between points is composed of $x$ horizontal
steps and $y$ vertical steps. There are thus $2^{\min(x,y)}$ ways to connect two
nodes that far apart.


### Not graph-based

The reason to avoid this is because the search-space grows much faster with lattice
size and budget. That being said, we can use some simply heuristics to weight
proposals using "common-sense".   


## Simulated annealing to explore the space of landscape modifications


The transition probability function, $q$, which gives the probability of moving from one
modification $i \in \mathbb{M}$ to a new proposed state $j \in \mathbb{M}$, as a
function of a chains temperature.

Here we define $q(i,j)$ using a logistic function,

$$q(i,j, \alpha) = \frac{1}{1 + e^{\alpha (s(j) - s(i))}}$$

$s(i)$ is the function that gives the score of a proposed modification. Here,
the mean time to extinction.


Simulated annealing can be written described as the following.

A markov-chain, denoted $\pi_\alpha$

***Figure 1: concept fig***


## Process-based optimization

Here we use occupancy dynamics as the process, although we emphasize that this method works for arbitraty process models
and is instead limited only by the computational demands of a given process model.


***Figure 2: MTE versus epoch fig***: shows the chains move toward higher extinction times over time, i.e. it works.


# Simulation of data for testing the algorithm

## Simulation of occupancy dynamics

## Simulation of landscapes

### Generation of landcover maps

### Generation of points

### Resistance values assigned to each land cover type

***Some type of performance fig vs. raster size and budget figure***

# Actual data st. lawrence lowlands




# Discussion
