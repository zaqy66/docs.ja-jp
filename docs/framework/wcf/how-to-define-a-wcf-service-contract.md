---
title: '方法 : Windows Communication Foundation サービス コントラクトを定義する'
ms.date: 09/14/2018
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: 4f85a51c47eb045d1d2f0111cb217199c9acf0d7
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2018
ms.locfileid: "46537879"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a>方法 : Windows Communication Foundation サービス コントラクトを定義する

これは、最初の基本的な Windows Communication Foundation (WCF) アプリケーションを作成するために必要な 6 つのタスクです。 6 つのすべてのタスクの概要については、「[チュートリアル入門](../../../docs/framework/wcf/getting-started-tutorial.md)」を参照してください。

 WCF サービスを作成するときに、最初のタスクは、サービス コントラクトを定義します。 サービス コントラクトは、サービスがサポートする操作を指定します。 操作は Web サービス メソッドと見なすことができます。 コントラクトは C++、C#、または Visual Basic (VB) インターフェイスを定義することで作成します。 インターフェイスの各メソッドは、特定のサービス操作に対応しています。 各インターフェイスには <xref:System.ServiceModel.ServiceContractAttribute> が適用されており、各操作には <xref:System.ServiceModel.OperationContractAttribute> 属性が適用されている必要があります。 <xref:System.ServiceModel.ServiceContractAttribute> 属性を持つインターフェイス内のメソッドに <xref:System.ServiceModel.OperationContractAttribute> 属性がない場合、そのメソッドはサービスによって公開されません。

 手順の後に、このタスクに使用するコード例を示します。

## <a name="define-a-service-contract"></a>サービス コントラクトを定義します。

1. プログラムを右クリックして、管理者として Visual Studio を開き、**開始**メニュー**詳細** > **管理者として実行**します。

2. WCF サービス ライブラリ プロジェクトを作成します。

   1. **[ファイル]** メニューで、**[新規作成]**、 > **[プロジェクト]** の順に作成します。

   2. **新しいプロジェクト**] ダイアログの左側にある [展開**Visual c#** または**Visual Basic**、クリックして、 **WCF**カテゴリ。 プロジェクト テンプレートの一覧は、ダイアログの中央のセクションに表示されます。 選択**WCF サービス ライブラリ**します。

   3. 入力`GettingStartedLib`で、**名前**textbox と`GettingStarted`で、**ソリューション名**ダイアログの下部にあるテキスト ボックス。

   > [!NOTE]
   > 表示されない場合、 **WCF**プロジェクト テンプレートのカテゴリをインストールする必要があります、 **Windows Communication Foundation** Visual Studio のコンポーネント。 **新しいプロジェクト** ダイアログ ボックスと書かれたリンクをクリックして**Visual Studio インストーラーを開く**します。 選択、**個々 のコンポーネント**] タブの [、し、検索して選択します**Windows Communication Foundation**下、**開発アクティビティ**カテゴリ。 選択**変更**コンポーネントのインストールを開始します。

   Visual Studio は、3 つのファイルを含むプロジェクトを作成します: IService1.cs (または IService1.vb)、Service1.cs (または Service1.vb) と App.config です。IService1 ファイルには、既定のサービス コントラクトが含まれています。 Service1 ファイルには、サービス コントラクトの既定の実装が含まれています。 App.config ファイルには、Visual Studio WCF サービス ホストに既定のサービスを読み込むために必要な構成が含まれています。 WCF サービス ホスト ツールの詳細については、次を参照してください[WCF サービス ホスト (WcfSvcHost.exe)。](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)

3. IService1.cs または IService1.vb ファイルを開き、名前空間宣言を残して、名前空間の宣言内のコードを削除します。 次のコードに示すように、名前空間宣言内に新しいインターフェイス `ICalculator` を定義します。

    ```csharp
    using System;
    using System.ServiceModel;

    namespace GettingStartedLib
    {
            [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
            public interface ICalculator
            {
                [OperationContract]
                double Add(double n1, double n2);
                [OperationContract]
                double Subtract(double n1, double n2);
                [OperationContract]
                double Multiply(double n1, double n2);
                [OperationContract]
                double Divide(double n1, double n2);
            }
    }
    ```

    ```vb
    Imports System.ServiceModel

    Namespace GettingStartedLib

        <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
        Public Interface ICalculator

            <OperationContract()> _
            Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
        End Interface
    End Namespace
    ```

     このコントラクトは、オンライン電卓を定義します。 `ICalculator` インターフェイスは <xref:System.ServiceModel.ServiceContractAttribute> 属性でマークされています。 この属性は、コントラクト名を区別するために使用される名前空間を定義します。 各電卓操作は <xref:System.ServiceModel.OperationContractAttribute> 属性でマークされています。

## <a name="next-steps"></a>次の手順

> [!div class="nextstepaction"]
> [方法: サービス コントラクトを実装します。](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a>関連項目

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [方法: サービス コントラクトを実装する](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [はじめに](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [自己ホスト](../../../docs/framework/wcf/samples/self-host.md)