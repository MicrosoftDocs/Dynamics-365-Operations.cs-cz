---
title: Funkce FORMATELEMENTNAME ER
description: Toto téma obsahuje obecné informace o použití funkce FORMATELEMENTNAME elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f716fe779903b4e9142b7959d868256f2d84c624
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755221"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="efa2d-103">Funkce FORMATELEMENTNAME ER</span><span class="sxs-lookup"><span data-stu-id="efa2d-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efa2d-104">Funkce `FORMATELEMENTNAME` vrací hodnotu *řetězec*, která představuje název aktuálního prvku formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="efa2d-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efa2d-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="efa2d-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="efa2d-106">Return values</span></span>

<span data-ttu-id="efa2d-107">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="efa2d-107">*String*</span></span>

<span data-ttu-id="efa2d-108">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="efa2d-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="efa2d-109">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="efa2d-109">Usage notes</span></span>

<span data-ttu-id="efa2d-110">Tuto funkci lze volat ve výrazech ER, které byly nakonfigurovány pro vlastnosti **název získaného datového klíče** a **hodnota získaného datového klíče** komponenty formátu ER ze skupiny **Text**, která se nachází v rámci komponenty **Společné\\Soubor**, kde je zapnutá možnost **Shromáždit podrobnosti výstupu**.</span><span class="sxs-lookup"><span data-stu-id="efa2d-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="efa2d-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="efa2d-111">Example</span></span>

<span data-ttu-id="efa2d-112">Další informace o způsobu použití těchto funkcí najdete v průvodci záznamem úloh [Elektronické výkaznictví - zdroj dat formátu výstupu pro inventuru a souhrn](tasks/er-format-counting-summing-1.md), část obchodního procesu **Získání/vývoj komponent služby/řešení**.</span><span class="sxs-lookup"><span data-stu-id="efa2d-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efa2d-113">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="efa2d-113">Additional resources</span></span>

[<span data-ttu-id="efa2d-114">Funkce shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="efa2d-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]