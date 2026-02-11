# Godot Improvement Proposals

This repository serves as the central hub for proposing, discussing, and
reviewing new features and enhancements in Godot Engine. While there exists
some leeway, most changes made to the engine must go through the proposal
process first. The goal is to determine whether the suggestion makes sense
for the majority of Godot users, and to figure out the best approach to
implement it.

As such, everyone is welcome to participate in ongoing discussions, or start
a new one.

> **Tip:** Use the [Godot proposals viewer](https://godot-proposals-viewer.github.io/)
> to view all open proposals on a single page. This allows for easy searching
> in proposal titles using <kbd>Ctrl + F</kbd> or <kbd>Cmd + F</kbd>.

Bug reports are not a subject of the proposal process. If you experience
an issue while using Godot that cannot be attributed to a missing feature,
please open a report in the [main Godot repository](https://github.com/godotengine/godot).
Feel free to open a pull-request based on any bug report as well!

## Suggesting improvements

You have two options to suggest future improvements for the engine:
[**issues**](https://github.com/godotengine/godot-proposals/issues/new/choose) and [**discussions**](https://github.com/godotengine/godot-proposals/discussions/new/choose).

To create a proposal [**issue**](https://github.com/godotengine/godot-proposals/issues/new/choose),
you should have a well-developed idea of the change you're suggesting, and put effort into a highly
detailed description of it. For instance, when proposing a new UI element, provide mockups and
thoroughly describe the element's behavior.

If you have a more general idea for an improvement without specific details, please start
a [**discussion**](https://github.com/godotengine/godot-proposals/discussions/new/choose) instead.

All proposals, both **issues** and **discussions**, will be discussed and evaluated by the
community, and may even end up being implemented by a fellow motivated Godot contributor.
Keep in mind though that all changes need the approval of Godot maintainers before they can
be merged.

## Rules for submitting a proposal

> **Note:** The following points describe requirements for a proposal issue. A
> [discussion](https://github.com/godotengine/godot-proposals/discussions/new/choose),
> on the other hand, can be started in any form.

1. **Put effort into the problem statement.** It is not enough to say a feature would be
"nice" or "helpful". Describe how the lack of it is impacting your ability to make games.
You should also describe which workarounds you tried and link related proposals. If you do
not provide a well-founded motivation, your proposal will be closed.

2. **Be specific with your solution.** It is not enough to describe just the idea; your proposal
should make all the necessary design decisions such that they can be discussed by the community.
Include images, mock-ups, diagrams, code, if applicable. If your solution lacks in detail,
is ambiguous, or otherwise low-effort, your proposal will be closed.

3. **Use one issue per proposal.** Do not cram multiple feature requests into a single proposal,
   as this makes it harder to discuss features individually.

4. **Have patience.** Godot is community-driven: if no other users are interested in
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

The following is a list of considerations that Godot maintainers use when deciding
to accept, close, or leave a proposal open.

These considerations are in balance; no one is more important than another.
Godot maintainers have discretion to weigh the factors as they see fit.

In addition, consider reading [this article](https://contributing.godotengine.org/en/latest/engine/guidelines/best_practices.html)
which describes technical considerations of Godot maintainers for new features.

#### 1. Does the proposal comply with the rules?

Read the proposal and check to see that it complies with the above-stated rules.
If it does not, close the proposal.

#### 2. How much support is the proposal receiving?

Evaluate the amount of support the proposal is receiving. This is an ongoing
analysis. If a proposal receives little support at first, it may receive
additional support later on.

#### 3. Can this proposal be implemented with an addon or GDExtension?

Evaluate whether it is possible for the solution to be implemented as an addon
or GDExtension.
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
