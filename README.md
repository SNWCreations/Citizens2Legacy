# Citizens2Legacy

This project brings back the support of
 Minecraft 1.20.1 for Citizens 2.

Developed for [The SRS Project](https://github.com/TheSRSProject)
 because our tech stack is based on Minecraft 1.20.1,
 so other older patch versions are not considered.

This is based on (my fork of)
 [GitPatcher](https://github.com/zml2008/gitpatcher),
 it makes us maintain the patches easier.

## Compiling

Run `gradlew applyPatches` to apply the patches
 to the upstream project.

Now the patched project is ready at `target` folder,
 use Maven to compile it, and you're good to go.

## Work with this project

This project (excluding the upstream part) is only
 used to patch the upstream using our own patches,
 so changes to the project should be commited to
 the `target` submodule.

The `upstream` submodule is only used to sync with
 the upstream. **DO NOT MODIFY IT.**

When updating the project is needed,
run `gradlew updateSubmodules` to sync the `upstream`
 submodule with upstream, and then run
 `gradlew applyPatches` to apply patches,
 solve the conflict and then use Git CLI to
 continue the process of applying patch, if any.

When your patches are commited to the target repository,
run `gradlew makePatches` to export them.

After that, your patches are ready to be commited to
 the bootstrap repository (this project).

## Disclaimer

This project is unaffiliated with
CitizensDev and will **NOT** be supported by them.

## License

Copyright (C) 2024 SNWCreations.

This project and the patches to the upstream project
 inside this project are licensed under MIT license.
See `LICENSE` file in this repository for the license
 content.