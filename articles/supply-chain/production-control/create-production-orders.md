---
title: "Vytvořit výrobní zakázky"
description: "Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d6b35c347aad64a44e827ecb86273f4767d8afd3
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="create-production-orders"></a><span data-ttu-id="f62ff-105">Vytvořit výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="f62ff-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f62ff-106">Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky.</span><span class="sxs-lookup"><span data-stu-id="f62ff-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="f62ff-107">Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení.</span><span class="sxs-lookup"><span data-stu-id="f62ff-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="f62ff-108">Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít.</span><span class="sxs-lookup"><span data-stu-id="f62ff-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="f62ff-109">Výrobní zakázka prochází výrobního cyklu několik fázemi.</span><span class="sxs-lookup"><span data-stu-id="f62ff-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="f62ff-110">Zakázce je po vytvoření přiřazen stav **Vytvořeno**.</span><span class="sxs-lookup"><span data-stu-id="f62ff-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="f62ff-111">Jakmile je objednávka dokončena, je jí přiřazen stav **Ukončeno**.</span><span class="sxs-lookup"><span data-stu-id="f62ff-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="f62ff-112">Díky možnosti nastavení parametrů v každé fázi může uživatel nakonfigurovat jednotlivé kroky.</span><span class="sxs-lookup"><span data-stu-id="f62ff-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="f62ff-113">Nastavení může být nastaveno pro jednoho uživatele nebo pro všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="f62ff-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="f62ff-114">Hlavními entitami výrobní zakázky jsou výrobní kusovník a výrobní postup.</span><span class="sxs-lookup"><span data-stu-id="f62ff-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="f62ff-115">Tyto položky jsou zkopírovány do výrobní zakázky na základě vybrané položky a množství, které chcete vyrobit.</span><span class="sxs-lookup"><span data-stu-id="f62ff-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="f62ff-116">Před zahájením výrobní zakázky je možné výrobní kusovník a postup upravit.</span><span class="sxs-lookup"><span data-stu-id="f62ff-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="f62ff-117">Výrobní zakázku lze vytvořit v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="f62ff-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="f62ff-118">Vytvoření při provedení hlavního plánování založeného na potřebném materiálu.</span><span class="sxs-lookup"><span data-stu-id="f62ff-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="f62ff-119">Vytvoření přímo z řádku prodejní objednávky nebo při vytvoření a odhadnutí výrobní zakázky vyšší úrovně (doložená dodávka).</span><span class="sxs-lookup"><span data-stu-id="f62ff-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="f62ff-120">Ruční vytvoření.</span><span class="sxs-lookup"><span data-stu-id="f62ff-120">Created manually.</span></span>





