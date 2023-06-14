[source,yaml]
----
param:
    -  name: prefetch-input
       value: gomod <1>
----
<1> Specifies lock file, relative to the package path. If the package manager lock file is located at the root directory of your repository, enter `gomod`. Otherwise, provide the path to the lock file in the JSON object format. For example, `{"type": "gomod", "path": "subpath/to/the/other/module"}`
