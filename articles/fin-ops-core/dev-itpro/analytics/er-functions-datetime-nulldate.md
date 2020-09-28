---
title: Funkce el. výkaznictví NULLDATE
description: Toto téma obsahuje obecné informace o použití funkce NULLDATE elektronického výkaznictví.
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744280"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="85e9f-103">Funkce el. výkaznictví NULLDATE</span><span class="sxs-lookup"><span data-stu-id="85e9f-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85e9f-104">Funkce `NULLDATE` vrátí hodnotu typu *datum* představující hodnotu **null** data (1. leden 1900).</span><span class="sxs-lookup"><span data-stu-id="85e9f-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="85e9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85e9f-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="85e9f-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="85e9f-106">Return values</span></span>

<span data-ttu-id="85e9f-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="85e9f-107">*Date*</span></span>

<span data-ttu-id="85e9f-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="85e9f-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="85e9f-109">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="85e9f-109">Example 1</span></span>

<span data-ttu-id="85e9f-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` vrátí hodnotu **null** data, 1 leden 1900, jako **"1900-01-01"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="85e9f-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="85e9f-111">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="85e9f-111">Example 2</span></span>

<span data-ttu-id="85e9f-112">Výraz `IF( Invoice.DocumentDate = NULLDATE(), true, false)` vrátí hodnotu **True**, pokud se hodnota pole **DocumentDate** shoduje s hodnotou **null** data.</span><span class="sxs-lookup"><span data-stu-id="85e9f-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="85e9f-113">V tomto příkladu **Invoice** představuje zdroj dat elektronického výkaznictví typu **záznamy Finance/Table** a odkazuje na tabulku CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="85e9f-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85e9f-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="85e9f-114">Additional resources</span></span>

[<span data-ttu-id="85e9f-115">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="85e9f-115">Date and time functions</span></span>](er-functions-category-datetime.md)
