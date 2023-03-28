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

# Assessment

Conceptionally an individual Assessment in ALADIN can be divided into **two** major parts. These parts are:

- Assessment Type and
- Assessment Instruction or Assessment Design.

## Assessment Type

An Assessment Type is a composition of individual [Assessment Generator functions](../ALADIN/ALADIN.md#assessment-generator) in a set configuration. As described in [the previous section](../ALADIN.md#assessment-generator) ALADIN provides a set of already defined functions, but also the ability to provide [custom code](../ALADIN.md#custom-nodes).

```{important}
The definition of an Assessment Type in ALADIN differs from the definition found in learning didactics.
For more information on the didactic sense of Assessment Types, see [here](https://www.niu.edu/citl/resources/guides/instructional-guide/formative-and-summative-assessment.shtml).
```

### Assessment Instance

An Assessment Instance is a concrete instance of an Assessment Type. It is the result of the execution of an Assessment Type by the Assessment Generator. It consists of a set of data relevant to the Assessment itself and a generated solution to the Assessment.
Functions that require user input, such as the initial parametrization, validation functions and hint generators, can be thought of static functions that are tied to the Assessment Type and may require the Assessment Instance as a second argument.

## Assessment Instruction|Design

An Assessment Design