# Style Guide

## Rule of Thumb

- Classes/ReactComponents: CamelCase starting with capital letter.
- Functions/.... : CamelCase starting with small letter.

- Classes/Objects: Noun (Manager/Runner)
- Functions: Verbs (manage/run)
- Arrays Plural

## Variable Name

prefix / name / highContext / lowContext


#### Suggestions

Adapter:
- parse/format

- sanitizer


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



