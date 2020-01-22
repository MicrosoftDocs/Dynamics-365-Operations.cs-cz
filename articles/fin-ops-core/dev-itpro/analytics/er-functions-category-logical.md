---
title: Seznam funkcí ER v logické kategorii
description: Toto téma obsahuje informace o logických funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916630"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="02425-103">Seznam funkcí ER v logické kategorii</span><span class="sxs-lookup"><span data-stu-id="02425-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02425-104">Logické funkce elektronického výkaznictví (ER) lze použít pro práci s logickými hodnotami k provádění více než jednoho porovnání v jednom výrazu nebo při testování více podmínek.</span><span class="sxs-lookup"><span data-stu-id="02425-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="02425-105">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="02425-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="02425-106">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="02425-106">List of supported functions</span></span>

| <span data-ttu-id="02425-107">Funkce</span><span class="sxs-lookup"><span data-stu-id="02425-107">Function</span></span> | <span data-ttu-id="02425-108">Popis</span><span class="sxs-lookup"><span data-stu-id="02425-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="02425-109">A</span><span class="sxs-lookup"><span data-stu-id="02425-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="02425-110">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud jsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="02425-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="02425-111">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="02425-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="02425-112">Pevný obal</span><span class="sxs-lookup"><span data-stu-id="02425-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="02425-113">Tato funkce vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu.</span><span class="sxs-lookup"><span data-stu-id="02425-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="02425-114">V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost.</span><span class="sxs-lookup"><span data-stu-id="02425-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="02425-115">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="02425-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="02425-116">Jestliže</span><span class="sxs-lookup"><span data-stu-id="02425-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="02425-117">Při splnění dané podmínky vrátí tato funkce první zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02425-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="02425-118">V opačném případě vrátí druhou zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02425-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="02425-119">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="02425-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="02425-120">Ne</span><span class="sxs-lookup"><span data-stu-id="02425-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="02425-121">Tato funkce vrací stornovanou logickou hodnotu zadané podmínky jako *logickou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02425-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="02425-122">Or</span><span class="sxs-lookup"><span data-stu-id="02425-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="02425-123">Tato funkce vrátí *logickou* hodnotu **NEPRAVDA**, pokud nejsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="02425-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="02425-124">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.</span><span class="sxs-lookup"><span data-stu-id="02425-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="02425-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="02425-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="02425-126">Tato funkce určuje, zda uvedený vstup odpovídá jakékoli hodnotě zadané položky v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="02425-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="02425-127">Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="02425-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="02425-128">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="02425-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="02425-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="02425-129">Additional resources</span></span>

[<span data-ttu-id="02425-130">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="02425-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="02425-131">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="02425-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="02425-132">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="02425-132">Electronic reporting formula language</span></span>](er-formula-language.md)
