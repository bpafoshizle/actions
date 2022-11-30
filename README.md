# Actions
Shared common workflow actions

The following reusable workflows are currently defined:

## <ins>Lint</ins>

**Description**: Lint Codebase Using Super-Linter

**Invoke**: `uses: bpafoshizle/actions/.github/workflows/lint.yml`

|Input|Description|Default|
|-----|-----------|-------|
|`linter-rules-path`|Tells Super-Linter where your rules files are located|`'app'`|
|`default-branch`|The name of the repository default branch for Super-Linter|`'main'`|
|`python-black-config-file`|Filename for black configuration (ex: .isort.cfg, pyproject.toml)|`'pyproject.toml'`|

## <ins>Docker Build</ins>

**Description**: Build Docker image to target platform(s) using buildx

**Invoke**: `uses: bpafoshizle/actions/.github/workflows/docker-build.yml`

|Parameter|Description|Default|
|-----|-----------|-------|
|`dockerfile`|Path to docker build file|`'Dockerfile'`|
|`platform`|Comma delimited list of platform architecute targets for the build image|`'linux/amd64'`|

## <ins>Docker Build and Push to GHCR</ins>

**Description**: Build Docker image to target platform(s) and push to ghcr using buildx


**Invoke**: `uses: bpafoshizle/actions/.github/workflows/docker-build-push-ghcr.yml`

|Parameter|Description|Default|
|-----|-----------|-------|
|`dockerfile`|Path to docker build file|`'Dockerfile'`|
|`platform`|Comma delimited list of platform architecute targets for the build image|`'linux/amd64'`|