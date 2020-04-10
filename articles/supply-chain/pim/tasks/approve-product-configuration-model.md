---
title: Schválení modelu konfigurace produktu
description: Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 317aa9ad5bc5953b7148846622b893e5b525c637
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150187"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="593d8-103">Schválení modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="593d8-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="593d8-104">Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.</span><span class="sxs-lookup"><span data-stu-id="593d8-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="593d8-105">Tento postup využívá model špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="593d8-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="593d8-106">Všimněte si, že tento model již byl schválen, ale postup vás provede celým procesem.</span><span class="sxs-lookup"><span data-stu-id="593d8-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="593d8-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="593d8-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="593d8-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="593d8-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="593d8-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="593d8-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="593d8-110">Pro tuto proceduru vyberte model špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="593d8-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="593d8-111">Klepněte na Verze.</span><span class="sxs-lookup"><span data-stu-id="593d8-111">Click Versions.</span></span>
5. <span data-ttu-id="593d8-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="593d8-112">Click New.</span></span>
6. <span data-ttu-id="593d8-113">V poli Číslo produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="593d8-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="593d8-114">Odkaz na produkt představuje verzi modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="593d8-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="593d8-115">V seznamu se zobrazí pouze základní produkty, které mají technologii konfigurace založenou na omezeních.</span><span class="sxs-lookup"><span data-stu-id="593d8-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="593d8-116">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="593d8-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="593d8-117">Vyberte, kdy bude verze modelu produktu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="593d8-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="593d8-118">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="593d8-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="593d8-119">Vyberte koncové datum, kdy této verzi modelu produktu vyprší platnost, nebo vyberte Nikdy.</span><span class="sxs-lookup"><span data-stu-id="593d8-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="593d8-120">Klepnutím na možnost Schválit otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="593d8-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="593d8-121">V poli Schválil(a) zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="593d8-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="593d8-122">Vyberte osobu, která je odpovědná za schválení modelů produktu pro použití v operacích.</span><span class="sxs-lookup"><span data-stu-id="593d8-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="593d8-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="593d8-123">Click OK.</span></span>
12. <span data-ttu-id="593d8-124">Vyberte možnost v poli Metoda cenových kalkulací.</span><span class="sxs-lookup"><span data-stu-id="593d8-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="593d8-125">Aktivujte verzi modelu výrobku.</span><span class="sxs-lookup"><span data-stu-id="593d8-125">Activate the product model version.</span></span> <span data-ttu-id="593d8-126">Pro jeden model produktu je možné současně mít aktivní pouze jeden produkt.</span><span class="sxs-lookup"><span data-stu-id="593d8-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="593d8-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="593d8-127">Close the page.</span></span>

