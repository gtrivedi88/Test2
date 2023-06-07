Enabling pre-fetch builds for Pip with Pip wheel dependencies
If your project depends on Pip wheels, it’ll need to be built from the source. To build from the source the following steps are involved:
Building wheels: Wheels are pre-built binary distributions that are easy to install. Installing from a wheel involves unzipping the wheel and copying the files to the appropriate location.
Building from source: Source distributions (`sdists`) require additional steps for installation. Pip needs to build a wheel from the `sdist` using PEP 517 build system. To accomplish this, pip installs the build system and its dependencies as defined in PEP 518.


Prerequisites:
Complete all the steps listed in the Enabling pre-fetch builds for pip with transitive dependencies section

Procedures:
In the root of your repository create a file, requirements-build.in.
Copy all the content from the pyproject.toml file to the requirements-build.in file.
Run `pip_find_builddeps.py` script and pip-compile the outputs using the following command:
`pip_find_builddeps.py requirements.txt \
--append \
--only-write-on-update \
-o requirements-build.in`
Note: This command generates a requirements-build.in file.
Use the pip-compile command to convert requirements-build.in into requirements-build.txt with the following command:
`pip-compile requirements-build.in --allow-unsafe --generate-hashes`
Note: This command creates a requirement-build.txt file
Add the requirement-build.txt file to your project. It does not require any changes to your build process. Pip will automatically install the build dependencies when needed for explicit installation. The purpose of the requirement-build.txt file is to enable Cachi2 to fetch the build dependencies and provide them to pip for offline installation in a network-isolated environment.
