---
title: Schválení modelu konfigurace produktu
description: Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920500"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="3c471-103">Schválení modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="3c471-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c471-104">Spuštění této procedury vyžaduje, aby nejméně jeden model konfigurace produktu byl k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3c471-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="3c471-105">Tento postup využívá model špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3c471-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="3c471-106">Všimněte si, že tento model již byl schválen, ale postup vás provede celým procesem.</span><span class="sxs-lookup"><span data-stu-id="3c471-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="3c471-107">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="3c471-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="3c471-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3c471-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3c471-109">Pro tuto proceduru vyberte model špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="3c471-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="3c471-110">Vyberte **Verze**.</span><span class="sxs-lookup"><span data-stu-id="3c471-110">Select **Versions**.</span></span>
1. <span data-ttu-id="3c471-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="3c471-111">Select **New**.</span></span>
1. <span data-ttu-id="3c471-112">V poli **Číslo produktu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3c471-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="3c471-113">Odkaz na produkt představuje verzi modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="3c471-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="3c471-114">V seznamu se zobrazí pouze základní produkty, které mají technologii konfigurace založenou na omezeních.</span><span class="sxs-lookup"><span data-stu-id="3c471-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="3c471-115">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="3c471-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="3c471-116">Vyberte, kdy bude verze modelu produktu k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3c471-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="3c471-117">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="3c471-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="3c471-118">Vyberte koncové datum, kdy této verzi modelu produktu vyprší platnost, nebo vyberte Nikdy.</span><span class="sxs-lookup"><span data-stu-id="3c471-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="3c471-119">Kliknutím na možnost **Schválit** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="3c471-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="3c471-120">V poli **Schválil(a)** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3c471-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="3c471-121">Vyberte osobu, která je odpovědná za schválení modelů produktu pro použití v operacích.</span><span class="sxs-lookup"><span data-stu-id="3c471-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="3c471-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c471-122">Select **OK**.</span></span>
1. <span data-ttu-id="3c471-123">Vyberte možnost v poli **Metoda cenových kalkulací**.</span><span class="sxs-lookup"><span data-stu-id="3c471-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="3c471-124">Aktivujte verzi modelu výrobku.</span><span class="sxs-lookup"><span data-stu-id="3c471-124">Activate the product model version.</span></span> <span data-ttu-id="3c471-125">Pro jeden model produktu je možné současně mít aktivní pouze jeden produkt.</span><span class="sxs-lookup"><span data-stu-id="3c471-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="3c471-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3c471-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]