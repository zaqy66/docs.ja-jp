---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: 8b6200f84f352d49cf142d9c8b97d1c2b36149b2
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180901"
---
# <a name="clientcredentials"></a><span data-ttu-id="e83ea-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="e83ea-102">ClientCredentials</span></span>
<span data-ttu-id="e83ea-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="e83ea-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e83ea-104">構文</span><span class="sxs-lookup"><span data-stu-id="e83ea-104">Syntax</span></span>  
  
```csharp
class ClientCredentials : Behavior  
{  
  string ClientCertificate;  
  string HttpDigest;  
  string IssuedToken;  
  string Peer;  
  string ServiceCertificate;  
  boolean SupportInteractive;  
  string UserName;  
  string Windows;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e83ea-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="e83ea-105">Methods</span></span>  
 <span data-ttu-id="e83ea-106">ClientCredentials クラスは、メソッドを一切定義しません。</span><span class="sxs-lookup"><span data-stu-id="e83ea-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e83ea-107">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e83ea-107">Properties</span></span>  
 <span data-ttu-id="e83ea-108">ClientCredentials クラスには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="e83ea-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="e83ea-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e83ea-109">ClientCertificate</span></span>  
 <span data-ttu-id="e83ea-110">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-110">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-111">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-112">クライアントがサービスに対して自身を認証するために使用する X.509 証明書です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="e83ea-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="e83ea-113">HttpDigest</span></span>  
 <span data-ttu-id="e83ea-114">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-114">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-115">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-116">現在の Http ダイジェスト資格情報です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="e83ea-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="e83ea-117">IssuedToken</span></span>  
 <span data-ttu-id="e83ea-118">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-118">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-119">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-120">ローカル セキュリティ トークン サービスにアクセスするために使用されるエンドポイント アドレスおよびバインディングです。</span><span class="sxs-lookup"><span data-stu-id="e83ea-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="e83ea-121">Peer</span><span class="sxs-lookup"><span data-stu-id="e83ea-121">Peer</span></span>  
 <span data-ttu-id="e83ea-122">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-122">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-123">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-124">ピア ノードがメッシュ内の他のノードに対して自身を認証するために使用する資格情報です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="e83ea-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="e83ea-125">ServiceCertificate</span></span>  
 <span data-ttu-id="e83ea-126">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-126">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-127">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-128">サービスの X.509 証明書です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="e83ea-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="e83ea-129">SupportInteractive</span></span>  
 <span data-ttu-id="e83ea-130">データ型 : boolean</span><span class="sxs-lookup"><span data-stu-id="e83ea-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="e83ea-131">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-132">資格情報が対話的なネゴシエーションをサポートしているかどうかを指定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="e83ea-133">UserName</span><span class="sxs-lookup"><span data-stu-id="e83ea-133">UserName</span></span>  
 <span data-ttu-id="e83ea-134">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-134">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-135">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-136">クライアントがサービスに対して自身を認証するために使用するユーザー名とパスワードです。</span><span class="sxs-lookup"><span data-stu-id="e83ea-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="e83ea-137">Windows</span><span class="sxs-lookup"><span data-stu-id="e83ea-137">Windows</span></span>  
 <span data-ttu-id="e83ea-138">データ型: string</span><span class="sxs-lookup"><span data-stu-id="e83ea-138">Data type: string</span></span>  
  
 <span data-ttu-id="e83ea-139">アクセスの種類 : 読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e83ea-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e83ea-140">クライアントがサービスに対して自身を認証するために使用する Windows 資格情報です。</span><span class="sxs-lookup"><span data-stu-id="e83ea-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e83ea-141">必要条件</span><span class="sxs-lookup"><span data-stu-id="e83ea-141">Requirements</span></span>  
  
|<span data-ttu-id="e83ea-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e83ea-142">MOF</span></span>|<span data-ttu-id="e83ea-143">Servicemodel.mof にて宣言済み。</span><span class="sxs-lookup"><span data-stu-id="e83ea-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e83ea-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="e83ea-144">Namespace</span></span>|<span data-ttu-id="e83ea-145">root\ServiceModel で定義</span><span class="sxs-lookup"><span data-stu-id="e83ea-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e83ea-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="e83ea-146">See Also</span></span>  
 <xref:System.ServiceModel.Description.ClientCredentials>
