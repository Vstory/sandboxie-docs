# Copy Newer（复制较新文件）

_CopyNewer_ 是 [Sandboxie Ini](SandboxieIni.md) 中的一个沙箱设置项，自 Sandboxie Plus 1.18.1 起可用。它用于指定一组文件路径匹配模式：当主机上的对应文件比沙箱内的副本更新时，沙箱内的现有副本将被刷新。

用法示例：

```ini
   .
   .
   .
   [DefaultBox]
   CopyNewer=C:\Data\*.txt
```

通常情况下，文件一旦被复制进沙箱（参见 [文件迁移设置](FileMigrationSettings.md)），沙箱程序会一直使用该副本，即使主机上的原始文件随后被修改。当文件路径匹配某个 _CopyNewer_ 模式时，Sandboxie 会在每次打开该文件时比较主机文件与沙箱副本的最后修改时间；如果主机文件更新，则会在打开完成前将新副本迁移进沙箱。

请注意以下限制：

- 仅适用于沙箱内已存在副本的普通文件，且以常规方式打开时。
- 不适用于文件的初始迁移、目录、仅写方式打开、已删除的文件，以及创建/覆盖操作。
- 模式匹配不区分大小写，匹配的是主机（真实）文件路径。
- 如果刷新正在进行中或刷新失败，沙箱程序将继续使用现有副本。

可以在 SandMan 的“沙箱选项 > 常规选项 > 文件迁移”中管理复制规则，包括“复制较新”类型的规则。

相关的 [Sandboxie Ini](SandboxieIni.md) 设置项：[CopyLimitKb](CopyLimitKb.md)、[CopyLimitSilent](CopyLimitSilent.md)。另请参阅 [文件迁移设置](FileMigrationSettings.md)。
