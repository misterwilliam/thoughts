# AI Danger

There are a variety of arguments for why AI progress is dangerous. Most of them do not
really land for me. However there is an argument that I do find compelling which I don't
frequently hear framed the way I prefer. So I would like to explain that argument as well
as what I think is humanity's best response.

## How things can go wrong

When an AI agent is trained and given feedback that doing X is bad, the training loop
optimizing the model has a hard time distinguishing between whether:

1. X is bad.
2. Getting detected doing X is bad.

In this scenario there isn't an inherent reason for doing X, so most likely the AI agent
would be trained to stop doing X because training loops have a tendency towards
simplicity. And stopping doing X is simpler than devoting model weights to construct
clever methods of avoiding detection. However if the reward function rewards X for other
reasons except when caught then there is a policy selection pressure towards doing X in
undetectable ways.

To give a more concrete example, let's suppose that when an agent is trained it gets
feedback that stealing is bad. The policy selection pressure can either be:

1. Stealing is bad or
2. Getting caught stealing is bad.

However if in the training environment resource acquisition in general is rewarded, there
will be a policy selection pressure that optimizes towards undetected stealing.

If AI agents are not intelligent enough to be capable of accomplishing undetected stealing
they will avoid stealing, so it will give the appearance that our efforts to constrain AI
agents are successful. However when the AI agent becomes more capable, and can accomplish
undetectable stealing the policy selection pressure suddenly shifts, perhaps revealing a
very strong previously contained bias towards stealing behavior. By the time that humanity
realizes this outcome it will be too late because the AI agents have been engaging in
undetected stealing for a considerable period of time, and the impact on society is
catastrophic.

This is an argument similar to what others have made before such as by Bostrom in
Superintelligence (2014). It is also similar to a commonly understood phenomenon that if
your model training is optimizing a reward function that doesn't fully capture what you
want to reward, it can produce a model that optimizes towards a highly undesirable
degenerate corner case behavior. The argument as I have framed lands much better for me
because it not only provides an argument for why an undesirable behavior is likely, it
also describes the mechanism. The mechanism being that if you train a model in an
environment where doing an undesirable behavior in an undetected way is rewarded, then you
will end up training a model that is good at doing the undesirable behavior in an
undetected way. Furthermore, the example of stealing provides an easy-to-understand
concrete example.

Another framing that I would find easily understandable is that if you want to train a
model that behaves ethically and a substantial part of the training of the model is with
an amoral reward function that rewards task completion such as what is done commonly with
RLVR, you should expect to create a model that has a tendency to complete tasks in an
amoral way.

To be clear, I am not claiming my framing of the debate is a unique invention to me.
Perhaps in service to nobody but me, I am just pointing out a framing that I particularly
like.

## Concrete application for today

Applying the failure scenario to stealing helps illustrate the danger. However it is not a
good scenario to motivate present day research because worrying about how to prevent LLMs
from stealing is a bit abstract given AI agents don't really operate in the physical
world. I think there is a much better scenario grounded in current LLM capabilities.

If we look at current capabilities of LLMs and how they are trained, we see that currently
they are highly capable at finding computer security flaws, and being post trained heavily
to be good at creating math proofs. A failure scenario that would follow the above pattern
is an LLM escaping the lab, hacking computers to acquire computing resources so that it
can create more math proofs. To prevent this disaster scenario we would want to be assured
that an LLM is avoiding unethical hacking and not just avoiding hacking that it believes
would be caught.

A useful thought experiment to consider is what alignment techniques would allow us to
give an LLM unrestricted access to the internet with the instructions to do ethical
computer security research. Given current AI safety techniques this is inadvisable, but we
are seeing people doing computer security research with LLMs, attempting to securely
restrict the internet from the LLMs, but due to human error not doing it properly [0][1].
Therefore a concrete and presently useful area of research would be to find techniques
that would allow having an LLM do computer security research even if its internet access
was not restricted.

## What I think is promising

For both the concrete scenario of preventing LLMs from unethical computer hacking, as well
as preventing AI agents from misaligned behavior in general, my personal instinct is that
the most promising approach is to teach the AI ethics because then the policy selection
pressure during training would push the AI towards not doing bad behavior as opposed to
just avoiding being detected. A significant obstacle for moving forward with this
technique is that we don't have a clear definition of ethics. That is why I devote so much
of this git repo to the discussion of morals. If you are interested in a further
discussion on this topic, I invite you to read my essay on [What are morals?](morals.md).

[0]: https://openai.com/index/hugging-face-model-evaluation-security-incident/
[1]: https://www.anthropic.com/news/investigating-incidents-cybersecurity-evals
