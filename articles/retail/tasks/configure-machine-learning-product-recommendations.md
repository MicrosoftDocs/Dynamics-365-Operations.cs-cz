--- 
title: " Konfigurace doporučení produktu využívajícího strojové učení"
description: "Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="7f611-103"> Konfigurace doporučení produktu využívajícího strojové učení</span><span class="sxs-lookup"><span data-stu-id="7f611-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7f611-104">Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS.</span><span class="sxs-lookup"><span data-stu-id="7f611-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="7f611-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="7f611-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7f611-106">Přejděte do nabídky Správa systému > Nastavení > Úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="7f611-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="7f611-107">V seznamu vyhledejte a vyberte záznam 'RetailSales'.</span><span class="sxs-lookup"><span data-stu-id="7f611-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="7f611-108">Klikněte na možnost Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="7f611-108">Click Refresh.</span></span>
4. <span data-ttu-id="7f611-109">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7f611-109">Click OK.</span></span>
5. <span data-ttu-id="7f611-110">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7f611-110">Close the page.</span></span>
6. <span data-ttu-id="7f611-111">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="7f611-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="7f611-112">Klepněte na kartu Strojové učení.</span><span class="sxs-lookup"><span data-stu-id="7f611-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="7f611-113">Vyberte možnost Ano v poli Povolit doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="7f611-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="7f611-114">Pokud se zobrazí zpráva "Nelze načíst modely doporučení", je to proto, že jste teprve nedávno aktualizovali úložiště entit a systém nemusel dokončit asimilaci nových dat.</span><span class="sxs-lookup"><span data-stu-id="7f611-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="7f611-115">2–3 hodiny počkejte a akci opakujte.</span><span class="sxs-lookup"><span data-stu-id="7f611-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="7f611-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7f611-116">Click Save.</span></span>
10. <span data-ttu-id="7f611-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7f611-117">Close the page.</span></span>


