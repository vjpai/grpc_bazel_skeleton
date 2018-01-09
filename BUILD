cc_binary(
    name = "greeter_client",
    srcs = ["greeter_client.cc"],
    deps = ["//protos:helloworld", "@grpc//:grpc++"],
)

cc_binary(
    name = "greeter_server",
    srcs = ["greeter_server.cc"],
    deps = ["//protos:helloworld", "@grpc//:grpc++"],
)
