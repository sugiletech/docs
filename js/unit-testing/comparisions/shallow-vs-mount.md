# Shallow vs Mount

||Shallow|Mount
|:---|---|---
|Function|shallow()|mount()
|Event Arguments|Need to pass event args|Need **NOT** pass event args
||`eventArgs.preventDefault()` fails
|Props|Props on the component can't be tested
|Props|`ShallowWrapper.props().propName` returns `undefined`
