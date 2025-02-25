---
title: no-control-regex
layout: doc
edit_link: https://github.com/eslint/eslint/edit/main/docs/src/rules/no-control-regex.md
rule_type: problem
---

<!--RECOMMENDED-->

Disallows control characters in regular expressions.

Control characters are special, invisible characters in the ASCII range 0-31. These characters are rarely used in JavaScript strings so a regular expression containing these characters is most likely a mistake.

## Rule Details

This rule disallows control characters in regular expressions.

Examples of **incorrect** code for this rule:

```js
/*eslint no-control-regex: "error"*/

var pattern1 = /\x1f/;
var pattern2 = new RegExp("\x1f");
```

Examples of **correct** code for this rule:

```js
/*eslint no-control-regex: "error"*/

var pattern1 = /\x20/;
var pattern2 = new RegExp("\x20");
```

## When Not To Use It

If you need to use control character pattern matching, then you should turn this rule off.

## Related Rules

* [no-div-regex](no-div-regex)
* [no-regex-spaces](no-regex-spaces)
