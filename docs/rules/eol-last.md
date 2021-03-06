---
title: ESLint
layout: doc
---
<!-- Note: No pull requests accepted for this file. See README.md in the root directory for details. -->
# Require file to end with single newline (eol-last)

Trailing newlines in non-empty files are a common UNIX idiom. Benefits of
trailing newlines include the ability to concatenate or append to files as well
as output files to the terminal without interfering with shell prompts. This
rule enforces newlines for all non-empty programs and disallows trailing
empty or whitespace-only lines.

## Rule Details

The following patterns are considered warnings:

<pre>
function doSmth() {
  ...
}
</pre>

<pre>
function doSmth() {
  ...
}



</pre>

<pre>
function doSmth() {
  ...
}
// spaces here
</pre>

The following patterns are not warnings:

<pre>
function doSmth() {
  ...
}

</pre>

## Version

This rule was introduced in ESLint 0.7.1.

## Resources

* [Rule source](https://github.com/eslint/eslint/tree/master/lib/rules/eol-last.js)
* [Documentation source](https://github.com/eslint/eslint/tree/master/docs/rules/eol-last.md)
