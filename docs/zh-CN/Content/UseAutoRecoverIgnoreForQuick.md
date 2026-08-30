# 在快速恢复中应用自动恢复忽略

_UseAutoRecoverIgnoreForQuick_ 是 [Sandboxie Ini](SandboxieIni.md) 配置文件中的一个沙箱设置，自 Sandboxie Plus 1.18.0 起可用。它用于指定是否将 [自动恢复忽略](AutoRecoverIgnore.md) 的排除列表同时应用于 [快速恢复](QuickRecovery.md) 窗口，从而在可恢复文件列表中隐藏匹配的文件。

用法示例：

```ini
   .
   .
   .
   [DefaultBox]
   UseAutoRecoverIgnoreForQuick=n
```

此设置默认为启用状态。设置为 _n_ 时，快速恢复窗口将显示所有可恢复文件，包括匹配 [自动恢复忽略](AutoRecoverIgnore.md) 模式的文件。

请注意，此设置仅在快速恢复窗口中未勾选“显示全部”复选框时生效。

在 SandMan 中，对应的选项为“沙箱选项 > 文件恢复 > 即时恢复”下的“使用上述排除列表在快速恢复窗口中隐藏匹配的文件”复选框。

相关的 [Sandboxie Ini](SandboxieIni.md) 设置项：[自动恢复忽略](AutoRecoverIgnore.md)、[恢复文件夹](RecoverFolder.md)。另请参阅 [快速恢复](QuickRecovery.md)。
