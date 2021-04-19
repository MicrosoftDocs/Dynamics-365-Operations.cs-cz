---
title: Inicializace počátečních dat v nových prostředích Commerce
description: Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792576"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="5399b-103">Inicializace počátečních dat v nových prostředích Commerce</span><span class="sxs-lookup"><span data-stu-id="5399b-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5399b-104">Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5399b-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5399b-105">Po zavedení řešení Commerce pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat konfiguraci Commerce.</span><span class="sxs-lookup"><span data-stu-id="5399b-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5399b-106">Před inicializací konfigurace Commerce se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde obchody nastavíte.</span><span class="sxs-lookup"><span data-stu-id="5399b-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="5399b-107">Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro Commerce.</span><span class="sxs-lookup"><span data-stu-id="5399b-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="5399b-108">Pro inicializaci konfigurace postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="5399b-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="5399b-109">Spusťte klienta aplikace Commerce.</span><span class="sxs-lookup"><span data-stu-id="5399b-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="5399b-110">Click **Retail a Commerce** &gt; **Nastavení centrály** &gt; **Parametry** &gt; **Parametry Commerce**.</span><span class="sxs-lookup"><span data-stu-id="5399b-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="5399b-111">Klepněte na tlačítko **Inicializovat**.</span><span class="sxs-lookup"><span data-stu-id="5399b-111">Click **Initialize**.</span></span>

<span data-ttu-id="5399b-112">Inicializace vytvoří následující výchozí data konfigurace:</span><span class="sxs-lookup"><span data-stu-id="5399b-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="5399b-113">Úlohy a dílčí úlohy plánovače Commerce</span><span class="sxs-lookup"><span data-stu-id="5399b-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="5399b-114">Schéma obchodního kanálu</span><span class="sxs-lookup"><span data-stu-id="5399b-114">Commerce channel schema</span></span>
- <span data-ttu-id="5399b-115">Plány distribuce Commerce</span><span class="sxs-lookup"><span data-stu-id="5399b-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="5399b-116">Výchozí rozložení obrazovky, které zahrnuje mřížky tlačítek, obrázky a motivy</span><span class="sxs-lookup"><span data-stu-id="5399b-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="5399b-117">Informace o časovém pásmu</span><span class="sxs-lookup"><span data-stu-id="5399b-117">Time zone information</span></span>
- <span data-ttu-id="5399b-118">Operace pokladních míst (POS)</span><span class="sxs-lookup"><span data-stu-id="5399b-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="5399b-119">Oprávnění POS</span><span class="sxs-lookup"><span data-stu-id="5399b-119">POS permissions</span></span>
- <span data-ttu-id="5399b-120">Sestavy kanálu</span><span class="sxs-lookup"><span data-stu-id="5399b-120">Channel reports</span></span>
- <span data-ttu-id="5399b-121">Metadata atributu</span><span class="sxs-lookup"><span data-stu-id="5399b-121">Attribute metadata</span></span>
- <span data-ttu-id="5399b-122">Šablony ověření entity</span><span class="sxs-lookup"><span data-stu-id="5399b-122">Entity validation templates</span></span>
- <span data-ttu-id="5399b-123">Dávková úloha pro vymazání historie relace Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="5399b-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="5399b-124">Dále protokolování, které se vztahuje k odvětví platební karty (PCI) je povoleni pro databázi aplikace Commerce.</span><span class="sxs-lookup"><span data-stu-id="5399b-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="5399b-125">Je možné konfigurovat plánovač Commerce samostatně.</span><span class="sxs-lookup"><span data-stu-id="5399b-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="5399b-126">Tato možnost umožňuje obnovíte konfiguraci plánovače Commerce na výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="5399b-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="5399b-127">Po dokončení inicializace je nutné nakonfigurovat další obchodní data.</span><span class="sxs-lookup"><span data-stu-id="5399b-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="5399b-128">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="5399b-128">Here are some examples:</span></span>

- <span data-ttu-id="5399b-129">Parametry obchodu</span><span class="sxs-lookup"><span data-stu-id="5399b-129">Commerce parameters</span></span>
- <span data-ttu-id="5399b-130">Parametry plánovače obchodu</span><span class="sxs-lookup"><span data-stu-id="5399b-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="5399b-131">Kanály Commerce</span><span class="sxs-lookup"><span data-stu-id="5399b-131">Commerce channels</span></span>
- <span data-ttu-id="5399b-132">Registry a zařízení</span><span class="sxs-lookup"><span data-stu-id="5399b-132">Registers and devices</span></span>
- <span data-ttu-id="5399b-133">Sortimenty</span><span class="sxs-lookup"><span data-stu-id="5399b-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]