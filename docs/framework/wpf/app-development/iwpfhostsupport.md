---
title: IWpfHostSupport
ms.date: 03/30/2017
helpviewer_keywords:
- IWpfHostSupport interface [WPF]
ms.assetid: cc5a0281-de81-4cc1-87e4-0e46b1a811e9
ms.openlocfilehash: 57d9ef87a078655a89a5869a48a1bd16f21b000f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43500927"
---
# <a name="iwpfhostsupport"></a>IWpfHostSupport
アプリケーションをホストする[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]PresentationHost.exe でコンテンツがホストと PresentationHost.exe 間の統合のポイントを提供するには、このインターフェイスを実装します。  
  
## <a name="remarks"></a>Remarks  
 [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] Web ブラウザーなどのアプリケーションをホストできます[!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)]コンテンツを含む[!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)]XAML が失われるとします。 ホストに[!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)]コンテンツ、[!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)]アプリケーションのインスタンスを作成する、 [WebBrowser コントロール](https://go.microsoft.com/fwlink/?LinkId=97911)します。 ホストされる[!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)]PresentationHost.exe、提供、ホスト型のインスタンスを作成します[!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)]コンテンツ ホストに表示するために、 [WebBrowser コントロール](https://go.microsoft.com/fwlink/?LinkId=97911)します。  
  
 有効になっている統合`IWpfHostSupport`PresentationHost.exe できます。  
  
-   検出し、ホスト アプリケーションが関心を未加工入力デバイス (ヒューマン インターフェイス デバイス) を登録します。  
  
-   未加工入力デバイスを登録し、適切なメッセージを転送から、ホスト アプリケーションへの入力メッセージを受信します。  
  
-   ホスト アプリケーションの進行状況とエラーのカスタム ユーザー インターフェイスをクエリします。  
  
> [!NOTE]
>  この API は、ローカル クライアント コンピューターでの使用のみを目的とし、サポートされています。  
  
## <a name="members"></a>メンバー  
  
|メンバー|説明|  
|------------|-----------------|  
|[GetRawInputDevices](../../../../docs/framework/wpf/app-development/getrawinputdevices.md)|PresentationHost.exe が、ホスト アプリケーションに必要な未加工入力デバイス (ヒューマン インターフェイス デバイス) を検出できるようにします。|  
|[FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md)|E_NOTIMPL が返されない限り、メッセージを受信するたびに PresentationHost.exe によって呼び出されます。|  
|[GetCustomUI](../../../../docs/framework/wpf/app-development/getcustomui.md)|既定では、PresentationHost.exe は、独自のデプロイの進行状況と配置エラー WPF コンテンツが展開されているときに表示されるユーザー インターフェイス。|
