# Releasing

## Versions

Releases continue upstream's version numbers, and each release increments the patch number, such as 0.8.4 and then 0.8.5. A patch release keeps source compatibility with upstream 0.8.2.

The version is declared in four places, which must match:

- `major_version`, `minor_version`, `patch_version`, `prerelease_flag` and `user_agent` in `websocketpp/version.hpp`
- `WEBSOCKETPP_MAJOR_VERSION`, `WEBSOCKETPP_MINOR_VERSION` and `WEBSOCKETPP_PATCH_VERSION` in `CMakeLists.txt`
- `PROJECT_NUMBER` in `Doxyfile`
- the heading of the newest section in `changelog.md`

Between releases, the `cpprest-lts` branch carries the next version with the pre-release flag `dev`, such as `0.8.5-dev`, and the newest changelog section is headed `HEAD`.

The version inside the code is plain numbers, without build metadata, because CMake does not accept build metadata in `project(VERSION)`. The release tag adds the semantic versioning build metadata `+cpprest-lts`, such as `0.8.5+cpprest-lts`, so that the source of the release is clear.

## Making a Release

These steps use 0.8.5 as an example.

1. Create `release/0.8.5` from `cpprest-lts`.
2. On `release/0.8.5`, commit the version change from `0.8.5-dev` to `0.8.5`. Set `prerelease_flag` to `""`, set `user_agent` to `"WebSocket++/0.8.5"`, and replace the `HEAD` changelog heading with `0.8.5 - YYYY-MM-DD`.
3. Open a pull request from `release/0.8.5` into `cpprest-lts`. When CI passes, merge it.
4. Tag the merge commit with the annotated tag `0.8.5+cpprest-lts`, and push the tag.
5. Create a GitHub release from the tag, named `WebSocket++/0.8.5+cpprest-lts`. Its notes are the changelog section for 0.8.5.
6. On `cpprest-lts`, commit the version change to `0.8.6-dev`, and add a new `HEAD` section at the top of `changelog.md`.

GitHub's source archive for the tag `0.8.5+cpprest-lts` has the top-level directory `websocketpp-0.8.5-cpprest-lts`, with `-` instead of `+`.
