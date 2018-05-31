Symphony-docs is a documentation repository for Symphony. CircleCI is active and any change pushed will trigger an automated sphinx-build to build the documents under **docs** folder into html.

## Document Format

Markdown and reStructuredText are both supported by the source parser of sphinx-build. You can choose any one as you like to write documents.

## Directory Structure

- **docs** is the source directory of sphinx-build. All documents must be placed under **docs**. 
- You can create **subdirectories** under **docs** to organize your documents. 
- **docs/index.rst** is the initial documentaiton file. Once you create a new folder under **docs**, you may also need to edit index.rst. 

## index.rst
An example is given below. Tables of contents from all those documents are inserted, with a maximum depth of two. You can use “globbing” in toctree directives, by giving the glob flag option. All entries are then matched against the list of available documents, and matches are inserted into the list alphabetically. 
```
.. toctree::
   :maxdepth: 2
   :caption: Contents:
   :glob:

   BPMN*
   symphony-cli/*
   *
```
For more detailed, you can refer to: [http://www.sphinx-doc.org/en/stable/markup/index.html](http://www.sphinx-doc.org/en/stable/markup/index.html)
