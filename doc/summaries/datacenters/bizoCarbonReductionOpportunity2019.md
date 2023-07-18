# bizoCarbonReductionOpportunity2019

```{bibliography}
:filter: key == "bizocarbonreductionopportunity2019"
```

```{admonition} Summary

The authors have done an extensive analysis of what a "typical" enterprise datacenter 
is, and how it is operated. They conclude that AWS is about 3.6 times more energu efficient, mostly becuase of more efficient equipment, and more efficient operations.

They have only analysed the use phase, not the manufacturing, distribution, or end-of-life phases.
```

## Snippets

Our results show that AWS’s infrastructure is 3.6 times more energy efficient
than the median of the surveyed US enterprise data centers. More than two-thirds
of this advantage is attributable to the combination of a more energy efficient
server population and much higher server utilization. AWS data centers are also
more energy efficient than enterprise sites due to comprehensive efficiency
programs that touch every facet of the facility.

```{note} 
Some reasons why AWS is more efficient:

1. Temperature control seems to be one source of difference. This paper
   claims that traditional datacenters are actively cooled with compressors,
   causing high energy consumption, whereas AWS uses evaporative cooling and
   servers that can operate on wide temperature bands.
2. Low electrical efficiency (below 80%) caused by out-dated equipment and
   inability to operate efficiently at low load.
```

The study shows that, on average, the target group of US enterprises tends to keep their servers
for a little over four years before upgrading, although the average masks a wider spread: some
keep a server for as long as seven or eight years while others say they refresh after less than
three years as a target - a quite aggressive approach. This policy is not strongly correlated with
company size or vertical. 

About 93% of the enterprises in the sample reported that they use virtualization (the rest of the 
respondents did not know).

[...] very few companies consistently outperform their peers,
indicating that even with initiatives to achieve best-in-class operational efficiency within an
organization, they are not generally effective enough to raise all aspects of enterprise operations
in line with best practices.

[...] the latest-generation Intel servers still show a factor of 2-3x difference between their peak
efficiency point (roughly 70% load) and their light load (10-20%) range. 

Data shows that virtualization and level of workload consolidation most strongly explain
the difference in efficiency among enterprises because both markedly increase utilization
levels. Perhaps more surprising is that the third-strongest factor that correlates with how well
enterprises fare against their peers is speed of technology adoption, which is statistically slightly
more influential than server lifecycle policy.

AWS also designs its own servers for maximum
efficiency, while enterprises might give more consideration to other features such as hardware
redundancy and expandability