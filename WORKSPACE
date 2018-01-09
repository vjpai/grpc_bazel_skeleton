workspace(name = "grpc_bazel_skeleton")

git_repository(
  name="com_google_absl",
  commit="6cf9c731027f4d8aebe3c60df8e64317e6870870",
  remote="https://github.com/abseil/abseil-cpp.git"
)

http_archive(
  name = "com_google_protobuf",
  urls = ['https://github.com/google/protobuf/releases/download/v3.5.0/protobuf-all-3.5.0.tar.gz'],
  strip_prefix = "protobuf-3.5.0"
)

#
# gRPC bits
#

git_repository(
  name = "grpc",
  remote = 'https://github.com/grpc/grpc.git',
  commit = '486761d04e03a9183d8013eddd86c3134d52d459'
)

new_http_archive(
    name = "com_github_madler_zlib",
    build_file = "BUILD.zlib",
    strip_prefix = "zlib-cacf7f1d4e3d44d871b605da3b647f07d718623f",
    url = "https://github.com/madler/zlib/archive/cacf7f1d4e3d44d871b605da3b647f07d718623f.tar.gz",
)

http_archive(
    name = "boringssl",
    # on the master-with-bazel branch
    url = "https://boringssl.googlesource.com/boringssl/+archive/886e7d75368e3f4fab3f4d0d3584e4abfc557755.tar.gz",
)

new_http_archive(
    name = "com_github_cares_cares",
    build_file = "BUILD.cares",
    strip_prefix = "c-ares-3be1924221e1326df520f8498d704a5c4c8d0cce",
    url = "https://github.com/c-ares/c-ares/archive/3be1924221e1326df520f8498d704a5c4c8d0cce.tar.gz",
)

new_local_repository(
    name = "cares_local_files",
    build_file = "BUILD.cares_local_files",
    path = 'third_party/cares'
)

# required binds...
bind(
    name = "protobuf",
    actual = "@com_google_protobuf//:protobuf",
)

bind(
    name = "protobuf_clib",
    actual = "@com_google_protobuf//:protoc_lib",
)

bind(
    name = "protocol_compiler",
    actual = "@com_google_protobuf//:protoc",
)

bind(
    name = "grpc_cpp_plugin",
    actual = "@grpc//:grpc_cpp_plugin",
)

bind(
    name = "grpc++",
    actual = "@grpc//:grpc++",
)

bind(
    name = "grpc++_codegen_proto",
    actual = "@grpc//:grpc++_codegen_proto",
)

bind(
    name = "protobuf_headers",
    actual = "@com_google_protobuf//:protobuf_headers",
)

bind(
    name = "zlib",
    actual = "@com_github_madler_zlib//:z",
)

bind(
    name = "libssl",
    actual = "@boringssl//:ssl",
)

bind(
    name = "cares",
    actual = "@com_github_cares_cares//:ares",
)

bind(
    name = "nanopb",
    actual = "@grpc//third_party/nanopb",
)
