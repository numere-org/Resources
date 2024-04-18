# Highlighted changes in this version

## UI changes

- Added feature of autowrapping for comments if line indicator is active.
- Using the new file dialog and selecting "App", one can create a custom app from some predefined templates
- The terminal rendering speed was increased, it provides global variables for autocompletion, autocompletion was improved generally
- The table viewer will now group common table header rows together, creating a virtual hierarchy. Strings are also automatically wrapped around and the grid lines can be hidden
- Folding has been enabled for LaTeX files and a simple lexer for INI files was added

## New and improved functionalities

- `getfilelist()` and `getfolderlist()` may now follow shell links (*.LNK files)
- `getuilang()` returns the user's current language, `getfilediff()` returns the unified diff of two files, the functions `to_utf8()` and `to_ansi()` can be used to convert to and from UTF-8 encoded strings
- `vectshift()` and `circshift()` perform element shifts in matrices
- Weibull probability functions and probability density functions for all distributions
- Multiple new string functions with corresponding methods: `firstch()`, `lastch()`, `startswith()`, `endswith()`
- New table methods: `TAB().insertXYZ()`, `TAB().removeXYZ()`, `TAB().reorderXYZ()` (`XYZ` means `rows`, `cols` or `cells`) and `TAB().shrink()`
- `TAB().convert()` now provides an `"auto"` mode and may now convert more different number formats (notably EU and US separators for decimals and thousands). `TAB().fndcols()` can now be used with regular expressions
- The `"value"` column type of tables was extended to provide far more different fundamental data types, e.g. `"value.f32"` or `"value.ui8"`. Some file types will now be loaded with the best fitting data type
- Loading and saving of regular file types with custom file extensions is now possible
- Procedures can now be called with relative namespaces
- Conditional expressions in `if` and `while`, which return multiple values, have now all return values being considered (implictly using `and()`)
- `leave` extends the functionality of `break` by jumping out of all nested control flow statements (with exception of `procedure ... endprocedure`)
- One can create QR codes with `qrcode`
- More interaction possibilities to interact with and create custom windows, layouts can now be defined dynamically via strings and custom windows may now be used as dialogs.

## Experimental features

- Conditional breakpoints (available via right-click in the editor)
- Column headlines are now usable for column indices, i.e. `TABLE(:, "MY-COL-HEADLINE")`

## General changes

- We now provide 32 bit and 64 bit versions. The 64 bit version is likely to be faster and more versatile so switching is greatly encouraged
- We'll now provide an up-to-date PDF documentation with every new release (including this one)
- File loading was improved in many scenarios
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a release candidate. Some features are subject to change. If you experience problems, please let us know
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).