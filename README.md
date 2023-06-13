Cachi2 supports pip by parsing *requirements.txt* files placed in the root of your repository and then downloading the specified dependencies. These files should be lockfiles, which include all the transitive dependencies. Each transitive dependency in the *requirements.txt* file must be pinned to a specific version.

It does not only parse requirements.txt files, instead it generically parses pip requirements files. The requirement is the internal format, not the file name as multiple files can be used to provide the dependencies.
