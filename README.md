I had this defintion on hermetic builds: Hermetic builds refer to a build process that is isolated from external dependencies, such as network access or a file system. This makes hermetic builds more secure and reliable.

SME feedback: I view hermetic builds just as being sealed off from unfettered access. This means that all required resources and dependencies MUST go through the build system. It allows the build system to ensure that it has the ability to collect, query, analyze, etc. all dependencies needed for the build. Hermetic itself does not necessarily have a direct connection to security/reliability. It might have implicit connections to it.

I think the wording should be changed a little. I was just trying to figure out what the definition sources were. There are many different ways that I have sen it be defined. As an example, builds are not being isolated from external dependencies as those are still being provided by Cachi2.

when it comes to hermetic since it was removed. From the SLSA perspective, my opinion is that it isn't necessarily that there is no network access, but no unfettered access by the build process as I have mentioned before. Any network access needed should either be done via the build platform before the build or done by the build platform during the build. This can ensure that all dependencies are actually known by the build platform for use in its provenance generation.

This is why I don't see that there are direct security/reliability changes with the introduction of hermetic builds. Instead, it makes it possible for us to accurately and completely identify all build dependencies. Being able to confidently declare the specific build dependencies is also a step towards reproducible builds which is a further step past hermetic.
