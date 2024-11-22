# Style Guide

[NAMING](NAMING.md)
[RULES](RULES.md)
[THESAURUS](THESAURUS.md)

## Rule of Thumb
- Use already decided terminology for the project.
- Modules should be cohesive and decoupled
- Consistent Return Type
- Consistent parameter types
- Non-Conflicting Variable names: (If the current project has ‘preference’ as a feature, Do not use it in variable names to denote anything else.)
- Non-Generic Variable names
- Layered Approach: (Example: Quantman FeatureFlags)
- Leave Code in a better State
- Refactoring old code is part of new implementation: (While implementing new feature, if the requirements for which the old code was writted has changed, then that old code should be changed as part of the current implementation. We should, work around patching things with old code which is no longer relevant.)

## File Structuring/Organising
- Top Level code files should clean/smaller. Bottom level files(in the call hierarchy), can be bigger.

- If you are working on a feature and are extracting helpers. Name the helper depending on what the helper contains. You should not name the helper based on the feature you are working on. If you are working on login and you need a url generator function, do not put it in a file called loginHelper.js

- If the utility is very common and will be required in other places, put it outside in common folder. Otherwises keep the helper within the component or module itself. 
