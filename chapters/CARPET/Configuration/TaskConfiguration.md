# Task Configuration

Tasks that are modelled in CARPET are defined in a JSON file and is split into three major configuration parts:

- [API](#api),
- [Worker](#worker),
- [UI](#ui).

## API

## Worker

## UI

### currentTask

The `currentTask` parameter is not optional and requires a `string`. It is the display-name of the task.

### taskMode

The `taskMode` parameter is not optional and can be one of the following:

- "practice",
- "strictPractice",
- "exam"

### taskData

`taskData` is automatically set by the system and holds the generated task data in an object.

### rootNode

The rootNode is the root node of the task tree. It is not optional and requires a `number` designating the starting view or node of the task.
