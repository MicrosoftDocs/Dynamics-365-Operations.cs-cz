---
title: Nebezpečné materiály
description: Toto téma obsahuje informace o dokumentech s nebezpečnými materiály a informace, které jsou uloženy ve vašem prostředí.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982301"
---
# <a name="hazardous-materials"></a><span data-ttu-id="e5492-103">Nebezpečné materiály</span><span class="sxs-lookup"><span data-stu-id="e5492-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5492-104">Informace o nebezpečných materiálech se nastavují ve správě informací o produktu.</span><span class="sxs-lookup"><span data-stu-id="e5492-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="e5492-105">Tento modul také poskytuje dokumenty, které lze vytisknout pomocí řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="e5492-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="e5492-106">Při expedici materiálů, které jsou klasifikovány jako nebezpečné, musí být do dodávek zahrnuty další dokumenty.</span><span class="sxs-lookup"><span data-stu-id="e5492-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="e5492-107">Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace o klasifikaci a vzájemně je propojit s položkami výdeje.</span><span class="sxs-lookup"><span data-stu-id="e5492-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="e5492-108">Tyto informace lze poté použít k přípravě dokumentace o dodávce.</span><span class="sxs-lookup"><span data-stu-id="e5492-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5492-109">V zájmu usnadnění správy zásilek nebezpečného zboží vám Microsoft Dynamics 365 Supply Chain Management umožňuje nastavit další referenční informace související s produkty.</span><span class="sxs-lookup"><span data-stu-id="e5492-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="e5492-110">Můžete také nastavit další dokumenty dodávky.</span><span class="sxs-lookup"><span data-stu-id="e5492-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="e5492-111">Systém však není automaticky kompatibilní s předpisy vaší země nebo oblasti.</span><span class="sxs-lookup"><span data-stu-id="e5492-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="e5492-112">Namísto toho je to nástroj, který může pomoci celkovému programu.</span><span class="sxs-lookup"><span data-stu-id="e5492-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="e5492-113">Před použitím této funkce je nutné provést následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="e5492-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="e5492-114">**Správa informací o produktech**: Nastavte kódy, které lze použít pro uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="e5492-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="e5492-115">**Řízení skladu:** Použijte další dokumenty dodávky pro vytisknutí informací o dodávce.</span><span class="sxs-lookup"><span data-stu-id="e5492-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="e5492-116">Řízení informací o produktech</span><span class="sxs-lookup"><span data-stu-id="e5492-116">Product information management</span></span>

<span data-ttu-id="e5492-117">V modulu Správa informací o produktu existuje řada nastavení tabulek, kde můžete přidat referenční informace, které jsou uvedeny v seznamech nebezpečného zboží pro silniční, leteckou a námořní dopravu.</span><span class="sxs-lookup"><span data-stu-id="e5492-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="e5492-118">Zde je přehled některých regulací, na které se často odkazuje:</span><span class="sxs-lookup"><span data-stu-id="e5492-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="e5492-119">**ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici</span><span class="sxs-lookup"><span data-stu-id="e5492-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="e5492-120">**CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="e5492-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="e5492-121">**IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="e5492-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="e5492-122">**IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží</span><span class="sxs-lookup"><span data-stu-id="e5492-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="e5492-123">Každé z těchto nařízení obsahuje seznam nebezpečného zboží, který obsahuje referenční kódy.</span><span class="sxs-lookup"><span data-stu-id="e5492-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="e5492-124">Seznamy pro jednotlivé typy přepravy jsou kombinovány se sdílenými mezinárodními klasifikacemi.</span><span class="sxs-lookup"><span data-stu-id="e5492-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="e5492-125">Supply Chain Management poskytuje referenční tabulku pro sdílené kódy v těchto seznamech.</span><span class="sxs-lookup"><span data-stu-id="e5492-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="e5492-126">Každý seznam obsahuje také některé jedinečné kódy, které lze definovat.</span><span class="sxs-lookup"><span data-stu-id="e5492-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="e5492-127">Chcete-li zahájit konfiguraci těchto informací, vytvořte nařízení, které lze použít ke konfiguraci počátečních parametrů.</span><span class="sxs-lookup"><span data-stu-id="e5492-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="e5492-128">Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="e5492-128">Warehouse management</span></span>

<span data-ttu-id="e5492-129">Při přípravě dodávky lze vytisknout několik nových sestav.</span><span class="sxs-lookup"><span data-stu-id="e5492-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="e5492-130">Tyto sestavy využívají informace, které nastavíte v modulu Správa informací o produktech.</span><span class="sxs-lookup"><span data-stu-id="e5492-130">These reports use the information that you set up in Product information management.</span></span>
