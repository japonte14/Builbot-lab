# Implement basic differential-drive robot kinematics

## Summary

Create the first independently testable model for the BuildBot Lab robot.

The model should calculate the robot's 2D position and orientation from the movement of its left and right wheels.

This Issue does **not** require a user interface, Python, Blockly, authentication, cloud storage, or a distance sensor.

## Why

Differential-drive movement is a foundational component of the proposed BuildBot Lab MVP.

Keeping this Issue independent from the UI will allow the mathematical behavior to be tested before building the visual simulator.

## Scope

Create a minimal robot state containing:

- X position
- Y position
- orientation
- wheel diameter or wheel radius
- distance between wheels

Provide a function that updates the robot state using left-wheel and right-wheel movement.

## Minimum behaviors

The implementation should support at least:

### Both wheels move the same distance

Expected conceptual behavior:

```text
left = right
→ robot moves straight
