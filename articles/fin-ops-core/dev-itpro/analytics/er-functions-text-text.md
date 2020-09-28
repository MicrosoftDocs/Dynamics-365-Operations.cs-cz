---
title: Funkce el. výkaznictví TEXT
description: Toto téma obsahuje obecné informace o použití funkce TEXT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743681"
---
# <a name="text-er-function"></a><span data-ttu-id="624c2-103">Funkce el. výkaznictví TEXT</span><span class="sxs-lookup"><span data-stu-id="624c2-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="624c2-104">Funkce `TEXT` vrátí zadané číslo jako hodnotu typu *řetězec* poté, co bylo převedeno na textový řetězec naformátovaný podle nastavení národního prostředí jazyka stávající instance aplikace.</span><span class="sxs-lookup"><span data-stu-id="624c2-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="624c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="624c2-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="624c2-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="624c2-106">Arguments</span></span>

<span data-ttu-id="624c2-107">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="624c2-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="624c2-108">Číslo, které mí být převedeno na textový řetězec.</span><span class="sxs-lookup"><span data-stu-id="624c2-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="624c2-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="624c2-109">Return values</span></span>

<span data-ttu-id="624c2-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="624c2-110">*String*</span></span>

<span data-ttu-id="624c2-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="624c2-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="624c2-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="624c2-112">Usage notes</span></span>

<span data-ttu-id="624c2-113">Co se týká hodnot typu *reálné číslo*, převod řetězce je omezen na dvě desetinná místa.</span><span class="sxs-lookup"><span data-stu-id="624c2-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="624c2-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="624c2-114">Example</span></span>

<span data-ttu-id="624c2-115">Jestliže je národní prostředí instance Microsoft Dynamics 365 Finance definováno jako **EN-US**, `TEXT (NOW ())` vrátí aktuální datum relace Finance, December 17, 2015, jako textový řetězec **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="624c2-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="624c2-116">`TEXT (1/3)` vrátí **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="624c2-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="624c2-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="624c2-117">Additional resources</span></span>

[<span data-ttu-id="624c2-118">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="624c2-118">Text functions</span></span>](er-functions-category-text.md)
