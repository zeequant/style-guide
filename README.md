# Style Guide

## Rule of Thumb


- Top Level code files should clean/smaller. Bottom level files(in the call hierarchy), can be bigger.
- Modules should be cohesive and decoupled
- Consistent Return Type
- Consistent parameter types
- Non-Conflicting Variable names
- Non-Generic Variable names
- Layered Approach
- While implementing new feature, if the requirements for which the old code was writted has changed, then that old code should be changed as part of the current implementation. We should, work around patching things with old code which is no longer relevant.

## Variable Name
- Classes/ReactComponents: CamelCase starting with capital letter.
- Functions/.... : CamelCase starting with small letter.
- Classes/Objects: Noun (Manager/Runner)
- Functions: Verbs (manage/run)

prefix / name / highContext / lowContext

#### Suggestions

- adapter
- parse/format
- featureFlag
- sanitizer
- 

#### Arrays:
- persons
- personList
- personGroup

```JS
const persons = [new Person()];
```

#### Array of Arrays:
- personLists
- personGroups

#### Boolean:
- isVisible
- shouldShow
- hasEdited

## Other

#### Prefer chaining


#### Prefer explicit methods

```JS
_.zip(names, ids, (nameId) => {
  const [name, id] = nameId;
});
```
