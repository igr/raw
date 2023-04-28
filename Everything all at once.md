# Everything all at once

The development of a feature does not happen at once. The development process depends on the component/team dependencies.

Example. Development dependency on a project may be:

```
Backend <- Frontend <- QA
```

Alas, the development of the feature goes in the _opposite_ order:

```
Backend -> Frontend -> QA
```

Like this:

![](g/value_cycle.png)