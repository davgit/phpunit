PHPUnit 3.8
===========

This is the list of changes for the PHPUnit 3.8 release series.

PHPUnit 3.8.0
-------------

* Implemented #382: Added the `$options` parameter to `PHPUnit_Framework_TestCase::getMockFromWsdl()` for configuring the `SoapClient`.
* Implemented #628: Added `PHPUnit_Framework_Assert::countOf(), a shortcut to get a `PHPUnit_Framework_Constraint_Count` instance.
* Implemented #711: `coverage-text` now has an XML `showOnlySummary` option.
* Implemented #719: The `--stderr` switch now respects `--colors` and `--debug`.
* Implemented #746: Allow identity checking for non-object types in all asserts that depend on `TraversableContains`.
* Implemented #758: Show a proper stack trace when @expectedException fails due to a unexpected exception being thrown.
* Implemented #773: Recursive and repeated arrays are more gracefully when comparison differences are exported.
* Implemented #813: Added `@before`, `@after`, `@beforeClass` and `@afterClass` annotations.
* Implemented #834: Added the `@requires OS` annotation.
* Implemented #835: Printers that extend `PHPUnit_TextUI_ResultPrinter` should have similar construction
* Implemented #838: Added a base test listener.
* Implemented #859: Added PHP label validation to attribute assertions.
* Implemented #869: Added support for the adjacent sibling selector (+) to `PHPUnit_Util_XML::findNodes()`.
* Implemented #871: Add Comparator for DateTime objects.
* Implemented #877: Added new HTML5 tags to `PHPUnit_Util_XML::findNodes()`.
* Added `--coverage-crap4j` switch to generate code coverage report in Crap4J XML format.
* `assertCount()`, `assertNotCount()`, `assertSameSize()`, and `assertNotSameSize()` now support all objects that implement the `Traversable` interface.
* A test will now fail in strict mode when it uses the `@covers` annotation and code that is not expected to be covered is executed.
* All relative paths in a configuration file are now resolved relative to that configuration file. When upgrading, you may need to update relative paths for the following configurations: `testSuiteLoaderFile`, `printerFile`, `testsuites/file`, `testsuites/exclude`.
* Fixed #240: XML strings are escaped by removing invalid characters.
* Fixed #261: `setUp()` and `setUpBeforeClass()` are run before filters are applied.
* Fixed #541: Excluded groups are counted towards total number of tests being executed.
* Fixed #789: PHP INI settings would not be passed to child processes.
* Fixed #806: Array references are now properly displayed in error output.
* Fixed #808: Resources are now reported as `resource(13) of type (stream)` instead of `NULL`.
* Fixed #873: PHPUnit suppresses exceptions thrown outside of test case function.
* Fixed: `phpt` test cases now use the correct php binary when executed through wrapper scripts.
* PHPUnit 3.8 is only supported on PHP 5.4.7 (or later).
