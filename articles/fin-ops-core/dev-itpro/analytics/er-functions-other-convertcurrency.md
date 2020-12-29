---
title: Funkce el. výkaznictví CONVERTCURRENCY
description: Toto téma obsahuje obecné informace o použití funkce CONVERTCURRENCY elektronického výkaznictví.
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
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686779"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="2cb9c-103">Funkce el. výkaznictví CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="2cb9c-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cb9c-104">Funkce `CONVERTCURRENCY` vrátí hodnotu typu *reálné číslo*, které představuje výsledek pro převedení zadané peněžní částky ze zadané zdrojové měny na zadanou cílovou měnu za použití nastavení zadané společnosti k zadanému datu.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cb9c-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="2cb9c-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2cb9c-106">Arguments</span></span>

<span data-ttu-id="2cb9c-107">`amount`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="2cb9c-108">Číselná hodnota, která představuje peněžní částku, která má být převedena.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="2cb9c-109">`source currency`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-109">`source currency`: *String*</span></span>

<span data-ttu-id="2cb9c-110">Kód zdrojové měny.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-110">The code of the source currency.</span></span>

<span data-ttu-id="2cb9c-111">`target currency`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-111">`target currency`: *String*</span></span>

<span data-ttu-id="2cb9c-112">Kód cílové měny.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-112">The code of the target currency.</span></span>

<span data-ttu-id="2cb9c-113">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-113">`date`: *Date*</span></span>

<span data-ttu-id="2cb9c-114">Hodnota typu *datum*, která představuje datum, které slouží k určení směnného kursu pro převod.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="2cb9c-115">`company`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-115">`company`: *String*</span></span>

<span data-ttu-id="2cb9c-116">Hodnota typu *řetězec* představující kód společnosti, která poskytuje nastavení použitá pro převod.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="2cb9c-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2cb9c-117">Return values</span></span>

<span data-ttu-id="2cb9c-118">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="2cb9c-118">*Real*</span></span>

<span data-ttu-id="2cb9c-119">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2cb9c-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="2cb9c-120">Example</span></span>

<span data-ttu-id="2cb9c-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` vrátí ekvivalent jednoho eura v amerických dolarech v aktuální den relace podle nastavení společnosti **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="2cb9c-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cb9c-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2cb9c-122">Additional resources</span></span>

[<span data-ttu-id="2cb9c-123">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="2cb9c-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
