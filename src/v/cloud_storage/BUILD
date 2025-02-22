load("//bazel:build.bzl", "redpanda_cc_library")

redpanda_cc_library(
    name = "remote_label",
    hdrs = [
        "remote_label.h",
    ],
    include_prefix = "cloud_storage",
    visibility = ["//visibility:public"],
    deps = [
        "//src/v/model",
        "//src/v/serde",
        "//src/v/serde:uuid",
    ],
)

redpanda_cc_library(
    name = "topic_mount_manifest_path",
    srcs = [
        "topic_mount_manifest_path.cc",
    ],
    hdrs = [
        "topic_mount_manifest_path.h",
    ],
    include_prefix = "cloud_storage",
    visibility = [
        "//visibility:public",
    ],
    deps = [
        "//src/v/base",
        "//src/v/model",
    ],
)

redpanda_cc_library(
    name = "cloud_storage",
    srcs = [
        "access_time_tracker.cc",
        "anomalies_detector.cc",
        "async_manifest_view.cc",
        "base_manifest.cc",
        "cache_probe.cc",
        "cache_service.cc",
        "download_exception.cc",
        "inventory/aws_ops.cc",
        "inventory/inv_consumer.cc",
        "inventory/inv_ops.cc",
        "inventory/ntp_hashes.cc",
        "inventory/report_parser.cc",
        "inventory/types.cc",
        "inventory/utils.cc",
        "materialized_manifest_cache.cc",
        "materialized_resources.cc",
        "offset_translation_layer.cc",
        "partition_manifest.cc",
        "partition_manifest_downloader.cc",
        "partition_path_utils.cc",
        "read_path_probes.cc",
        "recovery_errors.cc",
        "recovery_request.cc",
        "recovery_utils.cc",
        "recursive_directory_walker.cc",
        "remote.cc",
        "remote_file.cc",
        "remote_partition.cc",
        "remote_path_provider.cc",
        "remote_probe.cc",
        "remote_segment.cc",
        "remote_segment_index.cc",
        "segment_chunk.cc",
        "segment_chunk_api.cc",
        "segment_chunk_data_source.cc",
        "segment_meta_cstore.cc",
        "segment_path_utils.cc",
        "segment_state.cc",
        "topic_manifest.cc",
        "topic_manifest_downloader.cc",
        "topic_mount_handler.cc",
        "topic_mount_manifest.cc",
        "topic_path_utils.cc",
        "tx_range_manifest.cc",
        "types.cc",
    ],
    hdrs = [
        "access_time_tracker.h",
        "anomalies_detector.h",
        "async_manifest_view.h",
        "base_manifest.h",
        "cache_probe.h",
        "cache_service.h",
        "configuration.h",
        "download_exception.h",
        "fwd.h",
        "inventory/aws_ops.h",
        "inventory/inv_consumer.h",
        "inventory/inv_ops.h",
        "inventory/ntp_hashes.h",
        "inventory/report_parser.h",
        "inventory/types.h",
        "inventory/utils.h",
        "lifecycle_marker.h",
        "logger.h",
        "materialized_manifest_cache.h",
        "materialized_resources.h",
        "offset_translation_layer.h",
        "partition_manifest.h",
        "partition_manifest_downloader.h",
        "partition_path_utils.h",
        "read_path_probes.h",
        "recovery_errors.h",
        "recovery_request.h",
        "recovery_utils.h",
        "recursive_directory_walker.h",
        "remote.h",
        "remote_file.h",
        "remote_partition.h",
        "remote_path_provider.h",
        "remote_probe.h",
        "remote_segment.h",
        "remote_segment_index.h",
        "segment_chunk.h",
        "segment_chunk_api.h",
        "segment_chunk_data_source.h",
        "segment_meta_cstore.h",
        "segment_path_utils.h",
        "segment_state.h",
        "spillover_manifest.h",
        "topic_manifest.h",
        "topic_manifest_downloader.h",
        "topic_mount_handler.h",
        "topic_mount_manifest.h",
        "topic_path_utils.h",
        "tx_range_manifest.h",
        "types.h",
    ],
    include_prefix = "cloud_storage",
    visibility = ["//visibility:public"],
    deps = [
        ":remote_label",
        ":topic_mount_manifest_path",
        "//src/v/base",
        "//src/v/bytes:iobuf",
        "//src/v/bytes:iobuf_parser",
        "//src/v/bytes:iostream",
        "//src/v/bytes:streambuf",
        "//src/v/cloud_io:auth_refresh_bg_op",
        "//src/v/cloud_io:basic_cache_service_api",
        "//src/v/cloud_io:io_resources",
        "//src/v/cloud_io:io_result",
        "//src/v/cloud_io:remote",
        "//src/v/cloud_io:transfer_details",
        "//src/v/cloud_roles",
        "//src/v/cloud_storage_clients",
        "//src/v/cluster:nt_revision",
        "//src/v/cluster:run_quota",
        "//src/v/cluster:topic_configuration",
        "//src/v/compression",
        "//src/v/config",
        "//src/v/container:fragmented_vector",
        "//src/v/container:intrusive",
        "//src/v/hashing:xx",
        "//src/v/json",
        "//src/v/metrics",
        "//src/v/model",
        "//src/v/net",
        "//src/v/raft",
        "//src/v/random:time_jitter",
        "//src/v/reflection:adl",
        "//src/v/reflection:to_tuple",
        "//src/v/reflection:type_traits",
        "//src/v/resource_mgmt:io_priority",
        "//src/v/resource_mgmt:memory_groups",
        "//src/v/serde",
        "//src/v/serde:enum",
        "//src/v/serde:iobuf",
        "//src/v/serde:optional",
        "//src/v/serde:sstring",
        "//src/v/serde:vector",
        "//src/v/ssx:future_util",
        "//src/v/ssx:semaphore",
        "//src/v/ssx:sformat",
        "//src/v/ssx:task_local",
        "//src/v/ssx:watchdog",
        "//src/v/storage",
        "//src/v/utils:adjustable_semaphore",
        "//src/v/utils:delta_for",
        "//src/v/utils:directory_walker",
        "//src/v/utils:human",
        "//src/v/utils:lazy_abort_source",
        "//src/v/utils:log_hist",
        "//src/v/utils:mutex",
        "//src/v/utils:named_type",
        "//src/v/utils:retry_chain_node",
        "//src/v/utils:stream_provider",
        "//src/v/utils:stream_utils",
        "//src/v/utils:to_string",
        "//src/v/utils:token_bucket",
        "//src/v/utils:tracking_allocator",
        "@abseil-cpp//absl/container:btree",
        "@abseil-cpp//absl/container:node_hash_map",
        "@abseil-cpp//absl/container:node_hash_set",
        "@boost//:algorithm",
        "@boost//:beast",
        "@boost//:iterator",
        "@boost//:lexical_cast",
        "@boost//:outcome",
        "@boost//:property_tree",
        "@boost//:range",
        "@boost//:uuid",
        "@fmt",
        "@rapidjson",
        "@re2",
        "@seastar",
        "@zlib",
    ],
)
