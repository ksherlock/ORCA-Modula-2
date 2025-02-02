﻿2021 v1.1d4 Changes in the Compiler and libraries
-
* Corrected the min and max values of REAL and LONGREAL types.

* Attempt to trap a divide by zero when tokenizing a long real literal constant of 0.0.

Circa 2007 v1.1d3 Changes in the Compiler
-
* Bug in the calculation of the number of elements in a set based upon an
  enumerated type has been fixed.
* Forward references to exported items are now allowed.
* A set constructor must now comprise of constant expressions.
* Version number changed to be v1.1d1
* Assignment of a 3 byte set variable used to generate the wrong code.
* Disallow a parameter to be used as a control variable in a FOR statement.
* When a step of zero is used, ensure that the compiler can continue
  without crashing.
* When the NILCheck directive is on, NEW now generates code to check the
  result of the allocation.  If that result is NIL, then the program will
  terminate
* Set comparisons will now mask off unused bits so that they do not affect
  the comparison.  Some optimisation also added here.
* With NILCheck on, in rare cases of a dereference, the compiler could
  crash.
* Some left shift code for longwords has been fixed.
* CDA's now have more code in their headers, to initialise the CDA Console 
  driver.
* Passing a string constant as a non-var parameter could generate bad code.
* Command-. is not handled properly, even when the compiler is waiting for
  the user to un-pause an error. 

Changes in the Libraries
-
* Public flag added to EZTools, so that other modules may know when an
  application has started the desktop or graphics screen.
* Definition of Lists.MemberDrawProc has been fixed.  Second parameter is
  now an address.
* Calls to SysGraphTextStartup and SysGraphTextShutdown are made when
  either the desktop or graphics screens are started.
* A cursor has been added to the normal text screen read string routine.
* ReadLongInt now uses NumberConversion.StringToLongInt
* The terminal module no longer uses shell calls to monitor the keyboard. 
  uses it's own routines, so that they will work with or without the shell
  running.
* M2 termination codes are now translated to orca return codes, and
  displayed.  This involved a change to syslib.
* New modules:

    EZControls - Makes life easier for doing your own dialogs with extended
                 controls.
    EZLineEdit - Easy access to line edit values.

