---
title: Funkce el. výkaznictví NULLDATETIME
description: Toto téma obsahuje obecné informace o použití funkce NULLDATETIME elektronického výkaznictví.
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917481"
---
# <span data-ttu-id="198b8-103"><a name="NULLDATETIME">Funkce el. výkaznictví NULLDATETIME</a></span><span class="sxs-lookup"><span data-stu-id="198b8-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="198b8-104">Funkce `NULLDATETIME` vrátí hodnotu typu *datum a čas*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="198b8-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="198b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="198b8-105">Syntax</span></span>

```
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="198b8-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="198b8-106">Return values</span></span>

<span data-ttu-id="198b8-107">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="198b8-107">*DateTime*</span></span>

<span data-ttu-id="198b8-108">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="198b8-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="198b8-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="198b8-109">Example</span></span>

<span data-ttu-id="198b8-110">Funkce `DATETIMEFORMAT( NULLDATETIME(), "O")` vrátí řetězcovou hodnotu **1900-01-01T00:00:00.0000000+00:00**, pokud je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT) Koordinovaný světový čas** v sekci **Předvolby jazyka a země/oblasti**.</span><span class="sxs-lookup"><span data-stu-id="198b8-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="198b8-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="198b8-111">Additional resources</span></span>

[<span data-ttu-id="198b8-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="198b8-112">Date and time functions</span></span>](er-functions-category-datetime.md)
