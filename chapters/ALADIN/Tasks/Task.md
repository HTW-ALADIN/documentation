---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: "0.8"
    jupytext_version: "1.4.1"

kernelspec:
  display_name: Python 3
  name: python3
---

# Task

Conceptionally a Task in ALADIN can be thought of as one half of an Assessment. The second half is the Assessment Instruction or Design.

## Task Type

A Task Type is a composition of individual [Task Data Generator functions](../ALADIN.md#task-data-generator) in a set configuration. As described in [the previous section](../ALADIN.md#task-data-generator) ALADIN provides a set of already defined functions, but also the ability to provide [custom code](../ALADIN.md#custom-nodes).

```{important}
The definition of an Task Type in ALADIN should not be confused with the definition of Assessment Types found in learning didactics.
For more information on the didactic sense of Assessment Types, see [here](https://www.niu.edu/citl/resources/guides/instructional-guide/formative-and-summative-assessment.shtml).
```

### Task Instance

An Task Instance is a concrete instance of an Task Type. It is the result of the execution of an Task Type by the Task Data Generator. It consists of a set of data relevant to the Task itself and a generated solution to the Task.
Functions that require user input, such as the initial parametrization, validation functions and hint generators, can be thought of static functions that are tied to the Task Type and may require the Task Instance as a second argument.
