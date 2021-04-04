---
title: Funkce elektronického výkaznictví TODAY
description: Toto téma obsahuje obecné informace o použití funkce TODAY elektronického výkaznictví.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 9288baf4e6123a7c03152f524a852eae9b671dde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567909"
---
# <a name="today-er-function"></a><span data-ttu-id="b1585-103">Funkce elektronického výkaznictví TODAY</span><span class="sxs-lookup"><span data-stu-id="b1585-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1585-104">Funkce `TODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="b1585-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1585-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1585-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b1585-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b1585-106">Return values</span></span>

<span data-ttu-id="b1585-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="b1585-107">*Date*</span></span>

<span data-ttu-id="b1585-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="b1585-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b1585-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="b1585-109">Example</span></span>

<span data-ttu-id="b1585-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="b1585-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1585-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b1585-111">Additional resources</span></span>

[<span data-ttu-id="b1585-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="b1585-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]