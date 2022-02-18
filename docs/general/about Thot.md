# About Thot
The database is built using a data analysis and management tool Thot Data.  Detailed information about the program can be found on [Read the docs](https://thot-data-docs.readthedocs.io/en/latest/).

## Structure
An inspection of a database would reveals a hierarchical, branched folder structure. Each folder contains either an `_container.json` and `_scripts.json`, or `_asset.json` file, which create a link between scripts and data to be analyzed.

The files in the folder define whether it is a **container** or an **asset**.
- containers store other containers and assets
- assets point to a file to be analysed