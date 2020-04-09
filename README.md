# A trivial typescript repo that builds both with bazel and standard npm
# module handling
`app` imports module as `@root/module`.
Bazel build handles that on its own thanks to
[module_name](https://github.com/igors/bazel_modules_test/blob/master/module/BUILD.bazel#L8).
npm build just installs the symlink with [npm](https://github.com/igors/bazel_modules_test/blob/master/app/package.json#L16).
## Bazel build
`bazel run //app:bin`
## npm build
`cd modules && npm install && npm run build`

`cd app && npm install && npm run build`
