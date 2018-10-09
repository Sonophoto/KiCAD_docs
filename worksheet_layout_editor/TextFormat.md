# Text Format for Worksheet layout (template) files


**NOTICE:** This document is specifically written for programmers. You only need this information if you are writing plugins or external processing utilities. If you are not a programmer please use the instructions for the interactive GUI [Worksheet Layout Editor](https://github.com/Sonophoto/KiCAD_docs/tree/master/worksheet_layout_editor) to edit your worksheet templates and save the results.

Each line in a `.kicad_wks` is an individual record. Each record is written as an S-Expression which is a form of data serialization (aka pickling or marshalling) like JSON or XML. S-Expressions are based on ideas from the Lisp programming language. If you need to learn this technique:

An overview is at [Wikipedia: S-Expressions](https://en.wikipedia.org/wiki/S-expression).

There is an [Internet Draft: S-Expressions]( http://people.csail.mit.edu/rivest/Sexp.txt).

You can find parsers for many different languages at [Rosetta Stone: S-Expression](http://rosettacode.org/wiki/S-Expressions)

List of record types:

