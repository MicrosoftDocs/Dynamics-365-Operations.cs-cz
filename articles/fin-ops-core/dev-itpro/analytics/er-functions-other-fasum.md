---
title: Funkce el. výkaznictví FA_SUM
description: Toto téma obsahuje obecné informace o použití funkce FA_SUM elektronického výkaznictví.
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744288"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="3ae75-103">Funkce el. výkaznictví FA_SUM</span><span class="sxs-lookup"><span data-stu-id="3ae75-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ae75-104">Funkce `FA_SUM` vrátí hodnotu typu *kontejneru (záznam)*, která se skládá z dat pro částky dlouhodobého majetku pro zadanou položku dlouhodobého majetku, kód oceňovacího modelu a rozsah kalendářních dat.</span><span class="sxs-lookup"><span data-stu-id="3ae75-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae75-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ae75-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="3ae75-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3ae75-106">Arguments</span></span>

<span data-ttu-id="3ae75-107">`fixed asset code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3ae75-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="3ae75-108">Hodnota typu *řetězec* představující kód položky dlouhodobého majetku, pro kterou se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="3ae75-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="3ae75-109">`value model code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3ae75-109">`value model code`: *String*</span></span>

<span data-ttu-id="3ae75-110">Hodnota typu *řetězec* představující kód oceňovacího modelu, pro který se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="3ae75-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="3ae75-111">`start date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="3ae75-111">`start date`: *Date*</span></span>

<span data-ttu-id="3ae75-112">Hodnota typu *datum* představuje počáteční datum období, pro které jsou vypočteny částky dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3ae75-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="3ae75-113">`end date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="3ae75-113">`end date`: *Date*</span></span>

<span data-ttu-id="3ae75-114">Hodnota typu *datum* představuje koncové datum období, pro které jsou vypočteny částky dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3ae75-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ae75-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3ae75-115">Return values</span></span>

<span data-ttu-id="3ae75-116">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="3ae75-116">*Container (record)*</span></span>

<span data-ttu-id="3ae75-117">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="3ae75-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="3ae75-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="3ae75-118">Example</span></span>

<span data-ttu-id="3ae75-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` vrátí kontejner dat pro dlouhodobý majetek **COMP-000001**, který byl připraven pro **aktuální** (Current) oceňovací model a pro období od **Date1** (datum1) do **Date2** (datum2).</span><span class="sxs-lookup"><span data-stu-id="3ae75-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ae75-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3ae75-120">Additional resources</span></span>

[<span data-ttu-id="3ae75-121">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="3ae75-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]