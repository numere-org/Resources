# Highlighted changes in this version

## UI changes

- An optional feature to extract the argument types of functions, methods and procedures based upon their names, was added.
- Usability of mouse-over tooltips was improved. It should now be possible to show the fulltips of arguments inside of function parentheses again.
- The auto-indentation functionality does not interfere with CTRL-Z any more.

## New and improved functionalities

- The new plotting option `stacked` enables the stacking of `bars` and `hbars` on each other.
- Bar charts now always include the value y=0. In some situations it is reasonable to enable `origin=sliding` as an additional plotting option.
- One can now pass custom axis ticks using a list of strings instead of the newline-separated strings.

## Experimental features

- It is now possible to create new columns in tables if values are assigned to an unknown column using string indexing with the column headlines, i.e. `TABLE(:, "MY-COL-HEADLINE")`. The new column will be appended at the end of the table.
- `matop` functions now also accept matrix results as their scalar inputs. For consecutive scalar inputs, even a single vector can be passed, e.g. `matop zero({1,3})`
- We added support for coloured window themes. If you want to test it, the setting can be found at the end of the syntax colour list. Recommended colour sets are the blue set (foreground: `rgb(159,213,244)` and background: `rgb(234,245,253)`), the light grey set (foreground: `rgb(82,82,82)`, background: `rgb(181,183,185)`) and the splash-image set (foreground: `rgb(214,177,182)`, background: `rgb(222,237,234)`)

## General changes

- Increased performance of `stfa`, `audioread` and some statistics functions.
- `write` now uses `noquotes` as default. The parameter was removed and has no effect any more.
- If the values `nan` and `inf` are used within an index vector, then they are treated as invalid values and will always return an invalid value.
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a stable release and builds ontop of the changes from the last release candidate.
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).