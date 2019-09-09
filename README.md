This repo is to host the "Build Helper" app from Clever Dynamics.

The app includes a codeunit (90100) that is published as a web service to expose methods to help preparing and executing test suites as part of a Business Central AL build pipline.

**GetTests**

Takes three parameters:
- TestSuiteName (Code10) - to specify the test suite name to add test codeunits and methods to (DEFAULT is used if a value is not specified)
- StartID - the start of the range of IDs to add test codeunits from
- EndID - the end of the range of IDs to add test codeunits from

This method will filter for test codeunits in the specified range and add them and their test methods to the test suite specified. The DEFAULT test suite will be used if no value is provided.

**ClearTestSuite**

Takes a single parameter:
- TestSuiteName - the suite from which to clear the test codeunits and methods

This method removes all test codeunits and methods from the specified test suite.