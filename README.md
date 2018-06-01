Symphony-docs is a documentation repository for Symphony. CircleCI is active on the repository and any change pushed will trigger an automated sphinx-build to build the documents under **docs** folder to html.

## Document Format

**Markdown** and **reStructuredText** are both supported by the source parser of sphinx-build. You can choose any one as you like to write documents.

For rst, you can refer to [http://docutils.sourceforge.net/docs/user/rst/quickref.html](http://docutils.sourceforge.net/docs/user/rst/quickref.html) 

## Directory Structure

- **docs** is the source directory of sphinx-build. All documents must be placed under **docs**. 
- You can create **subdirectories** under **docs** to organize your documents. We suggest that one Symphony component has only one documentation. If you also have some image files for one document, we suggest to create sub-diretories.
- **docs/index.rst** is the initial documentaiton file. Once you create a new md/rst file or a new folder under **docs**, you may also want to edit index.rst to arrange the order of documentations. 
- You can add some key concepts of Symphony and some related external learning resources into **keyconcepts.md** and **learningresource.md**.

## index.rst
An example is given below. Tables of contents from all those documents are inserted, with a maximum depth of two. You can use “globbing” in toctree directives, by giving the glob flag option. All entries are then matched against the list of available documents, and matches are inserted into the list alphabetically. 
```
.. toctree::
   :maxdepth: 2
   :caption: Contents:
   :glob:

   keyconcepts
   bpmn*
   symphony-cli/*
   learningresource
   *
```
For more details, you can refer to: [http://www.sphinx-doc.org/en/stable/markup/index.html](http://www.sphinx-doc.org/en/stable/markup/index.html)
