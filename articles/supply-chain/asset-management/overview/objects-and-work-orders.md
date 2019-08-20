---
title: Majetek a pracovní příkazy
description: Toto téma popisuje majetek a pracovní příkazy v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783120"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="a777a-103">Majetek a pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="a777a-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a777a-104">Toto téma popisuje majetek a pracovní příkazy v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="a777a-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="a777a-105">Majetek a pracovní příkazy jsou ústředními částmi modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="a777a-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="a777a-106">*Majetek* je stroj nebo část stroje, která vyžaduje nepřetržitou údržbu a servis.</span><span class="sxs-lookup"><span data-stu-id="a777a-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="a777a-107">Majetek lze tvořit v hierarchické struktuře a může být spojen s funkčními místy.</span><span class="sxs-lookup"><span data-stu-id="a777a-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="a777a-108">Úlohy údržby lze plánovat na všech úrovních struktury majetku.</span><span class="sxs-lookup"><span data-stu-id="a777a-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="a777a-109">Pro každý majetek jsou nastaveny různé údaje, například informace o produktu, specifikace majetku a požadované plány údržby.</span><span class="sxs-lookup"><span data-stu-id="a777a-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="a777a-110">Následující ilustrace znázorňuje přehled dat o majetku a příslušnost majetku k typům práce.</span><span class="sxs-lookup"><span data-stu-id="a777a-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="a777a-111">Červený text se používá pro příklady, které zobrazují dědičnost a závislosti.</span><span class="sxs-lookup"><span data-stu-id="a777a-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Obrázek č. 1](media/05-overview-image.png)

<span data-ttu-id="a777a-113">Každý pracovní příkaz má typ pracovního příkazu, preventivní údržbu, opravnou údržbu nebo kontrolu.</span><span class="sxs-lookup"><span data-stu-id="a777a-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="a777a-114">Pracovní příkaz obsahuje jednu nebo více úloh pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="a777a-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="a777a-115">Každá úloha pracovního příkazu definuje úlohu, která musí být provedena na majetku a souvisejícím typu úlohy.</span><span class="sxs-lookup"><span data-stu-id="a777a-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="a777a-116">Příkladem souvisejících typů úloh jsou 10 000 km, 50 000 km, roční generální oprava a bezpečnostní prohlídka.</span><span class="sxs-lookup"><span data-stu-id="a777a-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="a777a-117">Jeden pracovní příkaz může být spojen s více majetky.</span><span class="sxs-lookup"><span data-stu-id="a777a-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="a777a-118">Následující ilustrace znázorňuje přehled klíčových dat v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="a777a-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Obrázek č. 2](media/06-overview-image.png)

<span data-ttu-id="a777a-120">Pracovní příkaz může být spojen s jiným pracovním příkazem a typy úloh mohou obsahovat následující úlohy, které tvoří pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="a777a-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="a777a-121">Obecně neexistují žádné závislosti mezi pracovními příkazy.</span><span class="sxs-lookup"><span data-stu-id="a777a-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="a777a-122">Proto mohou změnit stav svůj životního cyklu pracovního příkazu a mohou být naplánovány nezávisle na sobě.</span><span class="sxs-lookup"><span data-stu-id="a777a-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="a777a-123">Pracovní příkazy mohou být vytvářeny různými způsoby, které souvisejí s opravnou, preventivní nebo reaktivní údržbou.</span><span class="sxs-lookup"><span data-stu-id="a777a-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="a777a-124">Pracovní příkazy lze rovněž vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="a777a-124">You can also create work orders manually.</span></span> <span data-ttu-id="a777a-125">Následující ilustrace znázorňuje přehled procesu automatického nebo ručního vytváření pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="a777a-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Obrázek č. 3](media/07-overview-image.png)

<span data-ttu-id="a777a-127">Chcete-li naplánovat a spustit úlohu údržby v pracovním příkazu, je nutné provést několik kroků.</span><span class="sxs-lookup"><span data-stu-id="a777a-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="a777a-128">Následující ilustrace znázorňuje přehled zpracování pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="a777a-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Obrázek č. 4](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="a777a-130">Obecně, když pracujete v aplikaci Microsoft Dynamics 365 for Finance and Operations a modulu **Správa majetku**, vyberete **Nový** pro vytvoření nového záznamu, vyberete možnost **Upravit** pro aktualizaci existujícího záznamu a vyberete možnost **Uložit** pro uložení nových nebo upravených dat.</span><span class="sxs-lookup"><span data-stu-id="a777a-130">In general, when you work in Microsoft Dynamics 365 for Finance and Operations and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
