# open-webui mirror

## WARNING! As of Feb 23 2026, this mirror is obsolete!

The open-webui project [recently added](https://github.com/open-webui/open-webui/pull/21618) a workflow which publishes thier images to docker hub at `openwebui/open-webui`, therefore this mirror project is now (happily) obsolete.

- All users should switch to [`openwebui/open-webui`](https://hub.docker.com/r/openwebui/open-webui)
- Backplane mirroring workflows will stop on March 31st 2026
- All images will be removed from the docker hub `backplane/open-webui` repo on **August 31 2026**, the repo will be left intact but empty so that users can find this message.
- The backplane `backplane/open-webui` docker hub repo will be deleted **Jan 1 2027**
- The `backplane/open-webui-mirror` github repo will be archived **Jan 1 2027**

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
- Every day the most recent ([semver](https://semver.org/)) tag is automatically fetched from <https://github.com/open-webui/open-webui/tags> and images corresponding to that tag are mirrored to Docker Hub - even if there were no updates in the last 24 hours
- When a semver tag is mirrored from upstream, we create separate "major", "minor", and "patch" -level docker tags from it.
- Four variants are mirrored: `main` (no suffix), `ollama`, `slim`, and ~~`cuda`~~ (cuda mirroring is broken)
- Both the `linux/arm64` and `linux/amd64` architectures are mirrored for each variant.
- The list of mirrored image tags can be found here: <https://hub.docker.com/r/backplane/open-webui/tags>
