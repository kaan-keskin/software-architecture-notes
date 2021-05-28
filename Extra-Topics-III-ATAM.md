# Software Architecture Evaluation: The “4+1” View Model

**Author:** Kaan Keskin

Date: May 2021

Available at: https://github.com/kaan-keskin/software-architecture-notes

**Resources:**

- Clean Architecture - Robert C. Martin - 2018
- Software Architecture Lecture Notes - University of Alberta - 2017
- Code Complete 2 - Steve McConnell - 2009
- The Architecture Tradeoff Analysis Method - Rick Kazman, Mark Klein, Mario Barbacci, Tom Longstaff, Howard Lipson, Jeromy Carriere - Proceedings of ICECCS98 - July 1998
- Software Architecture - Wikipedia: https://en.wikipedia.org/wiki/Software_architecture

## Analyzing and Evaluating an Architecture

In addition to designing a system, it is important to know how to evaluate the design to determine if it addresses the concerns, or the requirements, of all stakeholders. **Analyzing and evaluating software architecture can be difficult due to the abstract nature of software.**

**It is important to methodically analyze and evaluate a system’s behaviors, quality attributes, and various characteristics.** 

In order to measure quality attributes, **quality attribute scenarios** can be used to determine if a system is able to meet requirements set for the attribute. 

There are two kinds of scenarios:

- A **general scenario**, which is used to characterize any system
- A **concrete scenario**, which is used to characterize a specific system

![ATAM Quality Attribute Scenario](./images/atam-scenario.png)

Both general and concrete scenarios have:
- A **stimulus source**, which is anything that creates a stimulus. It can be internal or external to the system.
- A **stimulus** is a condition that will cause the system to respond. As the source of the condition can originate internally or externally, types of conditions will need to be differentiated.
- An **environment** is the mode of the system when it is receiving a stimulus. This is an important aspect, particularly if the system involves distributed computing, or if it can exist in operational modes besides just running and stopped, like recovering from a failure.
- An **artifact** is the part of the system that is affected by the stimulus. In large-scale systems, a stimulus should not directly affect the entire system.
- A **response** is how the artifact will behave as a result of receiving a stimulus. This response could include handling an error, recovering from a failure, updating system logs, dispatching security alerts, or changing the current environments.
- A **response measure** is a metric used to quantify the response so that the quality attribute can be measured. The metric should be quantitative and objective, such as probability of failure, response time, repair time, and average system load.

Scenarios are built to identify situations that impact the quality attributes of a system. In the context of analyzing and evaluating architecture, you should focus on situations that are outside of the normal execution path. This means that scenarios involving incorrect input, heavy system loads, or potential security breaches should be prioritized highly.

It is a system’s “inability” to handle unexpected failures that stops it from achieving a specific quality attribute.


