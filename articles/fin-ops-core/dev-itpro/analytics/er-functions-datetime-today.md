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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411430"
---
# <a name=""></a><span data-ttu-id="4dbba-103"><a name="TODAY">Funkce elektronického výkaznictví TODAY</a></span><span class="sxs-lookup"><span data-stu-id="4dbba-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dbba-104">Funkce `TODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="4dbba-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dbba-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="4dbba-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="4dbba-106">Return values</span></span>

<span data-ttu-id="4dbba-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="4dbba-107">*Date*</span></span>

<span data-ttu-id="4dbba-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="4dbba-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="4dbba-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="4dbba-109">Example</span></span>

<span data-ttu-id="4dbba-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="4dbba-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dbba-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4dbba-111">Additional resources</span></span>

[<span data-ttu-id="4dbba-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="4dbba-112">Date and time functions</span></span>](er-functions-category-datetime.md)
