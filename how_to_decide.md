# The best way to make a decision

The best way to make a decision is to consider all options, consider the
outcomes with their likelihood, and select the option with the best expected
outcome. This decision policy is called maximum expected utility. It is best
decision policy more or less by definition. If you define the best decision as
the one with the best expected utility, maximum expected utility is the decision
policy that directs to pick that one. 

There are of course, practical limitations to adopting maximum expected utility
in day to day life. Enumerating all possible options, all possible outcomes time
consuming, and frequently impractical. Accurately estimating the probability of
various outcomes is more or less impossible. However, given that this is the
best possible way to make a decision, the practical option is to approximate
maximum expected utility as best you can.

When we consider how we make decisions in practice, in often looks nothing like
maximum expected utility. Let's examine some commonly used decision making
methods from a wide variety of fields. We know that maximum expected utility is
impractical, but it is optimal so we should approximate it as best we can.
Therefore when we evaluate other decision making methods, we should be
evaluating how well those methods approximate maximum expected utility, and what
are the pros and cons of any divergences from maximum expected utility.

In the following sections below, I will go through common decision making
methods that should be mostly familiar because they are common ways of
decision making that we do in our every day lives. In each section I describe
the pros and cons. While all the methods are inferior at least in a theoretical
sense, from a practical sense, I do think each approach does have merit and
deserves some place in our everyday decision making.

## Risk adjusted analysis

In risk adjusted analysis, we are not just trying to maximize the expected
utility, we are also taking into account the distribution of the utility and
adding an extra penalty for large amounts of uncertainty or especially low
utility outcomes.

This is kind of analysis is common in the financial world, and is the basis for
what is called
["Modern Portfolio Theory"](https://en.wikipedia.org/wiki/Modern_portfolio_theory)
where the best portfolio of financial assets is not the one with the best
expected returns, but the best risk adjusted returns. In this framework, all
possible portfolios are considered, and for each possible portfolio the expected
rate of return and variability of the return is considered. Then you are
supposed to select the variability of return you want to tolerate, and select
the portfolio with the best expected return given that level of variability of
return.

Risk adjusted analysis diverges from pure maximum expected utility by
introducing an explicit penalty for uncertainty and downside risk. However, it
requires you to decide your risk tolerance. If we consider the scenario where we
must make a sequence of decisions, the optimal risk tolerance we should select
is the amount that maximizes overall expected utility assuming that the
probability distribution of outcomes associated with each decision are not
impacted by the prior decision.

In other words, the risk adjusted methodology can be thought of as a useful
method for breaking up the analysis of a larger sequence of decisions into
multiple analyses for each individual decision.

This decomposition works particularly well in domains like finance, where outcomes
are fungible and additive—a dollar earned from decision 1 is equivalent to a
dollar earned from decision 5. However, for complex life decisions where the
utility function is something like overall happiness, this approach becomes
problematic due to path dependence. Your decision at step 3 depends heavily on
what happened in steps 1 and 2, and the outcomes of step 3 constrain your
options for step 4 in ways that are difficult to predict or decouple. A decision
that appears suboptimal in isolation might have opened up exceptional opportunities
later, or a seemingly good decision might have closed off paths that would have
been far better. Treating each decision independently by selecting a consistent
risk profile and assuming the results compound additively to overall happiness
oversimplifies the interdependence and timing effects inherent in human life
decisions.

## Capability / scenario based threat analysis

This is a common form of planning used in military planning. You consider the
capabilities of your adversary, and create a response strategy assuming that
your adversary will fully leverage all their capabilities to inflict maximal
harm to you. This is also similar to disaster planning or security threat planning.
The scenario we need to plan a response to is assumed.

The short coming of this technique is that it ignores does a poor job of incorporating
the probability the worst case scenario is going to occur. Additionally responses that
make sense assuming the worst case scenario happens, may be really bad strategies if
the worse case scenario wasn't going to happen. For example, consider if two neighboring
countries are currently at peace, and one nation stations troops on the border in proportion to
the military capability of the other country. This would naturally be interprted as an
escalatory act. Prior to the large number of troops massing on their border, the possibility
of military action might have been very remote, but now it is very possible. In this
hypotherical situation, massing troops was highly counter productive, there was no
threat of invasion originally, and now there is.

The benefit of this kind of planning is that there can be many situations where a good
response doesn't exist on a smooth dynamic. For example having fire extinguishers around
your house is completely useless if a fire never happens. If you were planning your shopping
list around what you were likely to need in the next week, you would never buy a fire
extinguisher. However there is a smooth dynamic around how many groceries you might want to
buy depending on all the relatively likely things that happen in the upcoming week. There
could be some uncertainty over how many meals you will need to cook, and therefore you will
need to slight adjust how much food you buy.

The key here is that capability / scenario based threat analysis is a common decision making
framework, and main flaw is that it does not incorporate the probability of various scenarios
very well. Furtherore sensible responses assuming the worst case scenario happens may be very
counterproductive.

From a game theoritic point of view this decision making policy can be called
[minimax strategy](https://en.wikipedia.org/wiki/Minimax).

## Principles based

Typically this is when you make a decision based upon some moral principles. For example you
might tell the truth because you think it is wrong to lie. This approach makes a lot of sense
if you priniciples are indeed as important to you as you think they are. However this approach
can lead you astray if the importance of the moral principle you are using was actually
inflated in your mind, and upon further more cool minded consideration, wasn't actually as
important as you thought it was.

For example you might have chosen to engage in argument with a family memeber because you felt
it was important to speak your truth on a topic that in reality is not that important such as
how to properly load a dishwasher. The maximal expected utility approach would have been to
consider all all options, consider the outcomes with their likelihood, and select the option
with the best expected outcome.

This kind of reasoning is also common in the political domain, where public policy decisions
are made based upon principles and not atleast explicitly an maximum expected utility approach.
For example the US Declaration of Independence justifies the formation of the government based
upon the principles of "Life, Liberty and the pursuit of Happiness" so not some probabilistic
argument that the expected outcomes of democratic governments are higher than non-democratic forms.

Maximum expected utility is essentially amoral. However morality can be incorporated if you
use moral considerations as part of how you compute utility which I think is the best approach
even if isn't explicitly stated that way. While a judge might
explain the reasoning behind a legal ruling purely in terms of principles, there is the assumed goal
that adhering to these principles is going to produced maximum expected utility for society.
Similarily for situations where principles are highly relevant, I think it is fine if the rationale
seems mostly driven by principles, but optimizing maximal expected utility should be the unstated
assumed goal behind all these principles.

## Heuristics

This form of decision making frequently shows up in business and competitive sports. There is a lot of
always do X.

The key flaw with heuristic based decisions, is that can be advertised as a set of principles that if
followed will guarantee good outcomes. It is important to recognize that this is just not true.

## Path of least resistance

## Tapping into your subconscious

This is a common approach suggested when trying to choose a partner partner or selecting a career
path. For example the amount of "chemistry" is typically a key factor in a choosing a romantic partner,
and "getting in touch with" some aspect of ourselves is a common advice in selecting a career. This
approach makes a lot of sense when we are struggling to understand what are utility function is. To
a certain extent we are incapable of understanding our preferences consciously. We deduce our prefences
by observing the reactions originating from our subconscious. However it is more universally agreed that
for the most important life decisions we have not had sufficient time to observe ourselves to understand
our preferences consciously. Therefore tapping into our subsconscious is unavoidable for the most
important decisions.

In these situations there is a strong tendency to using principle or heuristic based reasoning to avoid
admitting to ourselves that we don't understand what we want. As mentioned in the section on principle
based decision making it is easy to overestimate how strongly we hold our principles. And in the section
on heuristics it is easy to forget that heuristics don't always apply, and how common it is for there to
be contradictory heuristic that have become commonly accepted.

## OODA loop / multi-armed bandit

One can use a iterative planning process where one makes a decision that are
designed to be a mixture strategies to gathering information, and maximizing the
expected utility. These policies have formal names such as OODA loop, or
multi-armed bandit.
