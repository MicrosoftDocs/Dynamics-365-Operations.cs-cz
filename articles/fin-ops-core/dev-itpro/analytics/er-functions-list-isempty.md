---
title: Funkce elektronického výkaznictví ISEMPTY
description: Toto téma obsahuje obecné informace o použití funkce ISEMPTY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916124"
---
# <span data-ttu-id="5fd86-103"><a name="ISEMPTY">Funkce elektronického výkaznictví ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="5fd86-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fd86-104">Funce `ISEMPTY` vrátí *logickou hodnotu* **TRUE**, pokud zadaný seznam neobsahuje žádné záznamy.</span><span class="sxs-lookup"><span data-stu-id="5fd86-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="5fd86-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5fd86-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd86-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fd86-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="5fd86-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5fd86-107">Arguments</span></span>

<span data-ttu-id="5fd86-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="5fd86-108">`list`: *Record list*</span></span>

<span data-ttu-id="5fd86-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="5fd86-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5fd86-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5fd86-110">Return values</span></span>

<span data-ttu-id="5fd86-111">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="5fd86-111">*Boolean*</span></span>

<span data-ttu-id="5fd86-112">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="5fd86-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="5fd86-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="5fd86-113">Example 1</span></span>

<span data-ttu-id="5fd86-114">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `ISEMPTY(DS)` vrátí hodnotu **"FALSE"**.</span><span class="sxs-lookup"><span data-stu-id="5fd86-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5fd86-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="5fd86-115">Example 2</span></span>

<span data-ttu-id="5fd86-116">Výraz `ISEMPTY (SPLIT ("",1))` vrátí hodnotu **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5fd86-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fd86-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5fd86-117">Additional resources</span></span>

[<span data-ttu-id="5fd86-118">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="5fd86-118">List functions</span></span>](er-functions-category-list.md)
