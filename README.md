# open-webui mirror

Repo                                | URL
----------------------------------- | --------------------------------------------------------------------
`open-webui` GitHub Repo            | <https://github.com/open-webui/open-webui>
`open-webui` GHCR Repo              | <https://github.com/open-webui/open-webui/pkgs/container/open-webui>
`open-webui` Docker Hub Repo        | <https://hub.docker.com/r/backplane/open-webui>
`open-webui-mirror` GitHub Repo     | <https://github.com/backplane/open-webui-mirror/>

This repo mirrors the Docker images published on the [open-webui project](https://github.com/open-webui/open-webui)'s GitHub Container Registry [repo](https://github.com/open-webui/open-webui/pkgs/container/open-webui) onto Docker Hub.

## Notes

* **This unofficial mirror project is not affiliated with the `open-webui` project** and the only purpose of the mirror is to enable pulling their images without being logged into GHCR.
* Every day the most recent ([semver](https://semver.org/)) tag is automatically fetched from <https://github.com/open-webui/open-webui/tags> and images corresponding to that tag are mirrored to Docker Hub - even if there were no updates in the last 24 hours
* When a semver tag is mirrored from upstream, we create separate "major", "minor", and "patch" -level docker tags from it.
* All three variants are mirrored: `main` (no suffix), `ollama`, and `cuda`
* Both the `linux/arm64` and `linux/amd64` architectures are mirrored for each variant.
* The list of mirrored image tags can be found here: <https://hub.docker.com/r/backplane/open-webui/tags>

## Examples

### pulling a major version tag

```
docker pull backplane/open-webui:0
docker pull backplane/open-webui:0-cuda
docker pull backplane/open-webui:0-ollama
```

### pulling a minor version tag

```
docker pull backplane/open-webui:0.1
docker pull backplane/open-webui:0.1-cuda
docker pull backplane/open-webui:0.1-ollama
```

### pulling a specific patch version

```
docker pull backplane/open-webui:0.1.123
docker pull backplane/open-webui:0.1.123-cuda
docker pull backplane/open-webui:0.1.123-ollama
```
