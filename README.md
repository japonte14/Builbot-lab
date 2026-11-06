# BuildBot Lab 🤖

> Learn robotics by building, programming, simulating, and sharing virtual robots.

## Project Status

🚧 **Planning / Pre-development**

BuildBot Lab is currently in the conceptual design phase.

At this time:

- An initial Google Sites page exists with basic project information.
- The simulator has not yet been implemented.
- No functional prototype is available.
- No test results are available.

The features described below represent the proposed MVP and future vision. They should not be interpreted as already implemented.

---

## About BuildBot Lab

BuildBot Lab is an educational robotics project designed to help students understand how robots are built, programmed, and controlled without requiring access to a physical robot.

The primary audience is secondary-school students learning robotics for the first time.

The longer-term vision also includes an advanced learning path for university students, potentially including more complex systems such as industrial robots.

## The Problem

Learning robotics usually requires access to physical hardware, motors, sensors, electronics, workspace, and replacement components.

This may limit opportunities for students who want to experiment with robotics.

BuildBot Lab aims to provide a virtual environment where students can learn robotics concepts before, or alongside, building a physical robot.

## Proposed Learning Experience

The intended learning flow is:

1. Open BuildBot Lab.
2. Start with a predefined robot.
3. Configure basic characteristics of the robot.
4. Program the robot using visual blocks or Python.
5. Run the robot in a 2D simulation.
6. Read data from a virtual frontal distance sensor.
7. Navigate around obstacles.
8. Attempt a predefined challenge or design a simple scenario.
9. Save the project.
10. Share the project so another student can continue working on it.

## Proposed MVP

The first MVP is intentionally limited.

### Robot

A predefined differential-drive robot with:

- two driven wheels;
- configurable wheel diameter;
- configurable distance between the wheels;
- one frontal distance sensor.

### 2D Simulation

The proposed simulator should display:

- the robot;
- the starting position;
- a goal;
- obstacles;
- robot position and orientation.

The first version will focus on differential-drive kinematics rather than advanced physical simulation.

### Programming

Two programming modes are planned.

#### Visual programming

A block-based interface intended primarily for beginners.

The initial block set should cover:

- move;
- turn;
- stop;
- frontal distance;
- condition;
- repetition.

#### Python

Python will be the primary text-based programming language.

The exact student-facing API has not yet been finalized.

Example concept only:

```python
if robot.distance_front() < 20:
    robot.stop()
```

> The API above is illustrative and has not been implemented.

### Distance Sensor

The MVP will initially contain one frontal distance sensor.

Its exact:

- range;
- field of view;
- accuracy;
- units;
- simulation behavior;

still need to be defined.

### Challenges

The MVP is intended to support:

- predefined challenges;
- simple student-created scenarios;
- obstacles;
- start position;
- goal position.

The exact challenge-completion rules have not yet been defined.

## Projects and Collaboration

BuildBot Lab should be usable without creating an account.

A guest should eventually be able to:

- create and run projects;
- save work locally;
- export a project;
- import a project.

Registration will be introduced for cloud persistence and sharing.

For the MVP, collaboration is intended to be asynchronous rather than simultaneous.

A proposed flow is:

1. Student A creates a project.
2. Student A shares the project.
3. Student B opens it.
4. Student B creates a copy.
5. Student B modifies their copy.

Real-time collaborative editing is outside the initial MVP.

## Proposed Technology Stack

> ⚠️ These technologies are proposed and have not yet been implemented or validated for the project.

### Frontend
- React
- TypeScript
- Vite

### 2D simulation
- Konva / react-konva
- Custom differential-drive kinematics

### Programming
- Blockly for visual programming
- Python
- Pyodide running in a Web Worker

### State and project data
- Zustand
- Zod
- IndexedDB
- Versioned JSON project format

### Cloud
- Supabase is the current proposed option for:
  - authentication;
  - PostgreSQL database;
  - cloud project storage.

### Testing
- Vitest
- Playwright

### Collaboration and development
- Git
- GitHub
- GitHub Issues
- Pull Requests
- GitHub Actions

All of these technology choices must be validated during implementation.

## Development Roadmap

### Phase 1: Basic robot simulation
- [ ] Create application skeleton
- [ ] Display a predefined differential-drive robot
- [ ] Implement 2D coordinate system
- [ ] Implement basic differential-drive kinematics
- [ ] Add start and goal positions
- [ ] Add a basic obstacle
- [ ] Reset and run simulation

### Phase 2: Sensor and challenges
- [ ] Implement frontal distance sensor
- [ ] Implement obstacle detection
- [ ] Define challenge completion
- [ ] Create first predefined challenge

### Phase 3: Programming
- [ ] Define robot command API
- [ ] Integrate Blockly
- [ ] Integrate Python
- [ ] Evaluate Pyodide execution isolation
- [ ] Add execution limits and error handling

### Phase 4: Project creation
- [ ] Configure robot parameters
- [ ] Create scenario editor
- [ ] Export project as JSON
- [ ] Import project from JSON
- [ ] Save projects locally

### Phase 5: Accounts and cloud
- [ ] Evaluate and configure authentication
- [ ] Save projects in the cloud
- [ ] Create project dashboard
- [ ] Implement private-by-default projects
- [ ] Implement read-only sharing
- [ ] Allow users to duplicate shared projects

## Future Vision

The following ideas are explicitly outside the initial MVP:

- converting a robot photograph into a digital model;
- 3D simulation;
- industrial robot simulation;
- additional sensor types;
- advanced physics;
- real-time collaboration;
- automatic bill of materials;
- physical robot construction instructions;
- advanced university learning mode.

These are ideas for future exploration, not current capabilities.

## Safety, Privacy, and Student Data

BuildBot Lab is intended to serve secondary-school students.

Before public account registration is introduced, the project must review:

- privacy requirements;
- processing of minors' data;
- applicable age requirements;
- parental or guardian consent where applicable;
- account and data deletion;
- storage location;
- data minimization;
- project-sharing defaults.

No implementation should assume these questions have already been resolved.

## Contributing

BuildBot Lab is at an early stage.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) before proposing implementation changes.

## License

⚠️ **To be decided.**

A license has not yet been confirmed for the project. Do not assume that MIT or any other open-source license applies until a LICENSE file is added to the repository.
