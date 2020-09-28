---
title: Funkce el. výkaznictví LIST
description: Toto téma obsahuje obecné informace o použití funkce LIST elektronického výkaznictví.
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
ms.openlocfilehash: a31288885abda69873ae23b28a36e2a54852f593
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745146"
---
# <a name="list-er-function"></a><span data-ttu-id="104fa-103">Funkce el. výkaznictví LIST</span><span class="sxs-lookup"><span data-stu-id="104fa-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="104fa-104">Funkce `LIST` vrátí hodnotu typu *seznam záznamů*, která se skládá z nového seznamu záznamů vytvořeného ze zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="104fa-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="104fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="104fa-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="104fa-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="104fa-106">Arguments</span></span>

<span data-ttu-id="104fa-107">`record 1`: *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="104fa-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="104fa-108">Odkaz na zdroj dat datového typu *záznam*.</span><span class="sxs-lookup"><span data-stu-id="104fa-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="104fa-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="104fa-109">This argument is required.</span></span>

<span data-ttu-id="104fa-110">`record N`: *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="104fa-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="104fa-111">Odkaz na zdroj dat datového typu *záznam*.</span><span class="sxs-lookup"><span data-stu-id="104fa-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="104fa-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="104fa-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="104fa-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="104fa-113">Return values</span></span>

<span data-ttu-id="104fa-114">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="104fa-114">*Record list*</span></span>

<span data-ttu-id="104fa-115">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="104fa-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="104fa-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="104fa-116">Usage notes</span></span>

<span data-ttu-id="104fa-117">Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého záznamu, který je uveden v argumentech.</span><span class="sxs-lookup"><span data-stu-id="104fa-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="104fa-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="104fa-118">Example</span></span>

<span data-ttu-id="104fa-119">Zadáte zdroj dat **Záznam 1** typu *kontejner*.</span><span class="sxs-lookup"><span data-stu-id="104fa-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="104fa-120">Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:</span><span class="sxs-lookup"><span data-stu-id="104fa-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="104fa-121">**Kód:** Toto pole obsahuje výraz, který vrací hodnotu typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="104fa-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="104fa-122">**Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="104fa-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="104fa-123">Poté zadáte zdroj dat **Záznam 2** typu *kontejner*.</span><span class="sxs-lookup"><span data-stu-id="104fa-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="104fa-124">Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:</span><span class="sxs-lookup"><span data-stu-id="104fa-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="104fa-125">**Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="104fa-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="104fa-126">**JePlatný:** Toto pole obsahuje výraz, který vrací hodnotu typu *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="104fa-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="104fa-127">V tomto případě výraz `LIST('Record 1', 'Record 2')` vrátí nový seznam, který obsahuje dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="104fa-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="104fa-128">Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu *reálné číslo*, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.</span><span class="sxs-lookup"><span data-stu-id="104fa-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="104fa-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="104fa-129">Additional resources</span></span>

[<span data-ttu-id="104fa-130">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="104fa-130">List functions</span></span>](er-functions-category-list.md)
