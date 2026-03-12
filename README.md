# open-webui mirror

## WARNING! As of February 23, 2026, this mirror is obsolete!

The open-webui project [added](https://github.com/open-webui/open-webui/pull/21618) a workflow which publishes their images to Docker Hub at `openwebui/open-webui`, therefore this mirror project is now (happily) obsolete.

- All users should switch to [`openwebui/open-webui`](https://hub.docker.com/r/openwebui/open-webui)
- Backplane mirroring workflows will stop on March 31, 2026
- All images will be removed from the Docker Hub `backplane/open-webui` repo on **August 31, 2026**. The repo will be left intact but empty so that users can find this message.
- The backplane `backplane/open-webui` Docker Hub repo will be deleted **January 1, 2027**
- The `backplane/open-webui-mirror` GitHub repo will be archived **January 1, 2027**

## Overview

This repo mirrors the Docker images published on the [open-webui project](https://github.com/open-webui/open-webui)'s GitHub Container Registry [repo](https://github.com/open-webui/open-webui/pkgs/container/open-webui) onto Docker Hub.

| Repo                                                     | URL                                                                  |
| -------------------------------------------------------- | -------------------------------------------------------------------- |
| `open-webui` GitHub Repo                                 | <https://github.com/open-webui/open-webui>                           |
| `open-webui` GHCR Repo                                   | <https://github.com/open-webui/open-webui/pkgs/container/open-webui> |
| `openwebui/open-webui` Docker Hub Repo                   | <https://hub.docker.com/r/openwebui/open-webui>                      |
| `backplane/open-webui` Docker Hub Repo (obsolete mirror) | <https://hub.docker.com/r/backplane/open-webui>                      |
| `open-webui-mirror` GitHub Repo                          | <https://github.com/backplane/open-webui-mirror/>                    |

## Notes

- **This unofficial mirror project is not affiliated with the `open-webui` project** and the only purpose of the mirror is to enable pulling their images without being logged into GHCR.
- The most recent ([semver](https://semver.org/)) tag is automatically fetched daily from <https://github.com/open-webui/open-webui/tags> and mirrored to Docker Hub.
- When a semver tag is mirrored from upstream, we create separate "major", "minor", and "patch"-level Docker tags from it.
- Three variants are mirrored: `main` (no suffix), `ollama`, and `slim`. (Note: `cuda` mirroring is currently broken.)
- Both the `linux/arm64` and `linux/amd64` architectures are mirrored for each variant.
- The list of mirrored image tags can be found here: <https://hub.docker.com/r/backplane/open-webui/tags>
