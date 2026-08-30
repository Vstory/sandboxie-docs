# Copy Newer

_CopyNewer_ is a sandbox setting in [Sandboxie Ini](SandboxieIni.md), available since Sandboxie Plus 1.18.1. It specifies a list of file path patterns for which an existing sandbox copy of a file is refreshed when the matching file on the host has been modified more recently.

Usage:

```
   .
   .
   .
   [DefaultBox]
   CopyNewer=C:\Data\*.txt
```

Normally, once a file has been copied into the sandbox (see [File Migration Settings](FileMigrationSettings.md)), a sandboxed program keeps using that copy even if the original file on the host is changed later. When a file path matches a _CopyNewer_ pattern, Sandboxie compares the last-write time of the host file with the sandboxed copy each time the file is opened; if the host file is newer, a fresh copy is migrated into the sandbox before the open completes.

Please note the following limitations:

- It only applies to regular files that already have a copy inside the sandbox, when they are opened normally.
- It does not apply to the initial migration of a file, to directories, to write-only opens, to deleted files, or to create/overwrite operations.
- Pattern matching is case-insensitive and is applied to the host (true) file path.
- If a refresh is already in progress or fails, the existing sandbox copy remains available to the program.

Copy rules, including rules of type "Copy newer", can be managed in SandMan under Sandbox Options > General Options > File Migration.

Related [Sandboxie Ini](SandboxieIni.md) settings: [CopyLimitKb](CopyLimitKb.md), [CopyLimitSilent](CopyLimitSilent.md). See also [File Migration Settings](FileMigrationSettings.md).
