# Citizens2Legacy

This project brings back the support of
 older Minecraft versions for Citizens 2.

This branch is for Minecraft 1.20.1.

Developed for [The SRS Project](https://github.com/TheSRSProject)
 because our tech stack is based on Minecraft 1.20.1.

I also made a backport for other old patch versions,
 see them in their own branch (for example 1.20.4 version is
 at `ver/1.20.4` branch), but I am still mainly focused
 on 1.20.1 so updates of it will slower than this main branch.

This repository contains support for the following Minecraft versions:
* 1.20.1
* 1.18.2
* 1.20.4

This is based on (my fork of)
 [GitPatcher](https://github.com/zml2008/gitpatcher),
 it makes us maintain the patches easier.
_See my fork of it there: [Link](https://github.com/SNWCreations/gitpatcher)_

## Compiling

Run `git submodule update --init` if you forget to
 add `--recurse-submodules` flag while cloning this repository,
 this make sure the upstream repository exists so
 the patch would be able to be applied.

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
run `git pull` in `upstream` submodule to sync
 with upstream, and then run `gradlew applyPatches`
 to apply patches, solve the conflict and then use Git CLI to
 continue the process of applying patch, if any.

When your patches are commited to the target repository,
run `gradlew makePatches` to export them.

After that, your patches are ready to be commited to
 the bootstrap repository (this project).

## Disclaimer

This project is unaffiliated with
CitizensDev and will **NOT** be supported by them.

**DO NOT EXPECT THIS ALWAYS WORK, NO WARRANTY.**
If it does not work, you'll have to deal with the
 exceptions by yourself. Although issues are welcome,
 but I am still just focus on 1.20.1 unless my project
 has moved to other Minecraft version.

## License

Copyright (C) 2024 SNWCreations.

This project and the patches to the upstream project
 inside this project are licensed under Open Software License 3.0,
see `LICENSE` file in this repository 
 for the license content.
