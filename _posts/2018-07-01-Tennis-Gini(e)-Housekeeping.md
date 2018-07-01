---
layout: post
title: "The Tennis Gini(e) Part 3 of n"
date: 2018-07-01
---

<h2>
Some housekeeping
</h2>

<p>
We want to sketch out a quick roadmap of this project and then introduce a bit of a twist that I realized will probably make this project more complicated but arguably more meaningful.
</p>

<h3>
Project Plan
</h3>

<p>
The following is a rough idea of the steps I see for the Tennis Gini(e) project that will, I hope, settle once and for all just who the most dominant tennis player was – regardless of what portion of the post-1974 Open Era that individual played in.
</p>

<ul>
  <li>Develop a Monte Carlo model for 100 equally skilled players.  This will give us a base-line estimate for an expected value of a Gini Coefficient.</li>
  <li>Develop a Monte Carlo model that more closely fits the point distribution of a standard single-elimination bracket for an ATP tennis tournament. We will use this Gini Coefficient as the expected value to prove that current professional tennis players are not simply equally skilled with a few lucky individuals.</li>
  <li>Scrape weekly ATP point data from the organization’s web site.</li>
  <li>Wrangle the true ATP point data into a data frame, with keys of player names for the rows and dates for the columns.  (This is actually a slight modification based on the following section – originally I had planned to have the column index simply be the week’s Gini coefficient.)</li>
  <li>Calculate the Gini coefficient for each week.  Calculate a weighted point total for each first-place ranked player and populate into a single column of a new data frame (query whether this is necessary) with player names as row keys and Rank 1 as column key.</li>
  <li>Calculate a modified Gini coefficient for each week excluding the first-ranked player. Calculate a weighted point total for each second-ranked player and populate into the points data frame in a new Rank 2 column.</li>
  <li>Repeat this step for each rank through the top 100 players (or more, depending).</li>
  <li>Sum the Gini-weighted ranking points for each player earned at each ranking.  This in the basic reportable result: the player with the greatest Gini-weighted ranking point total across all weeks is the most dominant player, the “G.O.A.T” if you will.  (Honey, if you’re reading this – which you’re not – it could be Rafa.  It could. I don’t know. I’m just following the data.)</li>
  <li>Determine how we want to present the data.  Currently, I expect to put together an interactive Gini curve with:</li>
    <ul>
      <li>ghosted Lorenze curves for each week since 1974;</li>
      <li>the expected Gini curve from our tennis-specific model with a 99% confidence band (because I don’t want to hear about how Nassim Taleb showed that for 95% confidence, we need a p-value <0.11);</li>
      <li>a date selector so that we can identify a particular week, which will highlight that week’s Lorenze curve with Gini coefficient and list the ranked players, their points, and their weighted points; and</li>
      <li>perhaps the ability to simply fish around in the chart area.</li>
    </ul>
  <li>Put together a LaTeX paper discussing the development of the model and the results.</li>
  <li>Put together a stand-alone page with side-notes.</li>
  <li>Tweet the result with a link, sit back, and enjoy the sparks/fire works/explosive decompression of the various fan clubs!</li>
</ul>

<h3>
Whose Gini metric is it?
</h3>

<p>
One aspect of the Gini coefficient that we have to keep in mind is that it is a ratio of areas – and the ratio’s divisor is constant.  As a consequence of this, a functionally infinite number of sets of numbers that can give any since Gini result.  That is, two very different distributions can have the same Gini coefficient.  
</p>

<p>
For example, 
[need to add figs]
we could have (1) a few of the lowest point totals have zero or near-zero points and the rest are perfectly equal, and (2) all players have perfect equality except the the single best player, who has a substantial gap over the others.  
</p>

<p>
Both of these could have the same Gini coefficient, but the analysis would be extremely different.  Specifically for what we are looking at, in the first instance, one could argue that the second- through last-place players are, roughly,, well measured by the Gini number.  
</p>

<p>
But in the second example, this is patently not the case.  All players except the best have effectively failed to demonstrate any evidence that they are better than the tennis-specific expected Gini value. As a result, it would be completely counterproductive to credit these players with the Gini weighting that the top-ranked player solely created.
</p>

<p>
To correct for this, we have to recalculate the Gini for each ranking level.  The top-ranked player’s points are weighted by a Gini based on all players.  The second-ranked player’s points are weighted by a new Gini based on all players <em>excluding the player above</em> and based only on that player and those below.
</p>

<p>
This will offer us a meaning look at the extent to which players have demonstrated the performance gap between themselves and those that they out-paced.
</p>

<p>
Life intervenes, but we will continue to try to make headway on identifying the true greatest tennis player of all time – the Tennis Gini(e).  Stay tuned….
</p>
