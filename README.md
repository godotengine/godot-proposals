# Godot Improvement Proposals

Welcome to the official Godot improvement proposals repository!

Here, the [Godot](https://godotengine.org) community shares and discusses
ideas to improve the engine. 

Everyone is welcome to participate. If you have an idea, please read the [introduction below](#how-to-suggest-improvements)
to get started. We also encourage you to browse existing proposals and participate in their discussions.

> [!TIP]
> Use the [Godot proposals viewer](https://godot-proposals-viewer.github.io/)
> to browse proposals, and the [discussions tab](https://github.com/godotengine/godot-proposals/discussions)
> to browse ideas.

Bug reports are not a subject of the proposal process. If you experience
an issue while using Godot that cannot be attributed to a missing feature,
please [file a bug report](https://github.com/godotengine/godot/issues/new/choose) instead.

## How to suggest improvements

You have two options to suggest improvements for the engine: **issues** and **discussions**.

To create a proposal [**issue**](https://github.com/godotengine/godot-proposals/issues/new/choose),
you should have a well-developed idea of the change you're suggesting, and put effort into a highly
detailed description of it. Please read the [rules below](#rules-for-proposal-issues) before
you create a proposal issue. You may also wish to read about our [evaluation process](#how-we-evaluate-proposals)
to improve the chances of your proposal being accepted.

If you have a more general idea for an improvement without specific details, please start
a [**discussion**](https://github.com/godotengine/godot-proposals/discussions/new/choose) instead.

We also encourage you to iterate and expand upon ideas of other contributors and try to formulate
proposal [**issues**](https://github.com/godotengine/godot-proposals/issues/new/choose) (with appropriate attribution to those other contributors). This helps
the ideas come to fruition by giving the community something specific to discuss or implement.

All proposals, both **issues** and **discussions**, will be discussed and evaluated by the
community, and may even end up being implemented by a fellow motivated Godot contributor.
Keep in mind though that all changes need the approval of Godot maintainers before they can
be merged.

## Rules for proposal issues

> **Note:** The following points describe requirements for a proposal [**issue**](https://github.com/godotengine/godot-proposals/issues/new/choose).
> A [**discussion**](https://github.com/godotengine/godot-proposals/discussions/new/choose),
> on the other hand, can be started in any form.

1. **Do your research.** Before you post, discuss your idea with the [community](https://godotengine.org/community/),
to find if other people are experiencing the same problem and brainstorm solutions together.
Search existing [proposals](https://github.com/godotengine/godot-proposals/issues) and 
[ideas](https://github.com/godotengine/godot-proposals/discussions) for potential duplicates.
And search the internet and [asset library](https://godotengine.org/asset-library/asset) for
addons that can solve your problem without an engine change.

2. **Put effort into the problem statement.** It is not enough to say a feature would be
"nice" or "helpful". Describe how the lack of it is impacting your ability to make games.
You should also describe which workarounds you tried and link related proposals. If you do
not provide a well-founded motivation, your proposal will be closed.

3. **Be specific with your solution.** It is not enough to describe just the idea; your proposal
should make all the necessary design decisions such that they can be discussed by the community.
Include images, mock-ups, diagrams, code, if applicable. If your solution lacks in detail,
is ambiguous, or otherwise low-effort, your proposal will be closed.

4. **Use one issue per proposal.** Do not cram multiple feature requests into a single proposal,
   as this makes it harder to discuss features individually.

5. **Have patience.** Godot is community-driven: if no other users are interested in
your proposal, it will not be added to Godot. Remember that the more effort you put into your
proposal, the more likely it is to gather attention. You could also share and discuss it in
Godot's [community channels](https://godotengine.org/community/) to draw attention to it.

## What to do if your proposal is closed

We usually only close invalid, duplicate, and rejected proposals. We do not close proposals
lightly, but we can make mistakes: If you think we should re-open it, please join us in the
[contributor's chat](https://chat.godotengine.org) and describe the situation.

- **If your proposal was closed as invalid**, please review the rules above and put more
effort into your next proposal.

- **If your proposal was closed as a duplicate**, please review the linked proposal. If it is
truly duplicate, or more detailed than yours, we encourage you to support that proposal and
contribute to its discussion. If you think your proposal is sufficiently different to stand
on its own, please appeal this decision by making a comment.

- **If your proposal was rejected**, please review the stated problem and see if you can find
another solution. Often, solutions that are rejected for Godot can be implemented as a
[plugin](https://docs.godotengine.org/en/stable/tutorials/plugins/editor/index.html) or
[GDExtension](https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/index.html).

## How we evaluate proposals

The following is a list of considerations that Godot maintainers use when deciding to
[accept](https://contributing.godotengine.org/en/latest/feedback/ideas.html#how-are-proposals-accepted),
close, or leave a proposal open.

These considerations are in balance; no one is more important than another.
Godot maintainers have discretion to weigh the factors as they see fit.

In addition, consider reading [this article](https://contributing.godotengine.org/en/latest/engine/guidelines/best_practices.html)
which describes technical considerations of Godot maintainers for new features.

#### 1. Does the proposal comply with the rules?

Read the proposal and check to see that it complies with the [above-stated rules](#rules-for-proposal-issues).
If it does not, close the proposal.

#### 2. How much support is the proposal receiving?

Evaluate the amount of support the proposal is receiving. This is an ongoing
analysis. If a proposal receives little support at first, it may receive
additional support later on.

#### 3. Can this proposal be implemented with an addon or GDExtension?

Evaluate whether it is possible for the solution to be implemented as an addon
or [GDExtension](https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/index.html).
If it is possible for the proposal to be in an addon, it is less likely to be
accepted.

#### 4. Does this proposal benefit most users?

Determine whether this proposal benefits all users, or just certain users.
For example, a feature that can only be used for 3D FPS games is less
likely to be accepted than a feature that benefits all 3D games.

#### 5. Can this proposal be implemented in a robust, general-purpose way?

Determine whether the feature can be implemented in a robust way that benefits
all use-cases. For example, many games use an inventory system, but every game
implements inventory differently. Accordingly, a proposal for an inventory
system will likely not be accepted because it would be impossible for us to
implement an inventory system that works for most users that need an inventory
in their game.

#### 6. Does this proposal help users overcome a limitation?

Proposals that overcome a specific limitation are more likely to be accepted
than proposals that are just helpful. In short, need-to-have features will be
prioritized over nice-to-have features. Further, the core developers prioritize
changes that enable users to implement features themselves over implementing
those same features in core.

#### 7. How complex would the proposed change be?

A highly complex new feature involving substantial changes to core is less likely
to be accepted than a feature that can be contained within a single node, or a
group of nodes.

#### 8. Can the limitation be easily worked around?

If the feature is only intended to save users a few lines of code, it is unlikely
to be accepted.
