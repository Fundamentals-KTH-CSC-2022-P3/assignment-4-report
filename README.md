# Report for assignment 4

This is a template for your report. You are free to modify it as needed.
It is not required to use markdown for your report either, but the report
has to be delivered in a standard, cross-platform format.

## Project

Name:

URL:

One or two sentences describing it

## Onboarding experience

Did you choose a new project or continue on the previous one?

If you changed the project, how did your experience differ from before?

## Effort spent

For each team member, how much time was spent in

1. plenary discussions/meetings;

2. discussions within parts of the group;

3. reading documentation;

4. configuration and setup;

5. analyzing code/output;

6. writing documentation;

7. writing code;

8. running code?

For setting up tools and libraries (step 4), enumerate all dependencies
you took care of and where you spent your time, if that time exceeds
30 minutes.

## Overview of issue(s) and work done.

Title:

URL:

Summary in one or two sentences

Scope (functionality and code affected).

## Requirements for the new feature or requirements affected by functionality being refactored

> Optional (point 3): trace tests to requirements.

The requirements for the feature was specified on a very high level in the
[initial suggestion](https://github.com/google/gson/issues/783#issue-131196793).
To validate JSON against a JSON schema file was the main requirement, and some
suggestions regarding the design of the API and the implementation was made as
well. These were not seen as hard requirements by us - rather, we decided to
only see validation of JSON, in whatever way, as the only hard requirement
stated in this issue.

We could not base these requirements on code reviews or existing test cases,
since this issue is an enhancement, adding completely new functionality to the
project. We had to instead research the requirements based on external sources.

Validation of JSON is quite a complex task.
[https://json-schema.org](https://json-schema.org) has formal specifications of
JSON schemas, as well as more beginner friendly guides. When reading the 
[Getting Started Step-By-Step](https://json-schema.org/learn/getting-started-step-by-step)
guide and looking through the
[2020-12 draft of the JSON Schema Core specification](https://json-schema.org/draft/2020-12/json-schema-core.html)
we soon realized that a complete implementation of the entire specification
would be outside the scope of this assignment. We decided to specify a
subset of the features defined in the specification, and implement this
as a starting point, leaving room for a complete implementation if time allows.
These requirements are as follows:

- The root must contain the property `"$schema"` (but we don't care about the URI)
- The root must contain the property `"$id"` (but we don't care about the URI)
- Every data structure (can be nested) must specifiy the `"type"` property
- We also must support the following properties: 
  - `"title"`  (but we don't care about the content)
  -  `"description"`  (but we don't care about the content)
  - `"properties"` (only applicable if the `type` is `object`)
  -  `"required"` (only applicable if the `type` is `object`)
  - `"items"` (only applicable if the `type` is `array`)
  - `"minItems"` (only applicable if the `type` is `array`)
  - `"uniqueItems"` (only applicable if the `type` is `array`)
  - "`exclusiveMinimum`" (only applicable if the `type` is `number`)
  - "`minimum`" (only applicable if the `type` is `number`)
  - "`maximum`" (only applicable if the `type` is `number`)

## Code changes

### Patch

(copy your changes or the add git command to show them)

git diff ...

Optional (point 4): the patch is clean.

Optional (point 5): considered for acceptance (passes all automated checks).

## Test results

Overall results with link to a copy or excerpt of the logs (before/after
refactoring).

## UML class diagram and its description

### Key changes/classes affected

Optional (point 1): Architectural overview.

Optional (point 2): relation to design pattern(s).

## Overall experience

What are your main take-aways from this project? What did you learn?

How did you grow as a team, using the Essence standard to evaluate yourself?

Optional (point 6): How would you put your work in context with best software engineering practice?

Optional (point 7): Is there something special you want to mention here?