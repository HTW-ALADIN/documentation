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

# Preface

[**ALADIN**](./ALADIN/ALADIN.md) ([**A**ssessment](./Intro/Glossary.md#assessment) and so**l**ution(-hint)s gener**a**tor in the fiel**d** of **I**nformatics and adjacent discipli**n**es) is a framework for generating large amounts of [assessments](./Intro/Glossary.md), including their solutions and individual solution hints. [**ALADIN**](./ALADIN/ALADIN.md) ships with a set of already included [assessment types](./Assessments/AssessmentTypes.md), but also supports and strongly encourages the extension of new [assessment types](./Assessments/AssessmentTypes.md). [**ALADIN**](./ALADIN/ALADIN.md), although originally being focused on [assessments](./Intro/Glossary.md#assessment) close to the domain of Computer Science, is domain independent when declaring new [assessment types](./Assessments/AssessmentTypes.md).

## Assessment Declaration

[**ALADIN**](./ALADIN/ALADIN.md) provides a layer of abstraction for the declaration of [assessment](./Intro/Glossary.md#assessment) generators via a [domain specific language (DSL)](./Intro/Glossary.md#domain-specific-language-dsl) in a [JSON](./Intro/Glossary.md#json) format. While [**ALADIN**](./ALADIN/ALADIN.md) can be used as a standalone application to generate new [assessments](./Intro/Glossary.md#assessment) of a given [assessment type](./Assessments/AssessmentTypes.md), it also provides its own frontend to allow learners to solve the [assessments](./Intro/Glossary.md#assessment) dynamically, receive solution hints and solutions, as well as record, redirect, replay and resume [(4R-Principle)](./Intro/Glossary.md#4r-principle) their solution attempts in the corresponding frontend application ([**CARPET**](./CARPET/CARPET.md)). The [instructional design](./Intro/Glossary.md#instructional-design) of the [assessment type](./Assessments/AssessmentTypes.md) can also be declared via another [JSON](./Intro/Glossary.md#json)-based [DSL](./Intro/Glossary.md#domain-specific-language-dsl).

## Authoring Tool

To alleviate the complexity of declaring new [assessment types](./Assessments/AssessmentTypes.md) [**DJINN**](./DJINN/DJINN.md) (**D**eclarative **J**oint Authoring Tool for **I**nstructional Desig**n** Modeling and Assessme**n**t Generators).
