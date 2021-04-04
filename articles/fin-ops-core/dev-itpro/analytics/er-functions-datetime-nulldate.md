---
title: Funkce el. výkaznictví NULLDATE
description: Toto téma obsahuje obecné informace o použití funkce NULLDATE elektronického výkaznictví.
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563455"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="dbbc4-103">Funkce el. výkaznictví NULLDATE</span><span class="sxs-lookup"><span data-stu-id="dbbc4-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbbc4-104">Funkce `NULLDATE` vrátí hodnotu typu *datum* představující hodnotu **null** data (1. leden 1900).</span><span class="sxs-lookup"><span data-stu-id="dbbc4-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbbc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbbc4-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="dbbc4-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="dbbc4-106">Return values</span></span>

<span data-ttu-id="dbbc4-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="dbbc4-107">*Date*</span></span>

<span data-ttu-id="dbbc4-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="dbbc4-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="dbbc4-109">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="dbbc4-109">Example 1</span></span>

<span data-ttu-id="dbbc4-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` vrátí hodnotu **null** data, 1 leden 1900, jako **"1900-01-01"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="dbbc4-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="dbbc4-111">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="dbbc4-111">Example 2</span></span>

<span data-ttu-id="dbbc4-112">Výraz `IF( Invoice.DocumentDate = NULLDATE(), true, false)` vrátí hodnotu **True**, pokud se hodnota pole **DocumentDate** shoduje s hodnotou **null** data.</span><span class="sxs-lookup"><span data-stu-id="dbbc4-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="dbbc4-113">V tomto příkladu **Invoice** představuje zdroj dat elektronického výkaznictví typu **záznamy Finance/Table** a odkazuje na tabulku CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="dbbc4-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbbc4-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="dbbc4-114">Additional resources</span></span>

[<span data-ttu-id="dbbc4-115">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="dbbc4-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]