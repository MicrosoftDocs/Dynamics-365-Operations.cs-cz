---
title: Funkce el. výkaznictví FA_SUM
description: Toto téma obsahuje obecné informace o použití funkce FA_SUM elektronického výkaznictví.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: c31722537e2a6bae502800953939ca01da4527b9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567561"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="a2b02-103">Funkce el. výkaznictví FA_SUM</span><span class="sxs-lookup"><span data-stu-id="a2b02-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2b02-104">Funkce `FA_SUM` vrátí hodnotu typu *kontejneru (záznam)*, která se skládá z dat pro částky dlouhodobého majetku pro zadanou položku dlouhodobého majetku, kód oceňovacího modelu a rozsah kalendářních dat.</span><span class="sxs-lookup"><span data-stu-id="a2b02-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2b02-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="a2b02-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="a2b02-106">Arguments</span></span>

<span data-ttu-id="a2b02-107">`fixed asset code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="a2b02-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="a2b02-108">Hodnota typu *řetězec* představující kód položky dlouhodobého majetku, pro kterou se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="a2b02-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="a2b02-109">`value model code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="a2b02-109">`value model code`: *String*</span></span>

<span data-ttu-id="a2b02-110">Hodnota typu *řetězec* představující kód oceňovacího modelu, pro který se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="a2b02-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="a2b02-111">`start date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="a2b02-111">`start date`: *Date*</span></span>

<span data-ttu-id="a2b02-112">Hodnota typu *datum* představuje počáteční datum období, pro které jsou vypočteny částky dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a2b02-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="a2b02-113">`end date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="a2b02-113">`end date`: *Date*</span></span>

<span data-ttu-id="a2b02-114">Hodnota typu *datum* představuje koncové datum období, pro které jsou vypočteny částky dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a2b02-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="a2b02-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a2b02-115">Return values</span></span>

<span data-ttu-id="a2b02-116">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="a2b02-116">*Container (record)*</span></span>

<span data-ttu-id="a2b02-117">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="a2b02-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="a2b02-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="a2b02-118">Example</span></span>

<span data-ttu-id="a2b02-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` vrátí kontejner dat pro dlouhodobý majetek **COMP-000001**, který byl připraven pro **aktuální** (Current) oceňovací model a pro období od **Date1** (datum1) do **Date2** (datum2).</span><span class="sxs-lookup"><span data-stu-id="a2b02-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2b02-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a2b02-120">Additional resources</span></span>

[<span data-ttu-id="a2b02-121">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="a2b02-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]