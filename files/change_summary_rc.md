# Highlighted changes in this version

## UI changes

- The revision dialog now shows a built-in editor, where revision diffs can directly be examined
- Tabular data from datafiles can be previewed directly without loading it, by right-clicking on it in the file tree and selecting the corresponding option
- The parser model of the code editor was reworked from the ground up and can now show much better tooltips. Especially the detection of the object methods has been improved. In case of problems, there is an option for a complete reparse in the Tools menu
- The static code analyzer (using the new code parser) is now faster, more precise and will show, if the argument list does not match the function or method definition
- The selection appearance in the terminal was unified with the code editor and the flickering has been reduced
- Menu keybinds are now managed in a dedicated language file. You can make a copy of that file within the `<>/user/lang` folder to define your own keybinds

## New and improved functionalities

- Window layouts have been improved: you can now read and write properties of multple GUI elements at once, `treelist` accepts DictStructs during runtime and a new `flexgrid` group layouting option has been added
- The `inline` flag for procedures was improved, supporting more advanced procedures and even inlining only partly inlinable call trees
- DictStructs got new methods: `DCT.pick()`, `DCT.omit()` and `DCT.merge()` for extracting subsets and merging them, `DCT.renamekey()` for renaming a field, `DCT.contains()` for checking for field existence, and `DCT.encodexml()` and `DCT.decodexml()` for XML to and from string operations. Furthermore, `DCT.encodexml()` and `DCT.encodejson()` do now support pretty-printing
- `zip()` does now accept a single cluster as input and can therefore be used as its own inverse
- `swapbytes()` can perform endianness conversions on numerical datatypes
- Functions for SW tests have been added: `verifyval()`, `verifyneq()` and `verifyrange()`
- New functions for the new matrix operations (without `matop`, see below) have been added: `cat()`, `squeeze()`, `rotmat()`, `levicivita()`, `rank()`, `gaussjordan()`, `trilow()`, `triup()` and `insertscalardim()`
- New functions for Unicode support: `to_codepoints()` and `from_codepoints()`. There are also new string escape characters: `"\xHH"` (e.g. `"\xC3"`) for a single byte,  `"\0"` for escaping the 0-character and `"\uHHHH"` (`U+0000` up to `U+FFFF`) and `"\UHHHHHHHH"` (`U+00000000` up to `U+0010FFFF`) for Unicode code points encoded in hexadecimal values
- New string methods for Unicode support: `STR.chr()`, `STR.unicodelen`, `STR.normalize()` and `STR.collate()`

## Experimental features

- An initial PostgreSQL support has been added to the `database` command. It is still limited in the supported datatypes, though

## General changes

- Matrix operations via the `matop` command have been declared as deprecated. Matrix operations are now available in usual expressions at the cost of some smaller syntactical differences but at the benefit of supporting an arbitrary number of dimensions. There are also differences in the behavior of brace, bracket and parenthesis indexing. See the `matop` documentation article for further insights and guidelines for porting
- Code files and strings do now support Unicode using UTF-8 as internal encoding. String functions do now distinguish between unicode code points and bytes for this reason. See the `string` documentation article for further details
- Example scripts were updated to reflect the new functionalities. Some additional example files for objects and DictStructs have been added as well
- Many improvements and fixes

The complete list of changes can be found in the ChangesLog.

## Remarks

- This is a release candidate. Some features are subject to change. If you experience problems, please let us know
- If you experience troubles with downloads from SourceForge (esp. via MS Edge for Business), consider downloading from Github directly (see assets section at the end of the release notes).
- If your browser refuses to download or execute the installer binary, just *f-ing* use Firefox or `winget`.