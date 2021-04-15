---
title: Vylepšit model předpovědi (preview)
description: Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů.
author: ShivamPandey-msft
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 197aba724ea68ef79c2d16028c23533d952329a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809999"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="c165d-103">Vylepšit model předpovědi (preview)</span><span class="sxs-lookup"><span data-stu-id="c165d-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c165d-104">Toto téma popisuje funkce, které můžete použít ke zlepšení výkonu predikčních modelů.</span><span class="sxs-lookup"><span data-stu-id="c165d-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="c165d-105">Model začnete vylepšovat v pracovním prostoru **Předpovědi plateb zákazníka** v Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c165d-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="c165d-106">Kroky vylepšení jsou poté dokončeny v AI Builderu.</span><span class="sxs-lookup"><span data-stu-id="c165d-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="c165d-107">Vyberte historické výsledky</span><span class="sxs-lookup"><span data-stu-id="c165d-107">Select historical outcomes</span></span>

<span data-ttu-id="c165d-108">Nejprve vyberete jeden nebo více ze tří možných výsledků pro faktury: **Včas**, **Pozdě** a **Velmi pozdě**.</span><span class="sxs-lookup"><span data-stu-id="c165d-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="c165d-109">Měly by být vybrány všechny tři výsledky.</span><span class="sxs-lookup"><span data-stu-id="c165d-109">All three outcomes should be selected.</span></span> <span data-ttu-id="c165d-110">Pokud zrušíte výběr některého z výsledků, faktury se odfiltrují z procesu cvičení a přesnost predikce se sníží.</span><span class="sxs-lookup"><span data-stu-id="c165d-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="c165d-111">[![Potvrzování výsledků](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="c165d-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="c165d-112">Pokud vaše organizace vyžaduje pouze dva výsledky, změňte prahové hodnoty **Pozdě** a **Velmi pozdě** na 0 (nula) dnů.</span><span class="sxs-lookup"><span data-stu-id="c165d-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="c165d-113">Tímto způsobem efektivně sbalíte předpověď na binární stav **Včas** nebo **Pozdě**.</span><span class="sxs-lookup"><span data-stu-id="c165d-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="c165d-114">Vybrat pole</span><span class="sxs-lookup"><span data-stu-id="c165d-114">Select fields</span></span>

<span data-ttu-id="c165d-115">Při výběru polí, která chcete zahrnout do modelu, mějte na paměti, že seznam obsahuje všechna dostupná pole v tabulce Microsoft Dataverse, která je mapována na data v datovém jezeře Azure.</span><span class="sxs-lookup"><span data-stu-id="c165d-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="c165d-116">Některá z těchto polí by **neměla** být vybrána.</span><span class="sxs-lookup"><span data-stu-id="c165d-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="c165d-117">Pole, která by neměla být vybrána, spadají do jedné ze tří kategorií:</span><span class="sxs-lookup"><span data-stu-id="c165d-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="c165d-118">Pole je povinné pro tabulku Dataverse, ale v datovém jezeře pro ni neexistují žádná podpůrná data.</span><span class="sxs-lookup"><span data-stu-id="c165d-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="c165d-119">Pole je ID, a proto nemá smysl pro funkci strojového učení.</span><span class="sxs-lookup"><span data-stu-id="c165d-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="c165d-120">Pole představuje informace, které během predikce nebudou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="c165d-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="c165d-121">V následujících částech jsou uvedena pole, která jsou k dispozici pro entity faktury a zákazníka, a seznam polí, která by **neměla** být vybrána pro cvičení.</span><span class="sxs-lookup"><span data-stu-id="c165d-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="c165d-122">Kategorie, která je zadána pro každé z těchto polí, odkazuje na kategorie v předchozím seznamu.</span><span class="sxs-lookup"><span data-stu-id="c165d-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="c165d-123">Tabulka faktury Dataverse</span><span class="sxs-lookup"><span data-stu-id="c165d-123">Invoice Dataverse table</span></span>

<span data-ttu-id="c165d-124">Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku faktury.</span><span class="sxs-lookup"><span data-stu-id="c165d-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="c165d-125">[![Dostupná pole pro tabulku faktury](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="c165d-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="c165d-126">Následující pole by pro cvičení neměla být vybrána:</span><span class="sxs-lookup"><span data-stu-id="c165d-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="c165d-127">**Účet faktury** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="c165d-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="c165d-128">**Je zavřena** (kategorie 3) - Toto pole se používá k filtrování faktur ke cvičení (uzavřeno) a předpověď (neuzavřeno).</span><span class="sxs-lookup"><span data-stu-id="c165d-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="c165d-129">**Název** (kategorie 1)</span><span class="sxs-lookup"><span data-stu-id="c165d-129">**Name** (category 1)</span></span>
- <span data-ttu-id="c165d-130">**ID zdroje** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="c165d-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="c165d-131">**Záznam zdroje** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="c165d-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="c165d-132">**Zdrojová tabulka** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="c165d-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="c165d-133">Tabulka zákazníka Dataverse</span><span class="sxs-lookup"><span data-stu-id="c165d-133">Customer Dataverse table</span></span>

<span data-ttu-id="c165d-134">Následující obrázek zobrazuje pole, která jsou k dispozici pro tabulku zákazníka.</span><span class="sxs-lookup"><span data-stu-id="c165d-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="c165d-135">[![Dostupná pole pro tabulku zákazníka](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="c165d-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="c165d-136">Následující pole by pro cvičení nemělo být vybráno:</span><span class="sxs-lookup"><span data-stu-id="c165d-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="c165d-137">**Unikátní klíč řádku** (kategorie 2)</span><span class="sxs-lookup"><span data-stu-id="c165d-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="c165d-138">Filtry</span><span class="sxs-lookup"><span data-stu-id="c165d-138">Filters</span></span>

<span data-ttu-id="c165d-139">Filtry aktuálně nepodporují scénář predikce plateb zákazníka.</span><span class="sxs-lookup"><span data-stu-id="c165d-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="c165d-140">Proto vyberte **Přeskočit tento krok** a pokračujte na souhrnnou stránku.</span><span class="sxs-lookup"><span data-stu-id="c165d-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="c165d-141">[![Detailní model s filtry](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="c165d-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="c165d-142">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="c165d-142">Privacy notice</span></span>
<span data-ttu-id="c165d-143">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="c165d-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]