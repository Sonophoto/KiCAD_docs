# Text Format for Worksheet layout (template) files

**NOTICE:** This document is specifically written for programmers. You only need this information if you are writing plugins or external processing utilities. If you are not a programmer please use the instructions for the interactive GUI [Worksheet Template Editor](https://github.com/Sonophoto/KiCAD_docs/tree/master/worksheet_template_editor) to edit your worksheet templates and save the results.

If you are a programmer the following curated list is intended to help you get up to speed quickly with the file format used by the Worksheet Template Editor. Please write up a PR if you have additiona links.

## KiCAD: Uses "S-Expressions" for text data storage.

Each text line in a `.kicad_wks` is an individual record. Each record is written as an S-Expression which is a form of data serialization (aka pickling or marshalling) like JSON or XML. S-Expressions are based on ideas from the Lisp programming language. 

- If you need to learn this technique:

An overview is at [Wikipedia: S-Expressions](https://en.wikipedia.org/wiki/S-expression).

There is an [Internet Draft: S-Expressions]( http://people.csail.mit.edu/rivest/Sexp.txt).

You can find parsers for many different languages at [Rosetta Stone: S-Expression](http://rosettacode.org/wiki/S-Expressions)

## KiCAD: Relevant source code

Docs for file format: https://github.com/KiCad/kicad-source-mirror/blob/5.0/common/page_layout/page_layout_default_description.cpp

LEXER interface code: https://kicad-info.s3.dualstack.us-west-2.amazonaws.com/original/2X/4/44dbc845022890b690366f35acbd3e98a4ece286.h

KEYWORDS file: https://github.com/KiCad/kicad-source-mirror/blob/5.0/common/page_layout/page_layout_reader.keywords
