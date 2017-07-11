# ZetaPush Official Test Recipies

> This mono-repo contains all official test recipies

## Overview

- Test > tests to be executed
- Core > macros related to language syntax
- Common > macros related to services


## Documentation

Tests consist of a particular setup, handler(s) and macro call(s). Handlers will determine on macro calls if the result can be assigned to a success or not.

After a certain timeout, if the test has not been declared as a success, it is considered as a failure.
To neutralize this behavior, you need to place `zms_test_success` in your code.  
Moreover it is possible (but not mandatory) to add assertions which can stop the code execution if the evaluation returns false.

Example of assertion :

```
// considering resultOfMacro and expectedResult well defined
assert resultOfMacro == expectedResult "macro returned the expected value";

// this will be triggered only if the assertion didn't fail
zms_test_success;

```


