load("@rules_java//java:defs.bzl", "java_binary", "java_library", "java_test")

java_library(
    name="java-maven-lib",
    srcs = glob(["src/main/java/com/example/myproject/*.java"]),
    deps = [
        "@maven//:com_google_guava_guava"
        ]
)

java_binary(
    name="java-maven",
    main_class = "com.example.myproject.App",
    runtime_deps = [":java-maven-lib"]
)

java_test(
    name = "tests",
    srcs = glob(["src/main/java/com/example/myproject/*.java"]),
    test_class = "com.example.myproject.TestApp",
    deps = [
        "java-maven-lib",
        "@maven//:com_google_guava_guava",
        "@maven//:junit_junit"
    ]
)

