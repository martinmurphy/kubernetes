package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "ipconfig.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/util/ipconfig",
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/utils/exec:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["ipconfig_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/pkg/util/ipconfig",
    deps = ["//vendor/k8s.io/utils/exec:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
