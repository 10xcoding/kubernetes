package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["cidr_set_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//staging/src/k8s.io/component-base/metrics/testutil:go_default_library",
        "//vendor/k8s.io/klog/v2:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "cidr_set.go",
        "metrics.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/controller/nodeipam/ipam/cidrset",
    deps = [
        "//staging/src/k8s.io/component-base/metrics:go_default_library",
        "//staging/src/k8s.io/component-base/metrics/legacyregistry:go_default_library",
    ],
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
