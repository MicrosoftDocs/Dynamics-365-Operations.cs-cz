---
title: Funkce elektronického výkaznictví SESSIONNOW
description: Toto téma obsahuje obecné informace o použití funkce SESSIONNOW elektronického výkaznictví.
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
ms.openlocfilehash: a79e8055a4b5025e1b1c4ab91875cf165fa8b354
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563383"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="c9b5b-103">Funkce elektronického výkaznictví SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="c9b5b-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9b5b-104">Funkce `SESSIONNOW` vrátí hodnotu typu *datum a čas*, která představuje aktuální datum a čas relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="c9b5b-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9b5b-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="c9b5b-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="c9b5b-106">Return values</span></span>

<span data-ttu-id="c9b5b-107">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="c9b5b-107">*DateTime*</span></span>

<span data-ttu-id="c9b5b-108">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="c9b5b-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="c9b5b-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="c9b5b-109">Example</span></span>

<span data-ttu-id="c9b5b-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` vrátí aktuální datum a čas relace aplikace, 24. prosince 2015, jako **"24.12.2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="c9b5b-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9b5b-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c9b5b-111">Additional resources</span></span>

[<span data-ttu-id="c9b5b-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="c9b5b-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]