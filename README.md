# ibazel-no-workspace-file

demo repo showing the `ibazel` fails to find the workspace designated by `MODULE.bazel`

## issue

running:

```console
ibazel run //hello:hello
```

results in errors (but confusingly still executes the target):

```console
iBazel [6:27PM]: Querying for files to watch...
iBazel [6:27PM]: Error finding workspace: ibazel was not invoked from within a workspace

iBazel [6:27PM]: Error querying for source files: ibazel was not invoked from within a workspace

iBazel [6:27PM]: Error finding workspace: ibazel was not invoked from within a workspace

iBazel [6:27PM]: Error querying for source files: ibazel was not invoked from within a workspace

iBazel [6:27PM]: Running //hello:hello
Computing main repo mapping:
Loading:
Loading: 0 packages loaded
Analyzing: target //hello:hello (0 packages loaded, 0 targets configured)
INFO: Analyzed target //hello:hello (0 packages loaded, 671 targets configured).
 checking cached actions
INFO: Found 1 target...
 checking cached actions
 checking cached actions

INFO: Elapsed time: 0.373s, Critical Path: 0.00s
 checking cached actions
INFO: 0 processes.
 checking cached actions
INFO: Build completed successfully, 0 total actions
INFO: Analyzed target //hello:hello (0 packages loaded, 0 targets configured).
INFO: Found 1 target...
Target //hello:hello up-to-date:
  bazel-bin/hello/hello_/hello
INFO: Elapsed time: 0.532s, Critical Path: 0.29s
INFO: 6 processes: 4 internal, 2 darwin-sandbox.
INFO: Build completed successfully, 6 total actions
iBazel [6:27PM]: Starting...
iBazel [6:27PM]: Error finding workspace: ibazel was not invoked from within a workspace

Kips-MBP:ibazel-no-workspace-file klandergren$ 2024/03/06 18:27:57 hello world
```
