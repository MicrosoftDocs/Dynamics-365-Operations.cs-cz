---
title: Typy problémů pro neshody
description: Toto téma popisuje, jak vytvářet a používat typy problémů pro neshody.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956584"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="12ab9-103">Typy problémů pro neshody</span><span class="sxs-lookup"><span data-stu-id="12ab9-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12ab9-104">Toto téma popisuje, jak vytvářet a používat typy problémů pro neshody.</span><span class="sxs-lookup"><span data-stu-id="12ab9-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="12ab9-105">Stránku **Typy problémů** použijte k definování klasifikace problémů s kvalitou, které mohou nastat u různých typů neshod.</span><span class="sxs-lookup"><span data-stu-id="12ab9-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="12ab9-106">Pro každý typ problému, který vytvoříte, musíte určit typy neshod, se kterými lze typ problému použít.</span><span class="sxs-lookup"><span data-stu-id="12ab9-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="12ab9-107">Můžete nastavit následující typy neshod:</span><span class="sxs-lookup"><span data-stu-id="12ab9-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="12ab9-108">**Interní** – neshody tohoto typu se vztahují k zásobám na skladě (například k objednávkám kvality nebo karanténním příkazům).</span><span class="sxs-lookup"><span data-stu-id="12ab9-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="12ab9-109">**Odběratel** – neshody tohoto typu souvisejí s prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="12ab9-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="12ab9-110">**Dodavatel** – neshody tohoto typu souvisejí s nákupními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="12ab9-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="12ab9-111">**Požadavek na službu** – neshody tohoto typu souvisejí se servisními zakázkami.</span><span class="sxs-lookup"><span data-stu-id="12ab9-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="12ab9-112">**Výroba** – neshody tohoto typu souvisejí s dávkovými objednávkami nebo výrobními zakázkami.</span><span class="sxs-lookup"><span data-stu-id="12ab9-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="12ab9-113">**Výroba vedlejších produktů** – neshody tohoto typu souvisejí s dávkovými objednávkami vedlejších produktů.</span><span class="sxs-lookup"><span data-stu-id="12ab9-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="12ab9-114">Když vytváříte nový typ problému, vyberte v podokně akcí možnost **Typy neshody** k vytvoření seznamu jednoho nebo více typů neshod, které jsou autorizovány pro daný typ problému.</span><span class="sxs-lookup"><span data-stu-id="12ab9-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="12ab9-115">Typ problémů, který například souvisí s kódem defektu, je možné použít na všechny typy neshod.</span><span class="sxs-lookup"><span data-stu-id="12ab9-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="12ab9-116">Typ problému související se stížnostmi odběratelů se však může vztahovat pouze na typy neshod **Odběratel** a **Požadavek na službu**.</span><span class="sxs-lookup"><span data-stu-id="12ab9-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="12ab9-117">Příklady typů problémů</span><span class="sxs-lookup"><span data-stu-id="12ab9-117">Examples of problem types</span></span>

<span data-ttu-id="12ab9-118">Tady je několik příkladů scénářů pro typy problémů, které lze použít s různými typy neshod:</span><span class="sxs-lookup"><span data-stu-id="12ab9-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="12ab9-119">**Odběratel:** Odběratel podal stížnost, provedl vratku nebo nebyly splněny specifikace kvality.</span><span class="sxs-lookup"><span data-stu-id="12ab9-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="12ab9-120">**Dodavatel:** Produkt byl poškozen, nebyly splněny specifikace kvality nebo byl obdržen nesprávný produkt.</span><span class="sxs-lookup"><span data-stu-id="12ab9-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="12ab9-121">**Požadavek na službu:** Nebyly splněny specifikace kvality, odběratel podal stížnost nebo je vyžadována údržba stroje.</span><span class="sxs-lookup"><span data-stu-id="12ab9-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="12ab9-122">**Výroba:** Nebyly splněny specifikace kvality, je vyžadována údržba stroje nebo byl produkt poškozen.</span><span class="sxs-lookup"><span data-stu-id="12ab9-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="12ab9-123">**Výroba vedlejších produktů:** Nebyly splněny specifikace kvality, je vyžadována údržba stroje nebo byl produkt poškozen.</span><span class="sxs-lookup"><span data-stu-id="12ab9-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="12ab9-124">Vytvoření typu problému a jeho přiřazení k typům neshod</span><span class="sxs-lookup"><span data-stu-id="12ab9-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="12ab9-125">Přejděte k nabídce **Řízení zásob \> Nastavení \> Správa kvality \> Typy problémů**.</span><span class="sxs-lookup"><span data-stu-id="12ab9-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="12ab9-126">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="12ab9-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12ab9-127">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="12ab9-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="12ab9-128">**Typ problému** – zadejte jedinečné ID nebo název pro typ problému.</span><span class="sxs-lookup"><span data-stu-id="12ab9-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="12ab9-129">**Popis** – zadejte podrobný popis typu problému.</span><span class="sxs-lookup"><span data-stu-id="12ab9-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="12ab9-130">Zatímco je stále vybrán nový řádek, vyberte v podokně akcí možnost **Typy neshody**.</span><span class="sxs-lookup"><span data-stu-id="12ab9-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="12ab9-131">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="12ab9-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="12ab9-132">Poté pro nový řádek nastavte pole **Typ neshody** na typ neshody, který chcete povolit pro typ problému.</span><span class="sxs-lookup"><span data-stu-id="12ab9-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="12ab9-133">Opakujte předchozí krok pro každý další typ neshody, který chcete autorizovat pro typ problému.</span><span class="sxs-lookup"><span data-stu-id="12ab9-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="12ab9-134">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="12ab9-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12ab9-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="12ab9-135">Additional resources</span></span>

- [<span data-ttu-id="12ab9-136">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="12ab9-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="12ab9-137">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="12ab9-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="12ab9-138">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="12ab9-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="12ab9-139">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="12ab9-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="12ab9-140">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="12ab9-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="12ab9-141">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="12ab9-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="12ab9-142">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="12ab9-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="12ab9-143">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="12ab9-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
