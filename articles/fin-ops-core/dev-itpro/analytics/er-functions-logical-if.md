---
title: Funkce el. výkaznictví IF
description: Toto téma obsahuje obecné informace o použití funkce IF elektronického výkaznictví.
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
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041738"
---
# <span data-ttu-id="054ea-103"><a name="IF">Funkce el. výkaznictví IF</a></span><span class="sxs-lookup"><span data-stu-id="054ea-103"><a name="IF">IF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="054ea-104">Při splnění dané podmínky vrátí funkce `IF` první zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="054ea-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="054ea-105">V opačném případě vrátí druhou zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="054ea-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="054ea-106">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="054ea-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="054ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="054ea-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="054ea-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="054ea-108">Arguments</span></span>

<span data-ttu-id="054ea-109">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="054ea-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="054ea-110">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="054ea-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="054ea-111">`first value`: *kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="054ea-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="054ea-112">Výsledek, který je vrácen, pokud je podmínka splněna.</span><span class="sxs-lookup"><span data-stu-id="054ea-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="054ea-113">`second value`: *kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="054ea-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="054ea-114">Výsledek, který je vrácen, pokud podmínka není splněna.</span><span class="sxs-lookup"><span data-stu-id="054ea-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="054ea-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="054ea-115">Return values</span></span>

<span data-ttu-id="054ea-116">*kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="054ea-116">*Any of the supported data types*</span></span>

<span data-ttu-id="054ea-117">Výsledná hodnota některého z podporovaných datových typů.</span><span class="sxs-lookup"><span data-stu-id="054ea-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="054ea-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="054ea-118">Usage notes</span></span>

<span data-ttu-id="054ea-119">Zadané argumenty `first value` a `second value` musejí mít stejný datový typ.</span><span class="sxs-lookup"><span data-stu-id="054ea-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="054ea-120">Výjimka je vyvolána v době návrhu, pokud se datové typy konfigurovaných hodnot neshodují.</span><span class="sxs-lookup"><span data-stu-id="054ea-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="054ea-121">Jsou-li první a druhá hodnota datového typu *kontejner (záznam)* nebo *seznam záznamů*, výsledek obsahuje pouze pole, která existují v obou hodnotách.</span><span class="sxs-lookup"><span data-stu-id="054ea-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="054ea-122">Příklad</span><span class="sxs-lookup"><span data-stu-id="054ea-122">Example</span></span>

<span data-ttu-id="054ea-123">`IF (1=2, "condition is met", "condition is not met")` vrátí řetězec **"podmínka není splněna"**.</span><span class="sxs-lookup"><span data-stu-id="054ea-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="054ea-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="054ea-124">Additional resources</span></span>

[<span data-ttu-id="054ea-125">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="054ea-125">Logical functions</span></span>](er-functions-category-logical.md)
