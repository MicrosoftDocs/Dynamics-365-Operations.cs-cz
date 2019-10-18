---
title: Inicializace počátečních dat v nových prostředích Retail
description: Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025509"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="e9867-103">Inicializace počátečních dat v nových prostředích Retail</span><span class="sxs-lookup"><span data-stu-id="e9867-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9867-104">Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="e9867-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Retail.</span></span>

<span data-ttu-id="e9867-105">Po zavedení maloobchodního řešení pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat maloobchodní konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="e9867-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9867-106">Před inicializací konfigurace maloobchodu se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde maloobchody nastavíte.</span><span class="sxs-lookup"><span data-stu-id="e9867-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="e9867-107">Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro maloobchod.</span><span class="sxs-lookup"><span data-stu-id="e9867-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="e9867-108">Pro inicializaci konfigurace maloobchodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="e9867-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="e9867-109">Spusťte klienta aplikace Retail.</span><span class="sxs-lookup"><span data-stu-id="e9867-109">Start the Retail client.</span></span>
2. <span data-ttu-id="e9867-110">Klikněte na možnost **Maloobchod** &gt; **Nastavení centrály** &gt; **Parametery** &gt; **Parametry maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="e9867-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="e9867-111">Klepněte na tlačítko **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="e9867-111">Click **Initialize**.</span></span>

<span data-ttu-id="e9867-112">Inicializace vytvoří následující výchozí data konfigurace:</span><span class="sxs-lookup"><span data-stu-id="e9867-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="e9867-113">Úlohy a dílčí úlohy Maloobchodního plánovače</span><span class="sxs-lookup"><span data-stu-id="e9867-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="e9867-114">Schéma maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="e9867-114">Retail channel schema</span></span>
- <span data-ttu-id="e9867-115">Plány maloobchodní distribuce</span><span class="sxs-lookup"><span data-stu-id="e9867-115">Retail distribution schedules</span></span>
- <span data-ttu-id="e9867-116">Výchozí rozložení obrazovky, které zahrnuje mřížky tlačítek, obrázky a motivy</span><span class="sxs-lookup"><span data-stu-id="e9867-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="e9867-117">Informace o časovém pásmu</span><span class="sxs-lookup"><span data-stu-id="e9867-117">Time zone information</span></span>
- <span data-ttu-id="e9867-118">Operace pokladních míst (POS)</span><span class="sxs-lookup"><span data-stu-id="e9867-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="e9867-119">Oprávnění POS</span><span class="sxs-lookup"><span data-stu-id="e9867-119">POS permissions</span></span>
- <span data-ttu-id="e9867-120">Sestavy kanálu</span><span class="sxs-lookup"><span data-stu-id="e9867-120">Channel reports</span></span>
- <span data-ttu-id="e9867-121">Metadata atributu</span><span class="sxs-lookup"><span data-stu-id="e9867-121">Attribute metadata</span></span>
- <span data-ttu-id="e9867-122">Šablony ověření entity</span><span class="sxs-lookup"><span data-stu-id="e9867-122">Entity validation templates</span></span>
- <span data-ttu-id="e9867-123">Dávková úloha pro vymazání historie relace Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="e9867-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="e9867-124">Dále protokolování, které se vztahuje k odvětví platební karty (PCI) je povoleni pro databázi aplikace Retail.</span><span class="sxs-lookup"><span data-stu-id="e9867-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="e9867-125">Je možné Maloobchodní plánovač konfigurovat samostatně.</span><span class="sxs-lookup"><span data-stu-id="e9867-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="e9867-126">Tato možnost umožňuje obnovíte konfiguraci maloobchodního plánovače na výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="e9867-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="e9867-127">Po dokončení inicializace je nutné nakonfigurovat další data pro maloobchod.</span><span class="sxs-lookup"><span data-stu-id="e9867-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="e9867-128">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="e9867-128">Here are some examples:</span></span>

- <span data-ttu-id="e9867-129">Parametry maloobchodu</span><span class="sxs-lookup"><span data-stu-id="e9867-129">Retail parameters</span></span>
- <span data-ttu-id="e9867-130">Parametry programu Maloobchodní plánovač</span><span class="sxs-lookup"><span data-stu-id="e9867-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="e9867-131">Maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="e9867-131">Retail channels</span></span>
- <span data-ttu-id="e9867-132">Registry a zařízení</span><span class="sxs-lookup"><span data-stu-id="e9867-132">Registers and devices</span></span>
- <span data-ttu-id="e9867-133">Sortimenty</span><span class="sxs-lookup"><span data-stu-id="e9867-133">Assortments</span></span>
