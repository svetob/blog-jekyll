---
layout: single
title:  "Experiments over Discussions"
date:   2018-06-29 17:50:58 +0200
categories: "humans"
---

Remember the last time you had a long, heated discussion and found a perfect solution? Me neither.

Wouldn't it be amazing to have a better way to resolve our differences?

I recall a particularly exhausting discussion that went on for over a month. A few years ago, our team was working on a storage system with some extra bells and whistles. At some point we found a potential issue that could lead to lost updates.

We had two solution ideas. One simple bare-minimum fix, the other a major coordination overhaul. In many ways they were direct opposites.

"We've got to find the best solution", said someone. And just like that, all possible middle ground disintegrated into dust.

We wrote design documents. We held meetings. We discussed and argued. But we couldn't find agreement. As weeks went on, frustration and resentment grew.

What came of it all? Nothing. After a month with no agreement, we jumped onto a new project, leaving this issue to gather mold in a corner. Our attempt to find the best solution through discussion had failed.

What could we have done instead?


# Searching for an Experiment

Engineering is an art full of risks and unknowns - this is usually where disagreement is born. We learn through trial and error when applying our ideas to the real world. After testing and gaining information, we can rethink out approach. Why miss out on this process by trying to define your solution in advance?

Instead of looking for the perfect solution, search for the most valuable _experiment_. What can we try quickly that will answer our biggest questions? How can we easily find valuable information?

In our discussion, we could not even agree on the scope of the issue. Would it be common or rare? How much money would it cost us? Asking for answers would have helped us find great experiments. “Let’s find out how common this issue is” or “Let’s find out how many customers are noticing the issue”. We would learn later that the issue was very rare and had no proven customer impact. In short, it was not worth spending time on. If we had begun by gathering these facts, we could have saved ourselves a month of headache.


# Consent over Consensus

There was a fundamental issue at play in our months-long debate. For one solution to be “the best”, the other solution had to be less good. One person would have to lose face. There was no motivation for either side to yield ground.

Not only was the pursuit of agreement meaningless in finding the best solution. It was causing resentment, risking team members losing face. It was wasting time, preventing us from learning.

When looking for an experiment instead of a solution, you don’t actually need consensus. You only need _consent_. It’s okay not to agree, as long as a you find a way forward.

If you’re having problems agreeing on an experiment, here are some suggestions for moving forward:

- __Which experiment will take least time?__ Small, effort-less experiments mean little risk. If a test will take less than an hour, just sit down and do it.

- __Who is willing to actually do the work?__ Trust your team mates to make the right call. If Matt suggest a great experiment but only Lisa can actually spend time experimenting, let her choose what to spend time on.

- __Try both!__ If all else fails and you still can’t agree, just try all your ideas! Remember that the point is to learn and gather facts.


# Putting it all together

Fast forward to a few months later. We were facing incidents and performance issues with an unstable key-value store. Maintenance costs were through the roof and attempts to scale it up had failed. Again, there were many paths forward. As discussion arose, I was eager to go anywhere but back to the same state we had been a few months ago.

That afternoon, I suggested we try out the approach that was easiest to test. I hacked together a local test, replacing the database with an alternative one. It outperformed our production cluster on my laptop. There and then, discussion died. It didn't matter if it was the best way forward or not. What mattered was we had proof it would solve our problems.

There were still concerns about how it would scale. So, we began with what was most likely to fail - performance testing at scale. Our big project became a series of small experiments. A third of the way through the project, we knew for a fact it would work at scale, handling failures gracefully.

By testing in practice, assumptions became facts. As "I think" became "I know", risk vanished and discussion with it.

The next time you find yourselves at odds, aim for experiments over discussions. Look for consent over consensus. Spend your time learning instead of worrying.
