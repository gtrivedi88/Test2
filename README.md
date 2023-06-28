In {ProductName}, the File-based catalog offers a way to store and distribute operator metadata. It is a plain text-based (JSON or YAML) and declarative config evolution of the earlier SQLite database format, and it is fully backward compatible. The goal of this format is to enable Operator catalog editing, composability, and extensibility.

Previously, index images for operators were stored in a Postgres database. This made it difficult to manage the operator graphs, as changes to the database required a restart of the Operator Lifecycle Manager (OLM) controller. 

The File-based catalog solves this problem by storing the operator graphs n a collection of .yaml files. This makes it much easier to manage the graphs, as changes can be made without restarting the OLM controller.  In addition, {ProductName} can build, test, and release multiple components from a single FBC repository.
