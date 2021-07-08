---
title: Regulatory Configuration Service (RCS) - Odstranění prostředí RCS
description: Toto téma vysvětluje, jak může správce systému Regulatory Configuration Service (RCS) odstranit prostředí RCS a související data.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295811"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="5bed7-103">Regulatory Configuration Service (RCS) - Odstranění prostředí RCS</span><span class="sxs-lookup"><span data-stu-id="5bed7-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bed7-104">Toto téma vysvětluje, jak může správce systému Regulatory Configuration Service (RCS) odstranit prostředí RCS a související data.</span><span class="sxs-lookup"><span data-stu-id="5bed7-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="5bed7-105">Než budete moci dokončit postup uvedené v tomto tématu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="5bed7-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="5bed7-106">Musíte mít přidělenou roli **Systémový administrátor** pro prostředí RCS.</span><span class="sxs-lookup"><span data-stu-id="5bed7-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="5bed7-107">Role **Správce systému** musí mít přiřazenou roli **RCSDeleteEnvironmentDuty**.</span><span class="sxs-lookup"><span data-stu-id="5bed7-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="5bed7-108">Ostraňte prostředí RCS</span><span class="sxs-lookup"><span data-stu-id="5bed7-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="5bed7-109">Otevřete RCS a vyberte dlaždici pracovního prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="5bed7-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="5bed7-110">V části **Související odkazy** vyberte **Odstranit prostředí RCS**.</span><span class="sxs-lookup"><span data-stu-id="5bed7-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![V části Související odkazy vyberte Odstranit prostředí RCS.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="5bed7-112">V zobrazeném dialogovém okně zkontrolujte zprávy o rozsahu odstranění prostředí.</span><span class="sxs-lookup"><span data-stu-id="5bed7-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Zprávy v dialogovém okně Odstranit prostředí RCS](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="5bed7-114">Odstranění prostředí RCS nelze vrátit zpět.</span><span class="sxs-lookup"><span data-stu-id="5bed7-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="5bed7-115">Operace odstraní vybrané prostředí RCS a veškerá související data, včetně funkcí a konfigurací, které jsou uloženy v globálním úložišti.</span><span class="sxs-lookup"><span data-stu-id="5bed7-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="5bed7-116">Funkce a konfigurace sdílené s jinými organizacemi budou sdíleny a odstraněny, pokud nemají žádné závislosti.</span><span class="sxs-lookup"><span data-stu-id="5bed7-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="5bed7-117">Funkce a konfigurace, které mají závislosti, budou označeny jako ukončené.</span><span class="sxs-lookup"><span data-stu-id="5bed7-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="5bed7-118">Do pole, které je k dispozici, zadejte globálně jedinečný identifikátor (GUID) prostředí RCS a potvrďte, že jej chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="5bed7-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="5bed7-119">GUID prostředí je součástí zprávy o odstranění.</span><span class="sxs-lookup"><span data-stu-id="5bed7-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="5bed7-120">Zvolte **Odstranit prostředí**.</span><span class="sxs-lookup"><span data-stu-id="5bed7-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="5bed7-121">Vaše prostředí RCS a veškerá související data jsou nyní odstraněna.</span><span class="sxs-lookup"><span data-stu-id="5bed7-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5bed7-122">Po odstranění prostředí RCS není možné data obnovit.</span><span class="sxs-lookup"><span data-stu-id="5bed7-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="5bed7-123">Nové prostředí RCS lze vytvořit v jakékoli dostupné oblasti RCS.</span><span class="sxs-lookup"><span data-stu-id="5bed7-123">A new RCS environment can be created in any available RCS region.</span></span>
