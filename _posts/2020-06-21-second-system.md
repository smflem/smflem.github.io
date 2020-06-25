---
layout: post
title:  "The Second System trap"
date:   2020-06-21
---

Most people know Fred Brooks for his eponymous law from *The Mythical Man-Month* that states "Adding manpower to a late software project only makes it later".

I'm trying to get around to writing up this core thesis, but that essay spans just 13 pages of what is a 250+ page book of essays on software development. So I'm breaking off and examining smaller chunks of insight from his less-well-known writing.

First up, The Second System Trap:

>
>An architect's first work is apt be spare and clean. They know they don't know
>what they're doing, so they does it carefully and with great restraint.
>
>As they designs the first work, frill after frill and embellishment after
>embellishment occur to them. These get stored away to be used 'next time.'
>Sooner or later the first system is finished, and the architect, with firm
>confidence and a demonstrated mastery of that class of systems, is ready to
>build a second system.
>
>This second is the most dangerous system a person ever designs.
>
> -- Fred Brooks, *The Mythical Man-Month*
>

Though I don't have much experience in software development (a few classes in Python and SQL notwithstanding), this idea of the 'Second System Trap' resonated with me immediately.

When working in consulting I was often either performing analysis or, later, overseeing others in performing analysis. And there seemed to be a consistent pattern among 2nd year analysts (myself included) to tend to overbuild models and add functionality that was only marginally necessary or useful. These additions were not generally wrong per se, but often struck the wrong tradeoff between usefulness and time to implement.

In the context of consulting, this often took the form of unnecessary model 'flexibility' or analysis that answers questions that weren't asked (and don't need to be answered).

As Brooks talks about, in your first system (or your first year of work), you focus on just getting stuff to run (and on getting to the desired analytical output). These first efforts reveal directness in developing a base case or 1st order analysis (e.g., what % of people like product A), rather than complex scenario analysis or the quantification of 2nd order analysis (e.g., what % of people who like product A also like product B).

In this process, follow up questions inevitably arise from clients and supervisors, questions which often require additional model building and new functionality to answer. Even with best efforts to 'spec' the analysis beforehand, iteration and refinement are an inevitable and critical part of the process. In this, the analyst will pick up new tools and an emerging sense of worthwhile features (questions worth asking).

So, when it comes time to build the Second System, if the analyst is good they will want to be proactive in their efforts, using their new skills and sense of worthwhile questions to get ahead of the inevitable refinement requests. They will build out this system with, as Brooks says, 'frill after frill and embellishment after embellishment'.

It's worth noting the obvious here, necessary features are not considered frills. So to be considered a frill, a feature is not 100% necessary. In the context of consulting, the analysis answers a question that didn't need to be answered, often one whose answer is merely interesting but weighs little on the larger decisions being made.

One potential solution might seem obvious: the analyst should stick to the spec!

But this misses the nature of the work being done here. Consulting (and software development) are complex undertakings, where the granular details of execution are only understood at the time execution. Put differently, *figuring out the detailed questions and answers is the work*.

Therefore, we want the analyst to be proactive in thinking about new methods and new questions. They just need to refine their sense of what is necessary and what is a 'frill', often through accumulated experience (and thoughtful feedback). Consulting is an apprenticeship business, this is one reason why. This refinement of one's taste for questions and methods takes time and experience to develop. As Brooks puts it, "Obviously they can't skip their second system".

From the analyst's perspective then, the most useful mindset is one focused on testing and learning, where a given new question is a hypothesis of the form "Taking x minutes to answer question y will be worthwhile". Each check-in with a client or supervisor is a way to test whether this hypothesis was correct, with the goal being refinement of one's 'taste'.

While the 'Second System Trap' can't be avoided entirely (in that it is a necessary part of developing one's professional taste), it is a useful frame for thinking about supporting others through an important stage of their early career.
