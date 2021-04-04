---
title: Funkce el. výkaznictví NUMSEQVALUE
description: Toto téma obsahuje obecné informace o použití funkce NUMSEQVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 23dc112651e4425b8020ee5c843509b4df83e810
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563311"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="30d9d-103">Funkce el. výkaznictví NUMSEQVALUE</span><span class="sxs-lookup"><span data-stu-id="30d9d-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30d9d-104">Funkce `NUMSEQVALUE` vrátí *řetězcovou* hodnotu, která představuje novou vygenerovanou hodnotu číselné řady založenou na zadané číselné řadě, rozsahu a ID oboru.</span><span class="sxs-lookup"><span data-stu-id="30d9d-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="30d9d-105">ID oboru se rovná kódu společnosti, který je poskytnut v kontextu, ve kterém je spuštěn formát elektronického vykazování (ER).</span><span class="sxs-lookup"><span data-stu-id="30d9d-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="30d9d-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="30d9d-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="30d9d-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="30d9d-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="30d9d-108">Syntaxe 3</span><span class="sxs-lookup"><span data-stu-id="30d9d-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="30d9d-109">Argumenty</span><span class="sxs-lookup"><span data-stu-id="30d9d-109">Arguments</span></span>

<span data-ttu-id="30d9d-110">`number sequence code`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="30d9d-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="30d9d-111">Textová hodnota, která představuje kód číselné řady, ve které je požadována nová hodnota.</span><span class="sxs-lookup"><span data-stu-id="30d9d-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="30d9d-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="30d9d-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="30d9d-113">Hodnota *Int64*, která představuje ID záznamu v tabulce NumberSequenceTable, která obsahuje definici číselné řady, ve které je požadována nová hodnota.</span><span class="sxs-lookup"><span data-stu-id="30d9d-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="30d9d-114">`scope type`: *hodnota výčtu*</span><span class="sxs-lookup"><span data-stu-id="30d9d-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="30d9d-115">Hodnota výčtu **ERExpressionNumberSequenceScopeType**, která definuje obor číselné řady, ve které je požadována nová hodnota.</span><span class="sxs-lookup"><span data-stu-id="30d9d-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="30d9d-116">Dostupné typy oborů jsou **Sdílený**, **Právnická osoba** a **Společnosti**</span><span class="sxs-lookup"><span data-stu-id="30d9d-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="30d9d-117">`scope ID`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="30d9d-117">`scope ID`: *String*</span></span>

<span data-ttu-id="30d9d-118">Hodnota typu *řetězec* identifikující obor na základě zadaného typu oboru.</span><span class="sxs-lookup"><span data-stu-id="30d9d-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="30d9d-119">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="30d9d-119">Return values</span></span>

<span data-ttu-id="30d9d-120">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="30d9d-120">*String*</span></span>

<span data-ttu-id="30d9d-121">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="30d9d-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="30d9d-122">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="30d9d-122">Usage notes</span></span>

<span data-ttu-id="30d9d-123">Pro typ oboru **Sdílený** zadejte prázdný řetězec jako ID oboru.</span><span class="sxs-lookup"><span data-stu-id="30d9d-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="30d9d-124">Pro typy oborů **Společnost** a **Právnická osoba** zadejte kód společnosti jako ID oboru.</span><span class="sxs-lookup"><span data-stu-id="30d9d-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="30d9d-125">Pokud pro tyto typy oborů zadáte prázdný řetězec, použije se aktuální kód společnosti.</span><span class="sxs-lookup"><span data-stu-id="30d9d-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="30d9d-126">Při použití syntaxe 1 je požadována číselná řada pro typ oboru **Společnost** a kód společnosti je poskytnut v kontextu, ve kterém je spuštěn formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="30d9d-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="30d9d-127">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="30d9d-127">Example 1</span></span>

<span data-ttu-id="30d9d-128">Ve vašem formátu elektronického výkaznictví definujete zdroj dat **AskNumSeq** pro typ *parametru vstupu uživatele*.</span><span class="sxs-lookup"><span data-stu-id="30d9d-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="30d9d-129">Tento zdroj dat odkazuje na rozšířený datový typ (EDT) **popis**.</span><span class="sxs-lookup"><span data-stu-id="30d9d-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="30d9d-130">Dále definujete zdroj dat **NumSeq** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="30d9d-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="30d9d-131">Tento zdroj dat obsahuje výraz `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="30d9d-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="30d9d-132">Když je zavolán zdroj dat **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady, která byla zadána v době běhu zadáním jeho kódu do dialogového okna.</span><span class="sxs-lookup"><span data-stu-id="30d9d-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="30d9d-133">Číselná řada je požadována pro typ oboru **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="30d9d-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="30d9d-134">Kód společnosti je poskytnut v kontextu, ve kterém je spuštěn formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="30d9d-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="30d9d-135">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="30d9d-135">Example 2</span></span>

<span data-ttu-id="30d9d-136">V mapování modelu jsou definovány následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="30d9d-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="30d9d-137">Zdroj dat **LedgerParms** typu *tabulka*.</span><span class="sxs-lookup"><span data-stu-id="30d9d-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="30d9d-138">Tento zdroj dat odkazuje na tabulku LedgerParameters.</span><span class="sxs-lookup"><span data-stu-id="30d9d-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="30d9d-139">Zdroj dat **NumSeq** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="30d9d-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="30d9d-140">Tento zdroj dat obsahuje výraz `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="30d9d-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="30d9d-141">Když je volán datový zdroj **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady, která byla nakonfigurována v parametrech hlavní knihy pro společnost poskytující kontext, pod kterým běží formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="30d9d-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="30d9d-142">Tato číselná řada jedinečně identifikuje deníky a chová se jako číslo dávky propojující transakce dohromady.</span><span class="sxs-lookup"><span data-stu-id="30d9d-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="30d9d-143">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="30d9d-143">Example 3</span></span>

<span data-ttu-id="30d9d-144">V mapování modelu jsou definovány následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="30d9d-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="30d9d-145">Zdroj dat **enumScope** pro typ *výčet* aplikace Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="30d9d-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="30d9d-146">Tento zdroj dat odkazuje na výčet **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="30d9d-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="30d9d-147">Zdroj dat **NumSeq** typu *vypočítané pole*.</span><span class="sxs-lookup"><span data-stu-id="30d9d-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="30d9d-148">Tento zdroj dat obsahuje výraz `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="30d9d-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="30d9d-149">Když je volán datový zdroj **NumSeq**, vrátí novou vygenerovanou hodnotu číselné řady **Gene\_1**, která byla nakonfigurována pro společnost poskytující kontext, pod kterým běží formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="30d9d-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30d9d-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="30d9d-150">Additional resources</span></span>

[<span data-ttu-id="30d9d-151">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="30d9d-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]