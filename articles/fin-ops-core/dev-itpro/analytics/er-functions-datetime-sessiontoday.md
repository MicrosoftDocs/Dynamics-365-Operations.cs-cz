---
title: Funkce elektronického výkaznictví SESSIONTODAY
description: Toto téma obsahuje obecné informace o použití funkce SESSIONTODAY elektronického výkaznictví.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746764"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="e0796-103">Funkce elektronického výkaznictví SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="e0796-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0796-104">Funkce `SESSIONTODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="e0796-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0796-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0796-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e0796-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e0796-106">Return values</span></span>

<span data-ttu-id="e0796-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="e0796-107">*Date*</span></span>

<span data-ttu-id="e0796-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="e0796-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e0796-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="e0796-109">Example</span></span>

<span data-ttu-id="e0796-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="e0796-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0796-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e0796-111">Additional resources</span></span>

[<span data-ttu-id="e0796-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="e0796-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]