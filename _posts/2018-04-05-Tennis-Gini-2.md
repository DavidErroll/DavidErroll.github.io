---
layout: post
title: "Tennis Gini(e) 2"
date: 2018-04-05
---

<h2>
Gini Coefficient: A (somewhat) necessary side-note
</h2>
<h3>
What does it mean to be the best?
</h3>
<p>
One of the underlying premises of this investigation is the idea of identifying the "greatest tennis player of all time" implicitly assumes that we are not simply finding the <em>luckiest</em> player of all time.
</p>
<p>
Since ATP tennis tournaments invariably employ a single-elimination bracket-style format, the tournament is guaranteed to produce a single "winner." Ideally, this winner is the "best" player within the rules of the game. However, it is trivial to imagine games of pure luck that would also produce a winner in this format.  <em>E.g.</em>, there is no shortage of <a href="http://worldrps.com/">Rock</a>/<a href="https://kotaku.com/japans-most-intense-rock-paper-scissors-competition-1790085868">Paper</a>/<a href="https://priceonomics.com/the-world-of-competitive-rock-paper-scissors/">Scissors</a> tournaments, where while there is some element of skill in a player's ability to guess (or study) an opponent's actions, true skill is far from evident.  This, or a coin-flipping tournament, would produce a winner that would likely be best described as the luckiest rather than the best.
</p>
<p>
So there is a hypothesis that we are implicitly rejecting by searching for a greatest tennis player, <em>i.e.</em>, that not all tennis players are equally skilled.
</p>
<p>
OK – it seems a bit too obvious to even merit an effort at a proof.  After all, anyone who has played tennis – poorly, well, or first one and eventually the other – can tell you that:
</p>
<ol>
  <li>there are skills that can be taught, learned, and applied, and</li>
  <li>different people have different capacities to learn and apply these skills.</li>
</ol>

<p>
It's axiomatic. Isn't it?
</p>

<h3>
Incorporating <em>Gini</em>
</h3>

<p>
The <a href="https://en.wikipedia.org/wiki/Gini_coefficient">Gini Coefficient</a> is a measure of value dispersion or the level of inequality among values in a frequency distribution.  Originally proposed for use as a measure of income inequality in economic systems, the metric has been used in other fields, such as education, biochemistry, and engineering, as well.

At its heart, the Gini Coefficient is based on the plot of a <a href="https://en.wikipedia.org/wiki/Lorenz_curve">Lorenze Curve</a>, a graphical comparison of the cumulative portion of some factor (wealth, income, <em>etc</em>.) relative to the relevant proportion of the population.  

An example of a Lorenz curve for income inequality (below), illustrates how the measure presents the difference between the actual or estimated cumulative metric (the curve) versus a theoretically perfectly equal distribution (the straight line):
</p>

<p><a href="https://commons.wikimedia.org/wiki/File:Economics_Gini_coefficient2.svg#/media/File:Economics_Gini_coefficient2.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/Economics_Gini_coefficient2.svg/1200px-Economics_Gini_coefficient2.svg.png" alt="Economics Gini coefficient2.svg"></a><br>WikiMedia Commons (<a href="http://en.wikipedia.org/wiki/File:Economics_Gini_coefficient.svg">LINK</a>)
</p>

<p>
The Gini Coefficient is then calculated as the ratio of area A to the sum of areas A + B.  (Because the total area of A + B is always 0.5, this ratio may also be calculated as 2 * A or 1 - 2 * B.)





</p>
