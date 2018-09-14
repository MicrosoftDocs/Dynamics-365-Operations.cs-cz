--- 
title: " Konfigurace doporučení produktu využívajícího strojové učení"
description: "Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS."
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="53c7c-103"> Konfigurace doporučení produktu využívajícího strojové učení</span><span class="sxs-lookup"><span data-stu-id="53c7c-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="53c7c-104">Tato procedura aktualizuje data v úložišti entit, které používá systém strojového učení využívající doporučení produktu, a pak aktivuje doporučení produktu v klientech POS.</span><span class="sxs-lookup"><span data-stu-id="53c7c-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="53c7c-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="53c7c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="53c7c-106">Přejděte do nabídky Správa systému > Nastavení > Úložiště entit.</span><span class="sxs-lookup"><span data-stu-id="53c7c-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="53c7c-107">V seznamu vyhledejte a vyberte záznam 'RetailSales'.</span><span class="sxs-lookup"><span data-stu-id="53c7c-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="53c7c-108">Klikněte na možnost Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="53c7c-108">Click Refresh.</span></span>
4. <span data-ttu-id="53c7c-109">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="53c7c-109">Click OK.</span></span>
5. <span data-ttu-id="53c7c-110">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="53c7c-110">Close the page.</span></span>
6. <span data-ttu-id="53c7c-111">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="53c7c-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="53c7c-112">Klepněte na kartu Strojové učení.</span><span class="sxs-lookup"><span data-stu-id="53c7c-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="53c7c-113">Vyberte možnost Ano v poli Povolit doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="53c7c-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="53c7c-114">Pokud se zobrazí zpráva "Nelze načíst modely doporučení", je to proto, že jste teprve nedávno aktualizovali úložiště entit a systém nemusel dokončit asimilaci nových dat.</span><span class="sxs-lookup"><span data-stu-id="53c7c-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="53c7c-115">2–3 hodiny počkejte a akci opakujte.</span><span class="sxs-lookup"><span data-stu-id="53c7c-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="53c7c-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="53c7c-116">Click Save.</span></span>
10. <span data-ttu-id="53c7c-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="53c7c-117">Close the page.</span></span>


