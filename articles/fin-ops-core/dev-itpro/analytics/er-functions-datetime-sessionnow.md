---
title: Funkce elektronického výkaznictví SESSIONNOW
description: Toto téma obsahuje obecné informace o použití funkce SESSIONNOW elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5489fab61791654c2e583fc11b27aba09fb90c86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042290"
---
# <span data-ttu-id="d3f02-103"><a name="">Funkce elektronického výkaznictví SESSIONNOW</a></span><span class="sxs-lookup"><span data-stu-id="d3f02-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3f02-104">Funkce `SESSIONNOW` vrátí hodnotu typu *datum a čas*, která představuje aktuální datum a čas relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="d3f02-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3f02-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="d3f02-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d3f02-106">Return values</span></span>

<span data-ttu-id="d3f02-107">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="d3f02-107">*DateTime*</span></span>

<span data-ttu-id="d3f02-108">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="d3f02-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="d3f02-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="d3f02-109">Example</span></span>

<span data-ttu-id="d3f02-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` vrátí aktuální datum a čas relace aplikace, 24. prosince 2015, jako **"24.12.2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="d3f02-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3f02-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d3f02-111">Additional resources</span></span>

[<span data-ttu-id="d3f02-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="d3f02-112">Date and time functions</span></span>](er-functions-category-datetime.md)
