---
title: Vytvoření projektu integrátoru dat (Preview)
description: Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: 9ecf6ef7b7f052ebbb1201dcd04a7431f5b72ce5
ms.sourcegitcommit: b64c52d85aa6f110f3b1959a5521637dd8631b5b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867440"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="a1af4-103">Vytvoření projektu integrátoru dat (Preview)</span><span class="sxs-lookup"><span data-stu-id="a1af4-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a1af4-104">Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.</span><span class="sxs-lookup"><span data-stu-id="a1af4-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="a1af4-105">Přihlaste se do aplikace Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a1af4-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="a1af4-106">Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="a1af4-107">Než přejdete k dalšímu kroku, počkejte, dokud se neobnoví všechny datové entity.</span><span class="sxs-lookup"><span data-stu-id="a1af4-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="a1af4-108">Otevřete [portál Power Apps](https://make.powerapps.com/) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1af4-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="a1af4-109">Vyberte příslušné prostředí.</span><span class="sxs-lookup"><span data-stu-id="a1af4-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="a1af4-110">V levém navigačním podokně nalevo vyberte **Data \> Připojení**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="a1af4-111">Připojte se k příslušným instancím následujících položek:</span><span class="sxs-lookup"><span data-stu-id="a1af4-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="a1af4-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a1af4-112">Dynamics 365</span></span>
        - <span data-ttu-id="a1af4-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="a1af4-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="a1af4-114">Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1af4-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="a1af4-115">Vyberte **Integrátor dat**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="a1af4-116">Vyberte **Sady připojení**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="a1af4-117">Vyberte **Nová sada připojení**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="a1af4-118">Zadejte název připojení.</span><span class="sxs-lookup"><span data-stu-id="a1af4-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="a1af4-119">Vyberte odpovídající připojení pro následující položky:</span><span class="sxs-lookup"><span data-stu-id="a1af4-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="a1af4-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a1af4-120">Dynamics 365</span></span>
        - <span data-ttu-id="a1af4-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="a1af4-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="a1af4-122">Vyberte příslušné mapování organizace.</span><span class="sxs-lookup"><span data-stu-id="a1af4-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="a1af4-123">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-123">Select **Create**.</span></span>

5. <span data-ttu-id="a1af4-124">Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a1af4-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="a1af4-125">Vytvořte projekty integrace dat pro následující šablony pomocí sady připojení, kterou jste právě vytvořili:</span><span class="sxs-lookup"><span data-stu-id="a1af4-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="a1af4-126">Výsledky přehledu plateb zákazníka (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a1af4-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="a1af4-127">Pokud používáte verzi 10.0.17 nebo novější, musíte použít šablonu s názvem Výsledek platebních údajů zákazníka (CDS to Fin a Ops 10.0.17 +).</span><span class="sxs-lookup"><span data-stu-id="a1af4-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="a1af4-128">Výsledky časové řady cashflow (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a1af4-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="a1af4-129">Výsledky časové řady rozpočtu (CDS do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a1af4-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="a1af4-130">Nastavte vhodné plánování pro každý projekt.</span><span class="sxs-lookup"><span data-stu-id="a1af4-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="a1af4-131">Pokud nevidíte požadované entity v CDS, přejděte na **Kredit a inkasa > Nastavení > Finanční přehledy > Parametry finančních přehledů**, povolte funkci Předpovědi plateb zákazníka a klikněte na tlačítko **Vytvořit predikční model**.</span><span class="sxs-lookup"><span data-stu-id="a1af4-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="a1af4-132">Po dokončení nasazení modelu AI (úspěšně nebo neúspěšně) budou entity CDS potřebné k vytvoření integrace nasazeny do CDS.</span><span class="sxs-lookup"><span data-stu-id="a1af4-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a1af4-133">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="a1af4-133">Privacy notice</span></span>

<span data-ttu-id="a1af4-134">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="a1af4-134">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
