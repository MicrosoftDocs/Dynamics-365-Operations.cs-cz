---
title: Vytvoření projektu integrátoru dat (Preview)
description: Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186461"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="bdf56-103">Vytvoření projektu integrátoru dat (Preview)</span><span class="sxs-lookup"><span data-stu-id="bdf56-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bdf56-104">Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="bdf56-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="bdf56-105">Přihlaste se do aplikace Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bdf56-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="bdf56-106">Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="bdf56-107">Než přejdete k dalšímu kroku, počkejte, dokud se neobnoví všechny datové entity.</span><span class="sxs-lookup"><span data-stu-id="bdf56-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="bdf56-108">Otevřete [portál Power Apps](https://make.powerapps.com/) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="bdf56-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="bdf56-109">Vyberte příslušné prostředí.</span><span class="sxs-lookup"><span data-stu-id="bdf56-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="bdf56-110">V levém navigačním podokně nalevo vyberte **Data \> Připojení**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="bdf56-111">Připojte se k příslušným instancím následujících položek:</span><span class="sxs-lookup"><span data-stu-id="bdf56-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="bdf56-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bdf56-112">Dynamics 365</span></span>
        - <span data-ttu-id="bdf56-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="bdf56-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="bdf56-114">Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="bdf56-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="bdf56-115">Vyberte **Integrátor dat**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="bdf56-116">Vyberte **Sady připojení**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="bdf56-117">Vyberte **Nová sada připojení**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="bdf56-118">Zadejte název připojení.</span><span class="sxs-lookup"><span data-stu-id="bdf56-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="bdf56-119">Vyberte odpovídající připojení pro následující položky:</span><span class="sxs-lookup"><span data-stu-id="bdf56-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="bdf56-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bdf56-120">Dynamics 365</span></span>
        - <span data-ttu-id="bdf56-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="bdf56-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="bdf56-122">Vyberte příslušné mapování organizace.</span><span class="sxs-lookup"><span data-stu-id="bdf56-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="bdf56-123">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-123">Select **Create**.</span></span>

5. <span data-ttu-id="bdf56-124">Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="bdf56-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="bdf56-125">Vytvořte projekty integrace dat pro následující šablony pomocí sady připojení, kterou jste právě vytvořili:</span><span class="sxs-lookup"><span data-stu-id="bdf56-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="bdf56-126">Výsledky přehledu plateb zákazníka (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bdf56-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="bdf56-127">Pokud používáte verzi 10.0.17 nebo novější, musíte použít šablonu s názvem Výsledek platebních údajů zákazníka (CDS to Fin a Ops 10.0.17 +).</span><span class="sxs-lookup"><span data-stu-id="bdf56-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="bdf56-128">Výsledky časové řady cashflow (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bdf56-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="bdf56-129">Výsledky časové řady rozpočtu (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bdf56-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="bdf56-130">Nastavte vhodné plánování pro každý projekt.</span><span class="sxs-lookup"><span data-stu-id="bdf56-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="bdf56-131">Pokud nevidíte požadované entity v CDS, přejděte na **Kredit a inkasa > Nastavení > Finanční přehledy > Parametry finančních přehledů**, povolte funkci Předpovědi plateb zákazníka a klikněte na tlačítko **Vytvořit predikční model**.</span><span class="sxs-lookup"><span data-stu-id="bdf56-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="bdf56-132">Po dokončení nasazení modelu AI (úspěšně nebo neúspěšně) budou entity CDS potřebné k vytvoření integrace nasazeny do CDS.</span><span class="sxs-lookup"><span data-stu-id="bdf56-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
