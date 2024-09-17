# Citizens2Legacy

This project brings back the support of
 Minecraft 1.20.1 for Citizens 2.

Developed for The SRS Project because our tech stack
 is based on Minecraft 1.20.1, so other older patch
 versions are not considered.

## Compiling

Run `gradlew updateSubmodules` if upstream is not
 cloned while cloning this repository.

Then run `gradlew applyPatches` to apply the patches
 to the upstream project.

Now the patched project is ready at `target` folder,
 use Maven to compile it, and you're good to go.

## Work with this project

This project (excluding the upstream part) is only
 used to patch the upstream using our own patches,
 so changes to the project should be commited to
 the `target` submodule.

When your patches are ready to be saved, commit them
 and then just run `gradlew makePatches` to export them.

After that, your patches are ready to be commited to
 the bootstrap repository (this project).

## Disclaimer

This project is unaffiliated with
CitizensDev and will **NOT** be supported by them.

## License

Copyright (C) 2024 SNWCreations.

This project and the patches to the upstream project
 inside this project are licensed under MIT license.
