# ProjectBoard

This is a sample repository that acts as a demo for project organization.

## Issues

We can have 4 different issue types and nothing else, as described below. Each type of issue should be tagged with a relevant label (Feature, Bug, TechDebt, Task)

__Feature__: This type of issue describes a feature that should be added to the project. It represents a change in specification. It is the equivalent of a "user story" and ideally contains a detailed description of what needs to be done, all the edge cases and some design mockups if a UI change is required.

__Bug__: This type of issue represents something that works differently than the specification describes. Issues of this type should not be used for changes in requirements, no matter how small they are. 

__TechDebt__: A lot of features might be considered implemented, but there might be some leftover work left to be done on the engineering side, so that the feature is complete. This kind of work is not directly noticeable by Product and does not impact the feature functionality. Issues like that, with no acceptance criteria, should be qualified as "TechDebt". However, Product should be aware of the work involved in implementing this type of issues.

__Task__: This is an issue that makes sense only to Dev. "Task" issues cannot exist on their own, they should always belong to one issue of the above types (Feature, Bug, TechDebt). The association here is 1-to-many, meaning that an issue of type Feature, Bug or TechDebt can have more than one issues of type Task associated with it. Ideally, issues of this type reference their "parent" issue somewhere in their description.

## Milestones

Milestones can be used to group issues of type Feature, Bug or TechDebt. This is useful for planning and can be combined with setting a due date on the milestone. A milestone implies a batch release or what agile folks would call a "sprint".

## Projects

The repository should have at least one accompanying Project. The Project should have columns that group issues, making it clear what's going on at every given point in time. 

The columns should represent the steps the team takes until deployment, mirroring the issue lifecycle events. Anybody should be able to look at the project and get an idea of what's not yet picked up, what's in progress, who's blocked, what's ready for testing and what's deployed in production. 

In order to avoid project clutter, we can constraint the types of issues that should be visible on the project to only Feature, Bug and TechDebt.

If we want more details we can set up more than one projects, depending on how many teams are involved with the repository. For example, we could have one project for Product and one for Engineering. While the Product project deals with Feature, Bug and TechDebt issues, the Engineering board can show tasks as well. The Engineering board could also have more columns, like "Code review" or "In Develop".

## Labels

First of all, we should use labels to distinguish between the different issue types. Everything is an issue, but a Feature, Bug, TechDebt or Task has a different meaning.

Labels should help us overcome the limitations that columns provide. For example, an issue could be in the "In progress" column but underneath maybe it's done and pending code review or deployed in "develop" for testing by devs. Another good use-case is that an issue might be in the "In Staging" column, but we cannot know if it has been tested by Product and if they accepted or rejected it. 

It goes without saying that any issue could be stuck in any column, awaiting feedback, so we should create a label for that too.

To sum up, the following table sums up all the different labels and their meaning:

Label name | Meaning
-----------|---------
`feature` | This issue is of type "Feature"
`bug` | This issue is of type "Bug"
`techdebt` | This issue is of type "TechDebt"
`task` | This issue is of type "Task"
`help-wanted` | This issue is blocked. There is some work pending, some pre-requisite or an unanswered question.
`accepted` | This issue has been verified on the testing environment and should be deployed in the next release.
`rejected` | This issue has been tested on the testing environment but does not meet acceptance criteria. A comment should explain what should be changed.

## Workflow

TODO
