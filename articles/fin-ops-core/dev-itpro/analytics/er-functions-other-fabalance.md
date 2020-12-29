---
title: Funkce FA_BALANCE
description: Toto téma obsahuje obecné informace o použití funkce FA_BALANCE elektronického výkaznictví.
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
ms.openlocfilehash: 5570e1295ff6da0eadd7e18143a2206032597ae5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684828"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="06ccf-103">Funkce FA_BALANCE</span><span class="sxs-lookup"><span data-stu-id="06ccf-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06ccf-104">Funkce `FA_BALANCE` vrátí hodnotu typu *kontejner (záznam)*, která se skládá z dat pro zůstatek dlouhodobého majetku pro zadanou položku dlouhodobého majetku, vykazovaný rok a datum vykazování.</span><span class="sxs-lookup"><span data-stu-id="06ccf-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ccf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06ccf-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="06ccf-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="06ccf-106">Arguments</span></span>

<span data-ttu-id="06ccf-107">`fixed asset code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="06ccf-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="06ccf-108">Hodnota typu *řetězec* představující kód položky dlouhodobého majetku, pro kterou se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="06ccf-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="06ccf-109">`value model code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="06ccf-109">`value model code`: *String*</span></span>

<span data-ttu-id="06ccf-110">Hodnota typu *řetězec* představující kód oceňovacího modelu, pro který se počítá zůstatek.</span><span class="sxs-lookup"><span data-stu-id="06ccf-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="06ccf-111">`reporting year`: *výčtová hodnota*</span><span class="sxs-lookup"><span data-stu-id="06ccf-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="06ccf-112">Výčtová hodnota pro výčet aplikace **AssetYear** (rok majetku), která definuje období pro výpočet zůstatku.</span><span class="sxs-lookup"><span data-stu-id="06ccf-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="06ccf-113">`reporting date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="06ccf-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="06ccf-114">Hodnota typu *datum* definující datum výpočtu zůstatku.</span><span class="sxs-lookup"><span data-stu-id="06ccf-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="06ccf-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="06ccf-115">Return values</span></span>

<span data-ttu-id="06ccf-116">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="06ccf-116">*Container (record)*</span></span>

<span data-ttu-id="06ccf-117">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="06ccf-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="06ccf-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="06ccf-118">Example</span></span>

<span data-ttu-id="06ccf-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` vrátí kontejner dat zůstatků pro dlouhodobý majetek **COMP-000001** připravený pro **Current** (aktuální) oceňovací model k aktuálnímu datu relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="06ccf-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06ccf-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="06ccf-120">Additional resources</span></span>

[<span data-ttu-id="06ccf-121">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="06ccf-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
