---
title: Funkce el. výkaznictví TEXT
description: Toto téma obsahuje obecné informace o použití funkce TEXT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560054"
---
# <a name="text-er-function"></a><span data-ttu-id="7cb02-103">Funkce el. výkaznictví TEXT</span><span class="sxs-lookup"><span data-stu-id="7cb02-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cb02-104">Funkce `TEXT` vrátí zadané číslo jako hodnotu typu *řetězec* poté, co bylo převedeno na textový řetězec naformátovaný podle nastavení národního prostředí jazyka stávající instance aplikace.</span><span class="sxs-lookup"><span data-stu-id="7cb02-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cb02-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="7cb02-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="7cb02-106">Arguments</span></span>

<span data-ttu-id="7cb02-107">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="7cb02-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="7cb02-108">Číslo, které mí být převedeno na textový řetězec.</span><span class="sxs-lookup"><span data-stu-id="7cb02-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="7cb02-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7cb02-109">Return values</span></span>

<span data-ttu-id="7cb02-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="7cb02-110">*String*</span></span>

<span data-ttu-id="7cb02-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="7cb02-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7cb02-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="7cb02-112">Usage notes</span></span>

<span data-ttu-id="7cb02-113">Co se týká hodnot typu *reálné číslo*, převod řetězce je omezen na dvě desetinná místa.</span><span class="sxs-lookup"><span data-stu-id="7cb02-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="7cb02-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="7cb02-114">Example</span></span>

<span data-ttu-id="7cb02-115">Jestliže je národní prostředí instance Microsoft Dynamics 365 Finance definováno jako **EN-US**, `TEXT (NOW ())` vrátí aktuální datum relace Finance, December 17, 2015, jako textový řetězec **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="7cb02-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="7cb02-116">`TEXT (1/3)` vrátí **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="7cb02-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cb02-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7cb02-117">Additional resources</span></span>

[<span data-ttu-id="7cb02-118">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="7cb02-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]