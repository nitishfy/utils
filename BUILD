package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "http.go",
        "interface.go",
        "port_range.go",
        "port_split.go",
        "util.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/util/sets:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:golang.org/x/net/http2",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "http_test.go",
        "interface_test.go",
        "port_range_test.go",
        "port_split_test.go",
        "util_test.go",
    ],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/util/sets:go_default_library",
        "//vendor:github.com/spf13/pflag",
    ],
)
