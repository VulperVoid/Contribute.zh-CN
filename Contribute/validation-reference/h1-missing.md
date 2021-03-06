---
title: h1-missing
description: 有关 Docs 生成问题 issue h1-missing 的解释和解决方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459110"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>警告

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 是指 Markdown 文件中的第一个标题。 发布到 docs.microsoft.com 时，H1 以大字体显示在页面顶部。 H1 的创建方式为，以包含一个井号 (#) 的行开头，后跟空格，然后是标题文本。

## <a name="resolution"></a>解决方法

若要解决此问题，请将 H1 添加为文件中 YML 元数据块后的第一项内容：

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> 此规则不适用于包含的文件。 如果在包含的文件中收到 H1 警告，则很可能需要将包含的文件移动到 `includes` 文件夹。 `includes` 文件夹可以是文件路径中的任何级别。 根据路径，Docs 生成会将该文件识别为包含文件，并且不会运行 H1 验证。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]