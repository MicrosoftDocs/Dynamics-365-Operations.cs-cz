---
title: Kontrola kvality zboží
description: Toto téma vysvětluje, jak zpracovat objednávku kvality.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145610"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="e2706-103">Kontrola kvality zboží</span><span class="sxs-lookup"><span data-stu-id="e2706-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2706-104">Toto téma vysvětluje, jak zpracovat objednávku kvality.</span><span class="sxs-lookup"><span data-stu-id="e2706-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="e2706-105">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e2706-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="e2706-106">Před zahájením tohoto vzorového postupu je nutné potvrdit nákupní objednávku „000016“ a zaúčtovat příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="e2706-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="e2706-107">To způsobí automatické vytvoření objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="e2706-107">This will automatically create a quality order.</span></span> <span data-ttu-id="e2706-108">Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.</span><span class="sxs-lookup"><span data-stu-id="e2706-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="e2706-109">Vyberte objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="e2706-109">Select a quality order</span></span>
1. <span data-ttu-id="e2706-110">V podokně navigace přejděte na **Moduly > Řízení zásob > Periodické úlohy > Správa kvality > Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="e2706-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="e2706-111">Vyberte objednávku kvality, která byla vytvořena před zahájením tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="e2706-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="e2706-112">Záznam výsledků testu</span><span class="sxs-lookup"><span data-stu-id="e2706-112">Record test results</span></span>
1. <span data-ttu-id="e2706-113">Vyberte **Výsledky**</span><span class="sxs-lookup"><span data-stu-id="e2706-113">Select **Results**.</span></span>
2. <span data-ttu-id="e2706-114">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="e2706-114">Select **Edit**.</span></span>
3. <span data-ttu-id="e2706-115">V poli **Výsledné množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e2706-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="e2706-116">V poli **Výsledek** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="e2706-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="e2706-117">V tomto příkladu vychází výsledek z předem definovaného výsledku.</span><span class="sxs-lookup"><span data-stu-id="e2706-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="e2706-118">Běžně byste vytvořili záznam s mnohem přesnějšími výsledky, jako například s velikostí nebo jinou dimenzí.</span><span class="sxs-lookup"><span data-stu-id="e2706-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="e2706-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e2706-119">Select **Save**.</span></span>
6. <span data-ttu-id="e2706-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e2706-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="e2706-121">Ověřit objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="e2706-121">Validate the quality order</span></span>
1. <span data-ttu-id="e2706-122">Vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="e2706-122">Select **Validate**.</span></span>
2. <span data-ttu-id="e2706-123">V poli **Ověřil/a** vyberte uživatele provádějícího kontrolu z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="e2706-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="e2706-124">Klepněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="e2706-124">Click **Select**.</span></span>
4. <span data-ttu-id="e2706-125">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2706-125">Select **OK**.</span></span>
5. <span data-ttu-id="e2706-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e2706-126">Close the page.</span></span>

