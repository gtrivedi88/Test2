`pip` automatically installs the build dependencies when needed for explicit installation. The purpose of the *requirement-build.txt* file is to enable Cachi2 to fetch the build dependencies and provide them to `pip` for offline installation in a network-isolated environment.

I don't think that this is always true. Sometimes changes are needed to the build process so that certain build-time dependencies can be built first before they are needed.
