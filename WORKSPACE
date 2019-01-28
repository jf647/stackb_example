# Copyright 2019 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_stack_rules_proto",
    sha256 = "36f11f56f6eb48a81eb6850f4fb6c3b4680e3fc2d3ceb9240430e28d32c47009",
    strip_prefix = "rules_proto-d86ca6bc56b1589677ec59abfa0bed784d6b7767",
    urls = ["https://github.com/stackb/rules_proto/archive/d86ca6bc56b1589677ec59abfa0bed784d6b7767.tar.gz"],
)

load("@build_stack_rules_proto//github.com/gogo/protobuf:deps.bzl", "gogo_proto_compile", "gogo_proto_library")

gogo_proto_library()

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains()
