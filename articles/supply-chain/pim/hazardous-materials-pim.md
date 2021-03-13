---
title: Nebezpečné materiály
description: Toto téma obsahuje informace o dokumentech s nebezpečnými materiály a informace, které jsou uloženy ve vašem prostředí.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 156cd4ec3a1d1a08ba43832a93fde0d4f22ac2ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007634"
---
# <a name="hazardous-materials"></a><span data-ttu-id="82970-103">Nebezpečné materiály</span><span class="sxs-lookup"><span data-stu-id="82970-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="82970-104">Informace o nebezpečných materiálech se nastavují ve správě informací o produktu.</span><span class="sxs-lookup"><span data-stu-id="82970-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="82970-105">Tento modul také poskytuje dokumenty, které lze vytisknout pomocí řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="82970-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="82970-106">Při expedici materiálů, které jsou klasifikovány jako nebezpečné, musí být do dodávek zahrnuty další dokumenty.</span><span class="sxs-lookup"><span data-stu-id="82970-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="82970-107">Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace o klasifikaci a vzájemně je propojit s položkami výdeje.</span><span class="sxs-lookup"><span data-stu-id="82970-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="82970-108">Tyto informace lze poté použít k přípravě dokumentace o dodávce.</span><span class="sxs-lookup"><span data-stu-id="82970-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82970-109">Funkce nebezpečných materiálů v Microsoft Dynamics 365 Supply Chain Management poskytují kolekci užitečných polí s informacemi o produktu a souvisejících funkcích, které vám mohou pomoci zaznamenat a odkazovat na informace související s vašimi nebezpečnými produkty.</span><span class="sxs-lookup"><span data-stu-id="82970-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="82970-110">Tyto funkce vám také mohou pomoci navrhnout a vytisknout dodací doklady, které obsahují některé totožné informace o všech nebezpečných materiálech, které přepravujete.</span><span class="sxs-lookup"><span data-stu-id="82970-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="82970-111">Systém však automaticky nezajistí vaši plnou kompatibilitu se všemi platnými regulacemi vaší země nebo oblasti.</span><span class="sxs-lookup"><span data-stu-id="82970-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="82970-112">Ačkoli jsou tyto nástroje určeny k tomu, aby vám pomohly dodržovat společné předpisy, nejsou samy o sobě dostatečné ani zaručené.</span><span class="sxs-lookup"><span data-stu-id="82970-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="82970-113">Vaše organizace je odpovědná za to, že si je vědoma všech příslušných předpisů a že podniká všechny kroky nezbytné k jejich dodržování.</span><span class="sxs-lookup"><span data-stu-id="82970-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="82970-114">Před použitím této funkce je nutné provést následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="82970-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="82970-115">**Správa informací o produktech**: Nastavte kódy, které lze použít pro uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="82970-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="82970-116">**Řízení skladu:** Použijte další dokumenty dodávky pro vytisknutí informací o dodávce.</span><span class="sxs-lookup"><span data-stu-id="82970-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="82970-117">Řízení informací o produktech</span><span class="sxs-lookup"><span data-stu-id="82970-117">Product information management</span></span>

<span data-ttu-id="82970-118">V modulu Správa informací o produktu existuje řada nastavení tabulek, kde můžete přidat referenční informace, které jsou uvedeny v seznamech nebezpečného zboží pro silniční, leteckou a námořní dopravu.</span><span class="sxs-lookup"><span data-stu-id="82970-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="82970-119">Zde je přehled některých regulací, na které se často odkazuje:</span><span class="sxs-lookup"><span data-stu-id="82970-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="82970-120">**ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici</span><span class="sxs-lookup"><span data-stu-id="82970-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="82970-121">**CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="82970-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="82970-122">**IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží</span><span class="sxs-lookup"><span data-stu-id="82970-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="82970-123">**IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží</span><span class="sxs-lookup"><span data-stu-id="82970-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="82970-124">Každé z těchto nařízení obsahuje seznam nebezpečného zboží, který obsahuje referenční kódy.</span><span class="sxs-lookup"><span data-stu-id="82970-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="82970-125">Seznamy pro jednotlivé typy přepravy jsou kombinovány se sdílenými mezinárodními klasifikacemi.</span><span class="sxs-lookup"><span data-stu-id="82970-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="82970-126">Supply Chain Management poskytuje referenční tabulku pro sdílené kódy v těchto seznamech.</span><span class="sxs-lookup"><span data-stu-id="82970-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="82970-127">Každý seznam obsahuje také některé jedinečné kódy, které lze definovat.</span><span class="sxs-lookup"><span data-stu-id="82970-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="82970-128">Chcete-li zahájit konfiguraci těchto informací, vytvořte nařízení, které lze použít ke konfiguraci počátečních parametrů.</span><span class="sxs-lookup"><span data-stu-id="82970-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="82970-129">Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="82970-129">Warehouse management</span></span>

<span data-ttu-id="82970-130">Při přípravě dodávky lze vytisknout několik nových sestav.</span><span class="sxs-lookup"><span data-stu-id="82970-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="82970-131">Tyto sestavy využívají informace, které nastavíte v modulu Správa informací o produktech.</span><span class="sxs-lookup"><span data-stu-id="82970-131">These reports use the information that you set up in Product information management.</span></span>
