---
title: Seznam funkcí ER v logické kategorii
description: Toto téma obsahuje informace o logických funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686173"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="d8135-103">Seznam funkcí ER v logické kategorii</span><span class="sxs-lookup"><span data-stu-id="d8135-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8135-104">Logické funkce elektronického výkaznictví (ER) lze použít pro práci s logickými hodnotami k provádění více než jednoho porovnání v jednom výrazu nebo při testování více podmínek.</span><span class="sxs-lookup"><span data-stu-id="d8135-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="d8135-105">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="d8135-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="d8135-106">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="d8135-106">List of supported functions</span></span>

| <span data-ttu-id="d8135-107">Funkce</span><span class="sxs-lookup"><span data-stu-id="d8135-107">Function</span></span> | <span data-ttu-id="d8135-108">Popis</span><span class="sxs-lookup"><span data-stu-id="d8135-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d8135-109">A</span><span class="sxs-lookup"><span data-stu-id="d8135-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="d8135-110">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud jsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="d8135-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="d8135-111">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d8135-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="d8135-112">Pevný obal</span><span class="sxs-lookup"><span data-stu-id="d8135-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="d8135-113">Tato funkce vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu.</span><span class="sxs-lookup"><span data-stu-id="d8135-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="d8135-114">V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost.</span><span class="sxs-lookup"><span data-stu-id="d8135-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="d8135-115">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="d8135-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="d8135-116">Jestliže</span><span class="sxs-lookup"><span data-stu-id="d8135-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="d8135-117">Při splnění dané podmínky vrátí tato funkce první zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8135-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="d8135-118">V opačném případě vrátí druhou zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8135-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="d8135-119">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="d8135-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="d8135-120">Ne</span><span class="sxs-lookup"><span data-stu-id="d8135-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="d8135-121">Tato funkce vrací stornovanou logickou hodnotu zadané podmínky jako *logickou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8135-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="d8135-122">Or</span><span class="sxs-lookup"><span data-stu-id="d8135-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="d8135-123">Tato funkce vrátí *logickou* hodnotu **NEPRAVDA**, pokud nejsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="d8135-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="d8135-124">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.</span><span class="sxs-lookup"><span data-stu-id="d8135-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="d8135-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="d8135-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="d8135-126">Tato funkce určuje, zda uvedený vstup odpovídá jakékoli hodnotě zadané položky v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8135-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="d8135-127">Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8135-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="d8135-128">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d8135-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="d8135-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="d8135-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="d8135-130">Tato funkce určuje, zda uvedený vstup typu *Int64* nebo *Integer* odpovídá jakékoli hodnotě zadané položky v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8135-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="d8135-131">Vrátí *logickou hodnotu* **TRUE**, pokud zadaný vstup odpovídá výsledku spuštění zadaného výrazu pro alespoň jeden záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8135-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="d8135-132">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d8135-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="d8135-133">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d8135-133">Additional resources</span></span>

[<span data-ttu-id="d8135-134">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d8135-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d8135-135">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d8135-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="d8135-136">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d8135-136">Electronic reporting formula language</span></span>](er-formula-language.md)
