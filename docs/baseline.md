# Project Baseline

## Purpose

This document records the behavior of the application before
development changes are introduced.

The baseline is used to identify existing functionality,
limitations, and defects.

## Current Functionality

The application currently provides:

- Add Task
- Remove Task
- List Tasks
- Quit

## Manual Test Results

| Scenario | Result | Observed Behavior |
|---|---|---|
| Start application | PASS | Application starts and displays the menu |
| List when empty | PASS | Displays "No tasks to list." |
| Add single-word task | PASS | Task is added successfully |
| Add multi-word task | FAIL | Multi-word task handling is incorrect |
| Continue after adding | PASS | Application continues normally |
| Invalid menu input `abc` | FAIL | `InputMismatchException` is thrown |
| Invalid menu option `99` | PASS | Displays "Invalid option. Please try again." |
| Negative menu option `-1` | PASS | Displays "Invalid option. Please try again." |
| Quit | PASS | Application exits normally |
| Remove task | PASS | Task can be removed successfully |

## Known Issues

### 1. Multi-word task handling

Multi-word task input does not behave as expected.

This requires further investigation and will be addressed
through a separate development task.

### 2. Non-numeric menu input

Entering non-numeric input such as `abc` causes an
`InputMismatchException`.

The application should handle invalid input without
terminating unexpectedly.

## Baseline Status

The application is functional for its basic happy-path
operations, but input validation and error handling require
improvement.