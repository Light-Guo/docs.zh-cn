---
ms.openlocfilehash: cc6d96bd614ff015ae2125c0f1477e18a91a68f7
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2020
ms.locfileid: "67802601"
---
### <a name="svctraceviewer-combobox-high-contrast-change"></a>svcTraceViewer ComboBox 对比度更改

|   |   |
|---|---|
|详细信息|在 [Microsoft Service Trace Viewer 工具](~/docs/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe.md)中，在某些高对比度主题中，ComboBox 控件未以正确的颜色显示。 此问题已在 .NET Framework 4.7.2 中解决。 但是，由于 .NET Framework SDK 后向兼容性要求，因此默认情况下客户无法看到该修复程序。 .NET 4.8 通过将以下 [AppContext 配置开关](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)添加到 svcTraceViewer.exe.config 文件来表示此更改：<pre><code class="lang-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false;Switch.UseLegacyAccessibilityFeatures.2=false&quot; /&gt;&#13;&#10;</code></pre>|
|建议|<ul><li>如何选择退出更改 如果不希望更改高对比度行为，可通过从 svcTraceViewer.exe.config 文件中删除以下部分来禁用它：</li></ul><pre><code class="lang-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false;Switch.UseLegacyAccessibilityFeatures.2=false&quot; /&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|Version|4.8|
|类型|运行时|
