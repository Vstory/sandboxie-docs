# Use Auto Recover Ignore For Quick

_UseAutoRecoverIgnoreForQuick_ is a sandbox setting in [Sandboxie Ini](SandboxieIni.md), available since Sandboxie Plus 1.18.0. It specifies whether the [AutoRecoverIgnore](AutoRecoverIgnore.md) exclusion list is also applied to the [Quick Recovery](QuickRecovery.md) window, hiding matching files from the list of recoverable files.

Usage:

```
   .
   .
   .
   [DefaultBox]
   UseAutoRecoverIgnoreForQuick=n
```

This setting is enabled by default. Set it to _n_ to show all recoverable files in the Quick Recovery window, including files that match [AutoRecoverIgnore](AutoRecoverIgnore.md) patterns.

Note that this only takes effect when the "Show All" checkbox in the Quick Recovery window is not checked.

In SandMan, this corresponds to the "Use the above exclusion list to hide matching files from the Quick Recovery window" checkbox under Sandbox Options > File Recovery > Immediate Recovery.

Related [Sandboxie Ini](SandboxieIni.md) settings: [AutoRecoverIgnore](AutoRecoverIgnore.md), [RecoverFolder](RecoverFolder.md). See also [Quick Recovery](QuickRecovery.md).
