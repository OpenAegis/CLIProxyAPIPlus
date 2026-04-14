# CLIProxyAPI Plus

English | [Chinese](README_CN.md)

This repository is `lemon07r/CLIProxyAPIPlus`, a fork of the upstream [CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) Plus branch.

It stays close to upstream while carrying a small fork-specific patch stack that is applied during Docker builds from the files in [`patches/`](patches/). Those patches currently cover custom Copilot behavior, Copilot Claude endpoint handling, streaming fixes, and Antigravity compatibility/fingerprinting adjustments.

Published images for this fork are available on Docker Hub as [`lemon07r/cli-proxy-api-plus`](https://hub.docker.com/r/lemon07r/cli-proxy-api-plus). The fork is intended to stay in lockstep with upstream Plus features apart from the patch set above.

All third-party provider support is maintained by community contributors; upstream CLIProxyAPI does not provide technical support for fork-specific changes. If you need help with this fork, contact the corresponding fork maintainer.

## Fork Notes

- Fork customizations should be added as `.patch` files under [`patches/`](patches/) rather than committed as direct source edits.
- Docker builds apply patches in lexical order, so patch filenames define the customization order.
- If upstream changes break patch application, regenerate the affected patch against the new upstream baseline and keep the patch chain clean.

## Contributing

This project only accepts pull requests that relate to third-party provider support. Any pull requests unrelated to third-party provider support will be rejected.

If you need to submit any non-third-party provider changes, please open them against the [mainline](https://github.com/router-for-me/CLIProxyAPI) repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
