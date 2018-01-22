genrule(
    name = "copy_headers",
    srcs = [
        "//c-toxcore/toxav:public_headers",
        "//c-toxcore/toxcore:public_headers",
        "//c-toxcore/toxencryptsave:public_headers",
    ],
    outs = [
        "tox/toxav.h",
        "tox/tox.h",
        "tox/toxencryptsave.h",
    ],
    cmd = """
        cp $(location //c-toxcore/toxav:public_headers) $(GENDIR)/c-toxcore/tox/toxav.h
        cp $(location //c-toxcore/toxcore:public_headers) $(GENDIR)/c-toxcore/tox/tox.h
        cp $(location //c-toxcore/toxencryptsave:public_headers) $(GENDIR)/c-toxcore/tox/toxencryptsave.h
    """,
)

cc_library(
    name = "c-toxcore",
    hdrs = [
        "tox/tox.h",
        "tox/toxav.h",
        "tox/toxencryptsave.h",
    ],
    includes = ["."],
    visibility = ["//visibility:public"],
    deps = [
        "//c-toxcore/toxav",
        "//c-toxcore/toxcore",
        "//c-toxcore/toxencryptsave",
    ],
)
