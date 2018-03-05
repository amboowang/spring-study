## What's target platform in PDE

> The target platform specifies the Eclipse configuration that you are developing your plugins for. This is defined by the set of available plugins and features. It defaults to mirroring the configuration of the Eclipse instance that you are running, but in most cases you will want to change it to something more specific. For instance, you may be running Eclipse 3.6, but developing plugins for Eclipse 3.5, or you may be developing a plugin on top of WTP, but you don't need WTP functionality in your development eclipse instance.

## Eclipse Project/Classpath
> Eclipse is a runtime environment for plugins. Virtually everything you see in Eclipse is the result of plugins installed on Eclipse, rather than Eclipse itself.

> The .project file is maintained by the core Eclipse platform, and its goal is to describe the project from a generic, plugin-independent Eclipse view. What's the project's name? what other projects in the workspace does it refer to? What are the builders that are used in order to build the project? (remember, the concept of "build" doesn't pertain specifically to Java projects, but also to other types of projects)

> The .classpath file is maintained by Eclipse's JDT feature (feature = set of plugins). JDT holds multiple such "meta" files in the project (see the .settings directory inside the project); the .classpath file is just one of them. Specifically, the .classpath file contains information that the JDT feature needs in order to properly compile the project: the project's source folders (that is, what to compile); the output folders (where to compile to); and classpath entries (such as other projects in the workspace, arbitrary JAR files on the file system, and so forth).
