py_binary(
    name = "calculator",
    srcs = ["calculator.py"],
    visibility = ["//visibility:public"]
)

py_test(
    name = "calculator_test",
    srcs=["calculator_test.py"],
    deps = [
        "//projects/python:calculator"
    ]
)