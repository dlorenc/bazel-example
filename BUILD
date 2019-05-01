package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_docker//container:container.bzl", "container_image", "container_push", "container_bundle")


container_image(
    name = "app",
    base = "@distroless//image",
    cmd = ["foo"]
)

container_push(
    name = "push",
    image = ":app",
    registry = "gcr.io",
    repository = "tekton-testing-239316/app",
    format ="Docker",
)