---
description: How do I use this library?
icon: flask
---

# How to use

In order to be able to use this library, you can do the following actions:

* Get all chemical substances from the entire periodic table
* Get a specific substance from the periodic table by:
  * Atomic number
  * Symbol or name
* Get a list of substances from the periodic table by period and group

The above goals can be attained by calling the following functions from the periodic table static class responsible for loading information about every single substance, `PeriodicTableParser`:

* `GetSubstances()`
  * Gets all the substances from the whole table
  * Gets a list of substances that are found within a period and a group
* `GetSubstanceFromName()`
  * Gets a chemical substance from its name (case-insensitive)
* `GetSubstance()`
  * Gets a chemical substance from either its symbol or its atomic number

You can also check to see if a substance exists in the periodic table without having to handle exceptions thrown by the above functions using the following `IsRegistered()` functions:

* `AreSubstancesRegistered()`
  * Checks to see if there are substances within a period and a group
* `IsSubstanceRegisteredName()`
  * Checks to see if there is a chemical substance by its name (case-insensitive)
* `IsSubstanceRegistered()`
  * Checks to see if there is a chemical substance by either its symbol or its atomic number

The first time the library user calls any of these functions found within the `PeriodicTableParser` class, ChemiStar will cache the list of chemical substances after the list of substances has been populated. This is to speed up further queries.
