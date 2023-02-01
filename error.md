React Errors : Super expression must either be null or a function

`
Uncaught TypeError: Super expression must either be null or a function, not undefined
`

1、Forgotten export
---
The first culprit is usually that you have forgotten to export the component that you are trying to use and hence React finds that the Component you are trying to extend from is undefined . This is an easy to find and fix issue.

2、Using a default export incorrectly
---
If a component is exported with the default keyword then it must be imported as a default import and not as a named import.
For example if your export statement is export default Foo, then the correct way to import this component is import Foo from "./Foo" and not import { Foo } from "./Foo" . The latter import statement is for named exports.

3、Circular Dependencies
---
This is a an often missed culprit which I came across recently in one of the projects I was working on. After going into the depths of the google search rabbit hole, I finally came across a stack overflow answer that shed some light on why I was still getting the error inspite of the component being exported / imported correctly.
If you have dependencies of a cyclic nature like shown below, it will result in this error:
```javascript
class A extends B {}
class B extends C {}
class C extends A {}
```
