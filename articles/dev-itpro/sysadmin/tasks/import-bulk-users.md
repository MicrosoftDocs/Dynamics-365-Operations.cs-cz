--- 
title: "Hromadné importování uživatelů"
description: "Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Active Directory Azure."
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 54af656c040486f7de718ce589973a6ebe005850
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="772dc-103">Hromadné importování uživatelů</span><span class="sxs-lookup"><span data-stu-id="772dc-103">Import users in bulk</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="772dc-104">Tento postup mohou použít správci systému pro import velkého počtu uživatelů ze služby Active Directory Azure.</span><span class="sxs-lookup"><span data-stu-id="772dc-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="772dc-105">Spustit jako dávkovou úlohu</span><span class="sxs-lookup"><span data-stu-id="772dc-105">Run as a batch job</span></span>
1. <span data-ttu-id="772dc-106">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="772dc-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="772dc-107">Klikněte na Dávkový import.</span><span class="sxs-lookup"><span data-stu-id="772dc-107">Click Batch import.</span></span>
3. <span data-ttu-id="772dc-108">Rozbalte sekci Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="772dc-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="772dc-109">V poli Dávkové zpracování vyberte hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="772dc-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="772dc-110">Zadejte hodnotu do pole Popis úkolu.</span><span class="sxs-lookup"><span data-stu-id="772dc-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="772dc-111">V poli Skupina dávek zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="772dc-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="772dc-112">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="772dc-112">This is an optional step.</span></span>  
7. <span data-ttu-id="772dc-113">Vyberte možnost Ano v poli Soukromý.</span><span class="sxs-lookup"><span data-stu-id="772dc-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="772dc-114">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="772dc-114">This is an optional step.</span></span>  
8. <span data-ttu-id="772dc-115">Vyberte možnost Ano v poli Kritická úloha.</span><span class="sxs-lookup"><span data-stu-id="772dc-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="772dc-116">Tento krok je volitelný.</span><span class="sxs-lookup"><span data-stu-id="772dc-116">This is an optional step.</span></span>  
9. <span data-ttu-id="772dc-117">Vyberte volbu v poli Kategorie monitorování.</span><span class="sxs-lookup"><span data-stu-id="772dc-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="772dc-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="772dc-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="772dc-119">Spuštění v prostředí sandbox</span><span class="sxs-lookup"><span data-stu-id="772dc-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="772dc-120">Klikněte na Dávkový import.</span><span class="sxs-lookup"><span data-stu-id="772dc-120">Click Batch import.</span></span>
2. <span data-ttu-id="772dc-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="772dc-121">Click OK.</span></span>


