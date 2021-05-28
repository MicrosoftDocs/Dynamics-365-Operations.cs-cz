---
title: Diagnostické typy pro neshody
description: Toto téma popisuje, jak používat a vytvářet diagnostické typy, které lze použít s neshodami.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022269"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="b65cb-103">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="b65cb-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b65cb-104">Toto téma popisuje, jak používat a vytvářet diagnostické typy, které lze použít s neshodami.</span><span class="sxs-lookup"><span data-stu-id="b65cb-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="b65cb-105">Pomocí stránky **Typy diagnostiky** definujte klasifikaci akcí diagnostiky.</span><span class="sxs-lookup"><span data-stu-id="b65cb-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="b65cb-106">Poté, co vytvoříte opravu pro neshodu, vyberete diagnostiku.</span><span class="sxs-lookup"><span data-stu-id="b65cb-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="b65cb-107">Oprava určuje, jaký typ diagnostické akce se má provést pro schválenou neshodu a kdo ji má provést.</span><span class="sxs-lookup"><span data-stu-id="b65cb-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="b65cb-108">Určuje rovněž požadované datum dokončení a plánované datum dokončení.</span><span class="sxs-lookup"><span data-stu-id="b65cb-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="b65cb-109">Příklady typů diagnostik</span><span class="sxs-lookup"><span data-stu-id="b65cb-109">Examples of diagnostic types</span></span>

<span data-ttu-id="b65cb-110">Pracujete pro výrobní společnost a několik položek prošlo testy kvality.</span><span class="sxs-lookup"><span data-stu-id="b65cb-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="b65cb-111">Tyto položky jsou přesunuty do oblasti karantény a označeny jako nevyhovující produkty.</span><span class="sxs-lookup"><span data-stu-id="b65cb-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="b65cb-112">V Microsoft Dynamics 365 Supply Chain Management se vytvoří záznam o neshodě ke sledování podrobností pomocí řešení problému.</span><span class="sxs-lookup"><span data-stu-id="b65cb-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="b65cb-113">V tomto případě dochází k problémům s kvalitou, protože ložiska ve stroji, který balí položky, se pokazily a přehřívají se.</span><span class="sxs-lookup"><span data-stu-id="b65cb-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="b65cb-114">Oprava tohoto problému spočívá ve výměně dílů ve stroji.</span><span class="sxs-lookup"><span data-stu-id="b65cb-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="b65cb-115">Když konfigurujete typy diagnostiky, můžete vytvořit více záznamů, z nichž každý představuje jiný typ problému, který může stroj mít.</span><span class="sxs-lookup"><span data-stu-id="b65cb-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="b65cb-116">Alternativně můžete vytvořit jeden obecný diagnostický typ, který představuje opravu stroje.</span><span class="sxs-lookup"><span data-stu-id="b65cb-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="b65cb-117">Vytvoření typu diagnostiky</span><span class="sxs-lookup"><span data-stu-id="b65cb-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="b65cb-118">Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Typy diagnostiky**.</span><span class="sxs-lookup"><span data-stu-id="b65cb-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="b65cb-119">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="b65cb-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b65cb-120">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="b65cb-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b65cb-121">**Diagnostika** - Zadejte jedinečné ID nebo název pro typ diagnostiky.</span><span class="sxs-lookup"><span data-stu-id="b65cb-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="b65cb-122">**Popis** - Zadejte podrobný popis typu diagnostiky.</span><span class="sxs-lookup"><span data-stu-id="b65cb-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="b65cb-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b65cb-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b65cb-124">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b65cb-124">Additional resources</span></span>

- [<span data-ttu-id="b65cb-125">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="b65cb-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="b65cb-126">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="b65cb-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="b65cb-127">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="b65cb-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="b65cb-128">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="b65cb-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="b65cb-129">Typy problémů pro neshody</span><span class="sxs-lookup"><span data-stu-id="b65cb-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="b65cb-130">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="b65cb-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="b65cb-131">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="b65cb-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="b65cb-132">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="b65cb-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
