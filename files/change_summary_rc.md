# Highlighted changes in this version

## UI changes

- The starting page was greatly reworked and provides more options.
- Double-clicking on any embedded cluster in the table viewer window will open the embedded cluster in a new table viewer window. Standard variables can now also be viewed in a table viewer. This is especially useful for vectorial variables.
- The table viewer can now sort and filter the displayed table according a selected column.
- You can now change the file filters for each of the default folders in the left tree. The option can be found beneath the path settings in the settings dialog.
- Detection of readable and loadable files has been improved, so that you can now also read files without known extension.
- Table autosizing has been sped up and vertical alignment of cells with empty lines has been improved.
- The method autocompletion recommendation has been improved and should now return better fitting candidates. The autocompletion in the terminal is much faster now.
- Window layouts are now also part of the dependency analysis and will correctly return their event procedures.
- The command `install` will now automatically search through the package repository for a package with matching filename.
- Large tables won't calculate the complete stats anymore, if opened in the table viewer (this is for performance reasons).

## New and improved functionalities

- A possibility to define a post-install script for a package was added to the package creator. The "required version" of packages now uses the correct variant of the current version for checking, e.g. "v.1.1.7.2412". The package creator will now log the last modification time of each bundled procedure in its project file. Once the project is loaded again, it is checked, whether there have been any file modifications in the mean time.
- It is now possible to set a custom HTTP header and a payload if you want to interact with REST APIs using `url`.
- The command `print` can now also display a table's contents (the first and last 5 rows) in the terminal.
- The function `convertunit()` allows for unit conversions towards SI units (like the corresponding table methods).
- The function `getoverlap()` returns the overlap of all to be passed intervals.
- The functions `complement()`, `intersection()` and `union()` provide means to apply set theory operations.
- The new table method `TAB().replacevals()` can be used to replace every occurence of a set of values with new values.
- The option `nobars` can be used together with `hist` to switch the output graph to a dashed line plot with distinct marks at the bars' positions. This can be handy if you try to compare multiple histograms in a single diagram.
- Most table methods accept now table column names in addition to column IDs. Note: If there are multiple columns with the same name, in general, all will be used for the table method.
- The target folders used with `move` or `copy` can now contain wildcards within their path as well and will be replaced by their counterpart of the copied/moved filename, if it exists.
- Improved and cleaned the `stats` command: some field were renamed or replaced with more important values.
- The automatic type conversion now avoids automatic conversions from floating point to int.
- The function `cnt()` will now return 0 if `void` values are inserted as its argument (note that this is not true for an array of `void` values). Completely empty and uninitialized columns and empty tables will now also return `void` instead of `nan` or an empty string.
- The function `student_t` will no longer subtract 1 from the passed DOF internally.
- The interface for `odesolve` and `fit` have been adapted to follow the current syntax approach more.
- The return value of the table method `TAB().indexof()` has been changed to a cluster, where consecutive index sets are stored as embedded clusters.
- The table method `TAB().anovaof()` will now return the results of multi-dimensional ANOVAs in distinct embedded clusters.
- **Important:** The table methods `TAB().categoriesof()` and `TAB().categorize()` will now return an array of categories (see function `category()` for reference) instead of a key-value list. **This might break some code.**

## Experimental features

No experimental change in this release

## General changes

- The kernel was greatly rewritten and supports much more different types and functionalities. Strange typing problems shouldn't appear any more. Overall performance should be improved (although at the cost that some segments might run slower; we're still investigating)
- We now *only* provide a 64 bit version due to limitations of external libraries
- We'll now provide an up-to-date PDF documentation with every new release (including this one)
- A *Report an issue* feature has been added, which you can use even without an GitHub account. You can also check directly from NumeRe, whether a new release is available.
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a release candidate. Some features are subject to change. If you experience problems, please let us know
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).