package(default_visibility = ["//visibility:public"])

cc_library(
    name = "dribble_tactic",
    srcs = ["dribble_tactic.cpp"],
    hdrs = [
        "dribble_fsm.h",
        "dribble_tactic.h",
    ],
    deps = [
        "//shared:constants",
        "//software/ai/evaluation:pass",
        "//software/ai/hl/stp/action:stop_action",
        "//software/ai/hl/stp/tactic",
        "//software/ai/hl/stp/tactic/move:move_tactic",
        "//software/ai/intent:move_intent",
        "//software/logger",
    ],
)

cc_test(
    name = "dribble_fsm_test",
    srcs = ["dribble_fsm_test.cpp"],
    deps = [
        ":dribble_tactic",
        "//software/test_util",
        "@gtest//:gtest_main",
    ],
)

cc_test(
    name = "simulated_dribble_tactic_test",
    srcs = ["simulated_dribble_tactic_test.cpp"],
    deps = [
        ":dribble_tactic",
        "//software/simulated_tests:simulated_tactic_test_fixture",
        "//software/simulated_tests:simulated_test_main",
        "//software/simulated_tests/non_terminating_validation_functions",
        "//software/simulated_tests/terminating_validation_functions",
        "//software/simulated_tests/validation:validation_function",
        "//software/test_util",
        "//software/time:duration",
        "//software/world",
    ],
)
