# setup-docker-buildx-action
## Features

- Configure Docker Buildx
- Optional QEMU emulation
- Custom builder names
- Return builder information through outputs

## Inputs

| Input | Required | Default |
|---|---|---|
| enable-qemu | No | false |
| qemu-platforms | No | arm64 |
| builder-name | No | ci-builder |

## Outputs

| Output | Description |
|---|---|
| builder-name | Builder name |
| builder-driver | Builder driver |
| builder-platforms | Supported platforms |
| qemu-platforms | Configured QEMU platforms |

## Usage

```yaml
steps:
  - name: Setup Docker Buildx
    uses: clouduser8055/setup-docker-buildx-action@v1.0.0
    with:
      enable-qemu: "true"
      qemu-platforms: arm64
      builder-name: ci-builder
```

## Requirements

- GitHub Actions runner with Docker available
- Bash shell
- Docker Buildx setup actions access