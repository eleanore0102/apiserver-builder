load("@io_bazel_rules_go//proto:def.bzl", "go_grpc_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "OpenAPIv3.go",
        "OpenAPIv3.pb.go",
    ],
    importpath = "github.com/googleapis/gnostic/OpenAPIv3",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/golang/protobuf/proto:go_default_library",
        "//vendor/github.com/golang/protobuf/ptypes/any:go_default_library",
        "//vendor/github.com/googleapis/gnostic/compiler:go_default_library",
        "//vendor/gopkg.in/yaml.v2:go_default_library",
    ],
)

proto_library(
    name = "openapi_v3_proto",
    srcs = ["OpenAPIv3.proto"],
    visibility = ["//visibility:public"],
    deps = ["@com_google_protobuf//:any_proto"],
)

go_grpc_library(
    name = "openapi_v3_go_proto",
    importpath = "github.com/googleapis/gnostic/OpenAPIv3",
    proto = ":openapi_v3_proto",
    visibility = ["//visibility:public"],
    deps = ["@com_github_golang_protobuf//ptypes/any:go_default_library"],
)
