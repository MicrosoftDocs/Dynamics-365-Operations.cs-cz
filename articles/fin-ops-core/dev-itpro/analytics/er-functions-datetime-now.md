---
title: Funkce el. výkaznictví NOW
description: Toto téma obsahuje obecné informace o použití funkce NOW elektronického výkaznictví.
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
ms.openlocfilehash: 8e549634b3856777aff610fa0e61c19bcad71dd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563503"
---
# <a name="now-er-function"></a><span data-ttu-id="a124e-103">Funkce el. výkaznictví NOW</span><span class="sxs-lookup"><span data-stu-id="a124e-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a124e-104">Funkce `NOW` vrátí hodnotu typu *datum a čas*, která představuje aktuální datum a čas aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="a124e-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="a124e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a124e-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="a124e-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a124e-106">Return values</span></span>

<span data-ttu-id="a124e-107">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="a124e-107">*DateTime*</span></span>

<span data-ttu-id="a124e-108">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="a124e-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="a124e-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="a124e-109">Example</span></span>

<span data-ttu-id="a124e-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` vrátí aktuální datum/čas aplikačního serveru, například 24. prosince 2015 jako **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="a124e-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a124e-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a124e-111">Additional resources</span></span>

[<span data-ttu-id="a124e-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="a124e-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]