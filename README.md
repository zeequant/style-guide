# Style Guide

[NAMING](NAMING.md)

[RULES](RULES.md)

[THESAURUS](THESAURUS.md)

[TESTING](TESTING.md)

[TYPESCRIPT](TYPESCRIPT.md)

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
- File into global common folder if,
  - Methods will be used outside the module.
  - Methods are generic like capitalize/snakeCase
- File into relevant folder/module if,
  - Methods are only specific to that module.

#### File Naming
If you are working on a feature and are extracting helpers. Name the helper depending on what the helper contains. You should not name the helper based on the feature you are working on. If you are working on login and you need a url generator function, do not put it in a file called loginHelper.js

- Name your file / module based on its contents or what it is doing? 
- Do not name every file based on the current story you are doing!


## Self Review Code (Before Merging/Issuing a PR):
- Make your logic clearer, such that the code looks like pseudocode.
- DRY the code. 
- Extract code/functions into appropriate modules.
- Rearrange files if required.
- Rename variables so that they are more meaningful.
- Extract / Inline variables.
