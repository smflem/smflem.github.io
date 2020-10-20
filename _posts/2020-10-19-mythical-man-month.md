---
layout: post
title:  "The Mythical Man-Month"
date:   2020-10-19
---


Before reading [‘The Mythical Man-Month’](man-month_amazon), I was actually a bit skeptical that there would be much new insight to be gleaned within. Since the book was originally published in 1975, the software and computer industries have changed nearly beyond recognition, at the same time that the key lessons had seemingly been internalized by the community (at least from my outsider perspective).

The core lesson, the one people are likely most familiar with, is "Brooks’s Law": **“Adding manpower to a late software project makes it later”**.

So far, so relatively orthodox, with commentators like John Gruber able to [casually reference this](https://daringfireball.net/linked/2020/05/28/uber-counterfeit-capitalism) when discussing Uber’s iOS team (to give one recent example) and expect his technically-inclined audience to get it:

>I don’t know what the right number of iOS engineers at Uber is, but I do know that 400 is bananas. Too many cooks spoil the stew; 400 cooks don’t even fit in a kitchen.
>
>It’s like trying to build a better engineering team by buying 1,000 copies of Fred Brooks’s [The Mythical Man-Month](https://www.amazon.com/Mythical-Man-Month-Software-Engineering-Anniversary/dp/0201835959/?tag=df-amzn-20) and never once reading it.

Even if the example above indicates that teams might not necessarily abiding by this received wisdom, I don’t think its too much of a stretch to assert that knowledge (if not observance) of the ‘law’ is basically in the water at this point.

The really interesting thing then is why the law holds, and what that can tell us about the management of complex undertakings more generally.

To me, the underpinning of Brooks’s Law is that, for a given project, the impact of adding more contributors will depend on:

1. The ability to partition / subdivide tasks

2. The required coordination / interdependency between tasks

To take the most simple example, if a task is unpartitionable (cannot be subdivided), then adding people to the project will have no impact at all (as shown below).

![Unpartitionable task time](/images/man-month_unpartitionable.jpg)

One non-technical example might be that of a soloist performing a live violin concerto. Adding more violinists doesn't get the performance done any faster (nor any better, and perhaps worse).

At the other extreme, if a task is perfectly partitionable (can be subdivided into arbitrarily small chunks) with no need for communication between sub-tasks, then adding people to the project will allow predictable reduction in absolute time to completion.

![Perfectly partitionable task time](/images/man-month_perfectly_partitionable.jpg)

Image coding for machine-learning datasets is a potentially useful example. While it might take years of menial labor for a single individual to tag a large corpus of images as 'contains a bridge' or 'does not contain a bridge', when parallelized as a captcha or mechanical turk exercise, the work can be completed much more quickly.

This ability to partition tasks is intimately related to the cost of coordination between each potential contributor. Intuitively, we define 'partitionable' as those tasks that can be broken up and coordinated without intractable coordination costs.

In the image coding example, the millions of bridge-identifiers have no need of coordinating with each other in performing their task (assuming they know what a bridge roughly looks like). While a coordinated team of developers may be needed to develop the system to present images and capture results, once the system is set up there is minimal difference between one person coding a million images or a million people coding one image each.

But to my knowledge it has not yet proven rewarding to subdivide a concerto into individual notes for live performance by different musicians. The coordination required (e.g., timely handoffs, maintenance of rhythm, consistent interpretation of music to be performed) to maintain a high quality performance is untenable. (Incidentally, I suspect this is one of the reasons that deep work can seem so effective: it minimizes coordination costs between different temporal versions of ourselves.)

To put a finer point on this, for n nodes in a productive system requiring coordination between each node, there will be n(n-1)/2 connections. Coordination along each connection requires incremental effort. Thus, for tasks that can be partitioned, but that require coordination, we would expect the following results from adding more contributors.

![Complex interdependent task time](/images/man-month_complex_interdependent.jpg)

This is the situation that gives rise to Brooks's law. Given a need for coordination, incremental contributors can create more coordination costs than they add in productive effort, making the project even later than before.

While the above might seem straightforward, it can help explain many of the challenges in managing complex work, and point to potential vectors for improvement.

**1. Reduce the number of connections / interdependencies**

One straightforward (and common) way to resolve this is through hierarchy. Rather than have a team of 4  people (a, b, c, d) coordinating with each other, you might end up with b and c reporting into a, with d reporting into c. This team structure (not uncommon in strategy consulting) cuts the number of connections in half, from 6 to 3.

![Hierarchy](/images/man-month_hierarchy.jpg)

Another possible solution lies in reducing the number of nodes involved as much as possible. Brooks suggest two ways to achieve this: by breaking the work into expensive to coordinate and cheap to coordinate components, and by having each node produce more.

Brooks suggests the first could be achieved through a 'surgical team' design. In this, a system designer would be focused on, and responsible for, only what can not be easily partitioned further or is expensive to coordinate (e.g., the structuring of a proposed system). All other tasks (e.g., writing the software, debugging, pushing to production) could theoretically be taken on by others. In this way, the capacity of the critical nodes (the system designers) could be effectively expanded to encompass more of the hard to partition / coordinate design work. In this way, fewer designers would be required, reducing coordination costs.

But if the quantity of required work is fixed, this would necessarily mean more effort required from each individual contributor.

4 people working 70 hours per week have a higher effective capacity than 7 people working 40 hours per week, given coordination costs. If coordination costs are 5 hours for each connection[^1] (30 minutes of meetings per day for each coordinating pair), the first team would lose ~11% of their productive capacity to coordination. The second team would lose ~38%, and have to actually work ~51 hours per week to match the 4 person team's output.

To the extent you believe the math here, it is unrelenting. Certain types of complex knowledge workers can't reduce their hours without taking a disproportionate productivity hit, and those that are willing to work harder (e.g., [996](996_system)) will be able to consistently move faster and produce more.

**2. Reduce the coordination cost per connection**

Improvements here can be as myriad as the potential drivers of coordination costs. Because of their grounding in *how* the work gets done (rather than *what* works gets undertaken by whom), pathologies and remedies tend to be more specific to the people and processes being examined.

In a software context, this can mean building standardized interconnections between parts of a system (e.g., APIs), using better tools (e.g., git), or building efficient processes for coordination across a team (e.g., morning standups). Culture can also play a role here, in terms of how contributors communicate and work together.

In modern software development, the practice of 'DevOps' is focused on advancing solutions to many of these challenges in software development and deployment through the use of better tools, coordination and release processes. As Brooks outlines in another essay, there is [no silver bullet][silver_bullet] here. There are many ways to tackle these challenges in a specific organization or specific team. Some of them will ultimately prove effectively irreducible.




--

[^1]: To me, this feels realistic or even low, depending on the type of work being undertaken. I have heard of systems where 2 people will split a role for 50% pay / 60% work (e.g., 3 days of work each with Wednesday as overlap). If they would normally work 50 hours per week across 5 days, then the coordination effort (an extra half day for each of them) would actually be ~10 hours in total. If we assume 10 hours per connection in the problem above, coordination costs rise to ~21% of total effort for the 4 person team and *~75%* of effort for the 7 person team, requiring ~61 hours of effort per 7-person team member.


[man-month_amazon]:[https://www.amazon.ca/Mythical-Man-Month-Software-Engineering-Anniversary/dp/0201835959/]
[996_system]:[https://en.wikipedia.org/wiki/996_working_hour_system]
[silver_bullet]:[http://faculty.salisbury.edu/~xswang/Research/Papers/SERelated/no-silver-bullet.pdf]
