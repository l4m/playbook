## Part III Caring About Quality

## 9 Getting to "Done"

Ever watched little kids playing soccer?

Agile teams need to learn how to work together to meet their goals. Each person on the team plays a part in getting the work done. Help them get clear on exactly what being done means and how they can collaborate to make it happen.

#### 9.1 Who Does the Testing?

Testing is not one person's job; it's the responsibility of the whole team. As their coach, you can help them work out how to coordinate their efforts.

**Developers** need to make sure their code passes the story tests before they release it for further testing. This avoids wasting the time of customers and testers who pick up the code for testing next. Encorage developers to use their programming strengths to automate as much testing as possible, although they're unlikely to spot problems with software the just wrote.

**Customers** know most about the environment the software will be used in. Their focus is usually on whether the user can achieve the goal of the user story. Be aware that customers can miss edge cases, where the system need to handle errors or odd data. Urge the team to make the latest working version of the product easily available for customers to try out any time.

**Testers** excel at destructive testing, thinking about edge cases where the system may be abused. They help the team flesh out story tests and verify that story tests are passing. Testors often need support from developers to automate tests. Watch out for opportunities for them to pair up on this.

**External teams** may carry out specialized testing before the software can be released, like security testing, usability testing, or platform testing. Recommend that the team include time for responding to problems found by this specialized testing in their release plans.

For these different roles to collaborate, they need a shared definition of what "done" means.

#### 9.2 Defining What "Done" Means

Bring the whole team together to agreee what their definition of "done" should be. Ask the team what additional checks ought to be carried out per story before it can be considered "done."

Write up their customized definition of "done" on a whiteboard where everyone can see it. The team will probably revisit their definition of "done" in retrospectives, so expect it to evolve during the project.

#### 9.3 Planning in Testing

When the team is clear what has to happen, they're less likely to leave all the testing until the last day of the iteration. Take time in planning to talk with the whole team about what the testing tasks are.

**Invite testers to share their concerns.**
Make sure testers are invited to planning sessions, and encourage them to play an active role.

#### 9.4 Managing Bugs

For the team to get all stories to "done" by the end of the iteration, they need to be clear on how to handle bugs that come up during the iteration.

* If a story test is failing it needs to get fixed.
* If the software delivers the main benefit of the user story, the bug may be deferred until later.

The customer makes the decision to defer fixes.

##### Flagging Failing Tests

Discourage testers from burying bug reports in a bug tracker. Instead, encourage them to use the team board to flag failing tests, making them visible to the whole team. It should be clear when the team has more work to do before the story is complete.

Beware of allowing bug tracking software becoming a hidden backlog.

##### Finding Root Causes

Every time a bug is found, there's an opportunity for process improvement. Encourage the team to work out what caused it and think about how this might be avoided next iteration. This can be done as each bug comes up or can be discussed in the next retrospective.

#### 9.5 Getting Feedback Early

Early feedback can help nip problems in the bud. There's no need for a developer to implement a whole story before checking they're on the right track. It's important that any negative feedback is given in a way that developers will listen to.

#### 9.6 Recovering from Not Getting Done

Talk about what happened in the iteration demo and retrospective. Help the team understand why this happened, and ask for their ideas to prevent this from happening again.

* Clear the team board at the end of each iteration.
* Convince team members that saying, "no" is preferable to overcommittment.
* Remind them of their measured velocity when planning the next iteration.

#### 9.7 Hurdles

The following are some hurdles you may encounter.

##### It's Not My Problem

Look for ways to build a sense of accountablity for the whole team.

##### Working with Remote Testers

Get estimates of testing tasks in advance of iteration planning, so these can be considered alongside the development tasks.

##### Organization Mandates Use of a Bug Tracker

The job of testers is to "prevent defects" rather than collect them.

Recommend the team uses bug-tracking software only for bugs that are found after the iteration ends.

#### 9.8 Checklist

* Define what "done" means with the team. Display this as a check list in the team workspace. Include testing done by customers, developers, and testers, but exclude testing done outside the team.
* Make sure that testing is considered in iteration planning so testing tasks are understood by the whole team.
* Encrouage developers to work closely with testers and their customers to get early feedback on stories. Ask the customer to reserve time every day to answer questions from the team.
* Recommend that software is made available to customers during the iteration. Encourage the team to look for slices of user stories that can be delivered early rather than waiting until the iteration ends.
* Use the team board to display bugs that need to be fixed before the end of the iteration. Instead of creating a hidden backlog in the bug tracker, ask testers to work with the customer to turn bugs that are deferred into new user stories that can be planned into future iterations.
* If the team doesn't get all the stories done, talk about why this happened with the whole team in the demo or retrospective. Clear the board at the end of the iteration, and take any incomplete stories into iteration planning. Help the team gather velocity data so they don't overcommit in the next iteration.
