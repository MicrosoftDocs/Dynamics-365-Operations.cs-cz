---
title: Funkce el. výkaznictví DAYS
description: Toto téma obsahuje obecné informace o použití funkce DAYS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563479"
---
# <a name="days-er-function"></a><span data-ttu-id="d19df-103">Funkce el. výkaznictví DAYS</span><span class="sxs-lookup"><span data-stu-id="d19df-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d19df-104">Funkce `DAYS` vrátí hodnotu typu *celé číslo*, které představuje počet dní mezi jedním a druhým zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="d19df-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d19df-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="d19df-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d19df-106">Arguments</span></span>

<span data-ttu-id="d19df-107">`date 1`: *datum*</span><span class="sxs-lookup"><span data-stu-id="d19df-107">`date 1`: *Date*</span></span>

<span data-ttu-id="d19df-108">Hodnota kalendářního data, která představuje počáteční datum pro výpočet počtu dní.</span><span class="sxs-lookup"><span data-stu-id="d19df-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="d19df-109">`date 2`: *datum*</span><span class="sxs-lookup"><span data-stu-id="d19df-109">`date 2`: *Date*</span></span>

<span data-ttu-id="d19df-110">Hodnota kalendářního data, která představuje koncové datum pro výpočet počtu dní.</span><span class="sxs-lookup"><span data-stu-id="d19df-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="d19df-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d19df-111">Return values</span></span>

<span data-ttu-id="d19df-112">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="d19df-112">*Integer*</span></span>

<span data-ttu-id="d19df-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="d19df-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d19df-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="d19df-114">Usage notes</span></span>

<span data-ttu-id="d19df-115">Funkce `DAYS` vrátí kladnou hodnotu, pokud je první datum pozdější než druhé datum, vrátí **0** (nulu), když se první datum shoduje s druhým datem, nebo vrátí zápornou hodnotu, když je první datum dřívější než druhé.</span><span class="sxs-lookup"><span data-stu-id="d19df-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="d19df-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="d19df-116">Example</span></span>

<span data-ttu-id="d19df-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` vrací **-1**.</span><span class="sxs-lookup"><span data-stu-id="d19df-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d19df-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d19df-118">Additional resources</span></span>

[<span data-ttu-id="d19df-119">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="d19df-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]