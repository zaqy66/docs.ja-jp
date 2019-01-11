---
title: スタートアップ設定スキーマ
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 0a03438968f487f574606f415fb9d43223030038
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222156"
---
# <a name="startup-settings-schema"></a><span data-ttu-id="fd60c-102">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="fd60c-102">Startup settings schema</span></span>

<span data-ttu-id="fd60c-103">スタートアップ設定は、アプリケーションを実行する必要のある共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd60c-103">Startup settings specify the version of the common language runtime that should run the application.</span></span>  
  
|<span data-ttu-id="fd60c-104">要素</span><span class="sxs-lookup"><span data-stu-id="fd60c-104">Element</span></span>|<span data-ttu-id="fd60c-105">説明</span><span class="sxs-lookup"><span data-stu-id="fd60c-105">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fd60c-106">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="fd60c-106">\<requiredRuntime></span></span>](requiredruntime-element.md)|<span data-ttu-id="fd60c-107">バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd60c-107">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="fd60c-108">ランタイムのバージョン 1.1 でビルドされたアプリケーションは、**\<supportedRuntime >** 要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd60c-108">Applications built with runtime version 1.1 should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="fd60c-109">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="fd60c-109">\<supportedRuntime></span></span>](supportedruntime-element.md)|<span data-ttu-id="fd60c-110">アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd60c-110">Specifies which versions of the common language runtime the application supports.</span></span>|  
|[<span data-ttu-id="fd60c-111">\<startup></span><span class="sxs-lookup"><span data-stu-id="fd60c-111">\<startup></span></span>](startup-element.md)|<span data-ttu-id="fd60c-112">**\<requiredRuntime>** 要素と **\<supportedRuntime>** 要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="fd60c-112">Contains the **\<requiredRuntime>** and **\<supportedRuntime>** elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fd60c-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd60c-113">See also</span></span>

- [<span data-ttu-id="fd60c-114">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="fd60c-114">Configuration File Schema</span></span>](../index.md)  
- [<span data-ttu-id="fd60c-115">方法: .NET Framework 4 またはそれ以降のバージョンをサポートするアプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="fd60c-115">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)