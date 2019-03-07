---
title: " Vytvoření a přidružení hardwarové stanice"
description: Tato procedura vás provede postupem vytvoření nové hardwarové stanice.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "330556"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="1dbfb-103"> Vytvoření a přidružení hardwarové stanice</span><span class="sxs-lookup"><span data-stu-id="1dbfb-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1dbfb-104">Tato procedura vás provede postupem vytvoření nové hardwarové stanice.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="1dbfb-105">Bude vytvořený nový hardwarový profil a použije se pro přidání nových hardwarových stanic do předem definovaného obchodu (kanálu).</span><span class="sxs-lookup"><span data-stu-id="1dbfb-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="1dbfb-106">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1dbfb-107">Přejděte na Základy obchodování > Kanály > ..</span><span class="sxs-lookup"><span data-stu-id="1dbfb-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="1dbfb-108">> ..</span><span class="sxs-lookup"><span data-stu-id="1dbfb-108">> ..</span></span> <span data-ttu-id="1dbfb-109">> ..</span><span class="sxs-lookup"><span data-stu-id="1dbfb-109">> ..</span></span> <span data-ttu-id="1dbfb-110">> Profily hardwarové stanice.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="1dbfb-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-111">Click New.</span></span>
3. <span data-ttu-id="1dbfb-112">V poli ID hardwarové stanice zadejte „TestHWProfile“.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="1dbfb-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1dbfb-114">Zadejte číslo do pole Číslo portu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="1dbfb-115">V poli Profil hardwaru kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1dbfb-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1dbfb-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1dbfb-118">V poli Název balíčku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1dbfb-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1dbfb-120">Toto je standardní balíček, jehož součástí je nové prostředí.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="1dbfb-121">Číslo verze se může lišit.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-121">The version number may vary.</span></span>  
11. <span data-ttu-id="1dbfb-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-122">Click Save.</span></span>
12. <span data-ttu-id="1dbfb-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-123">Close the page.</span></span>
13. <span data-ttu-id="1dbfb-124">Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Všechny maloobchody.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="1dbfb-125">Vyberte ze seznamu řádek 17.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="1dbfb-126">Pokud používáte data ukázkové společnosti USRT jedná se o obchod Houston.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="1dbfb-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1dbfb-128">Přepněte rozšíření oddílu Hardwarové stanice.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="1dbfb-129">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-129">Click Add.</span></span>
18. <span data-ttu-id="1dbfb-130">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="1dbfb-131">V poli ID profilu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1dbfb-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1dbfb-133">Musí se jednat o nový profil hardwarové stanice vytvořený v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="1dbfb-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1dbfb-135">Do pole Název hostitele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="1dbfb-136">Zadejte hodnotu do pole ID terminálu EFT.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="1dbfb-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1dbfb-137">Click Save.</span></span>

