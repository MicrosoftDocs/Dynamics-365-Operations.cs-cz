---
title: Vytváření konfigurací založených na dimenzích
description: Tento postup popisuje, jak definovat konfiguraci produktu založeného na dimenzích.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920674"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="638bb-103">Vytváření konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="638bb-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="638bb-104">Tento postup popisuje, jak definovat konfiguraci produktu založeného na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="638bb-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="638bb-105">Jedná se o poslední postup v sérii, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="638bb-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="638bb-106">Spuštění tohoto postupu je závislé na datu vytvořeném v předchozích sedmi záznamech.</span><span class="sxs-lookup"><span data-stu-id="638bb-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="638bb-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="638bb-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="638bb-108">Vyhledání hlavního produktu založeného na dimenzích</span><span class="sxs-lookup"><span data-stu-id="638bb-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="638bb-109">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="638bb-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="638bb-110">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="638bb-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="638bb-111">Vyberte základní produkt založený na dimenzích, který jste vytvořili v prvním záznamu v tomto pořadí 8 záznamů.</span><span class="sxs-lookup"><span data-stu-id="638bb-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="638bb-112">Vytvoření konfigurací</span><span class="sxs-lookup"><span data-stu-id="638bb-112">Create configurations</span></span>

1. <span data-ttu-id="638bb-113">V podokně akcí **Analýza** klikněte na položku **Udržovat konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="638bb-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="638bb-114">Vyberte **Nakonfigurovat**.</span><span class="sxs-lookup"><span data-stu-id="638bb-114">Select **Configure**.</span></span>
1. <span data-ttu-id="638bb-115">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="638bb-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="638bb-116">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="638bb-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="638bb-117">Vyberte některou z položek v první konfigurační skupině.</span><span class="sxs-lookup"><span data-stu-id="638bb-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="638bb-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="638bb-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="638bb-119">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="638bb-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="638bb-120">Vyberte některou z položek ve druhé konfigurační skupině.</span><span class="sxs-lookup"><span data-stu-id="638bb-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="638bb-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="638bb-121">Select **OK**.</span></span>
1. <span data-ttu-id="638bb-122">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="638bb-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="638bb-123">Zadejte hodnotu do pole **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="638bb-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="638bb-124">Zadejte název konfigurace, který vám usnadní identifikaci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="638bb-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="638bb-125">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="638bb-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="638bb-126">Zadejte popis konfigurace vysvětlující její obsahuj.</span><span class="sxs-lookup"><span data-stu-id="638bb-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="638bb-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="638bb-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]