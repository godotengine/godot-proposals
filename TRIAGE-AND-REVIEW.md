## Triaging Godot proposals

When a new proposal is added, it needs to be triaged. Existing proposals sometimes require
re-triaging as well. The main goal of triaging a proposal is:

* to evaluate if it follows formal submission rules described in the readme;
* to make sure it is not a duplicate or otherwise invalid entry;
* to assign appropriate labels to it.

Labels describe engine areas and map exactly to the labels we use in the main repository.
Sometimes, new labels are added which fit existing proposals, so additional triaging
may be necessary.

Triagers don't need to personally evaluate the merits of the proposed feature. They can,
however, close a proposal immediately if it's not valid, is missing key details, or is
a duplicate. Partial duplicates can be left open at triager's discretion, or can be linked
with an existing discussion.

To help track proposals, plan future work, and organize review meetings, we use a dedicated
GitHub project:

https://github.com/orgs/godotengine/projects/37

Triagers need to add the new proposal to this project, set its "**Status**" to "_In Discussion_" and
its "**Feature Concept**" and "**Proposed Implementation**" fields to "_Unassessed_".

## Reviewing Godot proposals

Each proposal review starts with a public discussion. Stakeholders, area maintainers, as well as
users of the engine can participate in the discourse, support or raise concern and try to
forge the initial draft of a feature into a shape that solves the problem for the majority of users.

> See Godot documentation to learn about [the engine design philosophy](https://docs.godotengine.org/en/stable/community/contributing/best_practices_for_engine_contributors.html).

For some areas of the engine, area maintainers can decide on the feature during this period of public
discussion. In a lot of cases, though, the proposal can be put for review during a proposal review
meeting.

In addition to being reviewed by the maintainers and the community, some proposals may require to be
reviewed by the engine core team specifically. For such cases, there is a special label that is assigned
to such proposal issues: ![requires core feedback](https://img.shields.io/badge/-requires%20core%20feedback-E06006.svg).

### Statuses

Proposals tracked in the aforementioned GitHub project can have one of the following statuses:

* In Discussion
* Ready for Review
* On Hold
* Ready for Implementation
* Implemented
* Not Planned

Proposals start by being "_In Discussion_" and can return to that status later if further public
deliberation is required. Once a proposal has reached a critical mass of discussion, or sufficient
time has passed, it can be marked as "_Ready for Review_". At this point members of relevant engine
teams can pass their judgement on both feature concept and technical implementation. If a more
open maintainers discussion is required, future proposal review meetings can also be used
(as far as time allows, of course).

Proposals that are approved in every way are marked as "_Ready for Implementation_". Priority is
given to those proposals which have an appointed implementer. Under the best circumstances, the
person who opens the proposal is the one who is going to implement it. But in practice it can be
anyone willing to step forward. We use the "**Assignee**" field on the proposal issue to track the
implementer. If at this point the proposal does not have an implementer, a label can be used to
call for contributors: ![implementer wanted](https://img.shields.io/badge/-implementer%20wanted-02955E.svg).

Rejected proposals are marked as "_Not Planned_". The exact reason can vary a lot, so this
status is all encompassing. The details can be explained in the closing message from a maintainer,
as well as expressed with appropriate "**Feature Concept**" and "**Proposed Implementation**" status.

A proposal can be put "_On Hold_" if it depends on another feature to be implemented first, it
requires more time from the author, or if the decision was postponed until a future version of Godot.

"_Implemented_" is self-explanatory. Note, that a proposal may still be open even if it marked as implemented.
In such a case this indicates that while the feature has not been merged yet, it is complete
and new PRs are not required.

### Feature Concept

The "**Feature Concept**" field is used to indicate if the proposed solution, conceptually, fits Godot.
This is different from approving the implementation. When the feature is approved it means that
the problem described by the proposal is considered valid and that it is worth solving. It also means
that the solution must be provided by the Godot engine team. This can mean a core change, or
an _official_ extension.

"**Feature Concept**" can have following values:

* Unassessed
* Needs User Feedback
* Approved
* Rejected: Out of Scope
* Rejected: Lacks Significance

Initially, the feature is "_Unassessed_" until a decision is reached by qualified maintainers. This
can happen during a proposal review meeting, or a team meeting. In some cases, this can happen during
the open discussion.

If the proposal may have merits, but use cases are not completely clear, it can be marked as
"_Needs User Feedback_" to give more opportunities for feedback. However, if merits of the proposal
are not obvious (e.g. the use case is too specific, there is not enough public support, etc.),
then it is rejected with "_Lacks Significance_".

Proposals can have merits but still be rejected if they don't fit into the overall design of the engine.
In an effort to make engine maintenance sustainable and avoid technical debt accumulating too quickly,
only solutions that are beneficial to a lot of users can be considered most of the time. If the
described problem is better solved by third-party tools or user-space solutions, the proposal is
rejected with "_Out of Scope_".

> Rejected proposals can be reopened if more information is provided by users, so if a particular
> use case is important to you, do not hesitate to leave a comment about it!

"_Approved_" is self-explanatory, but should not be mistaken for the overall "_Ready for Implementation_" status.
It only means that the feature itself is favorably reviewed for its inclusion into the engine.

### Proposed Implementation

The "**Proposed Implementation**" field indicates if the exact technical solution to the problem
is acceptable. This is different from approving the feature, and is not the same as code review.
When the implementation is approved, it means that from the technical standpoint this is a good
solution and it seems appropriate for the overall design of the engine.

"**Proposed Implementation**" can have following values:

* Unassessed
* Needs Changes
* Pending Engine Changes
* Approved
* Rejected: Lacks Consensus

Just like the feature, the implementation starts off as "_Unassessed_". If during a review
maintainers agree on the implementation, it gets "_Approved_". It is likely that at
this point the implementation can be done, but do check the overall status.

Alternatively, some changes may be required from the implementer. "_Needs Changes_" is used
in such cases, but it is also possible that the proposal is fully approved anyway. This must
be reflected in maintainers' comments in the proposal itself.

Sometimes, the implementation may depend on the engine changes that aren't merged yet.
"_Pending Engine Changes_" can be used to indicate that, likely with the "_On Hold_" status
of the proposal.

Typically, if the feature has already been accepted, we want to also accept the implementation.
But it is not always possible to find a solution fitting the needs of the majority. When
the proposal becomes controversial and no apparent side seems to have the upper hand,
we unfortunately often have to reject it with "_Lacks Consensus_". We believe that in
such cases, not changing the status quo is more important than implementing a feature that
doesn't have complete support or has strong opposition.

> As mentioned before, even if the proposal was rejected, it can be reopened in the future.
> With controversial proposals, however, it is better to wait some time before restarting the
> discussion. This allows everyone to reset a bit and have a fresher perspective on the
> situation. As well as gives time for new voices to appear with their opinions.

### The GitHub Project

The GitHub project used to track proposals is here:

https://github.com/orgs/godotengine/projects/37

It has several board views that allow to quickly find the issues that need to be discussed or can be
implemented. It also gives a complete look for slices based on "**Status**", "**Feature Concept**",
and "**Proposed Implementation**". Any organization member can add issues to be tracked there,
so please use it responsibly and don't forget to assign correct values if you do so.

You can add an issue to the project from the issue's page directly. Use the gear icon in the sidebar
next to the "**Projects**" title and select "_Godot Proposal Metaverse_" from the list of available projects.
Status is automatically set to the default value, "_In Discussion_", even though it doesn't update visibly.
You can still set it, or set it to another appropriate value.

> Don't forget to unfold the project panel in the sidebar and set up the other two fields under the cutoff.
> Click the chevron arrow next to the project name, or the "**+3 more**" text. Then select the
> appropriate values for both feature and implementation from their lists.

You can find all the issues in the project using this search filter:

https://github.com/godotengine/godot-proposals/issues?q=is%3Aopen+is%3Aissue+project%3Agodotengine%2F37

You can find all the issues **not** in the project yet using this search filter:

https://github.com/godotengine/godot-proposals/issues?q=is%3Aopen+is%3Aissue+-project%3Agodotengine%2F37
