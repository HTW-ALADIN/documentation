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

# CARPET

CARPET (Graphi**c**al **A**ssessment Inte**rp**retation **E**ngine and Solution Attempt **T**racker) is a framework to support technology-enhanced items (TEI), with specialized interactions for collecting response data. These include interactions and responses beyond traditional selected-response or constructed-response, which are usually implemented according to the [QTI standard](https://www.1edtech.org/standards/qti/index#QTI3).
QTI is restrictive in terms of the types of interactions that can be implemented, and it is not always easy to implement custom interactions. CARPET is designed to be more flexible and to support a wider range of interactions.
The flexibility comes at the cost of not being able to directly use QTI-compliant authoring tools. However, CARPET has its own (relatively) lightweight domain specific language (DSL) for defining assessments. An overview can be found ([here](./SerialisedTaskSchema.md)).
An overview of available items is given in the [carpet-component-library](https://htw-aladin.github.io/LOOM/?path=/docs/introduction--docs).
