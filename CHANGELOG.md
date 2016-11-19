# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]

###Changed
 - Replaced javamake with javac in the build.xml of the root folder to make it compilable with Java 1.8 from @Andrej1A.
 - The ´tests´ target in the build.xml of the root folder is temporarily commented out, because there is a compilation error with BCEL from @Andrej1A.


## [0.4.2] - 2003-11-03
 - HTML report formatting with supporting Ant task

## [0.4.1] - 2003-08-26
 - bug fix for 794536

## [0.4] - 2003-08-25
 - filters allow patterns to match on supertypes and basic class attributes
 - severity levels allow rules to generate warnings instead of errors
 - XML reporting
 - message rules
 - from / to vars now available in access rule patterns as well as messages
 - added from-package / to-package vars
 - "regex" deprecated in favor of "class" (will make future features more readable)
 - ForEach now checks more than just the primary classes
 - better-structured event callbacks (inching closer to IDE integration)
 - Macker now uses BCEL for class parsing
 - parsing for superclass, interfaces, access modifiers
 - parsing distinguishes different types of signature-level reference
 - Macker now forces validation against its internal DTD
 - verbose output shows classes in sorted order
 - running under Java 1.4 no longer generates "major version" warning messages

## [0.3.1] - 2002-09-04
 - added a few examples
 - fixed broken links in docs
 - fixed output omission in non-forked ant task

## [version 0.3] - 2002-08-31
 - Macker now detects API-only accesses of other classes
 - rulesets now support input class subsetting
 - access rules now support custom error messages
 - Ant task supports custom classpath without forking
 - vast performance improvements through better regex caching
 - much-improved API for calling Macker from Java
 - addReachableClasses supports dynamic primary class detection
 - Macker now won't stop after the first ruleset that fails
 - bug fix for vars containing other vars
 - added void to primitive types (now necessary b/c of API parsing)
 - numerous output formatting tweaks (getting readable!)

## [version 0.2] - 2002-08-15
 - Macker really works

## [version 0.1] - 2002-08-03
 - Macker sorta works

## [version 0.0]
 - Macker doesn't work

___________________________

LIKELY FUTURE FEATURES
(with wild guesses at version numbers)

 - 0.4 filtering on attributes other than name
 - 0.5 forall / exists rules
 - 0.6 method patterns
 - 0.7 standard for rules export in META-INF
 - ?   parsing of references inside methods
 - ?   more flexible foreach scoping
 - ?   line numbers in output
 - ?   add reference type filters for access rules?
 - ?   regression tests?
