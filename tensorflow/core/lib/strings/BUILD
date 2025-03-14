package(
    default_visibility = [
        "//tensorflow:__subpackages__",
    ],
    licenses = ["notice"],  # Apache 2.0
)

# Todo(bmzhao): Remaining targets to add to this BUILD file are:
# base64, proto_serialization, proto_text_util, and all tests.
# Note: proto_serialization depends on target lib/hash:hash being added.

cc_library(
    name = "ordered_code",
    srcs = ["ordered_code.cc"],
    hdrs = ["ordered_code.h"],
    deps = [
        "//tensorflow/core/platform:logging",
        "//tensorflow/core/platform:macros",
        "//tensorflow/core/platform:stringpiece",
        "//tensorflow/core/platform:types",
    ],
)

cc_library(
    name = "scanner",
    srcs = ["scanner.cc"],
    hdrs = ["scanner.h"],
    deps = [
        ":string_utils",
        "//tensorflow/core/platform:macros",
        "//tensorflow/core/platform:stringpiece",
    ],
)

cc_library(
    name = "string_utils",
    srcs = [
        "numbers.cc",
        "str_util.cc",
        "strcat.cc",
    ],
    hdrs = [
        "numbers.h",
        "str_util.h",
        "strcat.h",
    ],
    deps = [
        "//tensorflow/core/lib/gtl:stl_util",
        "//tensorflow/core/platform:logging",
        "//tensorflow/core/platform:macros",
        "//tensorflow/core/platform:stringpiece",
        "//tensorflow/core/platform:stringprintf",
        "//tensorflow/core/platform:types",
        "@com_google_absl//absl/base:core_headers",
        "@com_google_absl//absl/strings",
        "@double_conversion//:double-conversion",
    ],
)

cc_library(
    name = "stringprintf",
    hdrs = ["stringprintf.h"],
    deps = ["//tensorflow/core/platform:stringprintf"],
)

filegroup(
    name = "legacy_lib_strings_all_headers",
    srcs = [
        "base64.h",
        "numbers.h",
        "ordered_code.h",
        "proto_serialization.h",
        "proto_text_util.h",
        "scanner.h",
        "str_util.h",
        "strcat.h",
        "stringprintf.h",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_strings_all_srcs",
    srcs = [
        "base64.cc",
        "numbers.cc",
        "ordered_code.cc",
        "proto_serialization.cc",
        "proto_text_util.cc",
        "scanner.cc",
        "str_util.cc",
        "strcat.cc",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_strings_all_tests",
    srcs = [
        "base64_test.cc",
        "numbers_test.cc",
        "ordered_code_test.cc",
        "proto_serialization_test.cc",
        "scanner_test.cc",
        "str_util_test.cc",
        "strcat_test.cc",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_proto_parsing_headers",
    srcs = [
        "numbers.h",
        "strcat.h",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_string_headers",
    srcs = [
        "numbers.h",
        "proto_serialization.h",
        "str_util.h",
        "strcat.h",
        "stringprintf.h",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_internal_public_string_headers",
    srcs = [
        "base64.h",
        "ordered_code.h",
        "proto_serialization.h",
        "proto_text_util.h",
        "scanner.h",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_lib_android_gif_internal_string_headers",
    srcs = [
        "numbers.h",
        "strcat.h",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_low_level_library_tests",
    srcs = [
        "base64_test.cc",
        "numbers_test.cc",
        "scanner_test.cc",
        "str_util_test.cc",
        "strcat_test.cc",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_strings_ordered_code_test",
    srcs = [
        "ordered_code_test.cc",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)

filegroup(
    name = "legacy_strings_proto_serialization_test",
    srcs = [
        "proto_serialization_test.cc",
    ],
    visibility = ["//tensorflow/core:__pkg__"],
)
