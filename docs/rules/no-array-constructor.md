---
title: ESLint
layout: doc
---
<!-- Note: No pull requests accepted for this file. See README.md in the root directory for details. -->
# Disallow creation of dense arrays using the `Array` constructor (no-array-constructor)

Use of the `Array` constructor to construct a new array is generally
discouraged in favour of array literal notation because of the single-argument
pitfall and because the `Array` global may be redefined. The exception is when
the Array constructor is used to intentionally create sparse arrays of a
specified size by giving the constructor a single numeric argument.

## Rule Details

The following patterns are considered warnings:

```js
Array(0, 1, 2)
```

```js
new Array(0, 1, 2)
```

The following patterns are not warnings:

```js
Array(500)
```

```js
new Array(someOtherArray.length)
```

## When Not To Use It

This rule enforces a nearly universal stylistic concern. That being said, this
rule may be disabled if the constructor style is preferred.

## Related Rules

* [no-new-object](no-new-object.html)
* [no-new-wrappers](no-new-wrappers.html)

## Version

This rule was introduced in ESLint 0.4.0.

## Resources

* [Rule source](https://github.com/eslint/eslint/tree/master/lib/rules/no-array-constructor.js)
* [Documentation source](https://github.com/eslint/eslint/tree/master/docs/rules/no-array-constructor.md)
