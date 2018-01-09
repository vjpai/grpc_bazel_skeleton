load("@grpc//bazel:grpc_build_system.bzl", "grpc_proto_library", "grpc_package")

grpc_package("protos", visibility="public")

grpc_proto_library(
    name = "helloworld",
    srcs = ["helloworld.proto"],
    well_known_protos = False,
    use_external = True,
)

