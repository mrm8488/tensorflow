licenses(["notice"])  # Apache 2.0

load("//tensorflow:tensorflow.bzl", "py_test")

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)

py_library(
    name = "converters",
    srcs = [
        "asserts.py",
        "break_statements.py",
        "builtin_functions.py",
        "call_trees.py",
        "continue_statements.py",
        "control_flow.py",
        "decorators.py",
        "for_loops.py",
        "list_comprehension.py",
        "logical_expressions.py",
        "side_effect_guards.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        "@gast_archive//:gast",
    ],
)

py_library(
    name = "test_lib",
    srcs = [
        "converter_test_base.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":converters",
        "//tensorflow/contrib/py2tf/pyct/static_analysis",
        "//tensorflow/contrib/py2tf/utils",
        "@gast_archive//:gast",
        "@six_archive//:six",
    ],
)

py_test(
    name = "asserts_test",
    srcs = ["asserts_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "break_statements_test",
    srcs = ["break_statements_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "builtin_functions_test",
    srcs = ["builtin_functions_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "call_trees_test",
    srcs = ["call_trees_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "continue_statements_test",
    srcs = ["continue_statements_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "control_flow_test",
    srcs = ["control_flow_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "decorators_test",
    srcs = ["decorators_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "for_loops_test",
    srcs = ["for_loops_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "list_comprehension_test",
    srcs = ["list_comprehension_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "logical_expressions_test",
    srcs = ["logical_expressions_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)

py_test(
    name = "side_effect_guards_test",
    srcs = ["side_effect_guards_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_lib",
        "//tensorflow/contrib/py2tf/pyct",
        "//tensorflow/python:client_testlib",
    ],
)
