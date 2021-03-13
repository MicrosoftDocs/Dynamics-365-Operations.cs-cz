---
title: Vylepšit model předpovědi (preview)
description: Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009361"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="65a23-103">Vylepšit model předpovědi (preview)</span><span class="sxs-lookup"><span data-stu-id="65a23-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="65a23-104">Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů.</span><span class="sxs-lookup"><span data-stu-id="65a23-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="65a23-105">Model začnete vylepšovat v pracovním prostoru **Předpovědi plateb zákazníka** v Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="65a23-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="65a23-106">Kroky vylepšení jsou poté dokončeny v AI Builderu.</span><span class="sxs-lookup"><span data-stu-id="65a23-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="65a23-107">Vyberte historické výsledky</span><span class="sxs-lookup"><span data-stu-id="65a23-107">Select historical outcomes</span></span>

<span data-ttu-id="65a23-108">Nejprve vyberete jeden nebo více ze tří možných výsledků pro faktury: **Včas**, **Pozdě** a **Velmi pozdě**.</span><span class="sxs-lookup"><span data-stu-id="65a23-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="65a23-109">Měly by být vybrány všechny tři výsledky.</span><span class="sxs-lookup"><span data-stu-id="65a23-109">All three outcomes should be selected.</span></span> <span data-ttu-id="65a23-110">Pokud zrušíte výběr některého z výsledků, faktury se odfiltrují z procesu cvičení a přesnost predikce se sníží.</span><span class="sxs-lookup"><span data-stu-id="65a23-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="65a23-111">[![Potvrzování výsledků](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="65a23-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="65a23-112">Pokud vaše organizace vyžaduje pouze dva výsledky, změňte prahové hodnoty **Pozdě** a **Velmi pozdě** na 0 (nula) dnů.</span><span class="sxs-lookup"><span data-stu-id="65a23-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="65a23-113">Tímto způsobem efektivně sbalíte předpověď na binární stav **Včas** nebo **Pozdě**.</span><span class="sxs-lookup"><span data-stu-id="65a23-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="65a23-114">Vybrat pole</span><span class="sxs-lookup"><span data-stu-id="65a23-114">Select fields</span></span>

<span data-ttu-id="65a23-115">Při výběru polí, která chcete zahrnout do modelu, mějte na paměti, že seznam obsahuje všechna dostupná pole v tabulce Microsoft Dataverse, která je mapována na data v datovém jezeře Azure.</span><span class="sxs-lookup"><span data-stu-id="65a23-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="65a23-116">Některá z těchto polí by **neměla** být vybrána.</span><span class="sxs-lookup"><span data-stu-id="65a23-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="65a23-117">Pole, která by neměla být vybrána, spadají do jedné ze tří kategorií:</span><span class="sxs-lookup"><span data-stu-id="65a23-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="65a23-118">Pole je povinné pro tabulku Dataverse, ale v datovém jezeře pro ni neexistují žádná podpůrná data.</span><span class="sxs-lookup"><span data-stu-id="65a23-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="65a23-119">Pole je ID, a proto nemá smysl pro funkci strojového učení.</span><span class="sxs-lookup"><span data-stu-id="65a23-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="65a23-120">Pole představuje informace, které během predikce nebudou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="65a23-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="65a23-121">V následujících částech jsou uvedena pole, která jsou k dispozici pro entity faktury a zákazníka, a seznam polí, která by **neměla** být vybrána pro cvičení.</span><span class="sxs-lookup"><span data-stu-id="65a23-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="65a23-122">Kategorie, která je zadána pro každé z těchto polí, odkazuje na kategorie v předchozím seznamu.</span><span class="sxs-lookup"><span data-stu-id="65a23-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="65a23-123">Tabulka faktury Dataverse</span><span class="sxs-lookup"><span data-stu-id="65a23-123">Invoice Dataverse table</span></span>

<span data-ttu-id="65a23-124">Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku faktury.</span><span class="sxs-lookup"><span data-stu-id="65a23-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="65a23-125">[![Dostupná pole pro tabulku faktury](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="65a23-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="65a23-126">Následující pole by pro cvičení neměla být vybrána:</span><span class="sxs-lookup"><span data-stu-id="65a23-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="65a23-127">**Účet faktury** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="65a23-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="65a23-128">**Je zavřena** (kategorie 3) - Toto pole se používá k filtrování faktur ke cvičení (uzavřeno) a předpověď (neuzavřeno).</span><span class="sxs-lookup"><span data-stu-id="65a23-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="65a23-129">**Název** (kategorie 1)</span><span class="sxs-lookup"><span data-stu-id="65a23-129">**Name** (category 1)</span></span>
- <span data-ttu-id="65a23-130">**ID zdroje** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="65a23-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="65a23-131">**Záznam zdroje** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="65a23-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="65a23-132">**Zdrojová tabulka** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="65a23-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="65a23-133">Tabulka zákazníka Dataverse</span><span class="sxs-lookup"><span data-stu-id="65a23-133">Customer Dataverse table</span></span>

<span data-ttu-id="65a23-134">Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku zákazníka.</span><span class="sxs-lookup"><span data-stu-id="65a23-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="65a23-135">[![Dostupná pole pro tabulku zákazníka](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="65a23-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="65a23-136">Následující pole by pro cvičení nemělo být vybráno:</span><span class="sxs-lookup"><span data-stu-id="65a23-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="65a23-137">**Unikátní klíč řádku** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="65a23-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="65a23-138">Filtry</span><span class="sxs-lookup"><span data-stu-id="65a23-138">Filters</span></span>

<span data-ttu-id="65a23-139">Filtry aktuálně nepodporují scénář predikce plateb zákazníka.</span><span class="sxs-lookup"><span data-stu-id="65a23-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="65a23-140">Proto vyberte **Přeskočit tento krok** a pokračujte na souhrnnou stránku.</span><span class="sxs-lookup"><span data-stu-id="65a23-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="65a23-141">[![Detailní model s filtry](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="65a23-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="65a23-142">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="65a23-142">Privacy notice</span></span>
<span data-ttu-id="65a23-143">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="65a23-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
