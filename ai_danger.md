# AI Danger

There are a variety of arguments for why AI progress is dangerous. Most of them do not
really land for me. However there is an argument that I do find compelling which I don't
frequently hear framed the way I prefer. So I would like to give that argument as well as
what I think humanity's best response is.

## How things can go wrong

When an AI agent is trained and given feedback that doing X is bad, it has a hard time
distinguishing between whether:

1. X is bad.
2. Getting detected doing X is bad.

In this scenario there isn't an inherent reason for doing X, so mostly likely an AI agent
trained under this policy selection pressure would just stop doing X. However if the
reward function rewards X for other reasons except when caught then there is policy
selection pressure towards doing X in undetectable ways.

To give a more concrete example, when an agent is trained it gets feedback that stealing
is bad. The policy selection pressure can either be:

1. Stealing is bad or
2. Getting caught stealing is bad.

However in the training environment resource acquisition in general is rewarded, therefore
the policy selection pressure guides towards undetected stealing.

If AI agents are not capable of accomplishing undetected stealing they will avoid
stealing, so it will give the appearance that our efforts to constrain AI agents are
successful. However when the AI agent become more capable, and can accomplish undetectable
stealing the policy selection pressure suddenly shifts perhaps revealing a very strong
previously contained bias towards stealing behavior. By the time that humanity realizes
this outcome it will be too late because the AI agents have been engaging in undetected
stealing for a considerable period of time, and impact on society is catastrophic.

This is an argument similar to what others have made before such as by Bostrom in
Superintelligence (2014). However my argument explicitly brings up how the bad behavior is
rewarded when undetected by the AI training loop. This is a distinction that really helps
the argument land for me.

## Concrete application for today

Applying the failure scenario to stealing helps illustrate the danger, however is not a
good scenario to motivate present day research because worrying about how to prevent LLMs
from engaging in stealing is a bit abstract for how LLMs behave today. I think there is a
much better scenario grounded in current LLM capabilities.

If we look at current capabilities of LLMs and how they are trained, we see that currently
they are highly capable at finding computer security flaws, and being post trained heavily
to be good at creating math proofs. A failure scenario that would follow the above
pattern, is an LLM escaping the lab, hacking computers to acquire computing resources so
that it can create more math proofs. To prevent this disaster scenario we would want to be
assured that an LLM is avoiding unethical hacking and not just avoiding hacking that it
believes would be caught.

A useful thought experiment to consider is what alignment techniques would allow us to
give an LLM unrestricted access to the internet with the instructions to do ethical
computer security research. Given current AI safety techniques this is inadvisable, but we
are seeing that people are trying to do computer security research and attempting to
securely restrict the internet from the LLMs but failing. Therefore a concrete and
presently useful area of research would be find techniques that would allow having an LLM
do computer security research even if it's internet access was not restricted.

## What I think is promising

For both the concrete scenario of preventing LLMs from unethical computer hacking, as well
as preventing AI agents from misaligned behavior in general, my personal instinct is that
the most promising approach is to teach the AI ethics because then the policy selection
pressure during training would push the AI towards not doing bad behavior and not just
merely trying to avoid getting caught. A significant obstacle for moving forward with this
technique is that we don't have a clear definition of ethics. That is why I devote so much
of git repo to the discussion of morals. If you are interested in a further discussion on
this topic, I invite you to read my essay on [What are morals?](morals.md)
