# Highlighted changes in this version

## UI changes

- The table viewer was improved and does now provide a categoricaly conditional cell colouring scheme
- The terminal history has now a search bar
- It is now possible to hide the main window using `set windowshown=false` and unhide it again. Using `set appautoclose=true`, the app will automatically close itself, once the last open window has been closed. Note that those settings are not saved and only affect NumeRe for the current running session.

## New and improved functionalities

- `remove` may now also remove folders (and folder structures recursively)
- *k* means clustering is now available as table method `TAB().kmeansof(...)`
- New functions: `uuid()`, `strjoin()`, `getdisplayscale()`, `is_void()`, `is_equal()`, `is_ordered()`, `is_unique()`
- New statistical functions: `rms()`, `skew()`, `exc()`, `stderr()`, `inv_pct()`
- New time-specific functions: `today()`, `get_utc_offset()`, `is_daylightsavingtime()`, `is_leapyear()`
- New noise functions: `ridgedmulti()`, `billownoise()`, `voronoinoise()`
- Functions for converting between different numerical data types and for creating categories were added.
- NumeRe can now interact with databases using the command `database`. Available interfaces for now are: MySQL/MariaDB, SQLite, ODBC. PostGreSQL is *NOT* supported right now due to dependency issues.
- Table method updates: Table method modifiers `.scwin()` and `.srwin()` have been added and can be used to define a moving window for multi argument functions. Table method handling has been improved and chaining with the new internal method system is now possible. The new table method modifier `.cells()` together with `.rows` or `.cols` allows for selection of table cells along the direction of application.
- Table columns can now have (physical) units to represent data even better. The units will be detected automatically (if possible), or you can use the dedicated methods to modify the unit of each column.
- Tables may now be exported in MarkDown and HTML format and it's now also possible to copy only a part of a table to another table at a desired location using `TAB(i1:i2,j1:j2) = TAB2(i1:i2,j1:j1)` syntax.
- Local variables may now also be declared within control flow blocks. Note that they are only declared for the first time per execution the control reaches their command.
- Index-based `for` loops can now have an additional condition as their second argument (i.e. `for (i = 1:0, a !=b)`), which is checked before each loop iteration.
- The interaction between custom windows and the `window` command has been cleaned and improved. Some interactions will now return more fitting data types. It might be possible that this change will break some existing solutions. Furthermore, the `textfield` can now be configured as `type=markup` to support simplified markdown styling.
- The tabs created with `group -style=tabs ...` in window layouts can now have an ID and an `onchange` event handler firing when the user changes the tab. It is also possible to access the properties of the tab group using `window ... -get` and `window ... -set`.
- The window command option `options={KEY-VALUE-LIST}` can be used to modify additional window element properties. This option is currently only supported for `tablegrid` elements, where one can change the minimal number of rows and cols.

## Experimental features

- Clusters can now be created as hierarchical data structures, i.e. clusters can now contain clusters in their fields. You can use the `.sel(ID)` method for navigating and `.unwrap` to unwrap the whole structure in a single-level cluster. Writing a set of values into a single cluster element will embed them as a sub-structure. Reading this single element, will return the embedded structure.

## General changes

- The kernel was greatly rewritten and supports much more different types and functionalities. Strange typing problems shouldn't appear any more. Overall performance should be improved (although at the cost that some segments might run slower)
- We now *only* provide a 64 bit version due to limitations of external libraries
- We'll now provide an up-to-date PDF documentation with every new release (including this one)
- A *Report an issue* feature has been added, which you can use even without an GitHub account
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a release candidate. Some features are subject to change. If you experience problems, please let us know
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).