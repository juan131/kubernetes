package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "kube-dns",
    library = ":go_default_library",
    tags = ["automanaged"],
)

go_library(
    name = "go_default_library",
    srcs = ["dns.go"],
    tags = ["automanaged"],
    deps = [
        "//cmd/kube-dns/app:go_default_library",
        "//cmd/kube-dns/app/options:go_default_library",
        "//pkg/client/metrics/prometheus:go_default_library",
        "//pkg/util/flag:go_default_library",
        "//pkg/util/logs:go_default_library",
        "//pkg/version:go_default_library",
        "//pkg/version/prometheus:go_default_library",
        "//pkg/version/verflag:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/spf13/pflag",
    ],
)
