---
title: "Amortizace konstantních nákladů na vyráběné zboží"
description: "Konstantní náklady na vyráběné zboží reflektují doby nastavení operace a komponenty s konstantní kvalitou nebo s konstantní odpadovostí."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7ccd5ce3e2ed58db8f13eebbcfa6fe5fb544d6c7
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="e7e86-103">Amortizace konstantních nákladů na vyráběné zboží</span><span class="sxs-lookup"><span data-stu-id="e7e86-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7e86-104">Konstantní náklady na vyráběné zboží reflektují doby nastavení operace a komponenty s konstantní kvalitou nebo s konstantní odpadovostí.</span><span class="sxs-lookup"><span data-stu-id="e7e86-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="e7e86-105">Koncept velikosti nákladové šarže slouží k amortizaci těchto konstantních nákladů ve vypočteném nákladu na vyráběnou položku.</span><span class="sxs-lookup"><span data-stu-id="e7e86-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="e7e86-106">Tento koncept má několik synonym, z nichž jedním je velikost účetní šarže.</span><span class="sxs-lookup"><span data-stu-id="e7e86-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="e7e86-107">Koncept amortizace konstantních nákladů má také několik synonym, z nichž jedním jsou proporční konstantní náklady.</span><span class="sxs-lookup"><span data-stu-id="e7e86-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="e7e86-108">Množství velikosti nákladové šarže pro vyráběnou položku je používáno ve výpočtu ceny kusovníku (BOM).</span><span class="sxs-lookup"><span data-stu-id="e7e86-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="e7e86-109">Množství závisí na způsobu zahájení a provedení výpočtu ceny kusovníku, jak je uvedeno dále:</span><span class="sxs-lookup"><span data-stu-id="e7e86-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="e7e86-110">Výchozí množství pro výpočet ve výpočtu ceny kusovníku položky − Standardní množství objednávky této položky (pro sklad) se chová jako výchozí možnost velikosti nákladové šarže, ale výchozí možnost by mohla být větší, aby reflektovala násobek množství objednávky položky.</span><span class="sxs-lookup"><span data-stu-id="e7e86-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="e7e86-111">Standardní množství objednávky této položky a jeho násobek lze definovat ve výchozím nastavení objednávky nebo v nastaveních objednávky specifických pro pracoviště.</span><span class="sxs-lookup"><span data-stu-id="e7e86-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="e7e86-112">Zadané množství pro výpočet ve výpočtu ceny kusovníku položky − Zadané množství pro výpočet se chová jako velikost nákladové šarže této položky.</span><span class="sxs-lookup"><span data-stu-id="e7e86-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="e7e86-113">Na počátku vypočtené množství používá standardní množství objednávky tohoto zboží, ale tuto výchozí hodnotu lze ručně přepsat.</span><span class="sxs-lookup"><span data-stu-id="e7e86-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="e7e86-114">Zadané množství pro výpočet reprezentuje velikost nákladové šarže dané položky a vyráběných komponent, které mají typ výroby Řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="e7e86-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="e7e86-115">Důvodem je předpoklad, že součást bude vyráběna v přesném množství.</span><span class="sxs-lookup"><span data-stu-id="e7e86-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="e7e86-116">Velikost nákladové šarže vyráběných součástí s produkcí typu kusovník bude odpovídat standardnímu množství objednávky.</span><span class="sxs-lookup"><span data-stu-id="e7e86-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="e7e86-117">Zadané množství pro výpočet pro objednávku ve výpočtu ceny kusovníku položky − Zadané množství pro výpočet se v případě, že výpočet ceny kusovníku používá režim rozpadu pro objednávku, chová jako velikost nákladové šarže položky a jejích vyráběných součástí.</span><span class="sxs-lookup"><span data-stu-id="e7e86-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="e7e86-118">Předpokládá se, že vyráběné součásti budou vyráběny ve stejném množství, stejně jako vyráběná součást s produkcí typu kusovník.</span><span class="sxs-lookup"><span data-stu-id="e7e86-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="e7e86-119">Zadané množství pro výpočet ve výpočtu ceny kusovníku specifickém pro objednávku − Výpočet ceny kusovníku specifický pro objednávku lze provést pro položku řádku kusovníku na prodejní objednávce, na prodejní nabídce nebo na servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="e7e86-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="e7e86-120">Určené množství pro výpočet využívá množství původní položky řádku, ale toto výchozí množství lze přepsat.</span><span class="sxs-lookup"><span data-stu-id="e7e86-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="e7e86-121">Můžete vybrat, zda bude výpočet ceny kusovníku specifický pro objednávku používat režim rozpadu pro objednávku nebo režim rozpadu na více úrovních.</span><span class="sxs-lookup"><span data-stu-id="e7e86-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="e7e86-122">Vypočtené množství amortizovaných konstantních nákladů na vyráběnou položku je označeno jako termínované náklady.</span><span class="sxs-lookup"><span data-stu-id="e7e86-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






