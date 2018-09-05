---
title: '方法: 別のワークフロー サービスを呼び出すワークフロー サービスを作成する'
ms.date: 03/30/2017
ms.assetid: 99b3ee3e-aeb7-4e6f-8321-60fe6140eb67
ms.openlocfilehash: 1b30da34f7c85cccd98b18cd32b81c83630989b2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/05/2018
ms.locfileid: "43725060"
---
# <a name="how-to-create-a-workflow-service-that-calls-another-workflow-service"></a>方法: 別のワークフロー サービスを呼び出すワークフロー サービスを作成する

ワークフロー サービスでは、別のワークフロー サービスから情報を取得することが必要になる場合があります。 このトピックでは、別のワークフロー サービスからワークフロー サービスを呼び出す方法について説明します。 このトピックでは、2 つのワークフロー サービスを作成します。入力文字列を反転させるメソッドを持つワークフロー サービスと、その最初のサービスを使用して文字列を反転させた後、入力文字列を大文字に変換するワークフロー サービスです。

### <a name="to-create-the-reverser-workflow-service"></a>Reverser ワークフロー サービスを作成するには

1.  Visual Studio を開きます。

2.  選択**ファイル** > **新しいプロジェクト**します。 下、**ワークフロー**内のノード、**インストールされたテンプレート**ペインで、 **WCF ワークフロー サービス アプリケーション**します。 ソリューションの名前を`NestedServices` をクリックし、 **OK**します。

3.  **サーバー**、ことを確認します**ローカル IIS Web サーバーを使用**が選択されています。 クリックして**仮想ディレクトリを作成**です。 クリックして**OK**仮想ディレクトリが正常に作成されたことを示すダイアログ ボックスでします。

4.  ソリューション エクスプローラで、名前を変更する Service1.xamlx`StringReverserService.xamlx`します。

5.  **プロジェクト プロパティ**に新しいプロジェクトのページで、をクリックして、 **Web**タブ。設定、**開始動作**に**特定ページ**StringReverserService.xamlx を開始するページとして選択します。

6.  デザイナーで StringReverserService.xamlx を開いて、既存の `ReceiveRequest` アクティビティおよび `SendReply` アクティビティを削除し、`ReceiveAndSendReply` アクティビティを既存のシーケンス アクティビティにドラッグします。

    1.  設定、 **OperationName** ReverseString にします。

    2.  設定、 **servicecontractname プロパティ**IReverseString にします。

    3.  選択、 **CanCreateInstance**チェック ボックスをオンします。

7.  選択、 **SequentialService**アクティビティ、およびクリック、**変数**デザイナーの下部にあるタブ。 StringToReverse と ReversedStringToReturn という文字列型の 2 つの新しい変数を作成します。

8.  をクリックして、**定義**のリンクを**受信**アクティビティ。 をクリックして、**パラメーター**、InputString という StringToReverse に代入する文字列型のパラメーターを作成します。

9. をクリックして、**定義**のリンクを**SendReplyToReceive**アクティビティ。 をクリックして、**パラメーター**ReversedStringToReturn に割り当てられている、String 型の代入される ReversedString というパラメーターを作成します。

10. サービスのロジックを実装するには、StringLibrary というプロジェクトで新しいクラスを作成します。  クラスの定義を次のコードに置き換えます。

    ```
    public class StringLibrary
        {
            public static String ReverseString(string StringToReverse)
            {
                char[] charArray = StringToReverse.ToCharArray();
                Array.Reverse(charArray);
                return new String(charArray);
            }
        }
    ```

11. 入力で ReverseString メソッドを呼び出して、ドラッグ、 **InvokeMethod**間の空白にアクティビティをツールボックスから、**受信**と**SendReply**アクティビティ。 アクティビティのプロパティを次のように設定します。

    1.  **MethodName**: ReverseString

    2.  **結果**: ReversedStringToReturn

    3.  **パラメーター**: 新しいパラメーターを作成、**方向**のを**型**文字列の**値**StringToReverse の。

    4.  **TargetType**: NestedServices.StringLibrary

12. F5 キーを押して、サービスをテストします。 表示される [WCF テスト クライアント] で、ReverseString() メソッドをダブルクリックします。 要求ペインで次のように入力します。 `Sample` InputString パラメーターの値。 クリックして**呼び出す**します。 サービスにより "elpmaS" が返されます。

### <a name="to-create-the-uppercaser-workflow-service"></a>UpperCaser ワークフロー サービスを作成するには

1.  NestedServices プロジェクトを右クリックして**追加** > **新しい項目の**します。 **ワークフロー**ノードの  **WCF ワークフロー サービス**、新しいサービスの名前と`UpperCaserService`します。 **[追加]** をクリックします。 これにより、UpperCaserService.xamlx という新しいワークフロー サービスがプロジェクトに追加されます。

2.  デザイナーで UpperCaserService.xamlx を開いて、既存の削除**ReceiveRequest**と`SendReply`アクティビティ、およびドラッグ、`ReceiveAndSendReply`を既存のシーケンス アクティビティにアクティビティ。

    1.  設定、 **OperationName** UpperCaseString にします。

    2.  設定、 **servicecontractname プロパティ**IUpperCaseString にします。

    3.  選択、 **CanCreateInstance**チェック ボックスをオンします。

3.  SequentialService アクティビティを選択し、クリックして、**変数**デザイナーの下部にあるタブ。 StringToUpper、StringToReverse、StringToReturn という文字列型の 3 つの新しい変数を作成します。

4.  をクリックして、**定義**のリンクを**受信**アクティビティ。 をクリックして、**パラメーター**、InputString という文字列 StringToUpper に代入する型のパラメーターを作成します。

5.  をクリックして、**定義**のリンクを**SendReplyToReceive**アクティビティ。 をクリックして、**パラメーター**StringToReturn に割り当てられている、String 型の代入される ModifiedString というパラメーターを作成します。

6.  サービスのロジックを実装するには、次のコードを使用して、StringLibrary クラスで新しいメソッドを作成します。

    ```
    public static String UpperCaseString(string StringToUpperCase)
    {
         return StringToUpperCase.ToUpper();

    }
    ```

7.  入力で UpperCaseString メソッドを呼び出して、ドラッグ、 **InvokeMethod**間の空白にアクティビティをツールボックスから、**受信**と**SendReply**アクティビティ。 アクティビティのプロパティを次のように設定します。

    1.  **MethodName**: UpperCaseString

    2.  **結果**: StringToReverse

    3.  **パラメーター**: 新しいパラメーターを作成、**方向**のを**型**文字列の**値**StringToUpper の。

    4.  **TargetType**: NestedServices.StringLibrary

8.  ここで、修正済みの文字列で最初のサービスを呼び出します。 プロジェクトを右クリックして**追加** > **サービス参照の**します。 サービスにサービス参照の追加 http://localhost/NestedServices/StringReverserService.xamlx 最初の Web サービスにアクセスするカスタム アクティビティを作成するプロジェクトをビルドします。

9. 新しいアクティビティのインスタンスを間、ワークフローにドラッグ、 **InvokeMethod**アクティビティと**SendReplyToReceive**アクティビティ。 変数 StringToReverse を新しいアクティビティの InputString プロパティに、変数 StringToReturn を StringToReturn プロパティに割り当てます。

10. NestedServices プロジェクトのプロパティ ページを開き、変更、**特定ページ**で、 **Web** UpperCaserService.xamlx にタブ。

11. F5 キーを押して、サービスをテストします。 表示される [WCF テスト クライアント] で、ReverseString() メソッドをダブルクリックします。 要求ペインで次のように入力します。 `Sample` InputString パラメーターの値。 クリックして**呼び出す**します。 サービスにより "ELPMAS" が返されます。

### <a name="to-create-a-client-to-call-the-services"></a>サービスを呼び出すクライアントを作成するには

1.  クライアントという新しいコンソール アプリケーション プロジェクトをソリューションに追加します。

2.  クライアント プロジェクトを右クリックして**追加** > **サービス参照の**します。 ウィンドウが表示されたら、次のようにクリックします。 **Discover**します。 StringReverserService.xamlx を選択し、名前空間として「ReverseService」と入力します。  **[OK]** をクリックします。

3.  Program.cs の Main メソッドを次のコードで置き換えます。

    ```
    static void Main(string[] args)
    {
        Console.Write("Input string to process:");
        String input = Console.ReadLine();
        var service = new ReverseService.ReverseStringClient();
        Console.WriteLine("Output from service: {0}", service.ReverseString(input));
        Console.ReadKey();
    }
    ```