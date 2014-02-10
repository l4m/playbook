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

### 10 Driving Development with Tests

Developers can be confident they're building on a solid foundation, and testers can focus on edge cases instead of wasting time on trivial problems.

#### 10.1 Introducing Test-Driven Development

Allow plenty of time for the team to make a transition to TDD. It's likely to take a couple of months before they're really driving their code with tests. Your first challenge with implementing TDD is working out where to start. We recommend you pick off one problem at a time rather than attempting to introduce TDD in one big bang.

##### Buy-in from the Team

The team has to make a shared commitment to write tests and run them. They need some compelling reasons before they will commit to taking on the extra work of writing automated tests. Make sure they understand the benefits of TDD and that they appreciate the drivers behind the change.

##### Time to Learn How to Write Tests

Once they're convinced about making the move to TDD, the team members need to learn how to do it.

##### Determining Where to Start Writing Tests

Gather the team together to agree on a test strategy for how different areas of the code will be tested. A good place to start is with unit tests.

A test is not a unit test if

* It talks to the database,
* it communicates across the network,
* it touches the file system,
* it can't run correctly at the same time as any of your other unit tests, or
* you have to do special things to your environment (such as editing config files) to run it.

Most teams we work with start with a basic rule: they'll write tests for new code and any changes to existing code.

#### 10.2 Continuous Integration

Continuous Integration (CI) is integrating code changes early and often. Working this way, the latest code is available to the whole team in small slices, as soon as it's ready, rather than in one big lump.

CI is an attitude, not a tool. It's a shared agreement by the team that:

1. When we get the latest code from the repository, it will always build successfully and pass all tests.
2. We will check in our code every two to four hours.

The vital part of adopting CI is that the team wholeheartedly embraces this philosophy, making sure all tests pass all the time.

**Start by building CI discipline.**
Every time a developer checks in code, they run the build and wait to see whether all tests pass before moving on to develop more code. If the tests don't pass, then the developer needs to fix the problem.

Keep your eyes open to see whether the team still takes responsibility for fixing broken builds. The key is improving feedback on build status so the team knows as soon as possible that the build is broken.

##### Improving Feedback on Build Status

It is important everyone on the team is alerted when the build is broken because their last check-in could have caused tests to fail. Make the failing tests more visible to the whole team by making the build page more interesting. Feedback needs to be fast as well as visible.

#### 10.3 Sustaining Test-Driven Development

Watch out for slow-running tests. Encourage the team to factor in time to improve their build scripts and infrastructure to avoid this.

Work with them to make test coverage more visible. Code coverage analysis tools can be used to measure this.

#### 10.4 Hurdles

The following are some hurdles you may encounter.

##### No Test Tools Available

If no commercial or open source tools are available write a simple automated test framework.

##### Maintain Test-First Discipline

Working in pairs to discuss design can help developers get started with TDD.

##### Everyone Works in Their Own Branch

This causes a problem because each integration may be quite time consuming, often revealing misunderstandings within the team caused by developers working in isolation. Each integration also brings with it the risk of breaking other code and introducing defects.

#### 10.5 Checklist

* Allow plenty of time for making the transition to Test-Driven Development. This is a large change for a team to take on board in one go. Take an iterative approach to introducing TDD. Spend time with the team understanding what the blockers are, and then apply the PrOpER cycle.
* A completely greenfield project can start with writing tests first. When the team has to retrofit tests to existing code, they'll need time to figure out where to start. They can start writing a few automated tests per day or work test-after rather than test-first until they have a handle on how to test any legacy code.
* The whole team has to agree to the approach; all developers will need to write and run tests for TDD to work. Make sure the team understands the problems that TDD will solve.
* Factor time into plans for the team to learn how to write automated tests. Support the team's learning by organizing training and coding dojos.
* Get the team together to agree on a test strategy; unit tests in the middle layer are usually a safe place to start. Don't forget to get agreement on automated testing basics, such as where tests will be stored and how they will be run. Review the test strategy with the team to work out where to go next.
* Continuous Integration is an attitude, not a set of tools. Suggest that the team start with a synchronous CI process before relying on a build server.
* If the team uses a CI server, make it easy for the team to take responsibility for fixing broken tests. Work on making build status visible to the whole team rather than buried in email.
* Watch out for slow-running tests. Encourage the team to factor time into their plans for improving their build scripts and infrastructure. Test coverage can help the team get a better understanding of how well they're doing.
