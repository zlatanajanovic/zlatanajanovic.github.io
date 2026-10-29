---
layout: post
title: "Who is in charge? Robot autonomy levels for human-in-the-loop systems"
date: 2026-10-28 10:00:00
description: Announcing our book chapter proposing a ladder of robot autonomy levels for human-in-the-loop systems.
tags: robotics autonomy human-in-the-loop
categories: research
permalink: /robot-autonomy-levels/
---

Robots can now pick, place, assemble, navigate, fly, dive and even fold laundry with impressive skill. Look closely at almost any real deployment, though, and you will still find a human in the loop: someone who teaches the robot, watches over it, corrects it, or takes over when something goes wrong.

This is not a temporary embarrassment on the way to full autonomy. Robots remain brittle at the edges of the conditions they were designed or trained for. Sensors degrade, environments change, objects behave unexpectedly, and small errors compound over long, multi-step tasks. Humans, in turn, bring judgement, context, adaptability and accountability. The real question is therefore not whether humans should be involved, but how: who leads the task, who supervises, and who is the fallback when the robot reaches its limits?

Surprisingly, robotics has no widely accepted way to answer that question. We are happy to announce our upcoming book chapter, _“Robot Autonomy Levels for Human-in-the-Loop Systems”_, which tries to provide one.

## Why levels of autonomy?

Automated driving has shown how useful a shared vocabulary can be. The SAE levels of driving automation made explicit what the car does, what the driver must supervise, and who handles fallback. Buyers, engineers and regulators can all reason with the same ladder.

Robotics is different. A single robot may switch between many tasks, tools and environments within one shift, and the human may act as operator, teacher, supervisor, collaborator or safety authority, sometimes all within the same hour. Existing robotics taxonomies, such as levels of robot autonomy for human-robot interaction, the autonomy levels proposed for medical robots, or NIST’s ALFUS framework for unmanned systems, show both the demand for levels and how hard it is to agree on one.

In the chapter, we propose a ladder adapted from driving, while being explicit about where the analogy breaks.

## The ladder

| Level | Name                 | Who does what                                                                                                                                                                |
| :---: | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   0   | Teleoperated         | The human directly controls the robot, and the robot executes commands.                                                                                                      |
|   1   | Assisted control     | The human leads, and the robot stabilises, constrains or amplifies what the human does, for example tremor suppression, collision avoidance or acting as a force multiplier. |
|   2   | Shared control       | Human and robot act together, and the human supervises continuously and can intervene at any moment.                                                                         |
|   3   | Conditional autonomy | The robot completes tasks alone within defined conditions. When it reaches its limits, it asks for help, explains why and stays safe while the human responds.               |
|   4   | High autonomy        | The robot also handles its own fallback within a bounded domain, so humans can supervise remotely, often one person for many robots.                                         |
|   5   | Full autonomy        | No human fallback at all. As in driving, this remains an aspirational upper bound.                                                                                           |

## Key insights

- **A human in the loop is not the same as a human in control.** Oversight is only meaningful if the person has enough information, authority, time and skill to act. Studies of marine robot operators show that a shift to human-in-the-loop autonomy can create blame culture and anxiety about responsibility when this is missing.
- **Levels describe tasks, not robots.** The same robot can run autonomously for one task and need close supervision for another. Labelling a whole robot “Level 3” hides more than it reveals.
- **Transitions are where things go wrong.** Mode confusion has been observed among drivers of Level 2 cars on the road, and takeover times vary widely between people and situations. Designing how authority shifts matters more than choosing the level.
- **Level 3 is the prize and the trap.** It is where productivity appears, because the worker can leave the robot and get on with their own tasks. It is also where Bainbridge’s “irony of automation” bites hardest: the less a human is needed, the harder it is to step in well.
- **A robot must know when it doesn’t know.** Robot-gated help requests only work if confidence is trustworthy, and built-in quality indicators can look reliable while hiding severe errors, as our Bluetooth ranging example shows.
- **More autonomy is not automatically better.** In a fan-blade polishing study, letting the robot do everything was fastest but gave workers the lowest sense of autonomy and engagement. With spinal-cord-injured users of an assistive arm, more autonomy reduced effort without raising satisfaction.
- **Intervene at the right level of abstraction.** Taking over which step comes next is much lighter than taking over the motion itself, so humans can supervise long tasks without micromanaging them.
- **Every intervention is also training data.** Corrections concentrate data exactly where a policy fails, so interactive systems can turn supervision into steady improvement.
- **Communication sets the ceiling.** For drones, underwater and remote robots, link quality, rather than the robot’s intelligence, often decides how much control can stay with the human.
- **Explanations should be actionable, not exhaustive.** Operators need to know why the robot stopped and what would let it continue. More transparency can add workload and bury what matters.
- **We are measuring the wrong timescale.** Most user studies last under two hours, too short for skill loss, trust calibration or dependency to appear at all. Long-term deployments are needed to see whether autonomy empowers workers or deskills them.

## What the chapter covers

We use the ladder as the backbone for a tutorial-style overview of human-in-the-loop robotics:

- **Conceptual foundations:** supervisory control, levels of automation, interaction paradigms, and human-in-, on- and out-of-the-loop.
- **System architectures:** human input as feedback, supervisory and mixed-initiative architectures, interfaces, communication constraints, sensing uncertainty and unreliable confidence indicators, and logging.
- **Decision-making and control:** teleoperation (including modern low-cost data collection systems), assisted teleoperation for humanoids and for people with motor impairments, shared control, learning from demonstration, interactive imitation learning with human- and robot-gated interventions, learning from human feedback, and safety layers.
- **Human factors:** workload, situation awareness, trust and its calibration, mode confusion, skill degradation, and human error.
- **Safety and assurance:** hazard analysis, safety modes for collaborative applications, runtime monitoring, and fail-safe versus fail-operational design.
- **Evaluation:** performance and human-centred metrics, autonomy quality metrics such as intervention frequency and help-request quality, and study designs that go beyond single lab sessions.
- **Ethics and regulation:** responsibility and accountability, explainability, fairness and the limits of human oversight, privacy, and standards.

## Application domains

To show how the ladder works in practice, we map several domains onto it:

- **Automated driving**, the reference case, from driver assistance through takeover requests to robotaxis in geofenced areas.
- **Drones, underwater and aerial robots**, where communication limits and observability decide how much control can remain with the human.
- **Industrial robotics**, from collaborative applications and intralogistics fleets to robots that act as force multipliers for workers and the first humanoid pilots in factories.
- **Deformable object manipulation**, with knot untangling as a running example that climbs the ladder from teleoperation to shared control.
- **Caregiving robotics**, where autonomy must be calibrated to the person, not just the task.
- **Robotics for science**, where self-driving laboratories show how autonomy can grow step by step while human expertise stays in control.

The chapter closes with open challenges: scaling human supervision to fleets of robots, the cost and imperfection of human feedback, continual learning with safety guarantees, and adaptive interfaces.

## Thank you

This chapter is the result of a broad collaboration across robotics, control, machine learning, human factors, safety engineering and design research. Many thanks to all co-authors:

Ezio Bartocci, Romana Blazevic, Martim Brandão, Dženita Džafić, Michael Gienger, Amer Kajmaković, Jane Jean Kiam, Jens Kober, Bettina Könighofer, Senka Krivić, Bakir Lačević, Maria Luce Lupetti, Georg Macher, Simon Manschitz, Luka Peternel, Jan Peters, Paolo Rocco, Omar Veledar and Jihong Zhu.

More details and a link to the chapter will follow soon. If you work on human-in-the-loop robotics, we would love to hear how you think about autonomy levels in your own systems, and where our ladder fits or breaks.
