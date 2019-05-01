load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "io_bazel_rules_docker",
    commit = "5edd38041535c2c07ca982218d184a5769e329c6",
    remote = "https://github.com/bazelbuild/rules_docker.git",
    shallow_since = "1553713324 -0400",
)

load(
    "@io_bazel_rules_docker//repositories:repositories.bzl",
    container_repositories = "repositories",
)

container_repositories()

load("@io_bazel_rules_docker//container:container.bzl", "container_pull")

container_pull(
    name = "distroless",
    digest = "sha256:1d71e323557502cc78ee6c237331a09b0c33ba59c14e5f683da3b1c6218779cc",
    registry = "gcr.io",
    repository = "distroless/base",
)