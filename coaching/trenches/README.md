# [Lean from the Trenches](http://www.amazon.com/gp/product/1934356859/ref=as_li_qf_sp_asin_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1934356859&linkCode=as2&tag=e2t-20)
Managing Large-Scale Projects with Kanban

## Part 1 -- How We Work

### 1 About the Project

Swedish national police authority digital investigation system. (PUST) The basic idea is to equip every police car with a small laptop, a mobile internet connection, and a web application that allows officers to handle all the investigation work quickly.

#### 1.1 Timeline

#### 1.2 How We Sliced the Elephant

The key to minimizing risk in large projects is to find a way to "slice the elephant," that is, find a way to release the system in small increments instead of saving up for a big-bang release at the end. Ideally, each increment should independently add value to the users and knowledge to the teams.

#### 1.3 How We Involved the Customer

One person acted as the main "customer." She had a list of epics and high level features. This is what we used for scheduling and release planning.

On-sites users with the development teams were there to give detailed feedback, see demos and answer questions.

Acceptance test groups would spend a couple of days trying the latest release candidate and giving feedback.

### 2 Structuring the Teams

One of the key challenges in software projects is how to organize people into decently sized teams and then how to coordinate between multiple teams.

We have five teams: one requirements team, three feature development teams, and one system test team. Some people are outside of the team structure to handle specialist functions and coordination.

**Feature teams:**
Collocated, cross-functional, self-organized, and capable of developing and testing a whole feature.

**Requirements team:**
* Some analysts are embedded in one of the feature teams and follow that team's features all the way through development into test, answering questions and clarifying requirements along the way.
* Some analysts focus on the "big picture" and aren't embedded in any feature team. They look further into the future to define high-level feature areas.
* The rest of the members of the analyst team are flexible  and move between the two other subroles depending on where they are needed most at the moment.

**Test team:**
* Some testers are embedded in a feature team and help that team get their software tested and debugged at a feature level.
* Some testers are "big-picture" testers and focus on doing high-level system tests and integration tests on release candidates as they come out.
* The rest of the test team members are flexible and move between the other two roles as needed.

The level of collaboration improved dramatically as we evolved to a more Scrum-like structure, with cross-functional teams of analysts, testers, and developer sitting together.

### 3 Attending the Daily Cocktail Party

People are everywhere, standing in small groups and communicating.

#### 3.1 First Tier: Feature Team Daily Stand-up

* What did I do yesterday?
* What am I doing today?
* What is blocking me?

#### 3.2 Second Tier: Sync Meetings per Speciality

Members of each speciality (requirements analysis, test development) meet separately to synchronize their work across all feature teams.

#### 3.3 Third Tier: Project Sync Meeting

Cross-team of the whole project. One person from each specialty and one person from each feature team as well as project manager, and others.

The project sync meeting is where we look at the big picture, focusing on the flow of functionality from analysis to production:
* Which team is doing what today?
* What is blocking our flow right now?
* Where is the bottleneck, and how can we alleviate it?
* Where will the bottleneck be next?
* Are we on track with respect to the release plan?
* Does anybody not know what to do today?

If some important topic comes up during a daily and can't be resolved within fifteen minutes, we schedule a follow-up meeting with the people needed to resolve that issue.

I was a bit concerned that people might think we were having too many meetings. That turned out not to be the case. On the contrary, the team members insist that these meetings are highly valuable, and I can see that the energy level is usually high and problems get solved.

This is a very effective way of "linking" communication channels and making sure that important knowledge, information, and decisions propagate quickly throughout the entire project.

Making decisions on-the-fly based on the current situation is the key to staying agile in a big project and not getting bogged down in bureaucracy.

### 4 The Project Board

The project board is the communication hub of the project. Ours is a several-meter-long whiteboard showing all key project features flowing through the pipeline from requirements, development, and system test, all the way into production.

A Kanban system tracks the flow of value from idea to production and limits the amount of work-in-progress at each step of the process.

The leftmost column is where ideas come from. These are high-level feature areas. Each feature area is written down on an epic card.

The second column is for analysis. Epics get analyzed and split into user stories at a feature level.

The third column is the product backlog. It contains feature cards.

The next columns are:

* Next Ten Features
* Dev in Progress
* System Test
* User Acceptance Test
* Production

To the casual observer glancing at the board, this system might look like a waterfall process: requirements analysis -> development -> system test -> acceptance test -> production. There's a big difference, though. In a waterfall model, the requirements are all completed before development starts, and development is completed before testing starts. In a Kanban system, these phases are all going on in parallel. It's a continuous flow of value from idea to production.

#### 4.1 Our Cadences

A cadence is something that happens over and over at regular intervals, forming a rhythm of heartbeat in the project.

* Retrospectives happen every second week. That's where we look for ways to improve the process.
* Planning happens every second week. That's where we decide which features to focus on next.
* Demo and system test is done in a continuous fashion, as features get done.
* Release to production is done approximately every second month.

#### 4.2 How We Handle Urgent Issues and Impediments

A traffic system metaphor is very helpful when dealing with Kanban boards. Think of the board as a series of roads, with each card representing a car trying to move across the board from left to right.

We want to optimize the flow; therefore, we don't want to fill up the board. We all know what happens to a traffic system when it is 100 percent full--the traffic system slows to a halt.

We need space, or slack, to absorb variation and enable fast flow.

Having slack in the system not only enables fast flow, it also enables escalation. On our board we use police car magnets to mark items that are urgent and need special treatment to move through the system faster.

We also mark impediments ("road blocks") using pink stickies including the date the issue came up

At the daily meetings we focus on removing these blockers. Just as with a traffic system, a blocker that stays around for too long will cause ripple effects throughout the whole system. Plus, nothing will flow faster that the bottleneck section of the road, so we focus all efforts on resolving these bottlenecks.

The project board is probably the single most important communication artifact in the project. It provides a high-level picture of what is going on in the project and illustrates flow and bottlenecks in real time.

### 5 Scaling the Kanban Boards

The speed of a project is largely determined by how well everyone understands what's going on. If everyone knows where we are right now and where we're going, it's much easier for everyone to move in the same direction.

The project board is a way to keep track of the big picture by showing project features as they move from requirements to development, to system test, and into production.

The collaboration between teams improved dramatically since each team could see how their actions influenced (and sometimes disrupted) the overall flow of features into production.

We decided to have a two-layer system of boards--one shared project board plus three team boards. The project board contains feature cards, and each feature team has their own board with the features they are working on plus the associated task breakdown.

### 6 Tracking the High-Level Goal

People are more likely to focus on the high-level goal if they know what it is. Our high-level project goal is usually posted right on the Kanban board. The release goal statement acts as a guiding light.

Consistently reevaluate the goal and discuss what needs to change to improve our confidence. These are typical actions:

* Remove an impediment
* Help a bottleneck
* Reduce scope
* Adjust the goal

If people can agree on a goal that they believe in, this has an immensely positive effect on self-organization and collaboration. Conversely, if people don't understand the goal or don't believe the goal is achievable, they will unconsciously disassociate with the business and focus on personal goals.

### 7 Defining Ready and Done

It's important to be very clear about what the columns on the board mean. At the top of most columns is the definition of done.

#### 7.1 Ready for Development

For a feature to be ready for development, it must have the following characteristics:

* It must have an ID.
* It must have a contact person.
* it must be valuable to customers.
* It must be estimated by the team.
* It must have an acceptance test scenario written on the backside of the card.

#### 7.2 Ready for System Test

"Ready for System Test" means that the feature team has done everything they can think of to ensure that this feature works and doesn't have any important defects. Our definition of ready for system test is there to keep the quality bar high and catch those pesky bugs early.

Here is our definition of ready for system test:

* Acceptance test automated
* Regression tests pass
* Demonstrated
* Clear check-in comments
* Tested in the development environment
* Merged to trunk

#### 7.3 How This Improved Collaboration

Collaboration problems gradually disappeared within a few weeks after everyone had agreed on the definitions.

### 8 Handling Tech Stories

Tech stories are things that need to get done but that are uninteresting to the customer, such as upgrading a database, cleaning out unused code, refactoring a messy design, or catching up on test automation for old features. Continuously identifying the next ten features and next five tech stories provides just enough of a work buffer to keep the feature teams from running out of things to work on.

### 9 Handling Bugs

#### 9.1 Continuous System Test

The Kanban system helped us see that we needed to do system test continuously instead of saving it until the end. Testing time may increase but total time to delivery decreases.

#### 9.2 Fix The Bugs Immediately!

Now when testers find a bug, they don't log it in the bug tracker. Instead, they write it down on a pink sticky not and go talk to developers.

The developer and tester sit together and fix the bug on the spot, or the developer fixes the bug on his own and then gets back to the tester immediately. The point is, no more handoffs, no more delays, and no more communicating through the bug tracker. This is more effective for many reasons:

* Finding and fixing bugs earlier is more effective than finding and fixing bugs later.
* Face-to-face communication is more effective than written communication.
* Everybody learns more, as developers and testers learn about each other's work.
* Less time is wasted managing long lists of old bugs.

#### 9.3 Why We Limit the Number of Bugs in the Bug Tracker

If the bug is not a blocker, we have to decide if it is more important that they top thirty bugs in the tracker. If so, then that other bug is removed from the top thirty list to make room for this one. If not, then we ignore the new bug. That way, they bug tracker continuously keeps us focused on the most important bugs and doesn't become an administrative burden.

#### 9.4 Visualizing Bugs

The top five bugs are on the board as a third input queue to development.

#### 9.5 Preventing Recurring Bugs

If you do cause-effect analysis on your bugs, you'll find that bugs aren't really a problem: they are a symptom. Bugs in your product are a symptom of bugs in your process. If you focus on fixing your process, you'll dramatically reduce the number of new bugs in your product.

### 10 Continuously Improving the Process

Our process was by no means designed up front. I would never have been able to figure all this out, especially not alone. And even if I could, there would be no buy-in from the project participants, so any process designed up front would never have reached further than the document it was written on.

Our process was discovered rather than designed. The first thing I did was put in place a process improvement engine. The basic formula is as follows:

* Clarity: Have physical boards in prominent locations that show everyone what is going on. And have a clear goal for the delivery that everyone can understand.
* Communication: Do process improvement workshops on a regular basis, both locally within each team and at the cross-team level.
* Data: Track some simple metrics that show us whether our process is improving. We measure velocity and cycle time.

The strategy is pretty simple: it's based on the assumption that people inherently want to succeed with their projects and that people inherently like to solve problems and improve their way of working. So, create an environment that enables and encourages these behaviors.

If everyone knows where we are going and where we are right now and if we have the right communication forums in place, then chances are people will self-organize to move in the right direction and continuously figure out ways of getting there faster.

This mind-set of motivating people to do evolutionary process improvement is the basis of both Agile and Lean.

#### 10.1 Team Retrospectives

Our process improvement workshops are basically Scrum-style sprint retrospectives.

Each team has a retrospective every week or two, and the length varies from thirty minutes to two hours.

**Goal:** Reflect on what is working well and what isn't, and decide what to change.

Typical changes include the following:

* Check in code more often.
* Change the time of the daily meeting or how the meeting is run.
* Update the code conventions.
* Identify a new team-internal role.

Another important function of the team-level retrospectives is to identify escalation points, that is, problems and improvement proposals that affect more than just this team and need to be solved together with the other teams.

#### 10.2 Process Improvement Workshops

The process improvement workshop is basically a scrum of scrums type of retrospective, with one person from each team and each specialty. This is the most effective place to trigger larger changes, such as those that affect multiple teams, and to follow up on the results of previous changes.

The stated purpose of this meeting is to clarify and improve our way of working. One of my most important tasks as coach was to set up and facilitate these process improvement workshops until they become part of the culture.

Having the process improvement workshop every week was rather intense, though; we barely had time to execute the changes from one meeting to the next. The positive side was that the frequent workshops drove us to implement change quickly. We also had to keep them short and focused, which forced us to prioritize only the most important changes and take small steps in our change process.

Rate of change is confusing when it happens without being given a change to understand or discuss the change. Once the most important problems are solved you can slow the rate of change to a more comfortable level.

Create a ring of chairs in the center of the room near a whiteboard.

At a high level, here's the process:

1. Set the stage: Open up the meeting and set the theme and focus.
2. Gather data: Go through what has happened since the last meeting, including victories and pain points. If we have a theme, go through concrete data relevant to that theme.
3. Generate insights: Discuss the data and what it means to us, focus on the most important pain points, and identify concrete options to alleviate them.
4. Decide what to do: Make decisions about which changes to implement.
5. Close the meeting: Decide who is going to do what and what will happen by next meeting.

Start with a round-robin question to get everyone talking--for example, "What is your feeling right now, using one word?" or "What is the most important thing you hope to get out of this meeting?"

Remind everyone of the purpose of the meeting and discuss the focus or theme.

Summarize:

* Key events and action items since last meeting.
* Positive developments and what is working well.
* Current pain points and challenges.
* Choose the issues to focus on.
* Discuss and analyze the problem and possible solutions.
* List options.
* Brainstorm advantages and disadvantages.
* Agree on changes to implement. Everyone should accept and support it.
* Identify concrete actions.

Making process improvement decisions means making changes. And since we are dealing with people, change means risk or resistance, especially from people who aren't at the meeting where the decision was made. By aiming for 100 percent consensus for each change, we dramatically reduce the risk of resistance and thereby dramatically increase the likelihood that the change will work. So, the few extra minutes spent on consensus building pays off in a big way.

#### 10.3 Managing the Rate of Change

Team members get confused (and sometimes frustrated) when the cross-team introduced new changes before the dust from previous changes had settled.

Whenever somebody wants to make a change that affects more than just his own team, they write a process improvement proposal. This is a lightweight version of the Lean A3 problem-solving process.

The process improvement proposal template forces you to think about why you want to make this change.

* What problem are you trying to solve?
* Who is affected by this change?
* What steps are involved in executing this change?

The answers to these questions are very helpful when determining the value vs. the cost of doing this change. You have to limit the amount of simultaneous process improvement initiatives.

> When in doubt, choose the simplest solution.

### 11 Managing Work in Progress

In any kind of workflow it is useful to distinguish work states and wait states. Work states are when something is happening.

Buffers are places things hang out while waiting for the next step in the process.

Sometimes we need a small buffer to ensure smooth flow between two processes. For example, the rate at which features get developed doesn't always perfectly match the rate at which features get system-tested. This type of buffering can be seen as "necessary waste." 

Unless the two machines happen to crank things out at exactly the same rate, we need a buffer to absorb the variability.

As the process improves, however, the need for these buffers is reduced. By clearly visualizing buffers on the board, we are more likely to keep asking ourselves whether we really need all these buffers and what we can do to reduce them.

#### 11.1 Using WIP Limits

At the top of each column on the board is the work in progress limits (WIP limits). The purpose of WIP limits is to avoid too much multitasking and overloading a downstream process. If the testers have too much work to do, we don't want developers to keep building new features and adding to their workload--instead, they should focus on helping test. WIP limits act as an alert signal to highlight the problem before it gets out of hand.

#### 11.2 Why WIP Limits Apply Only to Features

Tech stories and bug fixes aren't included in the WIP limit.

Small urgent issues may not need to be included in the WIP limit.

Tech stories often offload the downstream bottleneck. Therefore, a full WIP limit should encourage team members to work on tech stories.

We only include feature cards when measuring cycle time and calculating velocity.

One of the consequences to WIP limits is that people sometimes don't have anything to do. Or more specifically, WIP limits sometimes constrain people to do something different from what they would normally do.

> Focus on finishing things rather than starting things!

### 12 Capturing and Using Process Metrics

Process metrics are useful to find out what needs to be improved and if our changes are doing any good. They can also be useful for high-level release planning.

We track two process metrics:

* Velocity (features per week)
* Cycle time (weeks per feature)

#### 12.1 Velocity (Features per Week)

For velocity (throughput), we just count, at the end of each week, how many features have reached "Ready for Acceptance Test (This Week)." We write this number down in a velocity log at the bottom of the board.

Using this information, we generate a simple burn-up chart, showing the cumulative number of features that have been completed per week.

This information is useful in many ways.

1. reality check tool to make sure that the release plan is realistic
2. tool to predict approximately how many features will be done by a certain date
3. highlight problems
4. visualize process improvement (slope of curve increases)

Combining the velocity of tech stories as well would give total capacity.

#### 12.2 Why We Don't Use Story Points

In practice, feature sizes are quite evenly distributed. Higher precision does not always add value, so estimating in story points would have been a waste of time.

#### 12.3 Cycle Time (Weeks per Feature)

Cycle time means how long it takes for something to get done.

* Every time a feature is selected to be among the "Next Ten Features," we write a start date on the card.
* Every time a feature reaches "Ready for Acceptance Test," we note the finish date and write down the elapsed days for that feature in a spreadsheet.

We then visualize this using a control chart, where the height of each bar represents how long one specific feature tool to cross the board. This graph is useful in predicting how long it will take for a feature to get done.

Once you understand your cycle time, it's usually not too hard to shorten it dramatically, using techniques such as limiting WIP.

To guide improvement efforts, set challenging but realistic targets:

* More stable velocity: Velocity should be roughly the same every week instead of unevenly distributed. This gives fewer bottlenecks, easier release planning, and smoother flow in general.
* Higher velocity: Our average was three; we set the target to five.
* Lower cycle time: Our average was six weeks; we set the target to two.

Little's law in queuing theory is inescapable. The goal is to have a low enough WIP limit to keep people collaborating and to expose problems--but not low enough to expose all problems at once.

#### 12.4 Cumulative Flow

The Kanban board shows us bottlenecks in real time, which is great, but it does not show us historical trends. Cumulative flow diagrams are a popular tool in Kanban circles to visualize bottlenecks over time. Every day, count how many items are in each column. Then visualize it in a diagram. Although it may be hard to draw conclusions from this it may be useful to collect the data.

#### 12.5 Process Cycle Efficiency

This is tough when using manual Kanban systems.

Process Cycle Efficiency (%) = Touch Time/Elapsed Time

Elapsed time means how many days the feature took to cross the project board (= cycle time).

Touch time means how many days the feature actually spent in work in progress columns

### 13 Planning the Sprint and Release

The purpose of sprint planning meetings is to figure out what to do next. The meeting has two parts: backlog grooming and top ten selection.

#### 13.1 Backlog Grooming

Backlog grooming is all about getting features to the "Ready for Development" state. We do this in the first half of the sprint planning meeting. The product owner presents the next features to be developed.

We break the group into small cross-functional subgroups, typically with one requirements analyst, one developer, and one tester in each. Each subgroup takes a few feature cards, estimates them using Planning Poker and writes S, M, or L on the card. If the card is Large, they break it down further. They also discuss and agree on a suitable acceptance test and write it on the backside.

#### 13.2 Selecting the Top Ten Features

Now look at this pile of features and any still on the list and theme the conversation with, "Out of everything in the whole world that we might focus on next, what are the top ten features?"

Several aspects influence this decision:

* Business value--which features will the customers be happiest to see?
* Knowledge--which features will generate knowledge (and thereby reduce risk)?
* Resource utilization--we want a balance of feature areas so that each team has stuff to work on.
* Dependencies--which features are best built together?
* Testability--which features are most logical to test together and should therefore be developed in close proximity to each other?

#### 13.3 Why We Moved Backlog Grooming Out of the Sprint Planning Meeting

We wanted to keep the meeting time boxed and focused. A few days before the sprint planning meeting, one of the requirements analysts will have an informal conversation with a developer and a tester to discuss an upcoming feature. As a result of the conversation, that feature would be broken down, estimated, and given an acceptance test.

As much grooming as possible is completed before the sprint planning meeting.

#### 13.4 Planning the Release

We know are velocity and can calculate how long implementation will take as long as we know the number of features.

Take each epic and estimate how many features it will break into. This estimation requires effort from requirements analysts, developers, and testers. The process is similar to estimating story points; we are just asking "How many features is this epic?" instead of "How many story points?"

Once we have estimated the number of features for each epic, we can count the total number of features and divide by our historic velocity. This gives us just enough information to make a rough estimate.

As velocity stabilizes, we can make better and better predictions, so our answer might become more precise.

### 14 How We Do Version Control

Get your version control system in shape before you scale.

We decided to implement the mainline model, a stable-trunk pattern.

#### 14.1 No Junk on the Trunk

It is critically important to have a stable trunk at all times. A feature must be tested before code is checked into the trunk. This allows the product to grow in discrete steps, while always remaining stable and ready for system test. Mistakes are discovered quickly and fixed (or rolled back). The continuous integration system can't verify everything, but it will catch the most obvious issues such as broken builds or failing unit tests.

#### 14.2 Team Branches

Each team has a team branch that they use to check in and share code during development. Team branches have more lenient policies than the trunk.

Whenever the team feels that they have completed a feature and tested it as well as they can, they will do the following:

* Merge down from the trunk to the team branch.
* Do a final check to ensure that the team branch is stable.
* Merge the team branch up into the trunk.

Un-merged branches (or diverging code) are a form of technical debt.

#### 14.3 System Test Branch

System test goes on more or less continuously (rather than just at the end of the release cycle). We don't want features being added and updated while system test is going on. Whenever we are ready for a new round of system tests, we spawn off a system test branch from the trunk. If we find a bug in system test, a developer fixes that bug directly on the system test branch and directly merges the fix down to the trunk.

The version control system is really the heart of any multi team development project. As the organization becomes more Lean and Agile, the version control system usually needs to be evolved as well.

### 15 Why We Use Only Physical Kanban Boards

One of the main reasons is evolution.

Our board has changed structure many times. It took a couple of months before it started stabilizing. Anybody, could implement any of these changes physically on the board once we know exactly what we want it to look like.

The second reason we use a physical board: collaboration.

With an electronic board you lose most of the interaction, the part where people pick up a card from the wall and wave it while talking about it, or where people write stuff on the cards or move them around during the meeting. People would most likely update the board while sitting at their desk--which is more convenient but less collaborative.

Boards like this can change the culture of an organization. Patterns of interaction  change and trust between the teams is improved by collaborating in front of the board every day.

We do have several electronic tracking systems to complement the physical Kanban boards--things like the bug tracker and various spreadsheets for metrics and release planning. But the project board is the "master." Electronic docs that duplicate information are considered "shadows" of the board.

### 16 What We Learned

As you may have figured out, this case study is really all about organizational change! Here are some key takeaways points, from the perspective of a change agent.

#### 16.1 Know Your Goal

Get everyone together and agree on what "perfect" means in your context. What would a "perfect" process, organization, and work environment look like? This will just be your compass direction, so the goal doesn't have to be realistic. Perfection is a direction, not a place! Having a clearly defined direction makes it easier to focus and evaluate your improvement efforts.

#### 16.2 Experiment

Don't look for perfect solutions. It's probably not worth the wait, and you'll probably get it wrong anyway. Instead, look for small incremental improvements, and think of them as experiments. An experiment may or may not lead to the intended improvement, but it should always generate insights that can be used to design the next experiment.

A great process isn't designed; it is evolved. So, the important thing isn't your process; the important thing is your process for improving your process.

#### 16.3 Embrace Failure

Some changes just don't work. Some changes even make things worse. Don't worry about it, because few failures are irreversible. Fear of failure is the biggest enemy of innovation. Instead of asking "Why did we fail? Who screwed up?" ask "What did we learn, and what will we try next?"

The only real failure is the failure to learn from failure.

#### 16.4 Solve Real Problems

Whenever you're trying to change something, ask yourself continuously, "What problem am I trying to solve? Is it real or hypothetical? Is there any other more important problem what I should focus on instead?" When in doubt, ask people! It is very easy to fall into the trap of focusing on irrelevant or imagined problems, especially as external coach on a part-time basis.

#### 16.5 Have Dedicated Change Agents

Change is hard! Especially when it involves people. And organizational change always involves people. One critical success factor is having at least one dedicated change agent, someone who focuses almost entirely on driving, leading, and facilitating the change process.

Even better, have two change agents: one insider and one outsider. The insider (typically an employee) has the domain knowledge, knows who to talk to for what, and knows the history of the organization and what has worked in the past. The outsider (typically a consultant) provides a fresh perspective and experience from helping other companies go through the same type of change.

Culture can be defined as "things that everyone does without noticing it." An outsider is more likely to notice, and challenge, the status quo.

#### 16.6 Involve People

Most people like change; they just don't like to be changed. So, don't make any change without first involving the people who will be affected by it. Forcing people to change is usually ineffective, unnecessary, and, well, cruel. If people resist your great change proposal, you probably haven't made the problem clear enough. Or you're solving the wrong problem. Go back to your cause-effect diagram and think again!

Better yet, don't even make the change proposal yourself. Instead, visualize the problem that you think you see, and engage the people affected by the problem to propose solutions. People are much more likely to accept a change if it was their own idea!

Once everyone agrees that the problem really is a problem and that it is worth solving, they you're halfway to the solution!

## Part II -- A Closer Look at the Techniques

### 17 Agile and Lean in a Nutshell

Broadly speaking, Lean and Agile are two sets of highly compatible values and principles that outline how to succeed with product development. Scrum and XP and Kanban offer concrete techniques such as sprint planning meetings (Scrum), pair programming (XP), and limit work in progress (Kanban). These techniques can be seen as process tools.

#### 17.1 Agile in a Nutshell

##### Manifesto

* Individuals and interactions over processes and tools
* Working software over comprehensive documentation
* Customer collaboration over contract negotiation
* Responding to change over following a plan

##### Values

* Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
* Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
* Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
* Business people and developers must work together daily throughout the project.
* Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
* The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
* Working software is the primary measure of progress.
* Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
* Continuous attention to technical excellence and good design enhances agility.
* Simplicity--the art of maximizing the amount of work not done--is essential.
* The best architectures, requirements, and designs emerge from self-organizing teams.
* At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.

Any method or approach that follows these values and principles can be considered Agile. Many of the original manifesto authors hope that the term Agile will eventually fall out of use, signifying that the Agile values and principles have become simply "the way we do software."

#### 17.2 Lean in a Nutshell

Lean arose from manufacturing and the Toyota Production System (TPS).

##### Optimize the Whole

Optimizing a part of a system will always, over time, sub optimize the overall system.

* Focus on the entire value stream: From concept to cash. From customer request to deployed software.
* Deliver a complete product: Customers don't want software; they want their problems solved. Complete solutions are built by complete teams.
* Think long term: Beware of governance and incentive systems that drive short-term thinking and optimize local performance.

##### Eliminate Waste

Waste is anything that does not add customer value. The three biggest wastes in software development are the following:

* Building the wrong thing: "There is nothing so useless as doing efficiently that which should not be done at all."
* Failure to learn: Many of our policies--for example, governance by variance from plan, frequent handovers, and separating decision making from work--interfere with the learning that is the essence of development.
* Thrashing: Practices that interfere with the smooth flow of value--task switching, long list or requests, big piles of partly done work--deliver half the value for twice the effort.

##### Build Quality In

If you routinely find defects in your verification process, your process is defective.

* Final verification should not find defects: Every software development process ever invented had its primary purpose finding and fixing defects as early in the development process as possible.
* Mistake-proof your process with test-first development: Tests--including unit tests, end-to-end tests, and integration tests--must be available to establish confidence in the correctness of the system at any time during development, at every level of the system.
* Break dependencies: System architecture should support the addition of any feature at any time.

##### Learn Constantly

Planning is useful. Learning is essential.

* Predictable performance is driven by feedback: A predictable organization does not guess about the future and call it a plan; it develops the capacity to rapidly respond to the future as it unfolds.
* Maintain options: Think of code as an experiment--make it change tolerant.
* Last responsible moment: Learn as much as possible before making irreversible decisions. Don't make decisions that will be expensive to change before their time--and don't make them after their time!

##### Deliver Fast

Start with a deep understanding of all stakeholders and what they will value. Create a steady, even flow of work, pulled from this deep understanding of value.

* Rapid delivery, high quality, and low cost are fully compatible: Companies that compete on the basis of speed have a big cost advantage, deliver superior quality, and are more attuned to their customers' needs.
* Queuing theory applies to development, not just servers: Focusing on use creates traffic jams that reduce use. Drive down cycle time with small batches and fewer things in process. Aggressively limit the size and lists and queues.
* Managing workflow is a lot easier than managing schedules: The best way to establish reliable, predictable deliveries is to establish reliable, repeatable workflows with iterations or a Kanban system.

##### Engage Everyone

The time and energy or bright, creative people are the scarce resources in today's economy and the basis of competitive advantage.

People who are paid fairly and adequately are motivated by autonomy, mastery, and purpose.

* Autonomy: The most effective work groups are semi-autonomous teams with an internal leader who has end-to-end responsibility for complete, meaningful tasks.
* Mastery: Respect for people means providing the challenge, feedback, and environment that enables everyone to become excellent.
* Purpose: Tie work to value. Only by believing in the purpose of their work will people become engaged in achieving that purpose.

##### Keep Getting Better

Results are not the point--the point is to develop the people and the systems capable of delivering results.

* Failure is a learning opportunity: The most reliable performance comes when even small failures are deeply investigated and corrected--when noise is tolerated.
* Standards exist to be challenged and improved: Embody the current, best-known practice into standards that everyone follows, while encouraging everyone to challenge and change the standards.
* Use the scientific method: Teach teams to establish hypotheses, conduct many rapid experiments, create concise documentation, and implement the best alternative.

#### 17.3 Scrum in a Nutshell

Scrum is rooted in empirical process control and complex adaptive systems theory.

The core concepts of Scrum are as follows:

##### Ordered Product Backlog

The product owner defines a product vision and orders the backlog by business value and other factors such as risk and dependencies.

##### Cross-functional Teams

Each team has a product owner, who provides the vision and overall business priorities, and a Scrum master, who focuses on improving the team and removing impediments.

##### Sprints

Each iteration ends with a demonstration of a tested, potentially shippable release.

##### Continuously Adjusted Release Plan

The product owner optimizes the release play and updates priorities in collaboration with the customer, based on insights gained by inspecting the release after each iteration.

##### Continuously Adjusted Process

The team optimizes the development process by having a retrospective after each iteration.

So, with Scrum:

…we have a small team spending a short time building a small thing.

#### 17.4 XP in a Nutshell

Extreme Programming (XP) is based on the values of simplicity, communication, feedback, courage, and respect.

* Continuous integration
* Pair programming
* Test-driven development
* Collective code ownership
* Incremental design improvement

#### 17.5 Kanban in a Nutshell

Kanban is a Lean approach to Agile software development. Kanban is a Japanese word that means "visual card."

* Visualize the workflow
	* Split the work into pieces, write each item on a card, and put the card on the wall.
	* Use named columns to illustrate where each item is in the workflow.
* Limit work in progress (WIP): Assign explicit limits to how many items may be in progress at each workflow state.
* Measure and manage cycle time: Average the time to complete one item. Optimize the process to make the cycle time as small and predictable as possible.

This is basically a direct implementation of a Lean pull-scheduling system.

### 18 Reducing the Test Automation Backlog

Without test automation, making changes in the system is very hard, because things break without anybody noticing. This makes the team terribly afraid to change code and therefore reluctant to improve the design of the code, which lead to a downward spiral of worse and worse code as the system grows.

#### 18.1 What to Do About It

Let the team improve test coverage a little bit each iteration.

1. List your test cases.
2. Classify each test by risk, how expensive it is to do manually, and how expensive it is to automate.
3. Sort the list in priority order.
4. Automate a few tests each iteration, starting from the highest priority.

### 19 Sizing the Backlog with Planning Poker

Planning Poker is a simple but powerful tool that makes team estimating faster, more accurate, and more fun.

#### 19.1 Estimating Without Planning Poker

Teams are heavily influenced by who speaks first.

#### 19.2 Estimating With Planning Poker

* Everyone presents a card face down with their estimate.
* Cards are turned over simultaneously.
* Discuss estimates that are wildly divergent.
* Convergence

### 20 Cause-Effect Diagrams

Cause-effect diagrams are a simple and pragmatic way of doing root-cause analysis.

#### 20.1 Solve Problems, Not Symptoms

The key to effective problem solving is first to make sure you understand the problem you are trying to solve--why it needs to be solved, how you'll know when you've solved it, and what the root cause of it is.

If you "solve" the symptom without digging deeper, it's highly likely that the problem will just reappear later in a different shape.

Most problems in organizations are systemic. The "system" (your organization) has a glitch that needs to be fixed. Until you find the source of the glitch, most attempts to fix the problem will be futile or even counterproductive.

#### 20.2 The Lean Problem-Solving Approach: A3 Thinking

One of the core tenets of Lean thinking is Kaizen--continuous process improvement. Toyota attributes much of its success to its highly disciplined A3 thinking problem-solving approach.

With the A3 approach, a significant amount of time is spent analyzing and visualizing the root cause of a problem before proposing solutions.

#### 20.3 How to Use Cause-Effect Diagrams

Here's the basic process:

1. Select the problem and write it down.
2. Trace "upward" to figure out the business consequences, the "visible damage" that your problem is causing.
3. Trace "downward" to find the root cause.
4. Identify and highlight vicious cycles.
5. Iterate these steps a few times to refine and clarify your diagram.
6. Decide which root cause to address and how.

A countermeasure is an experiment, not a solution.

#### 20.9 Pitfalls

* Too Many Boxes and Arrows: Simplify.
* Oversimplification: This is intentional.
* Getting Personal: Avoid the "blame game." Assume all problems are systemic.

#### 20.10 Why Use Cause-Effect Diagrams?

* Create a common understanding
* Identify how problems affect the business
* Find root causes
* Eliminate vicious cycles

Cause-effect diagrams are useful, but they key point is really the problem solving approach itself: the questions asked and the resulting conversations and insights.

### 21 Final Words

Knowledge doesn't stick unless you practice. So, think about what you learned from this book and how this knowledge might come to use in your context. Then go experiment!
