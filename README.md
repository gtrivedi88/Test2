Note: If you add this parameter in a non-java application, that is the Buildah task, the build is automatically isolated from the network, as all the required dependencies are vendored in a git repository. However, if you want to restrict external network access during the build process, then you can use pre-fetch dependencies to pull in the package manager dependencies for the supported languages. For now, we have support for Go and Pip. But soon, we will have support for other languages.
