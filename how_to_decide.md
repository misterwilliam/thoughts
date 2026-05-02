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

## OODA loop / multi-armed bandit

One can use a iterative planning process where one makes a decision that are
designed to be a mixture strategies to gathering information, and maximizing the
expected utility. These policies have formal names such as OODA loop, or
multi-armed bandit.

## Contingency planning

## Principles based

## Heuristics

## Path of least resistance

## Tapping into your subconscious
