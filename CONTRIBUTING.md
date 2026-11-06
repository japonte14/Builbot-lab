# Contributing to BuildBot Lab

Thank you for your interest in BuildBot Lab.

BuildBot Lab is an early-stage educational robotics project. The project is currently in planning/pre-development, so architecture and implementation details may change.

## Before Contributing

Please read:

1. `README.md`
2. The relevant GitHub Issue
3. Existing discussion on that Issue

Do not implement features that have not been agreed upon in an Issue.

## Development Principles

### 1. Keep the MVP small

The initial goal is not to build a complete robotics platform.

The first objective is to demonstrate a small end-to-end learning experience:

**Configure → Program → Simulate → Observe → Complete a challenge**

### 2. Do not claim unverified functionality

Do not document a feature as working until it has been implemented and verified.

This includes:

- simulation accuracy;
- sensor accuracy;
- Python execution;
- Blockly integration;
- cloud persistence;
- compatibility;
- performance;
- test results.

### 3. Make robotics concepts understandable

The primary audience is secondary-school students.

Code and interfaces should prioritize:

- clarity;
- understandable terminology;
- predictable behavior;
- educational value.

Advanced capabilities should not make the beginner experience unnecessarily complex.

## Proposed Development Workflow

1. Select a GitHub Issue.
2. Discuss uncertainties in the Issue.
3. Create a branch.
4. Make one focused change.
5. Add or update tests when applicable.
6. Update documentation when behavior changes.
7. Open a Pull Request.
8. Reference the associated Issue.

Example branch names:

```text
feature/basic-robot
feature/distance-sensor
feature/scenario-editor
fix/robot-reset
docs/update-readme
```

## Pull Requests

A Pull Request should explain:

### What changed?

Describe the implementation.

### Why?

Explain which requirement or Issue it addresses.

### How was it verified?

List only tests or manual checks that were actually performed.

Example:

```text
Verification:
- [ ] Unit tests added
- [ ] Existing tests pass
- [ ] Tested manually
```

Do not check a box unless the corresponding verification was actually performed.

### Remaining limitations

Explicitly state anything that has not been tested or completed.

## Proposed Technology

The current technology direction includes:

- React
- TypeScript
- Vite
- Konva / react-konva
- Blockly
- Python / Pyodide
- Zustand
- Zod
- IndexedDB
- Supabase
- Vitest
- Playwright

These choices are proposals until they are validated during development.

Do not introduce another major framework or service without discussing it first.

## Testing Expectations

Tests do not currently exist because implementation has not started.

Once development begins, the intended test strategy is:

### Unit tests

Vitest is proposed for:

- differential-drive calculations;
- sensor calculations;
- project validation;
- challenge conditions.

### End-to-end tests

Playwright is proposed for critical user flows such as:

1. create/open project;
2. configure robot;
3. create program;
4. run simulation;
5. complete a challenge;
6. save/reopen the project.

Exact test cases must be created alongside the implementation.

## Security

Do not assume code supplied by a student is safe.

Python execution must eventually consider:

- infinite loops;
- execution time limits;
- memory consumption;
- browser responsiveness;
- exposed APIs;
- error recovery.

Security claims require verification.

## Student Privacy

Do not add unnecessary personal information to user profiles.

Before implementing features involving minors' data, authentication, analytics, public profiles, or project sharing, open an Issue describing the data involved and the reason it is required.

## Documentation

Documentation must distinguish between:

- implemented functionality;
- planned functionality;
- future ideas.

If something has not been verified, say so.

## License

The project's license has not yet been confirmed.

Contributors should not assume a specific open-source license until a LICENSE file is committed.
