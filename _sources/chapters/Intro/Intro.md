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

# Introduction

[**ALADIN**](../ALADIN/ALADIN.md) ([**A**ssessment](Glossary.md#assessment) and so**l**ution(-hint)s gener**a**tor in the fiel**d** of **I**nformatics and adjacent discipli**n**es) is a framework for generating large amounts of [assessments](Glossary.md#assessment), including their solutions and individual solution hints. [**ALADIN**](../ALADIN/ALADIN.md) ships with a set of already included [assessment types](../Assessments/AssessmentTypes.md), but also supports and strongly encourages the extension of new [assessment types](../Assessments/AssessmentTypes.md). [**ALADIN**](../ALADIN/ALADIN.md), although originally being focused on [assessments](Glossary.md#assessment) close to the domain of Computer Science, is domain independent when declaring new [assessment types](../Assessments/AssessmentTypes.md).

## Assessment Declaration

[**ALADIN**](../ALADIN/ALADIN.md) provides a layer of abstraction for the declaration of [assessment](Glossary.md#assessment) generators via a [domain specific language (DSL)](Glossary.md#domain-specific-language-dsl) in a [JSON](Glossary.md#json) format. While [**ALADIN**](../ALADIN/ALADIN.md) can be used as a standalone application to generate new [assessments](Glossary.md#assessment) of a given [assessment type](../Assessments/AssessmentTypes.md), it also provides its own frontend to allow learners to solve the [assessments](Glossary.md#assessment) dynamically, receive solution hints and solutions, as well as record, redirect, replay and resume [(4R-Principle)](Glossary.md#4r-principle) their solution attempts in the corresponding frontend application ([**CARPET**](../CARPET/CARPET.md)). The [instructional design](Glossary.md#instructional-design) of the [assessment type](../Assessments/AssessmentTypes.md) can also be declared via another [JSON](Glossary.md#json)-based [DSL](Glossary.md#domain-specific-language-dsl).

## Authoring Tool

To alleviate the complexity of declaring new [assessment types](../Assessments/AssessmentTypes.md) [**DJINN**](../DJINN/DJINN.md) (**D**eclarative **J**oint Authoring Tool for **I**nstructional Desig**n** Modeling and Assessme**n**t Generators).
