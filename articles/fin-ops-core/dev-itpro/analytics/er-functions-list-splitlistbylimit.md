---
title: Funkce elektronického výkaznictví SPLITLISTBYLIMIT
description: Toto téma obsahuje obecné informace o použití funkce SPLITLISTBYLIMIT elektronického výkaznictví.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743417"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="60cb0-103">Funkce elektronického výkaznictví SPLITLISTBYLIMIT</span><span class="sxs-lookup"><span data-stu-id="60cb0-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60cb0-104">Funkce `SPLITLISTBYLIMIT` rozdělí zadaný seznam na nový seznam dílčích seznamů (dávek).</span><span class="sxs-lookup"><span data-stu-id="60cb0-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="60cb0-105">Počet záznamů v každé dávce se dynamicky vypočítává.</span><span class="sxs-lookup"><span data-stu-id="60cb0-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="60cb0-106">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="60cb0-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cb0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60cb0-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="60cb0-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="60cb0-108">Arguments</span></span>

<span data-ttu-id="60cb0-109">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="60cb0-109">`list`: *Record list*</span></span>

<span data-ttu-id="60cb0-110">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="60cb0-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="60cb0-111">`limit value`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="60cb0-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="60cb0-112">Maximální hodnota limitu použitého k rozdělení původního seznamu na dávky.</span><span class="sxs-lookup"><span data-stu-id="60cb0-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="60cb0-113">`limit source`: *pole*</span><span class="sxs-lookup"><span data-stu-id="60cb0-113">`limit source`: *Field*</span></span>

<span data-ttu-id="60cb0-114">Platná cesta k poli datového typu *celé číslo* nebo *reálné číslo* v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="60cb0-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="60cb0-115">Hodnota v tomto poli definuje krok, o který je celková částka zvýšena.</span><span class="sxs-lookup"><span data-stu-id="60cb0-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="60cb0-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="60cb0-116">Return values</span></span>

<span data-ttu-id="60cb0-117">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="60cb0-117">*Record list*</span></span>

<span data-ttu-id="60cb0-118">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="60cb0-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="60cb0-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="60cb0-119">Usage notes</span></span>

<span data-ttu-id="60cb0-120">Vrácený seznam dávek obsahuje následující prvky:</span><span class="sxs-lookup"><span data-stu-id="60cb0-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="60cb0-121">**Value**: *seznam*</span><span class="sxs-lookup"><span data-stu-id="60cb0-121">**Value**: *List*</span></span>

    <span data-ttu-id="60cb0-122">Seznam záznamů, které patří do aktuální dávky.</span><span class="sxs-lookup"><span data-stu-id="60cb0-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="60cb0-123">**BatchNumber**: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="60cb0-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="60cb0-124">Číslo aktuální dávky ve vráceném seznamu.</span><span class="sxs-lookup"><span data-stu-id="60cb0-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="60cb0-125">Limit nebude použito na jednu položku z původního seznamu, když zdrojový limit překročí definovaný limit.</span><span class="sxs-lookup"><span data-stu-id="60cb0-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="60cb0-126">Příklad</span><span class="sxs-lookup"><span data-stu-id="60cb0-126">Example</span></span>

<span data-ttu-id="60cb0-127">Následující ilustrace znázorňuje formát elektronického vykazování (ER).</span><span class="sxs-lookup"><span data-stu-id="60cb0-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="60cb0-128">Následující obrázek zobrazuje formát a zdroje dat, které se pro něj používají.</span><span class="sxs-lookup"><span data-stu-id="60cb0-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="60cb0-129">Následující obrázek znázorňuje výsledek při spuštění formátu.</span><span class="sxs-lookup"><span data-stu-id="60cb0-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="60cb0-130">V takovém případě je výstup prostý seznam položek komodit.</span><span class="sxs-lookup"><span data-stu-id="60cb0-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="60cb0-131">Následující obrázek uvádí stejný formát, který byl upraven tak, aby obsahoval seznam položek komodit v dávkách, kdy musí jedna dávka zahrnovat komodity a celková hmotnost (weight) nesmí překračovat limit 9.</span><span class="sxs-lookup"><span data-stu-id="60cb0-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="60cb0-132">Následující obrázek znázorňuje výsledek při spuštění upraveného formátu.</span><span class="sxs-lookup"><span data-stu-id="60cb0-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="60cb0-133">Limit není použit na poslední položku v původním seznamu, protože hodnota (**11**) zdroje limitu (**weight**) překračuje definovaný limit (**9**).</span><span class="sxs-lookup"><span data-stu-id="60cb0-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="60cb0-134">Chcete-li ignorovat podseznamy při generování sestavy, dle potřeby použijte buď funkci `WHERE`, nebo výraz **Enabled** odpovídajícího prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="60cb0-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60cb0-135">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="60cb0-135">Additional resources</span></span>

[<span data-ttu-id="60cb0-136">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="60cb0-136">List functions</span></span>](er-functions-category-list.md)
