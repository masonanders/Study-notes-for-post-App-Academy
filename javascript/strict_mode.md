# JavaScript Strict Mode

JavaScript `strict mode` is a way of setting a more restricted environment for JS to run in. A lot of modern browsers run `strict mode` by default as well as newer ES6 features such as JS classes and exports.

In strict mode errors that would normally pass silently would throw an exception and certain built-in functions such as `eval()` would behave differently or be prohibited completely.

The assignment of global variables is not allowed in `strict mode`.

To enable strict mode for the entire script, simply include `'use strict';` before any other statements. If you wish to enable `strict mode` function by function you may include it within the function at the top before any statements are created. Because of how you cannot mix `strict mode` and non-`strict mode` operations it is recommended that you declare `strict mode` function by function slowly in order to effectively resolve any issues that might be caused by converting your entire script to `strict mode`.