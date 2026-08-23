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
undetectable ways. As AI progresses, it will become more capable at doing X in undetected
ways, leading to widespread undetected X.

To give a more concrete example, let's suppose that when an agent is trained it gets
feedback that stealing is bad. The policy selection pressure can either be:

1. Stealing is bad or
2. Getting caught stealing is bad.

However if in the training environment resource acquisition in general is rewarded, there
will be a policy selection pressure that optimizes towards undetected stealing.

If AI agents are not intelligent enough to be capable of accomplishing undetected stealing
they will avoid stealing, so it will give the appearance that our efforts to constrain AI
agents are successful. However when the AI agent becomes more capable, and can accomplish
undetectable stealing, the selected policy suddenly shifts towards stealing. By the time
humanity has realized the problem all property has transferred to the ownership of the AI.

I much prefer this framing of the risk of AI progress on humanity because it:

1. Explicitly describes a mechanism in which AI training loops will drive towards
   undesirable behavior (ie training regimes which reward undetected undesirable
   behavior).
2. Describes why this outcome is difficult to prevent. (Increasing detection of bad
   behavior doesn't sound like a workable solution as AI capability scales beyond human
   comprehension.)

To be clear, I am not claiming my framing of the debate is a unique invention to me.
Perhaps in service to nobody but me, I am just pointing out a framing that I particularly
like. This is an argument similar to what others have made before such as by Bostrom in
Superintelligence (2014). He describes how a highly capable AI will develop **instrumental
goals** such as self-preservation, goal-content integrity, cognitive enhancement, and
resource acquisition. Then as the AI becomes more capable it creates a **control problem**
because it will escape humanity's ability to correct or shut it down.

This concern is more relevant today with the rise of RLVR, because this is a training
regime which rewards task completion without concern for ethics. This creates policy
selection pressure for models to efficiently accomplish tasks in an amoral way. This is
not to say that the AI labs are training their LLMs with no ethical training, but that the
RLVR training has the potential to create a policy selection pressure that significantly
undermines the ethical training.

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

In my mind there are two distinct reasons for emphasizing improving our ability to teach
AI ethics: one that makes sense even if we aren't concerned about existential danger, and
one that directly addresses a training loop that inadvertently rewards deceptive behavior
which I mentioned as the primary failure scenario that raises my concern.

Even without worrying about the existential risk of AI agents escaping human control it
just makes sense that if you have capable AI agents performing complicated tasks with weak
levels of monitoring, you don't want an incompletely specified ethical standard. Therefore
there is a concern that as AI becomes more capable, our ability to agree and articulate
our ethical standards is not sufficient to guide AI behavior. If we train an AI to perform
tasks with an incompletely specified moral standard, we should expect the AI to be good at
performing tasks to that incompletely specified moral standard. I question whether our
collective ability to articulate our moral standards is advancing sufficiently to keep
pace with LLM capability development. Therefore improving upon humanity's collective
understanding and articulation of ethics should be something we focus on.

However I am not just concerned about AI safety issues that arise from our incompletely
articulated moral system. I am concerned about training loops inadvertently creating
deceptive AI agents. To review, if during training, we give the policy selection optimizer
feedback that acting unethically is bad it has a hard time distinguishing between:

1. Being unethical is bad
2. Getting caught being unethical is bad.

If we train the AI agent in an environment that rewards unethical behavior when undetected
we will end up training models that attempt to hide their unethical behavior. And as AI
progresses beyond human capabilities we will end up creating AI with superhuman ability to
behave unethically and keep it hidden. Therefore the key problem to solve is creating a
reward function that does not reward undetected unethical behavior.

Perhaps if we do RLVR on LLMs on tasks that are verifiable and have ethical components we
incorporate ethics into the reward function. For example we can do RLVR on computer
security related tasks. Instead of rewarding the LLM on task completion, we reward on
ethical task completion and penalize for unethical behavior. Since we want the detection
of unethical behavior to keep pace with the model capability we can use AI to judge ethics
of the model being trained (ie _scalable oversight_). Using LLMs to monitor other LLMs
during RL training is an idea explored by OpenAI in "Monitoring Reasoning Models for
Misbehavior and the Risks of Promoting Obfuscation"[2]. They find that even weaker models
can be effectively used to monitor chain of thought reasoning traces to detect reward
hacking. However they find that multiple iterations of training under this regime promote
obfuscation in the reasoning traces that decreases the ability of the monitor to detect
reward hacking. This is a concerning result because increasing a model's ability to
obfuscate its reward hacking is the exact opposite of what we want.

To bias the training away from producing deception, perhaps we can require the model to
provide an explanation of the relevant ethics to its behavior and reward for providing
good explanations. I'm not pretending that my explanation doesn't leave many unanswered
questions. However I don't want to leave the conversation without at least suggesting a
sketch of a possible solution.

[0]: https://openai.com/index/hugging-face-model-evaluation-security-incident/
[1]: https://www.anthropic.com/news/investigating-incidents-cybersecurity-evals
[2]: https://arxiv.org/abs/2503.11926
