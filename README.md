# homepage_optimization
A multivariate test to determine the optimal experimental conditions of a toy Netflix homepage
I. Summary
In this series of experiments, the goal was to optimize the Netflix homepage in order to minimize a user’s average browsing time. In this Netflix-inspired project, the factors I was able to manipulate and their ranges were Tile.Size (as proportion of page height) [0.1,0.5], Match.Score [0,100], Prev.Length (preview length in seconds) [30,120], and Prev.Type (preview type) {Teaser/Trailer (TT), Actual Content (AC)}. I conducted a series of experiments, a 2k factorial experiment followed by two central composite designs and a ‘radial’ search, in order to reduce the search space and to estimate the experimental condition that minimizes the metric of interest (Average Browse Time in minutes). The value and location of the predicted optimum are: 
|Preview length|Match score|Preview type|Tile size| Avg. browsing time|
|---|---|---|------|---|
