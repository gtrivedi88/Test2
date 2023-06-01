A hermetic build environment is one that is fully encapsulated and isolated from outside inflences. When a build is
run within a build platform, this encapsulation can guarantee that the platform has a complete picture of all
dependencies needed for the build. One class of hermetic build implementations is to restrict external network access
during the build itself, requiring that all dependencies are declared and pre-fetched before the build occurs.

In order to support this class of hermetic builds, not only does Cachi2 need to prefetch the dependencies, however,
but some build flows will need additional changes whether that is to the build process (i.e. leveraging defined 
[environment variables](#generate-environment-variables) or using Cachi2 to [inject project files](#inject-project-files))
