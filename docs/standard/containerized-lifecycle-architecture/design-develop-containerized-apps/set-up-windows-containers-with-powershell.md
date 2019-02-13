---
title: DockerFile で Windows PowerShell コマンドを使用して Windows コンテナー (Docker 標準ベース) を設定するには
description: Windows コンテナーで Docker を使用する場合は、PowerShell を使用する方法について説明します
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: df9e98e3f963b6492e1008455251b61a8cb6e771
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219972"
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a>DockerFile で Windows PowerShell コマンドを使用して Windows コンテナー (Docker 標準ベース) を設定するには

[Windows コンテナー](/virtualization/windowscontainers/about/index)、Docker イメージを既存の Windows アプリケーションを変換し、Docker エコシステムの残りの部分と同じツールで展開したりできます。

Windows コンテナーを使用するには、だけです、DockerFile で Windows PowerShell コマンドを記述する次の例に示すよう。

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

この場合、IIS だけでなく Windows Server Core 基本イメージをインストールする Windows PowerShell を使用しています。

同様の方法で使用することもできます Windows PowerShell コマンド、従来の ASP.NET などの追加コンポーネントを設定する 4.x および .NET 4.6、またはその他の Windows ソフトウェア、次のようにします。

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
>[前へ](visual-studio-tools-for-docker.md)
>[次へ](build-aspnet-core-applications-linux-containers-aks-kubernetes.md)
