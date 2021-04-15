---
title: Funkce el. výkaznictví NULLDATE
description: Toto téma obsahuje obecné informace o použití funkce NULLDATE elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746836"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="143e1-103">Funkce el. výkaznictví NULLDATE</span><span class="sxs-lookup"><span data-stu-id="143e1-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="143e1-104">Funkce `NULLDATE` vrátí hodnotu typu *datum* představující hodnotu **null** data (1. leden 1900).</span><span class="sxs-lookup"><span data-stu-id="143e1-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="143e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="143e1-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="143e1-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="143e1-106">Return values</span></span>

<span data-ttu-id="143e1-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="143e1-107">*Date*</span></span>

<span data-ttu-id="143e1-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="143e1-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="143e1-109">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="143e1-109">Example 1</span></span>

<span data-ttu-id="143e1-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` vrátí hodnotu **null** data, 1 leden 1900, jako **"1900-01-01"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="143e1-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="143e1-111">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="143e1-111">Example 2</span></span>

<span data-ttu-id="143e1-112">Výraz `IF( Invoice.DocumentDate = NULLDATE(), true, false)` vrátí hodnotu **True**, pokud se hodnota pole **DocumentDate** shoduje s hodnotou **null** data.</span><span class="sxs-lookup"><span data-stu-id="143e1-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="143e1-113">V tomto příkladu **Invoice** představuje zdroj dat elektronického výkaznictví typu **záznamy Finance/Table** a odkazuje na tabulku CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="143e1-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="143e1-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="143e1-114">Additional resources</span></span>

[<span data-ttu-id="143e1-115">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="143e1-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]