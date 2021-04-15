---
title: Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID
description: Toto téma obsahuje obecné informace o použití funkce CN_GBT_ADDITIONALDIMENSIONID elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744384"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="df80b-103">Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID</span><span class="sxs-lookup"><span data-stu-id="df80b-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df80b-104">Funkce `CN_GBT_ADDITIONALDIMENSIONID` vrací hodnotu typu *řetězec*, která představuje jedno ID dimenze financí, které je převzato ze zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="df80b-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="df80b-105">Zadaný řetězec představuje všechny dimenze jako seznam ID oddělených čárkami.</span><span class="sxs-lookup"><span data-stu-id="df80b-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="df80b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df80b-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="df80b-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="df80b-107">Arguments</span></span>

<span data-ttu-id="df80b-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="df80b-108">`text`: *String*</span></span>

<span data-ttu-id="df80b-109">Hodnota typu *řetězec*, která představuje všechny dimenze jako seznam ID oddělených čárkami.</span><span class="sxs-lookup"><span data-stu-id="df80b-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="df80b-110">`number`: celé číslo</span><span class="sxs-lookup"><span data-stu-id="df80b-110">`number`: Integer</span></span>

<span data-ttu-id="df80b-111">Hodnota typu *celé číslo* definující kód sekvence požadované dimenze v zadaném řetězci.</span><span class="sxs-lookup"><span data-stu-id="df80b-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="df80b-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="df80b-112">Return values</span></span>

<span data-ttu-id="df80b-113">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="df80b-113">*String*</span></span>

<span data-ttu-id="df80b-114">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="df80b-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="df80b-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="df80b-115">Example</span></span>

<span data-ttu-id="df80b-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` vrátí **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="df80b-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df80b-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="df80b-117">Additional resources</span></span>

[<span data-ttu-id="df80b-118">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="df80b-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]