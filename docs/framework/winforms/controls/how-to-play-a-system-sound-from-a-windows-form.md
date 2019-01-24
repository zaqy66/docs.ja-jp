---
title: '方法: Windows フォームからシステム サウンドを再生します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], playing for system events
- playing sounds [Windows Forms], Windows Forms
- system sounds [Windows Forms], playing from Windows Forms
- playing sounds [Windows Forms], system
- SoundPlayer class [Windows Forms], system sounds
- sounds [Windows Forms], playing
- examples [Windows Forms], sounds
ms.assetid: afb206ff-4824-4804-a8d4-185bf5ad8e7c
ms.openlocfilehash: 1883e73f3b1937e8568b751d1cb9f3b57548c010
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649506"
---
# <a name="how-to-play-a-system-sound-from-a-windows-form"></a>方法: Windows フォームからシステム サウンドを再生します。
実行時に `Exclamation` システム サウンドを再生するコード例を次に示します。 システムが出す音の詳細については、次を参照してください。<xref:System.Media.SystemSounds>します。  
  
## <a name="example"></a>例  
  
```vb  
Public Sub PlayExclamation()  
    SystemSounds.Exclamation.Play()  
End Sub  
```  
  
```csharp  
public void playExclamation()  
{  
    SystemSounds.Exclamation.Play();  
}  
```  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   <xref:System.Media?displayProperty=nameWithType> 名前空間への参照  
  
## <a name="see-also"></a>関連項目
- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
- [方法: Windows フォームからビープ音を再生します。](../../../../docs/framework/winforms/controls/how-to-play-a-beep-from-a-windows-form.md)
- [方法: Windows フォームからサウンドを再生します。](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
