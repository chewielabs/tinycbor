set(srcs
    "src/cborencoder_close_container_checked.c"
    "src/cborencoder.c"
    "src/cborerrorstrings.c"
    "src/cborparser_dup_string.c"
    "src/cborparser.c"
    "src/cborpretty_stdio.c"
    "src/cborpretty.c"
    "src/cbortojson.c"
    "src/cborvalidation.c"
)
set(pub_inc_dir "src")
set(pub_deps "")
set(priv_deps "")

idf_component_register(SRCS ${srcs}
                       INCLUDE_DIRS ${pub_inc_dir}
                       REQUIRES ${pub_deps}
                       PRIV_REQUIRES ${priv_deps})
