load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "gogo.pb.go",
        "helper.go",
    ],
    importpath = "github.com/gogo/protobuf/gogoproto",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
        "//vendor/github.com/gogo/protobuf/protoc-gen-gogo/descriptor:go_default_library",
    ],
)

proto_library(
    name = "gogoproto_proto",
    srcs = ["gogo.proto"],
    visibility = ["//visibility:public"],
    deps = ["@com_google_protobuf//:descriptor_proto"],
)

go_proto_library(
    name = "gogoproto_go_proto",
    importpath = "github.com/gogo/protobuf/gogoproto",
    proto = ":gogoproto_proto",
    visibility = ["//visibility:public"],
    deps = ["@com_github_golang_protobuf//ptypes/descriptor:go_default_library"],
)
