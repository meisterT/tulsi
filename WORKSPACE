load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "build_bazel_rules_apple",
    commit = "cd68dbfd4f4531270da498b3fc1f71fb66343d27",
    remote = "https://github.com/bazelbuild/rules_apple.git",
    shallow_since = "1570832445 -0700",
)

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)

apple_rules_dependencies()

# @build_bazel_rule_swift is already defined via apple_rules_dependencies above.
# This helps ensure that Tulsi, rules_apple, etc. are using the same versions.
load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

# @build_bazel_apple_support is already defined via apple_rules_dependencies above.
# This helps ensure that Tulsi, rules_apple, etc. are using the same versions.
load(
    "@build_bazel_apple_support//lib:repositories.bzl",
    "apple_support_dependencies",
)

apple_support_dependencies()
