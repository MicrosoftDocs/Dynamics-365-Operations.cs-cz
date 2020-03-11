---
title: Funkce elektronického výkaznictví SESSIONTODAY
description: Toto téma obsahuje obecné informace o použití funkce SESSIONTODAY elektronického výkaznictví.
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042252"
---
# <span data-ttu-id="7fd89-103"><a name="SESSIONTODAY">Funkce elektronického výkaznictví SESSIONTODAY</a></span><span class="sxs-lookup"><span data-stu-id="7fd89-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fd89-104">Funkce `SESSIONTODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="7fd89-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fd89-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="7fd89-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7fd89-106">Return values</span></span>

<span data-ttu-id="7fd89-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="7fd89-107">*Date*</span></span>

<span data-ttu-id="7fd89-108">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="7fd89-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="7fd89-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="7fd89-109">Example</span></span>

<span data-ttu-id="7fd89-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="7fd89-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fd89-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7fd89-111">Additional resources</span></span>

[<span data-ttu-id="7fd89-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="7fd89-112">Date and time functions</span></span>](er-functions-category-datetime.md)
