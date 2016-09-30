---
layout: post
title: Agile development processes
category: Agile
permalink: /agile-development/
---



### We have heard several risks to the waterfall approach. What are the risks to agile approach?

How do we deal with so many vendors? What if they use different languages and we don’t have staff familiar with those.

You would ensure that the vendors:

Build to common standards that are determined and controlled by the state
Deliver code with good test coverage
Use current and popular languages, tools and frameworks

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

### In waterfall approach [our contracting office] would approve the document, design, development, and testing. How in agile will the oversight of the vendor occur without such documentation. After release, what documentation will exist to assist with maintenance? What documents would the state rely on if expectations are not met and there is disagreement on what was previously agreed upon (yet no approved documents). What would be the impact of legal contract complications without such documentation?

Common misconception with agile is that just enough documentation gets interpreted as no documentation.  That is not true, agile prescribes creating documentation that is of value; rather than blindly creating documents that are prescribed by different phases of the SDLC.

Maintenance related docs (like deployment scripts/processes) fall under this umbrella.

As far as “oversight docs” like a requirements doc (used to gauge if the vendor “delivered” the functionality).  Expectations are managed in agile by having incremental releases.  Working software (or lack thereof) is the measure that can be used to assess the performance of a vendor.  Further, using working software as opposed to requirements documents as the gauge of performance allows for flexibility of discovery after each increment to adjust required functionality to be delivered.  I.e. A good vendor is not just one that delivers software functionality, but can also easily adapt to changing needs.

### How can the long term costs of Agile be compared to the locked in cost to Waterfall? How can a state estimate the full need for funding for the project? 

The locked in cost in waterfall is a piece of fiction, built upon further layers of fiction:

The requirements are well-known
The requirements do not change
Users are able to articulate their requirements well and the development team can implement these precisely without any loss of fidelity.

The return of the state’s investment should be measured in working software, not phase documents / gates of waterfall.  I.e. A fantastic requirements document will NOT be of value to the state’s constituents; only actual functionality will.   Based on that premise, waterfall will only be able to measure its return at the end of the project after most (if not all the costs) have been incurred as that is when working software is delivered.  This is a huge risk.  Agile incremental deliveries allows the state to measure returns at earlier phases (and less incurred costs) thus reducing the overall risk to the state.

Also, you should try to steer away from the conversation of “full funding” because no system is ever fully funded.  (Think O&M!).  Instead have the conversation on how agile can help manage investment risk better because you receive early indicators on whether or not the state is getting a return on the investment or not.

How do we evaluate between someone who has a COTS solution vs building from scratch with Agile?

How do all these modules really fit together?

How do COTS products fit into this? How much modification is ok?

### We found a commercial/off the shelf (COTS) tool that would mostly meet our needs, but we would need to modify it. How should we do that?

Configuring a COTS product to meet your needs is not inherently a problem. 18F frequently sees modifications to the underlying code base, which we call customization, grow to the point that the system cannot handle any updates from the COTS provider, which poses security risks and a risk to the long term viability of the tool. If you can already spot the ways that the tool does not meet your needs, it’s worth asking if your process could be adapted to meet the way the software already manages it. 

Maybe we can add another sentence (if Greg et al think it's accurate)
Alternatively, if process changes aren't feasible, state's can explore
requiring any COTS provider to offer a convenient to use plug-in or bridge
API that would allow independently developed custom code to meet the
state's unique business need without creating unique interdependencies that
will impact the COTS solution.

If the problem domain is core to your work and is where you would like to innovate rapidly, it will not make sense to choose COTS. On the other hand, if it is auxiliary to your work and you can adopt the process implemented by the COTS product, COTS would make sense.

Who is the system integrator? The state? A vendor? How does this work?

We don’t have the staff to be the systems integrator? What should we look for to get that done? 

We’ve had systems integrators before and they were the prime vendor responsible for the entire project? So how is this different?

Agile seems to require different skills of my staff, how do I know what skill we need in house and how do we get that training? Or can I hire a vendor to do that?

Once we hire an agile vendor, how do we know they’re going to deliver what we want?
Vendors that can do agile work will respond to the way you are working. We recommend having an empowered product owner - a single person 

What about governance? And IV&V? How does that work with agile development?
Isn’t this a lot more work for my staff? Is it really worth it?
Our mainframe is 30 years old and i can’t risk doing anything to make it stop working b/c it’s the only thing we have that works.

There are development patterns that would allow systems to gradually migrate away from a mainframe (or legacy system).  For example, the use of proxies to abstract out new code from legacy code. Mainframes are designed to be highly efficient in executing very specific functions; split those functions out one by one and replace them. Also ensuring that there are swift fallback/reversion processes in place hels

One can use agile prioritization techniques (like WSJF) you can identify the order of migration.  This prioritization technique isn’t based on expected benefit alone.  It also takes into consideration risk, effort and timing.

But the key to success is migrating piece by piece;  aiming to do a one big bang cut over to a new system is extremely risky.

We have lots of big projects coming up, what’s the best way to get started doing an agile project?

### What does a user centered design team actually do that’s different from how we’ve always done it?

Would recommend we not assume that other orgs are not doing user centered design.  First understand how they are sussing out features and what pain points they are experiencing.  From there, map how user centered design can help.

How do I have my users participate in feedback?
methods.18f.gov
