# Minwoo CHOI

Mechanical Engineering student at Seoul National University  
Minor in Philosophy

I like engineering problems that do not fit neatly inside one discipline. A system may work in a model and still fail because of its geometry, weight, wiring, sensor placement, control timing, or the way people have to use it.

Across robotics, assistive devices, and data systems, I have worked on turning those constraints into things that can be designed, built, and tested. My experience includes mechanical design, sensing, control, software, and early product development. I am still exploring where I can contribute most as an engineer.

## Selected work

### Surgeon Logger for laparoscopic surgery

**MediSC Lab, Seoul National University Hospital | 2025–2026**

General laparoscopic instruments are difficult to study from video alone. A tool can disappear behind tissue, while an IMU can estimate orientation but accumulates error when used to infer position. We needed a way to record instrument behavior and related signals in a form that could later support research on surgical systems.

I worked on the data-collection system and its mechanical design, bringing together camera, IMU, and force sensing, with phase-based UWB investigated as a possible source of position information. For use around surgical instruments, the design had to account for size, wireless operation, balance in the hand, and the separation of sterilizable parts from electronics. I helped translate those use constraints into design requirements and coordinate the industrial-design handoff to an external development partner.

I also worked on turning the recordings into usable episodes. Video, pose, and force signals had different sampling rates and start times, so combining them directly could pair an observation with the wrong action. I aligned the streams on a common timeline, interpolated pose and force data, and excluded damaged files. The resulting dataset contained 565 episodes and was used in subsequent policy research and robot rollouts.

This work taught me that a data system starts with physical choices: where a sensor can fit, what it can observe, and whether its measurements can be related to the instrument’s motion.

### Bimanual surgical-assistant robot

**MediSC Lab, Seoul National University Hospital | 2025–2026**

A surgical-assistant robot has to move instruments within a constrained workspace around an insertion point. The challenge was not simply commanding two arms to move. Their motion, the instrument geometry, the control mode, and the timing of the control loop all affected whether a movement was useful.

I worked on a four-degree-of-freedom remote-center-of-motion setup and on control and integration for a bimanual prototype. In a separate FR3 control effort, I worked on two-arm operation, input devices, trocar-frame capture, and gripper and cutter actuation. When the Cartesian-velocity approach proved limiting for the required posture behavior, joint-velocity control became the default while the earlier mode was retained. I also addressed real-time control-thread synchronization and supported hardware work for robot rollout.

The project made clear to me that a control command is only one part of the engineering problem. The robot has to move within its mechanical and workspace constraints, and the system needs a way to recover when an assumption or command does not hold.

### Jumping robot for uneven terrain

**SNU Bio-Robotics Lab | 2025**

A wheel-based robot can travel efficiently on flat ground, but uneven terrain may require jumping over obstacles. After a jump, an unstable landing can delay the next movement. We explored whether the robot could correct its attitude while airborne without giving up its wheel-based mobility.

I built a feedback-control approach using IMU measurements and a Kalman filter to estimate attitude, then used reaction torque from the wheels to correct the robot during flight. Adding an onboard computer increased the robot’s mass and raised its center of gravity, so I also modified the PCB shape and body structure to reduce weight. I assembled and tested the robot, then iterated between its physical configuration and control behavior.

The work connected estimation, dynamics, control, and packaging in a real prototype. It also showed me how a software solution can be limited by a mechanical change such as added mass or a shifted center of gravity.

### Universeat: pressure-injury prevention seat

**SNU Creative Design Fair and KDB Startup Competition | 2025–2026**

We set out to build a seat that could help reduce prolonged pressure on the same areas of the body. Our first mechanism rotated a central support, but the user’s weight placed high torque demands on the drive and created a risk of back-driving. Reinforcing parts would not address the underlying load path, so I helped redesign the support around linear motion and a worm-gear drive.

I led technical development across the mechanism, sensing, data processing, and app. To keep the sensing system affordable, we used 32 IMUs distributed through the seat to capture patterns of cushion deformation and tilt, rather than relying on a dense array of pressure sensors. I built the sensor and firmware workflow, collected repeated sitting data, trained a model to distinguish posture patterns, and connected the results to a Flutter app that displayed posture history and areas of pressure-concentration risk. I also compared cushion-channel geometries with CFD.

The project received fifth place among 61 teams at the SNU Creative Design Fair and the chairperson’s award at the KDB startup competition. More valuable to me than the awards was seeing how a change in mechanism, sensor choice, and user interface each shaped what the product could actually do.

### Autonomous crawling robot

**Mechanical Engineering capstone project**

We built a robot that had to crawl over obstacles, navigate autonomously, and launch a ball. I worked across the mechanism, motor actuation, and navigation logic, including a simple ray-tracing-based path-recognition approach.

The first build did not move as expected because friction and drive losses were larger than we had accounted for. I had spent substantial effort on the software, but the physical structure was preventing the robot from delivering the motion the software assumed. That experience changed how I approach integrated systems: before adding complexity to control, check whether the mechanism can produce the required movement in the first place.

## Product and team work

### Rosota Inc.

**Co-founder and COO | 2026**

Rosota grew out of a Seoul National University Hospital research team and worked on data infrastructure for Physical AI in conventional laparoscopic surgery. As a co-founder, I helped shape the company’s product direction and operating strategy, coordinated work across a ten-person team, and co-led a KRW 1.5 billion seed-fundraising effort.

One decision was where to focus limited people and time: on near-term product validation, or on a broader research program involving papers and foundational technology. I worked with the team to clarify what the product needed to validate next and which research efforts directly strengthened that product. This was a different kind of engineering work, but it relied on the same habit: make assumptions and constraints explicit, then turn them into a decision the team can act on.

## How I work

I start by asking what has to be true for a system to work in its actual setting. Then I try to make those conditions concrete: a load path, a measurable signal, a workspace boundary, a timing requirement, or a user constraint. I build or integrate enough of the system to test those assumptions, and use what fails to decide what to change next.

My projects have taken me through mechanical structures, embedded sensing, robot control, data pipelines, and product decisions. I am interested in roles where engineers have to work across those boundaries and carry a problem from an early design through prototype testing and improvement.

## Tools and methods

C++, Python, MATLAB, Arduino, ROS, Unity C#, Fusion 360

Mechanical design and prototyping  
Robot sensing, estimation, and control  
System integration and experimental data workflows

## Other interests

I study philosophy alongside engineering, with a particular interest in ethics and social philosophy. I also swim.
