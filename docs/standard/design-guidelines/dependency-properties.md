---
title: 依存関係プロパティ
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 212cfb1e-cec4-4047-94a6-47209b387f6f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75c83dc75d1c86c89169fcc54220ced2a195bfbe
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44079088"
---
# <a name="dependency-properties"></a><span data-ttu-id="f0e94-102">依存関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0e94-102">Dependency Properties</span></span>
<span data-ttu-id="f0e94-103">依存関係プロパティ (DP) は、たとえば (フィールド) の型の変数に格納することではなく、プロパティ ストアにその値を格納する標準プロパティです。</span><span class="sxs-lookup"><span data-stu-id="f0e94-103">A dependency property (DP) is a regular property that stores its value in a property store instead of storing it in a type variable (field), for example.</span></span>  
  
 <span data-ttu-id="f0e94-104">依存プロパティは、ある種のオブジェクトとそのコンテナーの間のリレーションシップを記述する「プロパティ」を表す、Get と Set の静的メソッドとしてモデル化された依存関係プロパティ (の位置など、`Button`上のオブジェクトを`Panel`コンテナーの場合)。</span><span class="sxs-lookup"><span data-stu-id="f0e94-104">An attached dependency property is a kind of dependency property modeled as static Get and Set methods representing "properties" describing relationships between objects and their containers (e.g., the position of a `Button` object on a `Panel` container).</span></span>  
  
 <span data-ttu-id="f0e94-105">**✓ DO** プロパティ スタイル設定、トリガー、データ バインディング、アニメーション、動的なリソース、および継承などの WPF 機能をサポートする必要がある場合は、依存関係プロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-105">**✓ DO** provide the dependency properties, if you need the properties to support WPF features such as styling, triggers, data binding, animations, dynamic resources, and inheritance.</span></span>  
  
## <a name="dependency-property-design"></a><span data-ttu-id="f0e94-106">依存関係プロパティのデザイン</span><span class="sxs-lookup"><span data-stu-id="f0e94-106">Dependency Property Design</span></span>  
 <span data-ttu-id="f0e94-107">**✓ DO** から継承<xref:System.Windows.DependencyObject>、または依存関係プロパティを実装する場合、そのサブタイプのいずれか。</span><span class="sxs-lookup"><span data-stu-id="f0e94-107">**✓ DO** inherit from <xref:System.Windows.DependencyObject>, or one of its subtypes, when implementing dependency properties.</span></span> <span data-ttu-id="f0e94-108">型は、プロパティ ストアの非常に効率的な実装を提供し、自動的に WPF データ バインドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f0e94-108">The type provides a very efficient implementation of a property store and automatically supports WPF data binding.</span></span>  
  
 <span data-ttu-id="f0e94-109">**✓ DO** 正規の CLR プロパティとパブリックな静的読み取り専用フィールドのインスタンスを格納する提供<xref:System.Windows.DependencyProperty?displayProperty=nameWithType>各依存関係プロパティです。</span><span class="sxs-lookup"><span data-stu-id="f0e94-109">**✓ DO** provide a regular CLR property and public static read-only field storing an instance of <xref:System.Windows.DependencyProperty?displayProperty=nameWithType> for each dependency property.</span></span>  
  
 <span data-ttu-id="f0e94-110">**✓ DO** 依存関係プロパティを実装するインスタンス メソッドを呼び出すことによって<xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType>と<xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType>です。</span><span class="sxs-lookup"><span data-stu-id="f0e94-110">**✓ DO** implement dependency properties by calling instance methods <xref:System.Windows.DependencyObject.GetValue%2A?displayProperty=nameWithType> and <xref:System.Windows.DependencyObject.SetValue%2A?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="f0e94-111">**✓ DO** "Property"のプロパティの名前をアスタリスクの依存関係プロパティの静的フィールドの名前</span><span class="sxs-lookup"><span data-stu-id="f0e94-111">**✓ DO** name the dependency property static field by suffixing the name of the property with "Property."</span></span>  
  
 <span data-ttu-id="f0e94-112">**X DO NOT** コード内の依存関係プロパティの既定値を明示的に設定を代わりにメタデータの設定です。</span><span class="sxs-lookup"><span data-stu-id="f0e94-112">**X DO NOT** set default values of dependency properties explicitly in code; set them in metadata instead.</span></span>  
  
 <span data-ttu-id="f0e94-113">プロパティの既定値を明示的に設定するをスタイル設定などのいくつかの暗黙的な方法で設定されているから、そのプロパティをできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0e94-113">If you set a property default explicitly, you might prevent that property from being set by some implicit means, such as a styling.</span></span>  
  
 <span data-ttu-id="f0e94-114">**X DO NOT** 静的フィールドにアクセスする標準コード以外のプロパティ アクセサーにコードを配置します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-114">**X DO NOT** put code in the property accessors other than the standard code to access the static field.</span></span>  
  
 <span data-ttu-id="f0e94-115">コードがしません実行をスタイル設定などの暗黙的な方法で、プロパティが設定されている場合のスタイルを設定するため、静的フィールドを直接使用します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-115">That code won’t execute if the property is set by implicit means, such as a styling, because styling uses the static field directly.</span></span>  
  
 <span data-ttu-id="f0e94-116">**X DO NOT** 依存関係プロパティを使用してセキュリティで保護されたデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-116">**X DO NOT** use dependency properties to store secure data.</span></span> <span data-ttu-id="f0e94-117">プライベートでも依存関係プロパティは、パブリックにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f0e94-117">Even private dependency properties can be accessed publicly.</span></span>  
  
## <a name="attached-dependency-property-design"></a><span data-ttu-id="f0e94-118">接続されている依存関係プロパティのデザイン</span><span class="sxs-lookup"><span data-stu-id="f0e94-118">Attached Dependency Property Design</span></span>  
 <span data-ttu-id="f0e94-119">依存関係プロパティが、前のセクションで説明されている宣言型の組み込みのプロパティを表しますたとえば、`Text`プロパティは、プロパティの`TextButton`、宣言します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-119">Dependency properties described in the preceding section represent intrinsic properties of the declaring type; for example, the `Text` property is a property of `TextButton`, which declares it.</span></span> <span data-ttu-id="f0e94-120">依存関係プロパティの特殊なは、接続されている依存関係プロパティです。</span><span class="sxs-lookup"><span data-stu-id="f0e94-120">A special kind of dependency property is the attached dependency property.</span></span>  
  
 <span data-ttu-id="f0e94-121">添付プロパティの典型的な例は、<xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType>プロパティ。</span><span class="sxs-lookup"><span data-stu-id="f0e94-121">A classic example of an attached property is the <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="f0e94-122">プロパティ ボタン (いないグリッドの) 列の位置を表しますは"にアタッチされている"ボタンのグリッドで、グリッドで、ボタンが含まれている場合にのみ関連します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-122">The property represents Button’s (not Grid’s) column position, but it is only relevant if the Button is contained in a Grid, and so it's "attached" to Buttons by Grids.</span></span>  
  
```xaml
<Grid>  
    <Grid.ColumnDefinitions>  
        <ColumnDefinition />  
        <ColumnDefinition />  
    </Grid.ColumnDefinitions>  
  
    <Button Grid.Column="0">Click</Button>  
    <Button Grid.Column="1">Clack</Button>  
</Grid>  
```  
  
 <span data-ttu-id="f0e94-123">添付プロパティの定義は、アクセサーが静的な Get と Set メソッドによって表されることを除いて、通常の依存関係プロパティのほとんどの場合ようになります。</span><span class="sxs-lookup"><span data-stu-id="f0e94-123">The definition of an attached property looks mostly like that of a regular dependency property, except that the accessors are represented by static Get and Set methods:</span></span>  
  
```csharp
public class Grid {  
  
    public static int GetColumn(DependencyObject obj) {  
        return (int)obj.GetValue(ColumnProperty);  
    }  
  
    public static void SetColumn(DependencyObject obj, int value) {  
        obj.SetValue(ColumnProperty,value);  
    }  
  
    public static readonly DependencyProperty ColumnProperty =  
        DependencyProperty.RegisterAttached(  
            "Column",  
            typeof(int),  
            typeof(Grid)  
    );  
}  
```  
  
## <a name="dependency-property-validation"></a><span data-ttu-id="f0e94-124">依存関係プロパティの検証</span><span class="sxs-lookup"><span data-stu-id="f0e94-124">Dependency Property Validation</span></span>  
 <span data-ttu-id="f0e94-125">プロパティは、多くの場合、検証と呼ばれるものを実装します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-125">Properties often implement what is called validation.</span></span> <span data-ttu-id="f0e94-126">プロパティの値を変更する試行したときに検証ロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-126">Validation logic executes when an attempt is made to change the value of a property.</span></span>  
  
 <span data-ttu-id="f0e94-127">残念なことに依存関係プロパティのアクセサーには、任意の検証コードを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f0e94-127">Unfortunately dependency property accessors cannot contain arbitrary validation code.</span></span> <span data-ttu-id="f0e94-128">代わりに、依存関係プロパティの検証ロジックは、プロパティの登録時に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0e94-128">Instead, dependency property validation logic needs to be specified during property registration.</span></span>  
  
 <span data-ttu-id="f0e94-129">**X DO NOT** プロパティのアクセサーの依存関係プロパティの検証ロジックを配置します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-129">**X DO NOT** put dependency property validation logic in the property’s accessors.</span></span> <span data-ttu-id="f0e94-130">代わりに、検証コールバックを渡す`DependencyProperty.Register`メソッド。</span><span class="sxs-lookup"><span data-stu-id="f0e94-130">Instead, pass a validation callback to `DependencyProperty.Register` method.</span></span>  
  
## <a name="dependency-property-change-notifications"></a><span data-ttu-id="f0e94-131">依存関係プロパティの変更通知</span><span class="sxs-lookup"><span data-stu-id="f0e94-131">Dependency Property Change Notifications</span></span>  
 <span data-ttu-id="f0e94-132">**X DO NOT** 依存関係プロパティのアクセサーでの変更通知のロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-132">**X DO NOT** implement change notification logic in dependency property accessors.</span></span> <span data-ttu-id="f0e94-133">依存関係プロパティに変更通知のコールバックを指定して使用する必要があります組み込みの変更通知機能があり、<xref:System.Windows.PropertyMetadata>します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-133">Dependency properties have a built-in change notifications feature that must be used by supplying a change notification callback to the <xref:System.Windows.PropertyMetadata>.</span></span>  
  
## <a name="dependency-property-value-coercion"></a><span data-ttu-id="f0e94-134">依存関係プロパティの値の強制型変換</span><span class="sxs-lookup"><span data-stu-id="f0e94-134">Dependency Property Value Coercion</span></span>  
 <span data-ttu-id="f0e94-135">プロパティ ストアが実際に変更する前に、setter をプロパティ set アクセス操作子に渡された値が変更されたときにプロパティの強制型変換が行われます。</span><span class="sxs-lookup"><span data-stu-id="f0e94-135">Property coercion takes place when the value given to a property setter is modified by the setter before the property store is actually modified.</span></span>  
  
 <span data-ttu-id="f0e94-136">**X DO NOT** 依存関係プロパティのアクセサーに強制変換ロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-136">**X DO NOT** implement coercion logic in dependency property accessors.</span></span>  
  
 <span data-ttu-id="f0e94-137">依存関係プロパティは、組み込みの強制型変換機能を持っているし、強制型変換のコールバックを指定することによって使用できます、`PropertyMetadata`します。</span><span class="sxs-lookup"><span data-stu-id="f0e94-137">Dependency properties have a built-in coercion feature, and it can be used by supplying a coercion callback to the `PropertyMetadata`.</span></span>  
  
 <span data-ttu-id="f0e94-138">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="f0e94-138">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="f0e94-139">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="f0e94-139">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0e94-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0e94-140">See also</span></span>

- [<span data-ttu-id="f0e94-141">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="f0e94-141">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="f0e94-142">共通デザイン パターン</span><span class="sxs-lookup"><span data-stu-id="f0e94-142">Common Design Patterns</span></span>](../../../docs/standard/design-guidelines/common-design-patterns.md)
