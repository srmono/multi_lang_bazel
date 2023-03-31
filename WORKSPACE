#Import Python Rule
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

rules_python_version = "740825b7f74930c62f44af95c9a4c1bd428d2c53" # Latest @ 2021-06-23

http_archive(
    name = "rules_python",
    # Bazel will print the proper value to add here during the first build.
    # sha256 = "FIXME",
    strip_prefix = "rules_python-{}".format(rules_python_version),
    url = "https://github.com/bazelbuild/rules_python/archive/{}.zip".format(rules_python_version),
)

#Tool chain registration
# load("@rules_python//python:repositories.bzl", "py_repositories", "python_register_toolchains")

# py_repositories()

# python_register_toolchains(
#     name = "python3_9",
#     # Available versions are listed in @rules_python//python:versions.bzl.
#     # We recommend using the same version your team is already standardized on.
#     python_version = "3.9",
# )

# load("@python3_9//:defs.bzl", "interpreter")

# load("@rules_python//python:pip.bzl", "pip_parse")

# # Create a central repo that knows about the dependencies needed from
# # requirements_lock.txt.
# pip_parse(
#     name = "python_deps",
#     python_interpreter_target = interpreter,
#     requirements_lock = "//third_pary:requirements.txt",
# )

# # Load the starlark macro which will define your dependencies.
# load("@python_deps//:requirements.bzl", "install_deps")
# # Call it to define repos for your requirements.
# install_deps()


#########################################
#Java Maven imports


RULES_JVM_EXTERNAL_TAG = "2.5"
RULES_JVM_EXTERNAL_SHA = "249e8129914be6d987ca57754516be35a14ea866c616041ff0cd32ea94d2f3a1"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        #"androidx.test.espresso:espresso-core:3.1.1",
        "junit:junit:4.12",
        "com.google.guava:guava:28.0-jre",
    ],
    repositories = [
        "https://jcenter.bintray.com/",
        # "https://uk.maven.org/maven2",
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
)