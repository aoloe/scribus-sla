# Proposal for a _structured_ Scribus file format

> **Work in progress** (early draft)

sla-2.0.xml contains 

## Basic concepts

- (Most) Default values should not be in the file.
  - Scribus should have int he code or in a schema the default value for a specific version
- The file format should be versioned (the Scribus version should be in the document, but it won't be read)
  - There should be code for migrating the files accross versions
  - The migration code should document the changes and carry incompatibility warnings for the user (specific to fields or general)

 

## Relax NG

`sla-2.0.rng` is a proposal for a file shema in Relax NG.

Relax NG has been chosen as the initial schema for drafting a new XML structure because it seems compact and flexible enough to help reasoning about our needs


Some resources about Relax NG:

- [Eric van der Vlist's book as a PDF and xml source files](https://notabug.org/koz.ross/relax-ng-textbook/)
- [RELAX NG Compact Syntax Tutorial](https://relaxng.org/compact-tutorial-20030326.html#id2814120)
- [Books](https://relaxng.org/#books)
- [Compact Syntax](https://www.xml.com/pub/a/2002/06/19/rng-compact.html)
- [RELAX NG Compact Syntax](https://relaxng.org/compact.html)
- [Validation with lxml](https://lxml.de/validation.html#relaxng)
- [How do I validate XML document using compact RELAX NG schema in Python?](https://stackoverflow.com/questions/1254919/how-do-i-validate-xml-document-using-compact-relax-ng-schema-in-python)
- [Wikipedia: Relax NG](https://en.wikipedia.org/wiki/RELAX_NG)
- [What is difference between XML Schema and DTD?](https://stackoverflow.com/questions/1544200/what-is-difference-between-xml-schema-and-dtd)
- []()

## TODO

- Create a basic `.rng` schema
- Create one or more matching `.xml` files
- Create a Python script that validates the xml with the `.rng` file.
- Document the matching of the new fiels in the `.rng` with the `.sla` format.
- Create a `.rng` file for the `.sla`
- Create a program to convert from `.sla` to `.rng`
