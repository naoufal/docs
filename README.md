# Crew Documentation

This is the docs repository for Crew.

## Building

Docs are built using [mkdocs][1]. First, install mkdocs with pip.

`pip install mkdocs`

After installing `mkdocs`, to build the docs simply run the following:

`mkdocs build --clean`

This will build the documentation into the `sites` directory. You can create a vhost to that directory to browse the
docs locally.

## Exporting documentation

For convenience, here's a method to download the documentation locally, assuming your host is set up as `docs.crew.dev`:

`wget -p -k --no-clobber --recursive --html-extension --domains docs.crew.dev http://docs.crew.dev/`

[1]: http://www.mkdocs.org/
