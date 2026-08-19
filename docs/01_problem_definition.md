# Problem Definition

## 1. Problem Statement

Robotic manipulation for surgical and other delicate applications requires precise motion, controlled grasping, and reliable interaction with physical objects. Unlike conventional industrial manipulation, where relatively rigid objects can often tolerate substantial gripping forces, delicate manipulation requires the end-effector to maintain a stable grasp while minimizing unnecessary interaction forces.

The core problem addressed by this project is the development of a **modular robotic gripper and manipulation system capable of controlled, repeatable grasping and interaction with delicate objects**, while providing a foundation for future integration of force sensing, visual perception, and intelligent control.

The immediate goal is not to develop a clinically deployable surgical instrument. The project is focused on developing and experimentally validating a laboratory-scale robotic manipulation platform that can serve as a foundation for future research in surgical robotics.

---

## 2. Background and Context

The robotic end-effector is a critical component of any manipulation system because it directly interacts with the target object. Its mechanical configuration, actuation mechanism, sensing capability, and control strategy strongly influence the quality and reliability of manipulation.

For delicate manipulation, an effective gripper should provide:

* stable and repeatable grasping;
* controlled finger motion;
* appropriate mechanical compliance or adaptability;
* compatibility with the robotic manipulator;
* provision for contact or force sensing;
* compatibility with visual perception; and
* a modular architecture that can be extended as the system develops.

The project investigates these requirements using the available robotic platform, embedded control hardware, candidate gripper designs, and supporting technical documentation.

The available **Svaya robotic platform** provides the basis for robotic manipulation experiments. Its API documentation, manuals, and application documentation will be used to establish the interface between the robotic arm and the proposed end-effector.

---

## 3. Current Starting Point

The project begins from an existing technical foundation rather than developing every component from scratch.

A literature survey of robotic grippers has been conducted to understand existing approaches, including underactuated and multi-finger gripper mechanisms.

The **ALARIS open-source three-finger underactuated gripper** has been identified as an initial mechanical reference. Its architecture is of particular interest because it provides:

* a three-finger grasping configuration;
* underactuated finger motion;
* servo-based actuation;
* a relatively compact mechanical design;
* 3D-printable components; and
* potential for integration with force/contact sensing.

ALARIS is therefore being treated as a **reference architecture and starting point**, not as the final solution. Its suitability for the intended manipulation tasks must be evaluated experimentally, and modifications may be required.

Embedded controllers such as **ESP32/ESP8266** provide a potential low-level interface for servo control, sensor acquisition, communication, and experimental data collection.

At the current stage, force sensing, camera-based perception, and AI/ML-based manipulation are **planned development directions rather than completed capabilities**.

---

## 4. Engineering Gap

Existing gripper designs provide solutions to specific grasping problems, but a complete manipulation system requires integration across several levels:

**mechanical grasping → actuation → robotic control → sensing → perception → feedback → intelligent manipulation**

The main engineering gap addressed by this project is therefore the transition from a mechanically actuated gripper to an **integrated and experimentally validated manipulation platform**.

The system must establish reliable basic grasping first and then provide a pathway toward:

* contact and force-aware manipulation;
* camera-assisted object interaction;
* closed-loop control;
* adaptive grasping; and
* intelligent task-level manipulation.

The project will consequently follow a staged development strategy rather than attempting to implement all capabilities simultaneously.

---

## 5. Project Objective

### Primary Objective

> **To design, integrate, and experimentally evaluate a modular robotic gripper and manipulation system capable of controlled and repeatable grasping, with an architecture that supports future force sensing, visual perception, and intelligent manipulation.**

### Supporting Objectives

1. Evaluate existing robotic gripper architectures and identify suitable design principles.
2. Study the ALARIS three-finger underactuated gripper as an initial reference architecture.
3. Determine the suitability of the selected gripper configuration for the intended manipulation tasks.
4. Modify or redesign the gripper where necessary.
5. Develop reliable servo-based actuation and embedded control.
6. Integrate the gripper with the available robotic platform.
7. Establish reliable communication between the robot, embedded controller, and gripper.
8. Investigate the integration of contact/force sensing.
9. Investigate camera-based object perception.
10. Develop repeatable grasping and manipulation experiments.
11. Quantitatively evaluate system performance and failure modes.
12. Establish a modular foundation for future intelligent manipulation research.

---

## 6. Scope

The project is intended to progress through the following major stages:

### Mechanical Development

* study existing gripper mechanisms;
* select an appropriate architecture;
* evaluate or modify the ALARIS design;
* develop CAD models;
* fabricate and assemble the prototype; and
* validate basic mechanical operation.

### Actuation and Control

* implement servo-based finger actuation;
* establish embedded control;
* control opening and closing;
* test repeatability; and
* establish communication with the higher-level system.

### Robotic Integration

* develop the mechanical mounting interface;
* integrate the gripper with the Svaya robotic platform;
* coordinate arm and gripper operation; and
* perform basic robotic manipulation experiments.

### Sensing and Perception

Subject to successful validation of the basic system:

* investigate force/contact sensing;
* acquire and analyse sensor data;
* integrate camera-based perception;
* detect and localize experimental objects; and
* use sensory information for manipulation feedback.

### Intelligent Manipulation

As a later development stage, the system may incorporate:

* adaptive grasping;
* grasp verification;
* force-aware control;
* object-specific manipulation strategies;
* visual feedback;
* gesture-based interaction; and
* AI/ML-based decision-making where experimentally justified.

---

## 7. Key Constraints

The development is subject to the following constraints:

* compatibility with the available Svaya robotic platform;
* available gripper hardware and CAD resources;
* available servo motors and embedded controllers;
* fabrication and laboratory resources;
* available CAD/manufacturing tools;
* robotic payload and workspace limitations;
* project development time;
* limited availability of sensing hardware; and
* the need to validate each subsystem before integrating higher-level functionality.

The system must therefore be developed incrementally, with mechanical and control reliability established before introducing sensing, perception, and intelligent algorithms.

---

## 8. Expected Outcome

The expected outcome is a **functional laboratory-scale robotic manipulation prototype** consisting of:

* a mechanically validated multi-finger gripper;
* controlled servo-based actuation;
* embedded control;
* integration with the available robotic platform;
* repeatable grasping and manipulation;
* provisions for contact/force sensing;
* provisions for camera-based perception; and
* an experimental framework for future closed-loop and intelligent manipulation.

The resulting platform should allow the performance of the gripper and manipulation system to be evaluated using measurable experimental criteria rather than qualitative demonstration alone.

---

## 9. Intended Application Direction

The project is motivated by potential applications in **robotic surgery and delicate robotic manipulation**, including future research involving robotic dentistry, ophthalmic manipulation, and other precision tasks.

However, the current prototype is intended strictly as a **research and laboratory platform**.

The project does not claim clinical suitability or readiness for surgical deployment. Any future surgical application would require additional work involving mechanical safety, force limits, materials, sterilization, reliability, fault handling, regulatory requirements, and extensive experimental and clinical validation.

---

## 10. Out of Scope

The following are outside the scope of the current project:

* human surgical testing;
* animal surgical testing;
* clinical deployment;
* autonomous surgery;
* medical-device certification;
* clinical safety certification;
* sterilization validation;
* regulatory approval; and
* claims of clinical efficacy.

AI/ML implementation is also not considered mandatory for the initial prototype. It will be introduced only after sufficient mechanical, control, sensing, and experimental foundations have been established.

---

## 11. Problem Definition Summary

The project addresses the following engineering problem:

> **Develop a modular robotic gripper system that can reliably grasp and manipulate defined objects using controlled actuation and robotic motion, while establishing the hardware and software foundation required for future force-aware, vision-assisted, and intelligent manipulation.**

The development strategy is therefore:

```text
Existing Gripper Research
          ↓
Gripper Architecture Selection
          ↓
Mechanical Development
          ↓
Actuation & Embedded Control
          ↓
Robot–Gripper Integration
          ↓
Reliable Basic Manipulation
          ↓
Force / Contact Sensing
          ↓
Visual Perception
          ↓
Closed-Loop Control
          ↓
Intelligent Manipulation
```

The fundamental principle of the project is:

> **Establish reliable mechanical manipulation first; introduce sensing and feedback next; develop intelligence only after the underlying system is experimentally validated.**
