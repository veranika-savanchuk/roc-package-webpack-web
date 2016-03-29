# Settings for `roc-package-webpack-web-dev`

## Build

| Name               | Description                                                                                              | Path                      | CLI option                  | Default          | Type                    | Required |
| ------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | ---------------- | ----------------------- | -------- |
| assets             | An array of files to include into the build process.                                                     | build.assets              | --build-assets              | `null`           | `[Filepath]`            | No       |
| disableProgressbar | Should the progress bar be disabled for builds.                                                          | build.disableProgressbar  | --build-disableProgressbar  | `false`          | `Boolean`               | No       |
| input              | The entry point for the build.                                                                           | build.input               | --build-input               | `"src/index.js"` | `Filepath / [Filepath]` | No       |
| mode               | What mode the application should be built for. Possible values are &quot;dev&quot; and &quot;dist&quot;. | build.mode                | --build-mode                | `"dist"`         | `/^dev|dist$/i`         | No       |
| output             | The output directory for the build.                                                                      | build.output              | --build-output              | `"build"`        | `Filepath / [Filepath]` | No       |
| outputName         | The name of the generated application bundle, will be appended &quot;roc.js&quot;.                       | build.outputName          | --build-outputName          | `"app"`          | `String / [String]`     | No       |
| path               | The basepath for the application.                                                                        | build.path                | --build-path                | `"/"`            | `Filepath`              | No       |
| targets            | For what targets the code should be built for.                                                           | build.targets             | --build-targets             | `["web"]`        | `/web/`                 | No       |

## Dev

| Name               | Description                                                                                              | Path                      | CLI option                  | Default          | Type                    | Required |
| ------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | ---------------- | ----------------------- | -------- |
| debug              | Filter for debug messages that should be shown during development, see https://npmjs.com/package/debug.  | dev.debug                 | --dev-debug                 | `"roc:*"`        | `String`                | No       |
| port               | Port for the dev server.                                                                                 | dev.port                  | --dev-port                  | `3001`           | `Integer`               | No       |

### DevMiddleware

| Name               | Description                                                                                              | Path                      | CLI option                  | Default          | Type                    | Required |
| ------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | ---------------- | ----------------------- | -------- |
| noInfo             | If no info should be sent to the console.                                                                | dev.devMiddleware.noInfo  | --dev-devMiddleware-noInfo  | `true`           | `Boolean`               | No       |
| quiet              | If nothing should be sent to the console.                                                                | dev.devMiddleware.quiet   | --dev-devMiddleware-quiet   | `false`          | `Boolean`               | No       |

### HotMiddleware

| Name               | Description                                                                                              | Path                      | CLI option                  | Default          | Type                    | Required |
| ------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | ---------------- | ----------------------- | -------- |
| noInfo             | If no info should be sent to the console.                                                                | dev.hotMiddleware.noInfo  | --dev-hotMiddleware-noInfo  | `false`          | `Boolean`               | No       |
| overlay            | If a overlay should be shown when an error has occurred.                                                 | dev.hotMiddleware.overlay | --dev-hotMiddleware-overlay | `false`          | `Boolean`               | No       |
| quiet              | If nothing should be sent to the console.                                                                | dev.hotMiddleware.quiet   | --dev-hotMiddleware-quiet   | `false`          | `Boolean`               | No       |
| reload             | If the browser should be reloaded if it fails to hot update the code.                                    | dev.hotMiddleware.reload  | --dev-hotMiddleware-reload  | `true`           | `Boolean`               | No       |