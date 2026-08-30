# Auto Recover Ignore

_AutoRecoverIgnore_ is a sandbox setting in [Sandboxie Ini](SandboxieIni.md). It specifies folders or file types that should be ignored by the Immediate Recovery extension of [Quick Recovery](QuickRecovery.md). For example:

```
   .
   .
   .
   [DefaultBox]
   AutoRecoverIgnore=.part
   AutoRecoverIgnore=%Desktop%
   AutoRecoverIgnore=C:\Folder
```

The first example excludes from Immediate Recovery any files ending in _.part_. These files are created by the download manager of the Mozilla browsers, and represent incomplete downloads. When the download completes, the _.part_ extension is removed from the file, thus making it eligible for Immediate Recovery. Note that _.part_ is a default setting.

The second and third examples exclude the specified folders from Immediate Recovery.

Since Sandboxie Plus 1.18.0, entries may contain the wildcards `*` (matches any number of characters), `?` (matches a single character), and `**` (matches any number of characters, including path separators). Paths are matched in their NT, DOS, and network-alias forms.

Since Sandboxie Plus 1.18.0, the exclusion list can also be applied to the [Quick Recovery](QuickRecovery.md) window; see [UseAutoRecoverIgnoreForQuick](UseAutoRecoverIgnoreForQuick.md).

Related [Sandboxie Control](SandboxieControl.md) setting: [Sandbox Settings > Recovery > Immediate Recovery](RecoverySettings.md#immediate-recovery)
