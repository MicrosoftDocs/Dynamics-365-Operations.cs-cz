---
title: Funkce el. výkaznictví GETENUMVALUEBYNAME
description: Toto téma obsahuje obecné informace o použití funkce GETENUMVALUEBYNAME elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570583"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="79a7e-103">Funkce el. výkaznictví GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="79a7e-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79a7e-104">Funkce `GETENUMVALUEBYNAME` vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="79a7e-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="79a7e-105">Pokud je nalezena hodnota *výčet*, funkce ji vrátí.</span><span class="sxs-lookup"><span data-stu-id="79a7e-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="79a7e-106">V opačném případě funkce vrátí hodnotu výčtu **null**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a7e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79a7e-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="79a7e-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="79a7e-108">Arguments</span></span>

<span data-ttu-id="79a7e-109">`enumeration data source path`: *výčet*</span><span class="sxs-lookup"><span data-stu-id="79a7e-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="79a7e-110">Platná cesta zdroje dat jednoho z následujících typů výčtu:</span><span class="sxs-lookup"><span data-stu-id="79a7e-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="79a7e-111">Výčet modelů elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="79a7e-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="79a7e-112">Výčet formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="79a7e-112">ER format enumeration</span></span>
- <span data-ttu-id="79a7e-113">Výčet Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="79a7e-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="79a7e-114">`enumeration value text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="79a7e-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="79a7e-115">Hodnota typu řetězec, která představuje název jedné hodnoty výčtu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="79a7e-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="79a7e-116">Return values</span></span>

<span data-ttu-id="79a7e-117">Hodnota typu *výčet* s možností nabytí hodnoty Null</span><span class="sxs-lookup"><span data-stu-id="79a7e-117">Nullable *Enum*</span></span>

<span data-ttu-id="79a7e-118">Výsledná výčtová hodnota.</span><span class="sxs-lookup"><span data-stu-id="79a7e-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="79a7e-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="79a7e-119">Usage notes</span></span>

<span data-ttu-id="79a7e-120">Není vyvolána žádná výjimka, pokud není nalezena hodnota typu *výčet* za použití názvu výčtové hodnoty, která je zadána jako hodnota typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="79a7e-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="79a7e-121">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="79a7e-121">Example 1</span></span>

<span data-ttu-id="79a7e-122">Na následujícím obrázku je výčet **ReportDirection** uveden v datovém modelu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="79a7e-123">Všimněte si, že pro výčtové hodnoty jsou definovány popisky.</span><span class="sxs-lookup"><span data-stu-id="79a7e-123">Notice that labels are defined for the enumeration values.</span></span>

![Dostupné hodnoty pro výčet datového modelu](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="79a7e-125">Následující obrázek znázorňuje tyto podrobnosti:</span><span class="sxs-lookup"><span data-stu-id="79a7e-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="79a7e-126">Zdroj dat **$Direction** je konfigurován v sestavě elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="79a7e-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="79a7e-127">Tento zdroj dat je konfigurován na základě výčtu modelu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="79a7e-128">Výraz `$IsArrivals` je určený k použití zdroje dat **$Direction** výčtu modelů jako parametr této funkce.</span><span class="sxs-lookup"><span data-stu-id="79a7e-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="79a7e-129">Hodnota tohoto porovnávacího výrazu je **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-129">The value of this comparison expression is **TRUE**.</span></span>

![Příklad výčtu mapování modelu dat](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="79a7e-131">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="79a7e-131">Example 2</span></span>

<span data-ttu-id="79a7e-132">Funkce `GETENUMVALUEBYNAME` a [`LISTOFFIELDS`](er-functions-list-listoffields.md) vám umožňují načíst hodnoty a štítky podporovaných výčtů jako textové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="79a7e-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="79a7e-133">(Podporované výčty jsou výčty aplikací, výčty datových modelů a výčty formátů.)</span><span class="sxs-lookup"><span data-stu-id="79a7e-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="79a7e-134">Na následujícím obrázku je datový zdroj **TransType** uveden v mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="79a7e-135">Tento zdroj dat odkazuje na výčet aplikace **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Zdroj dat mapování modelu, který odkazuje na výčet aplikace](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="79a7e-137">Následující obrázek je datový zdroj **TransTypeList**, který je konfigurován v mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="79a7e-138">Tento zdroj dat je konfigurován na základě výčtu aplikace **TransType**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="79a7e-139">Funkce `LISTOFFIELDS` se používá k vrácení všech hodnot výčtu jako seznam záznamů, které obsahují pole.</span><span class="sxs-lookup"><span data-stu-id="79a7e-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="79a7e-140">Tímto způsobem jsou vystaveny podrobnosti každé hodnoty výčtu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="79a7e-141">Pole **EnumValue** je nakonfigurováno pro zdroj dat **TransTypeList** pomocí výrazu `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="79a7e-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="79a7e-142">Toto pole vrací hodnotu výčtu pro každý záznam v tomto seznamu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-142">This field returns an enumeration value for every record in this list.</span></span>

![Zdroj dat mapování modelu, který vrací všechny hodnoty výčtu vybraného výčtu jako seznam záznamů](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="79a7e-144">Následující obrázek je datový zdroj **VendTrans**, který je konfigurován v mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="79a7e-145">Tento zdroj dat vrací záznamy transakcí dodavatele z aplikační tabulky **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="79a7e-146">Typ typ registru každé transakce je definován hodnotou pole **TransType**.</span><span class="sxs-lookup"><span data-stu-id="79a7e-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="79a7e-147">Pole **TransTypeTitle** je nakonfigurováno pro zdroj dat **VendTrans** pomocí výrazu `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="79a7e-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="79a7e-148">Toto pole vrací štítek hodnoty výčtu aktuální transakce jako text, pokud je tato hodnota výčtu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="79a7e-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="79a7e-149">Jinak bude vrácena hodnota prázdného řetězce.</span><span class="sxs-lookup"><span data-stu-id="79a7e-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="79a7e-150">Pole **TransTypeTitle** je vázáno na pole **LedgerType** datového modelu, které umožňuje použití těchto informací v každém formátu ER, který používá datový model jako zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="79a7e-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Zdroj dat mapování modelu, který vrací transakce dodavatele](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="79a7e-152">Následující ilustrace ukazuje, jak můžete použít [ladicí program zdroje dat](er-debug-data-sources.md) a otestovat nakonfigurované mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="79a7e-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Pomocí ladicího programu zdroje dat otestujte nakonfigurované mapování modelu](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="79a7e-154">Pole **LedgerType** datového modelu vystavuje popisky typů transakcí podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="79a7e-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="79a7e-155">Pokud plánujete použít tento přístup pro velké množství transakčních dat, musíte zvážit výkon provádění.</span><span class="sxs-lookup"><span data-stu-id="79a7e-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="79a7e-156">Více informací viz [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="79a7e-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79a7e-157">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="79a7e-157">Additional resources</span></span>

[<span data-ttu-id="79a7e-158">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="79a7e-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="79a7e-159">Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem</span><span class="sxs-lookup"><span data-stu-id="79a7e-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="79a7e-160">Funkce elektronického výkaznictví LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="79a7e-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="79a7e-161">Funkce elektronického výkaznictví FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="79a7e-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="79a7e-162">Funkce elektronického výkaznictví WHERE</span><span class="sxs-lookup"><span data-stu-id="79a7e-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]