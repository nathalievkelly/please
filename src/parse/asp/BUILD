go_library(
    name = 'asp',
    srcs = glob(['*.go'], exclude = [
        '*_test.go',
        '*.bindata.go',
    ]),
    deps = [
        '//src/cli',
        '//src/core',
        '//src/fs',
        '//third_party/go:logging',
    ],
    visibility = ['PUBLIC'],
)

go_test(
    name = 'parser_test',
    srcs = ['parser_test.go'],
    data = ['test_data'],
    deps = [
        ':asp',
        '//third_party/go:testify',
    ],
)

go_test(
    name = 'lexer_test',
    srcs = ['lexer_test.go'],
    deps = [
        ':asp',
        '//third_party/go:testify',
    ],
)

go_test(
    name = 'interpreter_test',
    srcs = ['interpreter_test.go'],
    data = ['test_data'],
    deps = [
        ':asp',
        '//src/core',
        '//src/parse/rules',
        '//third_party/go:testify',
    ],
)

go_test(
    name = 'logging_test',
    srcs = ['logging_test.go'],
    data = ['test_data'],
    deps = [
        ':asp',
        '//src/core',
        '//src/parse/rules',
        '//third_party/go:logging',
        '//third_party/go:testify',
    ],
)

go_test(
    name = 'util_test',
    srcs = ['util_test.go'],
    data = ['test_data'],
    deps = [
        ':asp',
        '//third_party/go:testify',
    ],
)
