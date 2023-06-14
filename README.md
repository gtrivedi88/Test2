[source,yaml]
----
param:
    -  name: prefetch-input
       value: pip <1>
----
<1> Specify the requirements files relative to the package path. If the requirements file is located at the root directory of your repository, enter `pip`. Otherwise, provide the path to the requirements file in the JSON object format. For example, `{"type": "pip", "path": "subpath/to/the/other/module"}`. Additionally, if you have multiple requirements files, you can provide the path to the lock file in the JSON array format. For example, `[{"path": ".", "type": "pip"}, {"path": "subpath/to/other/module", "type": "pip"}]`. Here, `.` indicates that the the requirements file is located at the root of the repository.
