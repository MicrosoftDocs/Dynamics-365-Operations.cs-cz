---
title: Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID
description: Toto téma obsahuje obecné informace o použití funkce CN_GBT_ADDITIONALDIMENSIONID elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686803"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="01783-103">Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="01783-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01783-104">Funkce `CN_GBT_ADDITIONALDIMENSIONID` vrací hodnotu typu *řetězec*, která představuje jedno ID dimenze financí, které je převzato ze zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="01783-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="01783-105">Zadaný řetězec představuje všechny dimenze jako seznam ID oddělených čárkami.</span><span class="sxs-lookup"><span data-stu-id="01783-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="01783-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01783-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="01783-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="01783-107">Arguments</span></span>

<span data-ttu-id="01783-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="01783-108">`text`: *String*</span></span>

<span data-ttu-id="01783-109">Hodnota typu *řetězec*, která představuje všechny dimenze jako seznam ID oddělených čárkami.</span><span class="sxs-lookup"><span data-stu-id="01783-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="01783-110">`number`: celé číslo</span><span class="sxs-lookup"><span data-stu-id="01783-110">`number`: Integer</span></span>

<span data-ttu-id="01783-111">Hodnota typu *celé číslo* definující kód sekvence požadované dimenze v zadaném řetězci.</span><span class="sxs-lookup"><span data-stu-id="01783-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="01783-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="01783-112">Return values</span></span>

<span data-ttu-id="01783-113">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="01783-113">*String*</span></span>

<span data-ttu-id="01783-114">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="01783-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="01783-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="01783-115">Example</span></span>

<span data-ttu-id="01783-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` vrátí **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="01783-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01783-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="01783-117">Additional resources</span></span>

[<span data-ttu-id="01783-118">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="01783-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
