licenses(["notice"])  # Apache 2

load(
    "@envoy//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "solo_filter_utility_lib",
    srcs = ["solo_filter_utility.cc"],
    hdrs = ["solo_filter_utility.h"],
    repository = "@envoy",
    deps = [
        "@envoy//include/envoy/server:filter_config_interface",
        "@envoy//include/envoy/upstream:cluster_manager_interface",
        "@envoy//source/common/common:assert_lib",
        "@envoy//source/common/common:logger_lib",
        "@envoy//source/common/common:utility_lib",
    ],
)

envoy_cc_library(
    name = "functional_stream_decoder_base_lib",
    srcs = ["functional_stream_decoder_base.cc"],
    hdrs = ["functional_stream_decoder_base.h"],
    repository = "@envoy",
    deps = [
        "//:functional_base_proto_cc",
        "//include/envoy/http:metadata_accessor_interface",
        "//source/common/config:solo_well_known_names_lib",
        "//source/common/http:solo_filter_utility_lib",
        "@envoy//include/envoy/registry",
        "@envoy//include/envoy/server:filter_config_interface",
        "@envoy//include/envoy/upstream:cluster_manager_interface",
        "@envoy//source/common/common:assert_lib",
        "@envoy//source/common/common:logger_lib",
        "@envoy//source/common/common:utility_lib",
        "@envoy//source/common/http:filter_utility_lib",
        "@envoy//source/common/http:utility_lib",
        "@envoy//source/common/protobuf:utility_lib",
        "@envoy//source/extensions/filters/http/common:empty_http_filter_config_lib",
    ],
)

envoy_cc_library(
    name = "route_enabled_filter_wrapper_lib",
    srcs = [],
    hdrs = ["route_enabled_filter_wrapper.h"],
    repository = "@envoy",
    deps = [
        "//source/common/http:solo_filter_utility_lib",
        "@envoy//include/envoy/server:filter_config_interface",
        "@envoy//source/common/common:assert_lib",
        "@envoy//source/common/common:utility_lib",
        "@envoy//source/common/http:utility_lib",
    ],
)
