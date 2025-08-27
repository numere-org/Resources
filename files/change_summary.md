# Highlighted changes in this version

## UI changes

- The default UI style has been changed to a more bluish theme. Click on "RESET" for the "UI THEME" within the "Style" tab in the settings dialog to load the new default theme (only if you want to change, of course).
- The default icon for files used within the file tree has been changed to appear more neutral

## New and improved functionalities

- The function `zip()` combines multiple arrays elementwise into embedded clusters in the returned cluster
- The function `getuserinfo()` will return a key-value list containing user information
- The command `mail` can be used to send e-mails via a SMTP server
- The `date()` function will now also accept strings as its "formatting type" parameter
- `getfileparts()` will now return the host as drive for UNC paths, i.e. `"\\MY.SERVER.TDL"`
- String functions, which convert one input into an array, do now return arrays of clusters (one for each input element). Notable candidates: `textparse()`, `to_value()`, `split()` and all character classifier functions like `is_alnum()`
- Functions for base-n encoding `encode_base_n()` and decoding `decode_base_n()` have been added

## Experimental features

- Structures were added: `dictstruct` (a structure/dictionary mixture), `file` (for arbitrary file accesses), `path` (for all type of paths), `queue` (FIFO storage) and `stack` (LIFO storage)
- `readxml()` can import XML files and `readjson()` can import JSON files (both are imported as `dictstruct` instances)
- The command `obj` can be used to declare procedure-local objects and structures (including categories)
- The index operator `VAR[IDX]` can now be used on usual vectors. It also accepts the dimension variable `nlen`

## General changes

- A duration type is now available to increase the date-time logic
- The performance of the new parser implementation was greatly improved and is now at about 70-80% of the previous approach for scalar operations
- Vectorial variables are now supported in `matop`, but not fully compatible to inline created vectors using the brace syntax `{x,y,z,...}`, because they will not be auto-expanded to matrices if necessary. To resolve this, either wrap the vectorial variable into additional braces or enclose it into an explicit `repmat()` call. This is a known issue and will be resolved in a future version together with the complete rework of `matop`.
- Variable method resolution is much more precise now
- It is now possible to use SQL placeholders in SQL statements and supply the parameters via `params=[PARAMLIST]`
- HTML exports of tables will now also parse a simplified markdown syntax, so that headlines, code segments, bold and italic text are possible
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a stable release and builds ontop of the changes from the last release candidate.
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).