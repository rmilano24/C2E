# Changelog

## 2.0.7 - 2018-05-08

### Added

- Added Support for [Schematic](https://github.com/nerds-and-company/schematic)

### Fixed

- Fix nested Super Table (in Matrix) fields needing each field handle to be unique

## 2.0.6 - 2018-04-25

### Added
- Added Matrix Layout option (thanks [@Rias500](https://github.com/Rias500))
- Added back support for `getRelatedElements()`

### Changed
- Now sets `$propagating` to `true` when saving blocks, if the owner element is propagating.

### Fixed
- Fixed a bug where relational fields within Super Table fields wouldn’t save relations to elements that didn’t exist on all of the sites the owner element existed on. ([#2683](https://github.com/craftcms/cms/issues/2683))
- Fix query issue when requesting from console (for static fields)
- Fixed validation-handling when used in a Matrix field. Would allow saving invalid field handles in this context.

## 2.0.5 - 2018-04-05

### Fixed
- Updates to be inline with Craft 3.0.0 GA, now minimum requirement
- Improve field validation
- Fix post location path for inner fields
- Fix some minor layout issues with Matrix combinations
- Fix row layout (and a few other things) not using `site` as the translation key
- Fix table fields rows now being able to be deleted
- Fix Row layout not respecting minRows value
- Field instructions should parse markdown
- Fix namespacing for nested Matrix fields
- Fix errors caused by SuperTableBlockElement.eagerLoadingMap()

## 2.0.4 - 2018-02-21

### Added
- Minimum requirement for Super Table is now `^3.0.0-RC10`

### Changed
- Make use of `FieldLayoutBehavior::getFields()` and `setFields()`
- No longer executes two queries per block type when preparing a Super Table block query.

### Fixed
- Fixed an issue caused when upgrading a multi-locale site from Craft 2 to Craft 3.
- Fixed typo in Super Table's field context column
- Fixed blocks not appearing during Live Preview

## 2.0.3 - 2018-02-12

### Fixed
- Ensure field names are required
- Fix missing field validation
- Fix plugin icon in some circumstances

## 2.0.2 - 2018-02-11

### Added
- Added migration to handle converting existing field and element types to new namespaced format
- Add some field properties for backward-compatibility with Craft 2 upgrades

### Fixed
- Fix missing `sortOrder` column in install migration

## 2.0.1 - 2018-02-11

### Fixed
- Fix migration to not rely on service class. Fixes #122
- Fix for leftover `sortOrder` for Block Types. Fixes #123

## 2.0.0 - 2018-02-10

### Added
- Craft 3 initial release.

## 1.0.6 - 2017-10-17

### Added
- Verbb marketing (new plugin icon, readme, etc).

### Changed
- Improved [Feed Me](http://sgroup.com.au/plugins/feedme) inside Matrix support.

## 1.0.5 - 2017-06-22

### Changed
- [Feed Me](http://sgroup.com.au/plugins/feedme) 2.0.6 support.
- Minor migration fix for pre 0.4.0.

## 1.0.4 - 2017-03-25

### Added
- Added Minimum Rows field setting.

### Changed
- `type` is now a reserved field handle.
- Blocks are now deleted when an owner is deleted (think deleting an entry also deletes blocks for that entry). Otherwise, end up with orphaned blocks.

## 1.0.3 - 2017-02-27

### Added
- [Feed Me](http://sgroup.com.au/plugins/feedme) 2.0 support.

### Changed
- Support for Craft 2.6.2951.

### Fixed
- Fix Row Layout and limit rows issue. Wait for removal contract function to fire before updating the `canAddMoreRows()` function. Otherwise, button stays disabled when blocks can still be added.
- Fix for selected fieldtype JS not firing on select in settings.
- Fix lack of translation for field titles and instructions.

## 1.0.2 - 2016-11-02

### Fixed
- Minor layout fixes for Matrix-ST-Matrix, in particular when a lot of blocks are present.

## 1.0.1 - 2016-08-29

### Fixed
- Minor layout fix for Matrix-ST-Matrix in Safari.

## 1.0.0 - 2016-08-29

### Changed
- Brand new (yet awfully familiar!) settings layout for Super Table. Provides much more flexibility, future growth and performance improvements.
- No more modal for editing field settings - now inline and Matrix-style.
- Added instructions field to Super Table. Appears as small `info` button on table headers.
- Allow fields to be translatable.
- Revert Row Layout `table-layout: fixed` behaviour. Row Layout labels will now fit to the longest label without word-breaking.
- Improved Linkit styling inside Super Table.
- Cleanup and organise css.
- Added sliding animation when adding/deleting blocks (thanks [@benjamminf](https://github.com/benjamminf)!)

### Fixed
- Fixed performance issues with modal field settings (the modal no longer exists).
- Fixed field settings validation not firing and providing feedback.
- Fixed field validation when inside Matrix.
- Fixed field validation when outside Matrix.
- Fixed some issues with an inner Matrix field.
- Update `prepForFeedMeFieldType` to handle static field option
- Field names are now compulsary.

## 0.4.8 - 2016-07-15

### Fixed
- Fixed minor issue where width column settings weren't being saved correctly.

## 0.4.7 - 2016-07-09

### Added
- Added support for eager loading.
- Added `blocks()` template tag for Super Table block elements.

### Changed
- Column layout width now allows either px or % values. Defaults to % if unit-less.

### Fixed
- Fix for certain fields not settings content properly from draft.
- Fixed column layout not applying width correctly.

## 0.4.6 - 2016-03-16

### Fixed
- Adding a new locale when using with a Craft Commerce product type results in a stuck background task [#58](https://github.com/engram-design/SuperTable/issues/58).
- Fix Table layout overflow issues with Matrix-in-SuperTable [#59](https://github.com/engram-design/SuperTable/issues/59)

### Changed
- Improvements to Feed Me support.

## 0.4.5 - 2016-02-29

### Fixed
- Correct plugin version number (oops!).

## 0.4.4 - 2016-02-28

### Fixed
- Fixed issue with rows not displaying correctly for Static Field option.

## 0.4.3 - 2016-02-28

### Fixed
- Fixed issue with JS not firing correctly in field settings - caused some field types to not allow editing of settings.
- Fixed issue where blocks were being overwritten when entries are saved as drafts.

### Changed
- You now have direct access to fields when using the Static Field option. No more looping or using `superTableField[0].fieldHandle`.

## 0.4.2 - 2016-01-13

### Fixed
- Fixed issue with plugin release feed url.
- Fixes for PHP 5.3 compatibility.

## 0.4.1 - 2015-12-01

### Fixed
- Some files not correctly updated (for some strange reason).

## 0.4.0 - 2015-12-01

### Added
- Craft 2.5 support, including release feed and icons.
- Support for [Feed Me](https://github.com/engram-design/FeedMe).
- Support for [Export](https://github.com/boboldehampsink/Export).

### Fixed
- Labels in Row Layout are now top-aligned.

## 0.3.8 - 2015-11-30

- Ensure Craft 2.3.2615 is minimum required version.

## 0.3.7 - 2015-11-30

- Added relations support, thanks to [joshangell](https://github.com/joshangell).

## 0.3.6 - 2015-11-30

- Fix for validation when inside a Matrix field.

## 0.3.5 - 2015-11-30

- Change to content table naming when inside Matrix field. When two Super Table fields in different Matrix fields had the same handle, when one ST field was deleted, content for both would be deleted. Now prefixes tables with Matrix field id - ie: `supertablecontent_matrixId_fieldhandle`. See [notes](https://github.com/engram-design/SuperTable/blob/master/README.md#updating-from-034-to-035).
- Fix for some UI elements not initializing for Matrix > Super Table > Matrix layout [#28](https://github.com/engram-design/SuperTable/issues/28).

## 0.3.4 - 2015-11-30

- Minor visual fix for Row layout and table overflow [#24](https://github.com/engram-design/SuperTable/issues/24).
- Fix for Table layout and deleting element select items [#25](https://github.com/engram-design/SuperTable/issues/25).

## 0.3.3 - 2015-11-30

- Minor fixes to issues introduced accidentally in 0.3.2.

## 0.3.2 - 2015-11-30

- Fix for Matrix-SuperTable-Matrix field configuration and correct namespacing. Caused numerous inner-Matrix issues.

## 0.3.1 - 2015-11-30

- Fix for field labels on inner-Matrix field being hidden [#16](https://github.com/engram-design/SuperTable/issues/16).
- Latest Redactor version fixes [#3](https://github.com/engram-design/SuperTable/issues/3).
- Fix for width not being applied for columns [#15](https://github.com/engram-design/SuperTable/issues/15).
- Fix issues with multiple Matrix Configurators causing many javascript issues [see Craft 2.4.2677](https://buildwithcraft.com/updates#build2677).

## 0.3.0 - 2015-11-30

- Added composer support.
- Improved performance (thanks to [@boboldehampsink](https://github.com/boboldehampsink) and [@takobell](https://github.com/takobell))

## 0.2.9 - 2015-11-30

- Added Static option for fields. Allows for blocks to be non-repeatable [see more](https://github.com/engram-design/SuperTable#staticoption).
- Fixed validation when creating Super Table fields.
- Added option to set the 'Add a row' button text.
- Added Max Rows option.
- Added required option for fields.

## 0.2.8 - 2015-11-30

- Minor fix for Row Layout and Element Selection fields. Clicking delete on an element select would remove the entire row.

## 0.2.7 - 2015-11-30

- Full support for Matrix.

## 0.2.6 - 2015-11-30

- Added Row layout option [see example](https://github.com/engram-design/SuperTable#layout)
- Removed background colouring for cells.

## 0.2.5 - 2015-11-30

- Added width option to each column.
- Added Label field type.
- Fixed some minor validation bugs.
- Fixed namespacing issues for element-selects and some other fields inside Matrix blocks.

## 0.2 - 2015-11-30

- Major refactor of field settings JS. Caused namespacing issues for certain field types.

## 0.1 - 2015-11-30

- Initial release.
