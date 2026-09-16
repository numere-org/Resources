# Highlighted changes in this version

## UI changes

- 3D matrices will now show their layers next to each other if inspected using the dataviewer.
- The code analyzer now understands better, what a wrapped line is and will examine the whole (logical) line at once and due to the highly flexible argument list of drawing functions, those are not checked by the code analyzer any more. Also, it won't mark methods that have no required arguments as lacking their parentheses if the user's intent is to stick with the default arguments.
- The new code parser will handle more constants and heuristics won't get overwritten by generic types like `"any"` any longer.

## New and improved functionalities

- Functions for bit-level logic and manipulation haven been added: `bitand()`, `bitor()`, `bitxor()`, `bitnot()`, `bitshift()`, `bitmask()` and `bitcast()`
- It is now possible to enforce an HTTP method in `url` by prefixing the URL in the command with the desired method. The return value of `url` is now always `STR`, even if the contents are byte counts, to make some special cases more robust.
- TLS and SSL certificates are now validated against a set of known trusted root CAs within `url` and `mail`. There is an option to supply an own certificate or to bypass the check completely.
- The table method `TAB().convert()` will now also try to convert to a categorical column, if the second argument is set to `"auto"`.
- Tables do now also correctly handle the `"duration"` data type.
- An option for a password entry dialog and for setting the `textfield` to password-mode has been added for both via the option `type=pwdentry`
- It is now possible to control the custom window resizing (`fixedsize`) and whether boxes for iconizing (`hideiconize`) and closing (`hideclose`) should appear.
- It is now possible to set the opening position of custom windows with `pos={x,y}` as well as fix the window to the uppermost z position `stayontop`.
- Improved the return of `fwt`, especially the enumeration of the coefficients.
- A logger object is now available and can be constructed using the function `logger()`.
- Dict objects can be used to map between two arbitrary types (requiring that the key type to supports a "less-than" relation). Those objects are constructed using the function `dict()`.
- The path object now has the two methods `PATH.twig` for getting the parent entry of the leaf and `PATH.leafless` for returning a new path without the current leaf.
- The function `tensorprod()` provides a n-dimensional tensorproduct and also contracts, if necessary. The function `trace()` was extended to support n-dimensional contraction as well.

## Experimental features

- `void` can be assigned to object variables to convert them to an `"object.void"` instance.

## General changes

- The package repository is now located in GitHub simplyfing the contribution process. It is possible to have secondary package repositories (even private ones), if they provide a similar REST API as GitHub or Gitlab. Look at the description of the [NumeRe::Packages](https://github.com/numere-org/NumeRe-Packages) repository for further insights.
- Tables do now favor `"value.f64"` over the previous behavior of converting to `"value.cf64"`. This will save a lot of space in many cases.
- The internal memory consumption of single values was reduced.
- There are now valid variable prefixes for logical values. Accepted are `l`, `b`, `is`, `do`, `has`. Examples `lSOMETHING bSOMETHING isSOMETHING doSOMETHING hasSOMETHING`
- All occurences of regular expressions have been updated to be more runtime-efficient.
- Curvilinear coordinates do now work more consistent across the plotting types.
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a stable release and builds ontop of the changes from the last release candidate.
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).
- If your browser refuses to download or execute the binary, just *f-ing* use Firefox or `winget`.