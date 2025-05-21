ESLint currently doesn't make it easy to use existing rules but disable their autofix behaviour.

see:
- https://github.com/eslint/eslint/issues/18696
- https://github.com/eslint/rfcs/pull/134

This can be extremely problematic while using autofix-on-save for certain rules where briefly commenting out a section of code during debugging will trigger a change that becomes an error when code is later uncommented.

Ideally this will be addressed, but in the meantime, this repo will contain forked rules with autofix disabled.


## Rules


#### `prefer-const`

Problematic example:
```js
let someVar = false; // <- will be changed to `const` on save
// if (someCondition) someVar = true
```



