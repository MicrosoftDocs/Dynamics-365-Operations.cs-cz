---
title: Funkce ER Base64StringToContainer
description: Toto téma obsahuje obecné informace o použití funkce Base64StringToContainer elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 612590dacc1887b87677c12eddaef42660a7a154
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561535"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="5b48e-103">Funkce ER Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="5b48e-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b48e-104">[Funkce](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` převede zadaný vstup datového typu *String* na položku datového typu *[Kontejner](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="5b48e-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b48e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b48e-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="5b48e-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5b48e-106">Arguments</span></span>

<span data-ttu-id="5b48e-107">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5b48e-107">`input`: *String*</span></span>

<span data-ttu-id="5b48e-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="5b48e-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b48e-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5b48e-109">Return values</span></span>

<span data-ttu-id="5b48e-110">*Kontejner*</span><span class="sxs-lookup"><span data-stu-id="5b48e-110">*Container*</span></span>

<span data-ttu-id="5b48e-111">Výsledná binární hodnota ve formátu binárního velkého objektu (BLOB).</span><span class="sxs-lookup"><span data-stu-id="5b48e-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5b48e-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="5b48e-112">Usage notes</span></span>

<span data-ttu-id="5b48e-113">Výjimka „Parametr není platný“ je vyvolána, pokud vstupní řetězec neposkytuje správnou skupinu schémat kódování binárního textu na Base64.</span><span class="sxs-lookup"><span data-stu-id="5b48e-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="5b48e-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="5b48e-114">Example</span></span>

<span data-ttu-id="5b48e-115">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="5b48e-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="5b48e-116">Kořenový zdroj dat **DocuTypeGroupEnum** typu *Dynamics 365 for Operations / Výčet*, který odkazuje na výčet aplikace **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="5b48e-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="5b48e-117">Kořenový zdroj dat **Zákazník** typu *Dynamics 365 for Operations / Záznamy tabulky*, který odkazuje na aplikační tabulku **CustTable**</span><span class="sxs-lookup"><span data-stu-id="5b48e-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="5b48e-118">Zdroj dat **\#Media** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5b48e-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="5b48e-119">Je přidán jako podřízený zdroj dat **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="5b48e-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="5b48e-120">Obsahuje výraz `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="5b48e-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="5b48e-121">Zdroj dat **\#MediaAsBase64String** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5b48e-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="5b48e-122">Je přidán jako podřízený zdroj dat **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="5b48e-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="5b48e-123">Obsahuje výraz `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="5b48e-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="5b48e-124">Zdroj dat **\#BlobFomBase64** typu *Vypočítané pole*, který je nakonfigurován následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5b48e-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="5b48e-125">Je přidán jako podřízený zdroj dat **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="5b48e-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="5b48e-126">Obsahuje výraz `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="5b48e-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="5b48e-127">V tomto příkladu zdroj dat **\#MediaAsBase64String** kóduje binární obsah aktuální přílohy média jako text, který představuje skupinu schémat kódování binárního textu na Base64.</span><span class="sxs-lookup"><span data-stu-id="5b48e-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="5b48e-128">Zdroj dat **\#BlobFomBase64** dekóduje řetězec Base64 a vrátí binární hodnotu ve formátu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5b48e-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Ukázka zdrojů dat na stránce návrháře mapování modelu ER](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="5b48e-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5b48e-130">Additional resources</span></span>

[<span data-ttu-id="5b48e-131">Funkce kontejneru</span><span class="sxs-lookup"><span data-stu-id="5b48e-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]