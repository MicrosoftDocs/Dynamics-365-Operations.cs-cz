---
title: Funkce el. výkaznictví LIST
description: Toto téma obsahuje obecné informace o použití funkce LIST elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563841"
---
# <a name="list-er-function"></a><span data-ttu-id="70a90-103">Funkce el. výkaznictví LIST</span><span class="sxs-lookup"><span data-stu-id="70a90-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70a90-104">Funkce `LIST` vrátí hodnotu typu *seznam záznamů*, která se skládá z nového seznamu záznamů vytvořeného ze zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="70a90-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70a90-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="70a90-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="70a90-106">Arguments</span></span>

<span data-ttu-id="70a90-107">`record 1`: *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="70a90-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="70a90-108">Odkaz na zdroj dat datového typu *záznam*.</span><span class="sxs-lookup"><span data-stu-id="70a90-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="70a90-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="70a90-109">This argument is required.</span></span>

<span data-ttu-id="70a90-110">`record N`: *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="70a90-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="70a90-111">Odkaz na zdroj dat datového typu *záznam*.</span><span class="sxs-lookup"><span data-stu-id="70a90-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="70a90-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="70a90-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="70a90-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="70a90-113">Return values</span></span>

<span data-ttu-id="70a90-114">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="70a90-114">*Record list*</span></span>

<span data-ttu-id="70a90-115">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="70a90-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="70a90-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="70a90-116">Usage notes</span></span>

<span data-ttu-id="70a90-117">Struktura vytvořeného seznamu obsahuje pouze pole, která jsou přítomna ve struktuře každého záznamu, který je uveden v argumentech.</span><span class="sxs-lookup"><span data-stu-id="70a90-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="70a90-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="70a90-118">Example</span></span>

<span data-ttu-id="70a90-119">Zadáte zdroj dat **Záznam 1** typu *kontejner*.</span><span class="sxs-lookup"><span data-stu-id="70a90-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="70a90-120">Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:</span><span class="sxs-lookup"><span data-stu-id="70a90-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="70a90-121">**Kód:** Toto pole obsahuje výraz, který vrací hodnotu typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="70a90-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="70a90-122">**Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="70a90-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="70a90-123">Poté zadáte zdroj dat **Záznam 2** typu *kontejner*.</span><span class="sxs-lookup"><span data-stu-id="70a90-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="70a90-124">Tento zdroj dat obsahuje následující vnořená pole typu *vypočítané pole*:</span><span class="sxs-lookup"><span data-stu-id="70a90-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="70a90-125">**Množství:** Toto pole obsahuje výraz, který vrací hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="70a90-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="70a90-126">**JePlatný:** Toto pole obsahuje výraz, který vrací hodnotu typu *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="70a90-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="70a90-127">V tomto případě výraz `LIST('Record 1', 'Record 2')` vrátí nový seznam, který obsahuje dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="70a90-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="70a90-128">Struktura tohoto seznamu se skládá z jednoho pole **Množství** typu *reálné číslo*, protože toto pole je jediné pole, které je přítomno v každém argumentu volané funkce.</span><span class="sxs-lookup"><span data-stu-id="70a90-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70a90-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="70a90-129">Additional resources</span></span>

[<span data-ttu-id="70a90-130">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="70a90-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]