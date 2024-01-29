# homepage_optimization
### I. Summary
In this series of experiments, the goal was to optimize the Netflix homepage in order to minimize a user’s average browsing time. In this Netflix-inspired project, the factors I was able to manipulate and their ranges were Tile.Size (as proportion of page height) [0.1,0.5], Match.Score [0,100], Prev.Length (preview length in seconds) [30,120], and Prev.Type (preview type) {Teaser/Trailer (TT), Actual Content (AC)}. I conducted a series of experiments, a $2^k$ factorial experiment followed by two central composite designs and a ‘radial’ search, in order to reduce the search space and to estimate the experimental condition that minimizes the metric of interest (Average Browse Time in minutes). The value and location of the predicted optimum are: 
|Preview length|Match score|Preview type|Tile size| Avg. browsing time|
|---|---|---|---|---|
|75|75|TT|0.2|10.0831|

### II. Introduction 
#### <ins>Problem statement</ins>
In this scenario, Netflix is experimenting with altering 4 features of their “Top Picks for …” row on their desktop homepage with the goal of reducing the amount of time users spend choosing what to watch. By streamlining the browsing experience, the idea is to increase user engagement by reducing decision paralysis and fatigue. As users get frustrated by the number of choices, they may leave the site.

The goal is to discern the statistical significance and measurable impact of each of the four factors (Tile.Size, Match.Score, Prev.Length, Prev.Type), in order to discover the optimal combination of feature levels that minimizes browsing time, while being mindful of the cost associated with conducting experiments.  

#### <ins>Experimental methodology</ins>
The experiments can be divided into two steps: factor screening and response surface design. In order to avoid extraneous data collection, I first employed a $2^k$ factorial experiment to filter any insignificant factors from the search space. Although $2^k$ factorial experiments are useful for screening, they are limited in their response optimization capabilities due to their limited number of conditions. 

To more rigorously search for the optimum within the search space, I conducted a central composite design (CCD) experiment. In 2 dimensions, this type of design requires data from 9 conditions, as opposed to the 4 conditions of a $2^k$ factorial design. These additional conditions allowed us to estimate the quadratic behavior of the response surface. From this, I was able to approximate the location of the minimum (stationary point) by setting the derivative of the estimated surface equal to zero. 

The calculated stationary point fell outside of any previously observed conditions, and so I conducted a second CCD experiment centered around the first stationary point. With this, I was able to define the final search area, where I collected data on conditions ‘radial’ to the second stationary point. 

In this report, we will look more closely at the experimental journey, including the experimental designs, specific conditions, and analyses that led to the findings about the optimal conditions to minimize browsing time.

### III. Experiments 
#### <ins>Feature Screening</ins>
The initial step was to reduce the search space by using a $2^4$ factorial design, as it is a low cost way to determine which factors are significant in impacting average browsing time. The experimental conditions of the $2^4$ factorial experiment are shown in Table A. 
