---
title: Funkce elektronického výkaznictví TODAY
description: Toto téma obsahuje obecné informace o použití funkce TODAY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683788"
---
# <a name="today-er-function"></a><span data-ttu-id="2c03c-103">Funkce elektronického výkaznictví TODAY</span><span class="sxs-lookup"><span data-stu-id="2c03c-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c03c-104">Funkce `TODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="2c03c-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c03c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c03c-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="2c03c-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2c03c-106">Return values</span></span>

<span data-ttu-id="2c03c-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="2c03c-107">*Date*</span></span>

<span data-ttu-id="2c03c-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="2c03c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="2c03c-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="2c03c-109">Example</span></span>

<span data-ttu-id="2c03c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="2c03c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c03c-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2c03c-111">Additional resources</span></span>

[<span data-ttu-id="2c03c-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="2c03c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
