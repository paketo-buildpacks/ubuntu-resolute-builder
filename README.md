# Paketo Ubuntu Resolute Builders

## `paketobuildpacks/ubuntu-resolute-builder`

This builder uses the [Paketo Ubuntu Resolute base images](https://github.com/paketo-buildpacks/ubuntu-resolute-base-images) with buildpacks for Java, Node.js, .NET, PHP, Procfile and Ruby.

For example, with the `pack` CLI, use `--buildpack` as follows:

```bash
pack build my-java-app \
--builder paketobuildpacks/ubuntu-resolute-builder
```

To see which versions of build and run images and the lifecycle are contained within a given builder version, see the [Releases](https://github.com/paketo-buildpacks/ubuntu-resolute-base-images/releases) on this repo. This information is also available in the [builder.toml](./builders/builder/builder.toml).

## General

- For more information about these builders and how to use them, visit the [Paketo builder documentation](https://paketo.io/docs/builders/).

- To learn about the build and the run images included in these builders, visit the [Paketo stack documentation](https://paketo.io/docs/stacks/).

## `paketobuildpacks/ubuntu-resolute-builder-buildpackless`

This builder uses the [Paketo Ubuntu Resolute base images](https://github.com/paketo-buildpacks/ubuntu-resolute-base-images) and contains **no buildpacks nor order groups**. To use this builder, you must specify buildpacks at build time using whatever mechanisms your CNB platform of choice offers.

For example, with the `pack` CLI, use `--buildpack` as follows:

```bash
pack build dotnet-with-buildpackless-builder \
--buildpack paketobuildpacks/dotnet-core \
--builder paketobuildpacks/ubuntu-resolute-builder-buildpackless
```

To see which versions of build and run images and the lifecycle are contained within a given builder version, see the [Releases](https://github.com/paketo-buildpacks/ubuntu-resolute-base-images/releases) on this repo. This information is also available in the [builder.toml](./builders/builder-buildpackless/builder.toml).
