@DMartin1989 suggested "an alternative raster representatio" instead of
"choropleth maps to represent census-type data". Acknowledged problems
due to "the aggregation of individual data to 'imposed' areal units
designed for "ease of enumeration" rather than "data-derived", so that
"data values for each zone may be as much a function of the zone
boundary locations as of the underlying distribution" (ie. MAUP
@Openshaw1983). By contrast, the physical environment can more
straightforwardly be mapped according to 'natural' boundaries. Social
areal units are "frequently least appropriate" for areas displaying the
most extreme socio-economic characteristics". Shows figure demonstrating
misleading unemployment choropleth for Cardiff with "disproportionate
and misleading visual impact". Regions of "highly divergent character are
grouped together within enumeration districts which must encompass the
entire land surface". "... more appropriate would be the geography of
the settlement pattern". Also pragmatic issues: vector maps require
digital boundary data, and digitizing is time consuming and error-prone.
"Some spatial disaggregation should be possible... by interpolation from
the population-weighted centroid locations available for census
e.d.s [enumeration districts]".

One approach has been aggregation to [raster] grid cells, but "the need
to preserve confidentiality" meant that data had to be suppressed for a
large number of rural grid squares. References Tobler1979. Two
approaches for assigning population values to 1km grid cells. First
simple, second dirichlet tesselation, proportion of Theissen polygons.
Problems with them.
"What is required is a technique which draws out all the latent
distributional information available from the centroid locations".
A centroid data distribution algorithm has been developed... "as these
are estimations based on aggregate data they do not conflict with the
confidentiality restrictions based on data collected for small areas".

Describes algorithm: "logic employed is essentially that of a
variable-kernel density estimator". Difficulty is that it offers no
measre of the accuracy of the population values assigned to each cell.
A more common approach is... interpolation algorithms.

apocalyptic warning! "before the widespread adoption of vector GIS for
such data makes possible the reproduction of acknowledged and
fundamental errors on a scale never encountered before"!

---

@JMennis2003 gives a review of areal interpolation and *dasymetric
mapping*: "a kind of areal interpolation that uses ancillary... data to
aid in the areal interpolation process".

---

MGoodchildEtAl1993
"we define the set of discrete objects used to describe the spatial
variation of a parameter as its spatial basis".
"in this paper we assume space to be continuous"
"the most common form of spatial basis change... occurs when data must
be transferred from one set of reporting zones or areas to a second,
independent set"
"arises because of the general lack of coordination and commonality of
objectives between data-collecting agencies"
"zones often change through time, making longitudinal analysis
difficult"

"possible to obtain digital boundary files... but the sheer number of
the smaller units make this impractical"... "in the near future, this
may become less of a constraint".

alternative hypotheses:
- radially symmetric kernel functions
- maximally smooth estimation
- piecewise approximation

generalizations:
- uniform target-zone densities
- conrol zones

estimation issues:
- uniform density assumption
- may imply negative population values!
- Poisson regression does 'not allow' spatial dependence
- could instead impose constraints on coefficients
- another approach is to take the Bayesian perspective suggested by
  Geweke 1986, 1988
- or could implement lognormal regression instead of normal regression
  (results in a particular form of heteroscedasticity)

---

@AMugglinEtAl1999 Bayesian Areal Interpolation

"for reasons of confidentiality or convenience" data are frequently
reported as aggregate counts over regions.

"Areal interpolation is closely related to *kriging*, which is the
smoothing of a spatially indexed response surface given its exact values
at only a few locations". cf. Tobler1979.

Three major types of areal interpolation:
1. cartographic methods, including simple proportionate areal
   interpolation, and dasymetric mapping of homogeneous regions
2. regression methods
3. density surface methods. Tobler1979 is foremost.

Useful for data display and trend detection but not for *statistical
inference*. "Inferential tools... require both a statistical framework
for modeling the underlying physical process, and techniques for
estimating the variability of the various estimates and predictions".
argues for "a hierachical Bayesian approach".
"Bayesian methods have enjoyed increasing use in applications involving
complex data sets... where classical (frequentist) methods are either
infeasbile or reliant on unrealistic assumptions or approximations"
facilitated by MCMC computational methods for obtaining samples from teh
assocated posterior distributions of the parameters of interest.
in geography ~ Hepple 1995a, 1995b; MugglinCarlin1998.



