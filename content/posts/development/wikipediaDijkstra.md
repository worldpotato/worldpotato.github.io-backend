---
title: "Wikipedia Dijkstra"
date: 2020-02-02T13:55:49+01:00
draft: false
tags: ["Dijkstra", "Development", "Wikipedia", "Graph", "Navigation"]
---

Do you know the game where you try to go from one Wikipedia page to another with less clicks as possible?
If not, pick a stranger person in the subway and play it together or against each other. It's a nice way to make new friends (or enemies).

But at the end you ask yourself if your way was the best way possible. 
Even if you won the battle.
The nice thing is you can see the internet as a [graph](https://en.wikipedia.org/wiki/Graph) where a site is a node and a link is edge.
And with that in mind you can simply use the [dijkstra algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm) to calculate the best route between two websites. 
But the whole internet is a little bit too much.
So we can limit it to nodes with `wikipedia.org` as domain.
That are still 6 mio nodes but OK.

That's just some thoughts about a possible new project.
We are not sure how to implement the adjacent matrix or list.
And we don't have any idea how to crawl Wikipedia.
We want to use python, that's sure.

If you have an ideas, let me know.

Cheers!
