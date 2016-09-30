---
layout: post
title: Agile development processes
category: Agile
permalink: /agile-development/
---

### We have heard several risks to the waterfall approach. What are the risks to agile approach?  
- Incorrectly using Agile as justification for poor or no architecture/design or documentation
- Not getting the benefits because of ‘agilefall’ - that is, incomplete or incorrect or uninformed adoption of agile techniques

### How do we deal with so many vendors? What if they use different languages and we don’t have staff familiar with those.

You would ensure that the vendors:

- Build to common standards that are determined and controlled either by the state or by the entire technical project team
- Build with agreed engineering practices across the entire program
- Use IV&V to monitor consistency across teams
- Use project-wide Definition of Ready and  Definition of Done
- Organize by Feature Teams
- Conduct synchronized, system-wide sprint reviews
- Maintain standards for automated test
- Deliver code with good test coverage
- Use current and popular languages, tools and frameworks
- Include “non-functional requirements (NFRs)” in all solicitations, specifying required technology stack, tools, and other technical constraints

### Let’s say we build a new system with 12 modules, how do we maintain that system? Do we keep all of those vendors on board through the life of the project?

No. If the modules are open source and built with standard languages, libraries, and frameworks, other vendors can jump in to add features or make fixes as necessary. This frees the state from having to rely on any given vendor for anything as new vendors can swap in and out.

With iterative and incremental goals of agile development, continuous integration and continuous deployment activities become de facto needs of systems.  As a result, comprehensive automation (testing and deployment) becomes baked in as part of the development process.  This automation helps reduce the reliance on institutional knowledge from vendors leading to the reduction of barriers to entry for other vendors to maintain the system.  Increasing competition amongst vendors and thus keeping costs down to the state.

### What happens when something goes wrong and vendors all blame each other? How does the problem get fixed quickly and who pays for that?

With every release, you would have deployed code that is tested in the field. You could have an acceptance period. The state would be responsible for problems discovered after this period. It would be treated as fresh development that can be contracted out to any developer. This is a fact of (software development) life that has to be accepted.

### Who do we call when something goes wrong?

One of the great strengths of agile development is that delivery is incremental, which spreads the risk across the entire development process rather than loading all of it at the very end. When things go wrong, they’re smaller problems that can be fixed more quickly and more easily.

If you discover a bug in the software, you would hire a vendor to fix it. It doesn’t have to be the same vendor that originally produced the code. In fact, the bug could simply be added to the product backlog and the next vendor would pick it up.

If a vendor isn’t producing to the level you expect, you can simply not hire them for any subsequent work. The amount of time and effort lost is limited to that one development period, possibly as short as a few weeks, rather than the entire life of the project.

### Pitfalls of the Strangler pattern in legacy system replacement

During the period when the legacy system is also operational, you have two systems - for the users, for maintenance

You may stop investment after initial wins and prolong this aforementioned period, for too long (perhaps forever)

It is rarely the case with large systems that one size fits all. More typically one size fits none. Be purposeful in your choice of technical strategy for your local program

### In waterfall approach [our contracting office] would approve the document, design, development, and testing. How in agile will the oversight of the vendor occur without such documentation. After release, what documentation will exist to assist with maintenance? What documents would the state rely on if expectations are not met and there is disagreement on what was previously agreed upon (yet no approved documents). What would be the impact of legal contract complications without such documentation?

Common misconception with agile is that just enough documentation gets interpreted as no documentation.  That is not true, agile prescribes creating documentation that is of value; rather than blindly creating documents that are prescribed by different phases of the SDLC.

Maintenance related docs (like deployment scripts/processes) fall under this umbrella.

As far as “oversight docs” like a requirements doc (used to gauge if the vendor “delivered” the functionality).  Expectations are managed in agile by having incremental releases.  Working software (or lack thereof) is the measure that can be used to assess the performance of a vendor.  Further, using working software as opposed to requirements documents as the gauge of performance allows for flexibility of discovery after each increment to adjust required functionality to be delivered.  I.e. A good vendor is not just one that delivers software functionality, but can also easily adapt to changing needs.

Documentation as the bedrock of oversight is an artifact of waterfall development, because there is no product available to assess or examine until the end of the (usually very long) project. Agile IV&V must concentrate on evaluating the actual product, each sprint, throughout the development period.

### How can the long term costs of Agile be compared to the locked in cost to Waterfall? How can a state estimate the full need for funding for the project? 

The locked in cost in waterfall is a piece of fiction, built upon further layers of fiction:

- The requirements are well-known
- The requirements do not change
- Users are able to articulate their requirements well and the development team can implement these precisely without any loss of fidelity.

Further the return of the state’s investment should be measured in working software, not phase documents / gates of waterfall.  I.e. A fantastic requirements document will NOT be of value to the state’s constituents; only actual functionality will.   Based on that premise, waterfall will only be able to measure its return at the end of the project after most (if not all the costs) have been incurred as that is when working software is delivered.  This is a huge risk.  Agile incremental deliveries allows the state to measure returns at earlier phases (and less incurred costs) thus reducing the overall risk to the state.

Also, you should try to steer away from the conversation of “full funding” because no system is ever fully funded.  (Think O&M!).  Instead have the conversation on how agile can help manage investment risk better because you receive early indicators on whether or not the state is getting a return on the investment or not.

### How do we evaluate between someone who has a COTS solution vs building from scratch with Agile?

If there is a COTS system that will fit your requirements, including evolution from your existing legacy system, then it is quite likely there is a possibility of cost savings. Be sure to include in your analysis the evolution from legacy, ongoing O&M costs, costs related to being locked in to a single vendor, and costs associated with maintaining the inevitable customizations you will make to the COTS product.

### How do all these modules really fit together?
There are two distinct levels of “fitting together”. 
- One is at the user interface level where good and consistent application of HCD principles across all modules will provide similar user experiences to people using each module. For instance, if I have to look up a person, the presentation of that person’s information should look the same regardless of which module I am currently working in. 
- The second “fitting together” is at the technical level, and this is a key point. _The modules need not know about each other at all._ Each module should communicate directly with the database and act directly on data. There should be no need for “integration” between modules. So the modules fit together by operating on the same data independently.

### How do COTS products fit into this? How much modification is ok?
Modification of COTS products carries with it many hidden, non-obvious costs (such as support of the modified code, receiving updates on the COTS software).  It should be avoided as much as possible.

### We found a commercial/off the shelf (COTS) tool that would mostly meet our needs, but we would need to modify it. How should we do that?

Configuring a COTS product to meet your needs is not inherently a problem. 18F frequently sees modifications to the underlying code base, which we call customization, grow to the point that the system cannot handle any updates from the COTS provider, which poses security risks and a risk to the long term viability of the tool. If you can already spot the ways that the tool does not meet your needs, it’s worth asking if your process could be adapted to meet the way the software already manages it. 

Maybe we can add another sentence
Alternatively, if process changes aren't feasible, state's can explore
requiring any COTS provider to offer a convenient to use plug-in or bridge
API that would allow independently developed custom code to meet the
state's unique business need without creating unique interdependencies that
will impact the COTS solution.

If the problem domain is core to your work and is where you would like to innovate rapidly, it will not make sense to choose COTS. On the other hand, if it is auxiliary to your work and you can adopt the process implemented by the COTS product, COTS would make sense.

### Who is the system integrator? The state? A vendor? How does this work?
Just as the role of Project Manager changes in an agile project, so does the role of system integrator. The state can become the system integrator if there is the will and the budget, a system integrator can be engaged as in the past, or you can take advantage of the agile approach and not use a system integrator. There will be a few things that require an overall project view that require some technical expertise, but they will be orders of magnitude less than with a multi-vendor waterfall project.

### We don’t have the staff to be the systems integrator? What should we look for to get that done? 

### We’ve had systems integrators before and they were the prime vendor responsible for the entire project? So how is this different?

### Agile seems to require different skills of my staff, how do I know what skill we need in house and how do we get that training? Or can I hire a vendor to do that?
This is where 18F, in particular, can help the most. 

### Once we hire an agile vendor, how do we know they’re going to deliver what we want?
Vendors that can do agile work will respond to the way you are working. We recommend having an empowered product owner - a single person
In a well-run agile project you will get working product from your vendors every two weeks. If you don’t, then you have a problem. If you do, then you can evaluate their deliverables every two weeks

### What about governance? And IV&V? How does that work with agile development?
In a well-run agile project you will get working product from your vendors every two weeks. If you don’t, then you have a problem. If you do, then you can evaluate their deliverables every two weeks
### Isn’t this a lot more work for my staff? Is it really worth it?
One of the benefits of agile development is that productivity is much higher than the alternative. That is, you can expect more and better output from your project in a well-run agile project. There are many reasons for this. 

### Our mainframe is 30 years old and i can’t risk doing anything to make it stop working b/c it’s the only thing we have that works.

There are development patterns that would allow systems to gradually migrate away from a mainframe (or legacy system).  For example, the use of proxies to abstract out new code from legacy code. Mainframes are designed to be highly efficient in executing very specific functions; split those functions out one by one and replace them. Also ensuring that there are swift fallback/reversion processes in place hels

One can use agile prioritization techniques (like WSJF) you can identify the order of migration.  This prioritization technique isn’t based on expected benefit alone.  It also takes into consideration risk, effort and timing.

But the key to success is migrating piece by piece;  aiming to do a one big bang cut over to a new system is extremely risky.

### We have lots of big projects coming up, what’s the best way to get started doing an agile project?
A common approach is to start with a small, less important project in order to develop understanding of agile project management, then expand. It is certainly much more difficult (and higher risk), and requires more coaching and training, to dive right into a large, high profile, critical project first

### What does a user centered design team actually do that’s different from how we’ve always done it?

Would recommend we not assume that other orgs are not doing user centered design.  First understand how they are sussing out features and what pain points they are experiencing.  From there, map how user centered design can help.

### How do I have my users participate in feedback?
If possible, have vendors perform user research as part of their build-out of the platform
Ask users for feedback early and often: in person and on the site itself
methods.18f.gov has a list of practices to enable users to participate in feedback.
