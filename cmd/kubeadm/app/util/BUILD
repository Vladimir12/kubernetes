package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "arguments.go",
        "copy.go",
        "endpoint.go",
        "error.go",
        "marshal.go",
        "template.go",
        "version.go",
    ],
    importpath = "k8s.io/kubernetes/cmd/kubeadm/app/util",
    deps = [
        "//cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//vendor/gopkg.in/yaml.v2:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/net:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/validation:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/scheme:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "arguments_test.go",
        "endpoint_test.go",
        "error_test.go",
        "marshal_test.go",
        "template_test.go",
        "version_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//cmd/kubeadm/app/apis/kubeadm/scheme:go_default_library",
        "//cmd/kubeadm/app/apis/kubeadm/v1alpha1:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//cmd/kubeadm/app/util/apiclient:all-srcs",
        "//cmd/kubeadm/app/util/audit:all-srcs",
        "//cmd/kubeadm/app/util/config:all-srcs",
        "//cmd/kubeadm/app/util/dryrun:all-srcs",
        "//cmd/kubeadm/app/util/etcd:all-srcs",
        "//cmd/kubeadm/app/util/kubeconfig:all-srcs",
        "//cmd/kubeadm/app/util/pubkeypin:all-srcs",
        "//cmd/kubeadm/app/util/staticpod:all-srcs",
        "//cmd/kubeadm/app/util/token:all-srcs",
    ],
    tags = ["automanaged"],
)
